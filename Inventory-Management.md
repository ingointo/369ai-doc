### **Inventory Management**


### **Inventory Screen - Conceptual Documentation**


#### **Purpose:**
The Inventory Management module allows users to track and manage inventory items. It supports functions such as scanning inventory, searching by box number, viewing inventory details, assigning responsible employees, and performing box-related operations.

#### **Key Features:**
1. **Inventory List:** Displays a list of all inventory items.
2. **Scan and Search:** Allows users to scan box codes or search by box number to retrieve inventory details.
3. **Inventory Detail View:** Displays detailed information about selected inventory, including responsible employees and actions like form submission for opening requests.
4. **FAB Actions:** Floating Action Button (FAB) to access common actions like scanning or searching inventory.
5. **Pagination Support:** Fetches more data when scrolling to the end of the list.
6. **Empty State Handling:** Provides a visual indication when no inventory data is available.

---

### **Technical Documentation**

#### **File Location:**
`src/screens/Inventory/InventoryScreen.js`

#### **State Variables:**
- `isFocused` (boolean): Tracks whether the screen is focused.
- `isVisibleModal` (boolean): Controls visibility of the input modal.
- `isFabOpen` (boolean): Manages the state of the Floating Action Button (FAB).
- `scanLoading` (boolean): Indicates loading status during scan actions.
- `modalLoading` (boolean): Indicates loading status during modal input search.
- `getDetail` (object): Holds detailed information about the selected inventory.
- `employee` (array): Stores employee data fetched for dropdown selections.
- `isVisibleCustomListModal` (boolean): Controls the custom list modal visibility.
- `isVisibleEmployeeListModal` (boolean): Manages visibility of the employee list modal.

#### **Functions:**
1. **`isResponsibleOrEmployee(inventoryDetails)`**
   - Checks if the current user is responsible for the inventory or an employee.
2. **`useEffect` (Multiple)**
   - Fetches employee data and refetches inventory data when the screen gains focus.
3. **`fetchData()`**
   - Fetches the inventory list data using `fetchInventoryBoxRequest`.
4. **`handleScan(scannedData)`**
   - Handles the scanning of inventory boxes and navigates based on scan results.
5. **`handleModalInput(text)`**
   - Handles searching for inventory by box name from the input modal.
6. **`handleLoadMore()`**
   - Fetches more inventory data when the user scrolls to the bottom.
7. **`handleBoxOpeningRequest(value)`**
   - Navigates to the inventory form based on the selected reason.
8. **`renderItem(item)`**
   - Renders individual inventory items or an empty state.
9. **`renderInventoryRequest()`**
   - Renders the list of inventory items or an empty state message.

#### **UI Components:**
- **SafeAreaView:** Wrapping component ensuring content is within safe area boundaries.
- **FAB.Group:** Floating action button with multiple options (scan, search by box).
- **FlashList:** List view optimized for performance, displaying inventory items.
- **InputModal:** Modal for entering box numbers.
- **CustomListModal:** List modal allowing selection of actions (like "Open Box").
- **EmployeeListModal:** Modal to assign an employee to the inventory item.
- **OverlayLoader:** Loader displayed during data fetching or scanning.

#### **Displayed Fields:**
- **Inventory List Screen:** Displays items from inventory including employee names, box numbers, etc.
- **Empty States:** Displays a message when no inventory data is available.
- **Detail Screen:** Displays inventory item details such as employees, responsible person, temporary assignees, and actions that can be taken (opening requests).

#### **Other Considerations:**
- **API Calls:** 
   - `fetchInventoryBoxRequest` for fetching inventory data.
   - `fetchInventoryDetails` and `fetchInventoryDetailsByName` for getting specific inventory information based on scans or search input.
   - `fetchEmployeesDropdown` for retrieving a list of employees for selection in the employee assignment process.

### **Open Inventory Box Request - Conceptual Documentation**
 
#### **Purpose:**
The **Inventory Creation** module allows users to create requests for inventory box actions, such as opening or managing inventory items, and submitting these requests for processing. It facilitates interactions with various inventory types such as sales, service, and returns.

#### **Key Features:**
1. **Inventory Details View:** Displays information about the inventory box, including name and associated items.
2. **Dynamic Fields:** Form fields dynamically update based on the selected reason (e.g., sales, service, returns).
3. **Item Management:** Users can choose items from the inventory and adjust their quantities as necessary.
4. **Request Submission:** Users can submit requests with remarks and item details, creating an inventory box request.
5. **Dropdown Integration:** Supports dropdown lists for selecting related references such as sales or purchase orders.
6. **Error Handling:** Validates form inputs, such as ensuring the correct quantity is selected based on reason.

---

### **Technical Documentation**

#### **File Location:**
`src/screens/inventory/InventoryForm.js`

