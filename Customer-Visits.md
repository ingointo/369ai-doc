### **Customer Visit Module - Conceptual Documentation**

---

### **1. Visit Listing Screen**

#### **Purpose:**
The **Visit Listing Screen** provides users with an overview of all customer visits, allowing them to filter, search, and browse through visit records. This screen enables users to quickly find relevant visits based on various criteria like dates, employees, departments, brands, and customers. It serves as a starting point to access detailed information about individual visits.

#### **Key Features:**

- **Filter Visits:** Users can apply filters (date range, employees, departments, brands, and customers) to refine the visit list.
- **View Visit Details:** Users can select a visit from the list to navigate to the detailed view of that visit.
- **Pagination and Load More:** Supports efficient loading of large visit data through paginated requests. Users can load more results as they scroll.
- **Search and Sort Options:** Users can use various filters to narrow down the list of visits, making it easier to find relevant entries.

---

### **2. Visit Details Screen**

#### **Purpose:**
The **Visit Details Screen** offers an in-depth view of a specific customer visit, showing comprehensive information such as date, time, location, and the people involved. It also includes any attached images and relevant visit remarks. This screen allows users to gain a complete understanding of a particular visit, including customer interactions, time tracking, and next scheduled visits.

#### **Key Features:**

- **Detailed Visit Information:** Displays information such as the date of the visit, employee name, customer name, site/location, and contact details.
- **Attached Images:** Shows images related to the visit (e.g., site photos or documents).
- **Navigation to Map View:** If the visit has location data, users can navigate to a map view to see the exact location.
- **Visit Remarks:** Provides insights into the purpose and outcome of the visit, including next scheduled visit information.

---

### **3. Customer Visit Creation**

**Objective:**
The "Create Customer Visit" feature enables users to log new customer visits by filling out a multi-tab form. It organizes details across three tabs: `Customer`, `Visit Details`, and `In & Out`. Each tab collects critical information related to the customer, visit purpose, remarks, and timing for the visit. This ensures that all relevant visit details are documented accurately and consistently for future reference or reporting.

**Flow:**
1. **Customer Information (Tab 1)**: Users select or input customer-related data, such as customer name, site location, contact person, and visit purpose. Optionally, they can add the next visit date and relevant contact information.
2. **Visit Details (Tab 2)**: This tab captures remarks and optionally allows users to upload images related to the visit.
3. **In & Out (Tab 3)**: Users input the actual `Time In` and `Time Out` for the visit, ensuring accurate tracking of the visit duration.

Once all the information is filled, the user can submit the visit. If the data passes validation checks, it is saved to the backend via an API request.

---


### **Customer Visit Module**

---

### **1. Visit Listing Screen**

#### **File Location:**
`./src/screens/Home/Options/Visits`

#### **State Variables:**

- **`formData` (Object):**  
  Holds the current filter selections:
  - `fromDate` / `toDate`: Date range for filtering.
  - `selectedCustomer`: Selected customer to filter visits.
  - `selectedEmployees`: Selected employees for filtering.
  - `selectedDepartments`: Selected departments.
  - `selectedBrands`: Selected brands.

- **`dropdown` (Object):**  
  Holds dropdown data for filters:
  - `employees`, `departments`, `brands`, `customers`: List of selectable options for filtering.

- **`isVisible` (Boolean):**  
  Controls the visibility of filter dropdown sheets.
  
- **`selectedType` (String):**  
  Tracks the currently selected dropdown filter type (e.g., `employee`, `customer`).

#### **Functions:**

- **`fetchCustomerVisitList` (Function):**
  Fetches the list of customer visits based on the current filter criteria. Uses the `formData` state to send the selected filters to the backend.

- **`handleLoadMore` (Function):**
  Loads more visit data when the user reaches the end of the current list. This function is tied to pagination and appends more results to the list.

- **`handleDateConfirm` (Function):**
  Updates the date range filter when a user selects new dates from the date picker. Once confirmed, it updates the `formData` state with new dates.

- **`handleFieldChange` (Function):**
  Updates the selected filter value (e.g., employee, customer) based on user input. This modifies the `formData` state to reflect the change.

- **`applyFilters` (Function):**
  Executes the filtering process by applying the selected filter criteria from `formData` and fetching the updated list of visits.

- **`clearFilters` (Function):**
  Resets all filters to their default values (e.g., no date, no selected employees, departments, brands, or customers).

#### **UI Components:**

- **`PressableInput`:**  
  Custom input component used for filter fields like `fromDate`, `toDate`, and dropdown selectors (e.g., employee, customer).

- **`VisitList`:**  
  Displays the list of visits. Each visit is presented as a tappable item, allowing navigation to the Visit Details screen.

