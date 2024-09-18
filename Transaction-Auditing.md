### **Audit Form - Conceptual Documentation**

**Purpose:**
The Audit Form module is designed to streamline and automate the process of auditing various types of business transactions, such as invoices, vendor bills, sales returns, cash receipts, and payments. The module allows users to scan transaction data, display relevant details, validate the audit, and attach relevant documents or images. It also provides functionality to handle errors, ensure warehouse consistency, and submit the final audit for storage and further review.

**Key Features:**
1. **Transaction Scanning**: Automatically extracts and displays key details from scanned transaction data.
2. **Error Handling**: Validates essential fields and ensures consistency between the scanned transaction and logged-in user.
3. **Document & Signature Attachment**: Allows users to attach images and collect signatures from customers or vendors for auditing.
4. **Form Reset**: Resets the form after every scan to allow for fresh inputs.
5. **Audit Submission**: Submits the collected data for audit storage and displays success/error messages.

---

### **Audit Form - Technical Documentation**

**File Location:**  
`components/forms/AuditForm.js`

**State Variables:**
- `scrollEnabled`: Controls the scrolling functionality.
- `isSubmiting`: Tracks the form submission state.
- `url`: Stores the signature URL after it’s collected from the user.
- `imageUrls`: Stores the URLs of images attached to the audit.
- `displayBillDetails`: Stores the details of the scanned bill.
- `collectionType`: Stores the collection type based on the scanned transaction.
- `errors`: Tracks validation errors in the form.
- `ledger`: Stores ledger details for the transaction.
- `scannedBillDetails`: Holds the full details of the scanned bill.
- `remarks`: Stores remarks entered by the user.
- `splittedBillName`: Stores the bill name extracted from the scanned data.
- `loginUser`: Retrieves the current logged-in user from the `authStore`.

**Functions:**
1. **`resetFormState()`**: Resets all state variables to their default values after each transaction scan.
2. **`handleScan(data)`**: Extracts transaction details based on scanned data and sets the state accordingly. It supports various transaction types like Invoice, Vendor Bill, Sales Return, etc.
3. **`validate()`**: Validates the form fields before submission and checks for warehouse consistency. Triggers the `handleSubmitAudit()` if valid.
4. **`handleSubmitAudit()`**: Prepares the audit data and sends it to the server for storage. Displays success or error messages based on the response.
5. **`handleDeleteImage(index)`**: Deletes the attached image from the `imageUrls` array by index.
6. **`renderItem({ index, item })`**: Renders images in a list, allowing users to view and delete attached images.

**UI Components:**
1. **`NavigationHeader`**: Displays the audit form's title and a back button.
2. **`RoundedScrollContainer`**: Wraps the form fields and makes the content scrollable.
3. **`FormInput`**: Used for displaying non-editable form fields like Date, Branch, Collection Type, Customer, Invoice Number, and Total Amount.
4. **`Button` & `LoadingButton`**: Standard buttons used for the "Scan" action and submission of the audit.
5. **`SignaturePad`**: Allows the user to collect and attach a customer/vendor signature.
6. **`FlatList`**: Displays attached images in a grid format.
7. **`ActionModal`**: Modal for attaching files (images).

**Displayed Fields:**
- **Date**: The current date, displayed in a non-editable field.
- **Branch**: The name of the logged-in user's company or branch.
- **Customer Name**: The name of the customer/vendor from the scanned data.
- **Invoice Number**: The invoice or transaction number from the scanned data.
- **Total Amount**: The total amount involved in the transaction.
- **Collection Type**: The type of collection (derived from scanned data).
- **Signature**: Signature field for customers/vendors.
- **Remarks**: A text field for entering remarks.

**Other Considerations:**
- **Error Handling**: Uses the `setErrors` function to display validation messages.
- **Toast Notifications**: Provides success and error feedback via `react-native-toast-message`.

Here’s a detailed breakdown of both the conceptual and technical documentation for the `AuditScreen` module:

### Audit Screen - Conceptual Documentation

**Purpose:**
The `AuditScreen` component is used to display a list of auditing records. It fetches and displays audit data, supports pagination, and provides a button for users to navigate to the `AuditForm` screen for adding new audits.

**Key Features:**
1. **Data Fetching:** Retrieves auditing data from the API.
2. **Pagination:** Loads more data as the user scrolls to the end of the list.
3. **Empty State:** Displays a message when no data is available.
4. **Navigation:** Allows navigation to the `AuditForm` screen to create a new audit entry.
5. **Loading Indicator:** Shows a loading animation while data is being fetched.

### Audit Screen - Technical Documentation

**File Location:**
- `src/screens/AuditScreen.js`

**State Variables:**
- **data:** Array holding the fetched audit records.
- **loading:** Boolean indicating if data is currently being fetched.

**Functions:**
1. **`useFocusEffect`:** Fetches audit data when the screen is focused.
2. **`useEffect`:** Fetches data when the screen is focused.
3. **`handleLoadMore`:** Loads more audit data when the user scrolls to the end of the list.
4. **`renderItem`:** Renders each item in the list, showing an empty state if necessary.
5. **`renderEmptyState`:** Renders an empty state message when no data is available.
6. **`renderContent`:** Renders the list of audits and a loading indicator.
7. **`renderAuditing`:** Conditionally renders either the empty state or the content based on data availability.

**UI Components:**
- **`SafeAreaView:`** Ensures that the content is displayed within the safe area boundaries of the device.
- **`NavigationHeader:`** Displays the header with the title "Transaction Auditing" and a back button.
- **`RoundedContainer:`** Provides styling with rounded corners for the main content area.
- **`FlashList:`** Displays a scrollable list of audit records with support for pagination.
- **`EmptyState:`** Displays an image and message when no data is available.
- **`FABButton:`** A floating action button that navigates to the `AuditForm` screen.
- **`AnimatedLoader:`** Shows a loading animation while fetching data.

**Display Fields:**
- **Audit Records:** Each record is rendered by `AuditList`. Fields displayed in the list are defined by the `AuditList` component.

**Additional Information:**
- **Pagination Threshold:** The `FlashList` component's `onEndReachedThreshold` is set to 0.2, meaning it will trigger `handleLoadMore` when the user scrolls to 20% from the bottom.
- **Loading Indicator:** The `ListFooterComponent` in `FlashList` shows the `AnimatedLoader` when data is being loaded.
