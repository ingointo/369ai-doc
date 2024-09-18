
## **Visit Plan Screen**

### **Conceptual Documentation**

**Purpose:**
The `VisitsPlanScreen` component is designed to display a list of visit plans for a specific date. Users can view, filter, and manage visit plans, including sending plans for approval and navigating to details or creation forms.

**Key Features:**
- **Date Selector:** Allows users to pick a date and view visit plans for that day.
- **Approval Button:** Enables sending selected visit plans for approval.
- **Loading and Empty States:** Displays loading animations and messages when no data is available.
- **FAB Button:** Provides quick access to the Visit Plan creation form.
- **Modal Windows:** Confirmation and rules modals for user interactions.

**Technical Documentation**

**File Location:** `src/screens/Home/Options/VisitsPlan/VisitPlanScreen.js`

**State Variables:**
- `isVisible` - Controls the visibility of the rules modal.
- `date` - The selected date for which visit plans are fetched.
- `isConfirmationModalVisible` - Manages the visibility of the confirmation modal.
- `showButton` - Object to conditionally show approval and visit buttons.

**Functions:**
- `fetchData` - Fetches visit plans for the specified date and employee.
- `fetchMoreData` - Fetches additional visit plans for pagination.
- `handleLoadMore` - Triggers fetching of more data when scrolled to the end.
- `updatePendingApproval` - Updates the approval status of selected visit plans.
- `renderItem` - Renders each item in the list, including empty states.
- `renderEmptyState` - Displays an empty state when no data is available.
- `renderContent` - Renders the list of visit plans with a loading footer.
- `renderVisitPlan` - Conditionally renders the visit plans or empty state.

**UI Components:**
- `NavigationHeader` - Displays the header with navigation controls.
- `VerticalScrollableCalendar` - Calendar for selecting dates.
- `RoundedContainer` - Container with rounded corners for styling.
- `FABButton` - Floating action button for creating new visit plans.
- `RulesModal` - Modal for displaying rules related to visit plans.
- `ConfirmationModal` - Modal for confirming actions like sending plans for approval.

**Display Fields:**
- Visit plans are displayed in a list format with options to load more data and a floating button to create new visit plans.

---

## **Visit Plan Form**

### **Conceptual Documentation**

**Purpose:**
The `VisitPlanForm` component is used for creating and submitting a new visit plan. It allows users to input details such as customer, assigned employee, date and time, visit purpose, and remarks.

**Key Features:**
- **Form Inputs:** Allows users to input and select visit plan details.
- **Date & Time Pickers:** Enables users to select or input date and time.
- **Dropdowns:** For selecting customer, assignee, visit purpose, etc.
- **Validation:** Ensures required fields are filled before submission.
- **Submission Button:** Submits the form data to create a new visit plan.

**Technical Documentation**

**File Location:** `src/screens/Home/Options/VisitsPlan/VisitPlanForm.js`

**State Variables:**
- `isSubmitting` - Indicates whether the form is in the process of submission.
- `isVisible` - Controls visibility of dropdown sheets.
- `selectedType` - Determines which dropdown sheet is shown.
- `isTimePickerVisible` - Manages visibility of the time picker.
- `isDateTimePickerVisible` - Manages visibility of the date-time picker.
- `errors` - Holds validation errors for form fields.
- `formData` - Holds the form data being entered by the user.
- `dropdown` - Contains dropdown options for form fields.

**Functions:**
- `handleFieldChange` - Updates form field values and handles validation errors.
- `fetchDropdownData` - Fetches dropdown data for form inputs.
- `handleTimeChange` - Updates date-time based on time picker input.
- `handleDateChange` - Updates date-time based on date picker input.
- `toggleBottomSheet` - Toggles visibility of the dropdown sheets.
- `validateForm` - Validates form fields before submission.
- `handleSubmit` - Submits the form data to create a new visit plan.

**UI Components:**
- `FormInput` - Input fields with dropdowns for selecting values.
- `DropdownSheet` - Custom dropdown component for selection.
- `LoadingButton` - Button with a loading indicator for form submission.
- `DateTimePickerModal` - Modals for selecting date and time.

**Display Fields:**
- **Customer Name:** Select customer for the visit.
- **Assigned To:** Select employee assigned for the visit.
- **Date & Time:** Select date and time of the visit.
- **Visit Purpose:** Select the purpose of the visit.
- **Remarks:** Additional comments or notes.

---

## **Visit Plan Details**

### **Conceptual Documentation**

**Purpose:**
The `VisitPlanDetails` component provides a detailed view of a specific visit plan. It displays all relevant details and offers options to approve or schedule a new visit if applicable.

**Key Features:**
- **Detail Display:** Shows detailed information about a visit plan.
- **Conditional Buttons:** Approve button and New Visit button are shown based on the visit plan status and user role.
- **Loading and Confirmation:** Includes a loading overlay and confirmation modal for actions.

**Technical Documentation**

**File Location:** `src/screens/Home/Options/VisitsPlan/VisitPlanDetails.js`

**State Variables:**
- `details` - Holds the visit plan details fetched from the API.
- `isLoading` - Indicates whether data is being fetched.
- `isConfirmationModalVisible` - Manages visibility of the confirmation modal.
- `showButton` - Object to conditionally display approval and visit buttons.

**Functions:**
- `fetchDetails` - Fetches visit plan details and determines button visibility based on the fetched data.
- `updateApprovalStatus` - Updates the approval status of the visit plan.
- `showToastMessage` - Displays messages for user feedback.

- `fetchDetails`
  - **Purpose:** Fetches visit plan details and determines button visibility based on the fetched data.
  - **Button Visibility Condition:** Updates the `showButton` state to conditionally show the approval button if the `approval_status` is 'Pending' and the current user is the visit employee's manager, or the visit button if the `approval_status` is 'Approved' and the visit status is 'Not visited' and the current user is the visit employee.

- `updateApprovalStatus`
  - **Purpose:** Updates the approval status of the visit plan.
  - **Button Visibility Condition:** This function is invoked when the approval button is pressed. The visibility of the approval button is controlled based on the conditions defined in the `fetchDetails` function.

- `showToastMessage`
  - **Purpose:** Displays a toast message for user feedback.
  - **Button Visibility Condition:** This function does not affect button visibility but provides feedback based on actions like fetching details or updating approval status.


**UI Components:**
- `NavigationHeader` - Displays the screen title and back navigation button.
- `DetailField` - Component to display individual fields of visit plan details.
- `LoadingButton` - Button for approving or creating a new visit.
- `OverlayLoader` - Loader shown while fetching data.
- `ConfirmationModal` - Modal for confirming approval actions.

**Display Fields:**
- **Visit Date:** Date of the visit.
- **Customer Name:** Name of the customer.
- **Assigned To:** Employee assigned for the visit.
- **Created By:** Person who created the visit plan.
- **Approval Status:** Current approval status.
- **Visit Purpose:** Purpose of the visit.
- **Visit Status:** Current status of the visit.
- **Remarks:** Any additional comments or notes.