- **`DropdownSheet` & `MultiSelectDropdownSheet`:**  
  Custom dropdown sheets for single-select and multi-select filtering options (e.g., selecting employees, departments).

---

### **2. Visit Details Screen**

#### **File Location:**
`./src/screens/Home/Options/Visits`

#### **State Variables:**

- **`details` (Object):**  
  Stores detailed information about the selected visit, fetched from the backend. This includes fields like:
  - `date`
  - `employeeName`
  - `customerName`
  - `location`
  - `contactPerson`
  - `contactNo`
  - `nextVisitDate`
  - `visitPurpose`
  - `timeIn`
  - `timeOut`
  - `remarks`
  - `images`

#### **Functions:**

- **`fetchCustomerVisitDetails` (Function):**
  Fetches detailed information for a specific customer visit using the visit ID. This data populates the `details` state with all relevant visit information.

- **`handleMapIconPress` (Function):**
  Opens a map view if the visit's location is available. This allows the user to view the exact location of the visit on a map.

- **`fetchDetails` (Function):**
  Triggers the fetching of visit details when the screen is focused, ensuring the latest information is displayed when the user navigates to the screen.

#### **UI Components:**

- **`DetailField`:**  
  Custom component for rendering individual pieces of visit information. Each `DetailField` represents a specific detail, such as the visit date, employee name, or remarks.

- **`UploadsContainer`:**  
  Displays a grid of images attached to the visit. This is useful for showing visual documentation of the visit (e.g., site photos, work progress).

- **`NavigationHeader`:**  
  Provides a header with navigation options, including back navigation to return to the Visit Listing Screen.

---

This structure breaks down both the conceptual and technical aspects of the **Customer Visit Module**, making it easier for future developers to understand the purpose of each screen and its underlying implementation.


### **3. Customer Visit Creation**


#### **File Location:**
`./src/screens/Home/Options/Visits/VisitFormTabs`

**Component: `VisitFormTabs`**

**Imports:**
- **Core Libraries**: 
  - `react-native`, `expo-location`
  - API calls (`fetchPipelineDetails`, `fetchVisitPlanDetails`)
  - Utility functions (`validateFields`, `showToast`, `post`)
  - Custom components: `SafeAreaView`, `NavigationHeader`, `CustomTabBar`, `OverlayLoader`, etc.

**States:**
- **formData**: Holds the form values, e.g., customer name, site location, visit purpose, and timestamps (time in, time out).
- **isLoading & isSubmitting**: Flags to manage loading states while fetching data or submitting the form.
- **errors**: Stores validation errors to highlight incorrect or missing fields.
- **index**: Manages the current tab in the form (Customer, Visit Details, In & Out).
  
**API Calls:**
1. **`fetchVisitPlanDetails`**: Fetches details from a visit plan when provided a `visitPlanId`. Populates `customer`, `employee`, `dateAndTime`, and other related fields.
2. **`fetchPipelineDetails`**: If a `pipelineId` is available, it retrieves the associated customer details and updates the form accordingly.
3. **`post("/createCustomerVisitList")`**: Submits the entire form data to the server for creating a new customer visit.

**Tabs:**
1. **Customer Tab (`Customer`)**: 
   - Fields: `Customer Name`, `Employee Name`, `Site Location`, `Contact Person`, `Next Visit Date`, and `Visit Purpose`.
   - Fetches data from various dropdowns (customer list, site locations, visit purposes).
   - Allows the user to select values through modals and date pickers.
  
2. **Visit Details Tab (`VisitDetails`)**:
   - Fields: `Remarks`, `Image Upload`.
   - Enables attaching images and displaying thumbnails for uploaded images.
  
3. **In & Out Tab (`InAndOut`)**:
   - Fields: `Time In`, `Time Out`.
   - Date picker to select both fields, representing the duration of the customer visit.
  
**Form Validation (`validateFields`)**:
- Validates specific fields (`customer`, `dateAndTime`, `remarks`, `visitPurpose`, `timeIn`, `timeOut`) before submission. Displays errors if any fields are missing or invalid.

**Submission (`submit`)**:
- Compiles the form data into the required structure (e.g., `employee_id`, `date_time`, `customer_id`).
- Sends an API request to save the visit, and on success, a toast notification is shown, and the user is navigated back to the previous screen.

---

**Key Components:**
- **`TabView`**: Manages the display of multiple tabs.
- **`OverlayLoader`**: Displays a loading spinner during data fetching or form submission.
- **`DateTimePickerModal`**: Provides date and time selection functionality.
- **`ActionModal` & `DropdownSheet`**: Handles image uploads and dropdown selections for various fields.


## Documentation

[Documentation](https://linktodocumentation)


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`API_KEY`

`ANOTHER_API_KEY`