#### **State Variables:**
1. **`itemsList` (array):** Holds the list of items in the inventory box.
2. **`isVisible` (boolean):** Controls the visibility of the dropdown sheet for selecting reference types.
3. **`selectedType` (string):** Tracks the type of reference being selected (e.g., sales, service).
4. **`chosenItem` (object | null):** Stores the currently selected item from the inventory.
5. **`loading` (boolean):** Controls the display of a loading indicator during request submission.
6. **`formData` (object):** Contains the user-inputted data for reason, references, and remarks.
7. **`dropdown` (object):** Stores dropdown options for various references like invoice, service, and returns.

#### **Functions:**
1. **`useEffect (fetchData)`**
   - Fetches dropdown data for invoice, service, purchase, stock transfer, and vendor bill when the component mounts.
2. **`handleFieldChange(field, value)`**
   - Updates the formData state based on user inputs for various fields.
3. **`handleQuantityChange(id, text)`**
   - Validates and updates the quantity of an inventory item based on the selected reason.
4. **`handleInventoryBoxRequest()`**
   - Submits the inventory box request by posting the form data to the server, including error handling and loading indicators.
5. **`renderDynamicField()`**
   - Renders dynamic form fields depending on the selected reason (e.g., sales, service).
6. **`toggleBottomSheet(type)`**
   - Controls the visibility of the dropdown sheet and sets the type of reference being selected.
7. **`renderBottomSheet()`**
   - Displays the dropdown options for selecting references like sales, service, and returns.
8. **`handleChooseItem(item)`**
   - Toggles the selection of an inventory item.

#### **UI Components:**
- **SafeAreaView:** Ensures that content is rendered within the safe boundaries of the device screen.
- **NavigationHeader:** Displays a navigation bar with the module’s title and back button.
- **RoundedScrollContainer:** A scrollable container for the form and inventory list.
- **FormInput:** Custom text input fields for various form elements, like selecting reasons and remarks.
- **DropdownSheet:** A modal component that shows dropdown options for selecting references like sales or services.
- **FlatList:** A list component that renders the inventory items, allowing selection and quantity changes.
- **OverlayLoader:** A loader displayed when the request is being processed.
- **Button:** A submit button to confirm and send the inventory box request.

#### **Displayed Fields:**
1. **Inventory Box Name:** The name of the inventory box (read-only).
2. **Reason:** A field that allows users to select the reason for creating the inventory request.
3. **Dynamic Fields:** Depending on the selected reason, fields for sales, service, returns, etc., are displayed.
4. **Item List:** A list of items within the inventory box, allowing users to select items and adjust their quantities.
5. **Remarks:** A multi-line input field where users can add additional comments or information regarding the request.

#### **Additional Considerations:**
1. **Data Validation:**
   - The system checks that a reason and at least one item are selected before submitting.
   - Quantity validation ensures that selected quantities do not exceed the available amount for certain reasons.
   
2. **Dropdown Data:**
   - Dropdown options are fetched from various APIs (`fetchInvoiceDropdown`, `fetchServiceDropdown`, etc.) and populated into the relevant fields.

3. **Submission Logic:**
   - The formData is structured into a request payload that includes items, quantities, reason, references, and remarks. It is submitted via a POST request to the `/createInventoryBoxRequest` endpoint.

---
### **Inventory Details - Conceptual Documentation**

**Purpose:**
The **Inventory Details** module is designed to display detailed information about a specific inventory box. This includes the box name, associated warehouse, date of creation, and a list of items inside the box.

**Key Features:**
- Displays the details of a selected inventory box such as box name, warehouse, and date.
- Lists all items in the inventory box.
- Provides an empty state visual when there are no items.
- Allows navigation back to the main inventory screen.

---

### **Inventory Details - Technical Documentation**

**File Location:**
- Path: `./src/modules/inventory/InventoryDetails.js`

**State Variables:**
1. **inventoryDetails:** Holds the information about the inventory box and its items, passed via the route parameters.

**Functions:**

1. **renderItem(item):** 
   - Renders an individual item from the inventory box. If the item is empty, it renders an `EmptyItem` component.
   - Uses the `InventoryBoxList` component to display items.
   
2. **renderEmptyState():** 
   - Returns the UI for the empty state, showing an image and message when no items are available.

3. **renderContent():**
   - Displays the list of items using a `FlatList`, showing each box item. If no items are available, it renders the empty state.

**UI Components:**
- **SafeAreaView:** Provides a safe area container for the content, ensuring it doesn’t overlap with the status bar.
- **NavigationHeader:** Custom header that includes a back button to navigate back to the previous screen.
- **RoundedScrollContainer:** Wraps content in a scrollable container with rounded edges.
- **DetailField:** Custom component used to display label-value pairs (e.g., Inventory Box name, Warehouse, and Date).
- **Text:** Used to display the label "Box Items."
- **FlatList:** Used to display the inventory box items list.
- **EmptyState:** Component displayed when the inventory box has no items.

**Displayed Fields:**
- **Inventory Box Name:** Shows the name of the selected inventory box.
- **Warehouse:** Displays the name of the warehouse associated with the inventory box.
- **Date:** Shows the creation date of the inventory box, formatted as `yyyy-MM-dd hh:mm a`.
- **Box Items List:** Displays a list of items in the inventory box or an empty state message if no items are available.

---
