# **369ai.Biz** 

## **Table of Contents**

1. [Introduction](#1-introduction)  
   1.1 [Overview](#11-overview)  
   1.2 [Purpose of the Project](#12-purpose-of-the-project)  
   1.3 [Technologies Used](#13-technologies-used)  
   1.4 [Prerequisites](#14-prerequisites)

2. [Project Structure](#2-project-structure)  
   2.1 [Overview](#21-overview)  
   2.2 [Explanation of Folder and File Organization](#22-explanation-of-folder-and-file-organization)  
   2.3 [Detailed Project Structure for 369ai.Biz](https://github.com/ingointo/369ai-doc/blob/main/project-structure.md)

3. [Components Documentation](#3-components-documentation)  
   3.1 [Overview](#31-overview)  
   3.2 [Component Index](#32-component-index) 

4. [Store Documentation](#4-store-documentation)  
   4.1 [auth](#41-auth)  
   4.2 [box](#42-box)  
   4.3 [currency](#43-currency)  
   4.4 [product](#44-product)  

5. [API Documentation](#5-api-documentation)  
   5.1 [Folder Structure & Explanation](#51-folder-structure)  

6. [Hooks Documentation](#6-hooks-documentation)   
   6.1 [Folder Structure & Explanation](#61-folder-structure) 

7. [Navigation Documentation](#7-navigation-documentation)   
   7.1 [Structure](#71-structure)     
   7.2 [Navigators](#72-navigators)   
   7.3 [Navigation Flow](#73-navigation-flow)  
   7.4 [Key Features](#74-key-features)

8. [Utils Documentation](#8-utils-documentation)  
   8.1 [Overview](#81-overview)   
   8.2 [Folder Structure](#82-folder-structure)  
   8.3 [Common Utilities](#83-common-utilities)   
   8.4 [Config Utilities](#84-config-utilities)  
   8.5 [Formatter Utilities](#85-formatter-utilities)    
   8.6 [Validation Utilities](#86-validation-utilities)  
   8.7 [Usage Examples](#87-usage-examples)  
   1.  [String Utilities](#1-string-utilities)  
   2.  [Toast Utility](#2-toast-utility)  
   3.  [Date Formatting](#3-date-formatting)  
   4.  [Get Config](#4-get-config)  
   5.  [Data Fromatting](#5-data-formatting)  
   6.  [Field Validation](#6-field-validation)  
   7.  [Validation Functions](#7-validation-functions)  

9. [Step-by-Step Guide for Dynamically Building an Expo App with Different Currencies and Project Name/ID](#9-step-by-step-guide-for-dynamically-building-an-expo-app-with-different-currencies-and-project-nameid)  

  



## 1. Introduction

### 1.1 Overview
369ai.Biz is a comprehensive cross-platform employee management and enterprise resource planning (ERP) application designed to streamline business operations across various domains. Built using React Native, it offers an all-in-one solution for managing multiple facets of a company’s workflow, from employee attendance, task manager, transaction auditing, visits plan, customer visits, customer relationship management (CRM) and inventory management(INVMGT) ,...

The application is designed for businesses seeking to improve operational efficiency by centralizing core functions into a single, accessible platform. The app targets business managers, employees, and administrative staff who need to track tasks, manage projects, and handle client relationships efficiently.

### 1.2 Purpose of the Project

The purpose of **369ai.Biz** is to provide businesses with a powerful, unified platform that simplifies and automates critical operational processes. By integrating multiple modules—such as employee management, inventory tracking, task management, CRM, and auditing—into a single, cross-platform mobile application, this project aims to:

- **Streamline Business Operations**: Centralize various business functions to reduce complexity, minimize errors, and enhance productivity.
- **Improve Workflow Efficiency**: Enable managers and employees to handle tasks, track progress, and collaborate effectively from any location.
- **Enhance Customer Relationship Management**: Provide tools for managing leads, enquiries, and pipelines to improve customer interactions and business growth.
- **Optimize Resource Management**: Inventory, spare parts request, and quick service to ensure the effective use of company resources.
<!-- - **Ensure Compliance and Auditing**: Facilitate proper documentation and transaction auditing to maintain compliance with business processes and regulations. -->

### 1.3 Technologies Used

- **React Native**: A framework for building native applications using React.
- **Expo**: A platform that streamlines the development and deployment of React Native apps.
- **Zustand**: A lightweight state management library for React and React Native applications.
- **React Navigation**: A robust library for managing routing and navigation within React Native apps, including stack, tab, and drawer navigators.
  - **`@react-navigation/native-stack`**: Provides stack navigation with a more native-like experience.
  - **`@react-navigation/bottom-tabs`**: Tab navigation for switching between screens.
  - **`@react-navigation/material-top-tabs`**: Provides top tab navigation.
- **Axios**: A promise-based HTTP client for making API requests.
- **Date-fns**: A modern JavaScript library for working with dates.
- **Lodash**: A utility library offering helpful functions for working with arrays, objects, and other data types.
- **Immer**: A library for creating immutable state updates.
- **React Native Reanimated**: Enables smooth animations and gesture handling.
- **React Native Gesture Handler**: Enhances touch-based interactions in React Native applications.
- **React Native Paper**: A UI component library that adheres to Material Design principles.
- **React Native Maps**: Provides maps functionality in React Native applications.
- **React Native Camera & Barcode Scanner**: Enables camera access and barcode scanning functionalities.
- **Lottie React Native**: Used to add animations in the app with minimal effort.
- **Tailwind CSS**: A utility-first CSS framework used for styling React Native components through the NativeWind library.
- **Moment.js**: A library for parsing, manipulating, and formatting dates and times.
- **React Native SVG & Charts**: Used for rendering SVG elements and charts.
- **React Native Modal**: Provides modal views for custom user interactions.
- **React Native Toast Message**: Displays customizable toast notifications within the app.
- **React Native Webview**: Embeds web content in React Native apps.
- **React Native Signature Canvas**: Allows users to capture signatures within the application.
- **Babel**: A JavaScript compiler that helps transform your JavaScript code to be compatible across different browsers and environments.

### 1.4 Prerequisites
- Node.js (v14 or later)
- Expo CLI
- Yarn or npm (use yarn instead of npm that is better & faster in my exp.. )
- eas login 

## 2. Project Structure

### 2.1 Overview

The following is the structure of the project that provides an organized overview of directories and files:

### 2.2 Explanation of Folder and File Organization

- **`App.js`**: The entry point of the React Native app.

-  **`app.json`**:
   Configuration file for the Expo application.

- **`assets`**:
   This directory contains the application's static assets like icons, images, fonts, and animations.
   - **android/**: Icons for Android devices.
   - **animations/**: Lottie JSON files for app animations.
   - **fonts/**: Urbanist font family used for text rendering.
   - **icons/**: Various categories for bottom tabs, modals, etc.
   - **images/**: General app imagery like empty states, headers, banners, logos, etc.

- **`src`**:
   This is the main source directory that contains all the logic and components.
   
   - **api/**:
     Handles API configuration and requests.
     - `config/`: API configuration files.
     - `details/`: API related to fetching detailed information.
     - `dropdowns/`: API for dropdown-related data.
     - `endpoints/`: Centralized endpoints.
     - `services/`: General API services used across the app.
     - `uploads/`: API for handling file uploads.
     - `utils/`: Utility functions like error handling.

   - **components/**:
     This folder contains all the reusable components for the application.
     - **Calendar/**: Calendar-related components like `CalendarScreen` and `VerticalScrollableCalendar`.
     - **Categories/**: Components related to categories, like `CategoryList`.
     - **Common/**: Contains common reusable components for the application.
        - **`BottomSheets/`**: Dropdown Components Single selection `DropdwonSheet` & Multiple selection `MultiSelectDropdownSheet` and styles for various bottom sheets used for displaying like additional information or options.
        - **`Button/`**: Components related to button likes `FABButton` , `LoadingButton` ,  `PressableInput` including different styles and also loading variations used across the application.
        - **`CheckBox/`**: Components for checkbox elements, including custom checkboxes and related functionality.
        - **`Detail/`**: Components for displaying detailed information, such as `DetailField` , `DetailCheckBox`, `ProductDetail` .
        - **`TextInput/`**: Components for text input fields, including variations like password fields and search inputs.
        - **`empty/`**: Components for empty listing & fill the empty space.

      - **CRM/**: Components handling CRM functionalities like `FollowUpList`, `Meetingslist`, and `VisitList`.
       - **Header/**: Components for headers including `NavigationHeader` and `BottomSheetHeader`.
      - **Loader/**: Loading animations and overlays like `AnimatedLoader` and `OverlayLoader`.
      - **Modal/**: Various modals like `ActionModal`,  `AddUpdateModal`, `ConfirmationModal`, `CustomListModal`, `LogoutModal` and more.
      - **Options/**: Components for handling different options or list items.
      - **Product/**: Components for displaying product-related data.
      - **Scanner/**: Barcode and other scanner-related components.
      - **containers/**: Containers for managing layouts like `RoundedScrollContainer`, `SafeAreaView`, and more.
  - **`constants/`**: Constants used throughout the app.
  - **`hooks/`**: Custom React hooks.
  - **`navigation/`**: Navigation setup and configurations.
  - **`screens/`**: Feature-specific screens.
  - **`store/`**: Redux or Zustand state management.
  - **`utils/`**: Utility functions and helpers.

## 3. Components Documentation

### 3.1 Overview
Each component in this project is reusable and designed for flexibility this can be easily integrated into any React Native project. Below is a detailed breakdown of each component, including prop descriptions and default values. 

### 3.2 Component Index
1. [CalendarScreen](#1-calendarscreen)
2. [VerticalScrollableCalendar](#2-verticalscrollablecalendar)
3. [DropdownSheet](#3-dropdownsheet)
4. [MultiSelectDropdownSheet](#4-multiselectdropdownsheet)
5. [Button](#5-button)
6. [FABButton](#6-fabbutton)
7. [LoadingButton](#7-loadingbutton)
8. [PressableInput](#8-pressableinput)
9. [CheckBox](#9-checkbox)
10. [DetailCheckBox](#10-detailcheckbox)
11. [SafeAreaView](#11-safeareaview)
12. [SearchContainer](#12-searchcontainer)
13. [RoundedContainer](#13-roundedcontainer)
14. [RoundedScrollContainer](#14-roundedscrollcontainer)
15. [BottomSheetHeader](#15-bottomsheetheader)
16. [NavigationHeader](#16-navigationheader)
17. [AnimatedLoader](#17-animatedloader)
18. [OverlayLoader](#18-overlayloader)
19. [CustomTabBar](#19-customtabbar)
20. [DetailField](#20-detailfield)
21. [TextInput](#21-textinput)


### 1. CalendarScreen

A scrollable calendar interface.

### Usage
```jsx
import { CalendarScreen } from '@components/Calendar';

<CalendarScreen 
  markedDates={{ '2024-09-05': { marked: true } }} 
  onDayPress={(day) => console.log(day)}
  theme={{ selectedDayBackgroundColor: 'blue' }} 
/>
```

### Props

| Prop           | Type     | Description                                      | Default Value |
| -------------- | -------- | ------------------------------------------------ | ------------- |
| `markedDates`  | Object   | Object containing marked dates                   | `{}`          |
| `onDayPress`   | Function | Function called when a date is pressed            | `() => {}`    |
| `theme`        | Object   | Custom theme for calendar appearance             | `{}`          |
| `style`        | Object   | Additional styles for the calendar component      | `{}`          |

---

### 2. VerticalScrollableCalendar

A vertical scrollable calendar interface.

### Usage

```jsx
import { VerticalScrollableCalendar } from '@components/Calendar';

<VerticalScrollableCalendar 
  date={new Date()} 
  onChange={(day) => console.log(day)} 
/>
```

### Props

| Prop         | Type     | Description                                    | Default Value |
| ------------ | -------- | ---------------------------------------------- | ------------- |
| `date`       | Date     | The current selected date                      | `new Date()`  |
| `onChange`   | Function | Function called when the user selects a new day | `() => {}`    |

---

### 3. DropdownSheet

A bottom sheet dropdown for selecting options.

### Usage


```jsx
import { DropdownSheet } from '@components/common/BottomSheets';

<DropdownSheet 
  isVisible={true} 
  items={[{ label: 'Option 1' }, { label: 'Option 2' }]} 
  onValueChange={(item) => console.log(item)} 
  title="Select Option" 
  onClose={() => console.log('Sheet closed')} 
/>
```

### Props

| Prop            | Type      | Description                                             | Default Value   |
| --------------- | --------- | ------------------------------------------------------- | --------------- |
| `isVisible`     | Boolean   | Controls the visibility of the bottom sheet             | `false`         |
| `items`         | Array     | Array of items to display in the dropdown               | `[]`            |
| `onValueChange` | Function  | Function called when an item is selected                | `() => {}`      |
| `title`         | String    | Title to display at the top of the dropdown             | `''`            |
| `onClose`       | Function  | Function called when the sheet is closed                | `() => {}`      |

---

### 4. MultiSelectDropdownSheet

A bottom sheet dropdown for selecting multiple options.

### Usage
```jsx
import { MultiSelectDropdownSheet } from '@components/common/BottomSheets';

<MultiSelectDropdownSheet 
  isVisible={true} 
  items={[{ label: 'Option 1' }, { label: 'Option 2' }]} 
  onValueChange={(selectedItems) => console.log(selectedItems)} 
  title="Select Multiple" 
  previousSelections={['Option 1']} 
  onClose={() => console.log('Sheet closed')} 
/>
```

### Props

| Prop                | Type      | Description                                                   | Default Value   |
| ------------------- | --------- | ------------------------------------------------------------- | --------------- |
| `isVisible`         | Boolean   | Controls the visibility of the bottom sheet                   | `false`         |
| `items`             | Array     | Array of items to display in the dropdown                     | `[]`            |
| `onValueChange`     | Function  | Function called when items are selected                       | `() => {}`      |
| `title`             | String    | Title to display at the top of the dropdown                   | `''`            |
| `previousSelections`| Array     | List of items selected previously                             | `[]`            |
| `onClose`           | Function  | Function called when the sheet is closed                      | `() => {}`      |

### 5. Button

A customizable button with loading state and disabled state handling.

### Usage

```jsx
import { Button } from '@components/common/Button';

<Button 
  title="Submit" 
  onPress={() => console.log('Button Pressed')} 
  backgroundColor="#3498db" 
  color="white"
  loading={false} 
  disabled={false}
/>
```

### Props

| Prop            | Type     | Description                                     | Default            |
| --------------- | -------- | ----------------------------------------------- | ------------------ |
| `title`         | string   | The text to display inside the button            | `Submit`           |
| `onPress`       | function | Function to call when the button is pressed      | `() => {}`         |
| `color`         | string   | Text color of the button                        | `white`            |
| `backgroundColor`| string   | Background color of the button                  | `COLORS.button`    |
| `disabled`      | boolean  | Disable the button interaction                  | `false`            |
| `loading`       | boolean  | Display a loading spinner instead of text       | `false`            |

---

### 6. FABButton

A Floating Action Button (FAB) to trigger an action, commonly used for adding items.

### Usage

```jsx
import { FABButton } from '@components/common/Button';

<FABButton onPress={() => console.log('FAB Pressed')} />
```

### Props

| Prop      | Type     | Description                       | Default |
| --------- | -------- | ---------------------------------- | ------- |
| `onPress` | function | Function to call when FAB is pressed | `() => {}` |

---

### 7. LoadingButton

A button with a loading spinner to indicate a process in progress.

### Usage

```jsx
import { LoadingButton } from '@components/common/Button';

<LoadingButton 
  title="Loading..." 
  onPress={() => console.log('Loading Button Pressed')} 
  backgroundColor="#27ae60" 
  loading={true} 
/>
```

### Props

| Prop            | Type     | Description                                     | Default            |
| --------------- | -------- | ----------------------------------------------- | ------------------ |
| `title`         | string   | The text to display inside the button            | `Submit`           |
| `onPress`       | function | Function to call when the button is pressed      | `() => {}`         |
| `color`         | string   | Text color of the button                        | `white`            |
| `backgroundColor`| string   | Background color of the button                  | `COLORS.button`    |
| `loading`       | boolean  | Display a loading spinner instead of text       | `false`            |

---

### 8. PressableInput

An input field that can be pressed to trigger an action, with optional icon support.

### Usage

```jsx
import { PressableInput } from '@components/common/Button';

<PressableInput 
  placeholder="Press here" 
  handlePress={() => console.log('Input pressed')} 
  dropIcon="chevron-down" 
/>
```

### Props

| Prop         | Type     | Description                                          | Default      |
| ------------ | -------- | ---------------------------------------------------- | ------------ |
| `placeholder`| string   | Placeholder text for the input                       | `''`         |
| `dropIcon`   | string   | Name of the icon to display on the right             | `''`         |
| `handlePress`| function | Function to call when the input is pressed           | `() => {}`   |

---
### 9. CheckBox

A checkbox with a label, customizable to handle checked and unchecked states.

### Usage

```jsx
import { CheckBox } from '@components/common/CheckBox';

<CheckBox 
  label="Accept Terms" 
  checked={true} 
  onPress={(newValue) => console.log(newValue)} 
/>
```

### Props

| Prop      | Type     | Description                               | Default   |
| --------- | -------- | ----------------------------------------- | --------- |
| `label`   | string   | The label text displayed next to the checkbox | `''`    |
| `checked` | boolean  | Whether the checkbox is checked            | `false`   |
| `onPress` | function | Function called when the checkbox is pressed | `() => {}` |

---

### 10. DetailCheckBox

A read-only checkbox used specifically for displaying the checked or unchecked state in detailed views. For interactive checkboxes, consider using the [CheckBox](#9-checkbox) component instead.

### Usage

```jsx
import { DetailCheckBox } from '@components/common/Detail';

<DetailCheckBox 
  label="Is Active" 
  checked={true} 
/>
```

### Props

| Prop      | Type     | Description                         | Default   |
| --------- | -------- | ----------------------------------- | --------- |
| `label`   | string   | The label text displayed next to the checkbox | `''` |
| `checked` | boolean  | Whether the checkbox is checked     | `false`  |

---


### 11. SafeAreaView
A view that takes care of safe area constraints, ensuring content does not overlap system UI like the status bar.

### Usage

```jsx
import { SafeAreaView } from '@components/containers';

<SafeAreaView backgroundColor="blue">
  <Text>Content within safe area</Text>
</SafeAreaView>
```

### Props

| Prop             | Type      | Description                                                | Default Value             |
| ---------------- | --------- | ---------------------------------------------------------- | ------------------------- |
| `children`       | Node      | The content to display inside the safe area                | `null`                    |
| `backgroundColor`| String    | Background color of the SafeAreaView                       | `COLORS.primaryThemeColor`|

---


### 12. SearchContainer
A search input component with a magnifying glass icon.

### Usage

```jsx
import { SearchContainer } from '@components/containers';

<SearchContainer placeholder="Search" onChangeText={(text) => console.log(text)} />
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `placeholder`    | String    | Placeholder text for the search input                      | `''`             |
| `onChangeText`   | Function  | Function to call when the input text changes               | `() => {}`       |

---

### 13. RoundedContainer
A container with rounded top corners.

### Usage

```jsx
import { RoundedContainer } from '@components/containers';

<RoundedContainer backgroundColor="lightgrey">
  <Text>Content goes here</Text>
</RoundedContainer>
```

### Props

| Prop             | Type     | Description                                                | Default Value    |
| ---------------- | -------- | ---------------------------------------------------------- | ---------------- |
| `children`       | Node     | The content to display inside the container                 | `null`           |
| `backgroundColor`| String   | Background color of the container                          | `COLORS.white`   |

---

### 14. RoundedScrollContainer
A scrollable container with rounded top corners, useful for wrapping content that may require scrolling.

### Usage

```jsx
import { RoundedScrollContainer } from '@components/containers';

<RoundedScrollContainer backgroundColor="lightgrey">
  <Text>Scrollable content goes here</Text>
</RoundedScrollContainer>
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `children`       | Node      | The content to display inside the container                 | `null`           |
| `backgroundColor`| String    | Background color of the container                          | `COLORS.white`   |
| `borderRadius`   | Boolean   | Whether to apply rounded corners to the container          | `true`           |
| `scrollEnabled`  | Boolean   | Whether scrolling is enabled                               | `true`           |

---


### 15. BottomSheetHeader
A header component for bottom sheets with an optional "plus" icon for additional actions.

### Usage

```jsx
import { BottomSheetHeader } from '@components/Header';

<BottomSheetHeader title="Title" plusIcon onPress={() => console.log('Plus icon pressed')} />
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `title`          | String    | The text to display in the header                          | `''`             |
| `plusIcon`       | Boolean   | Whether to show the plus icon                              | `false`          |
| `onPress`        | Function  | Function to call when the plus icon is pressed             | `() => {}`       |

---

### 16. NavigationHeader
A customizable header with a back button, optional icons, and a logo.

### Usage

```jsx
import { NavigationHeader } from '@components/Header';

<NavigationHeader
  title="Page Title"
  onBackPress={() => console.log('Back pressed')}
  iconOneName="home"
  iconOnePress={() => console.log('Home icon pressed')}
/>
```

### Props

| Prop             | Type      | Description                                                | Default Value             |
| ---------------- | --------- | ---------------------------------------------------------- | ------------------------- |
| `title`          | String    | Title to display in the header                             | `''`                      |
| `onBackPress`    | Function  | Function to call when the back button is pressed           | `() => {}`                |
| `iconOneName`    | String    | Name of the first icon to display on the right side        | `''`                      |
| `iconOnePress`   | Function  | Function to call when the first icon is pressed            | `() => {}`                |
| `iconTwoName`    | String    | Name of the second icon to display                         | `''`                      |
| `iconTwoPress`   | Function  | Function to call when the second icon is pressed           | `() => {}`                |
| `iconThreeName`  | String    | Name of the third icon to display                          | `''`                      |
| `iconThreePress` | Function  | Function to call when the third icon is pressed            | `() => {}`                |

---

### 17. AnimatedLoader
A component that displays an animated loader, useful for showing loading states.

### Usage

```jsx
import { AnimatedLoader } from '@components/Loader';

<AnimatedLoader visible={true} animationSource={require('path-to-animation.json')} />
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `visible`        | Boolean   | Controls the visibility of the loader                      | `false`          |
| `animationSource`| Object    | Path to the Lottie animation JSON                          | `null`           |

---

### 18. OverlayLoader
An overlay loader that covers the entire screen with a loading indicator.

### Usage

```jsx
import { OverlayLoader } from '@components/Loader';

<OverlayLoader visible={true} backgroundColor="rgba(0, 0, 0, 0.5)" />
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `visible`        | Boolean   | Controls the visibility of the overlay loader              | `false`          |
| `backgroundColor`| String    | Background color of the overlay                            | `transparent`    |

---

### 19. CustomTabBar
A custom tab bar for React Native Top tab navigation.

### Usage

```jsx
import { CustomTabBar } from '@components/TabBar';

<CustomTabBar scrollEnabled={true} />
```

### Props

| Prop             | Type      | Description                                                | Default Value    |
| ---------------- | --------- | ---------------------------------------------------------- | ---------------- |
| `scrollEnabled`  | Boolean   | Enables or disables scrolling on the tab bar               | `true`           |

---

### 20. DetailField

A detail view field for displaying non-editable information with optional icons.

### Usage

```jsx
import { DetailField } from '@components/common/Detail';

<DetailField 
  label="Username" 
  value="John Doe" 
  iconName="account" 
/>
```

### Props

| Prop      | Type     | Description                          | Default   |
| --------- | -------- | ------------------------------------ | --------- |
| `label`   | string   | The label text displayed above the input | `''`    |
| `value`   | string   | The value displayed inside the input | `''`     |
| `iconName`| string   | Name of the icon to display on the right | `''`    |

---

### 21. TextInput
A customizable `TextInput` component that includes features like error handling, password hiding, icons, and label with optional asterisk for required fields.

#### Usage

```jsx
import { TextInput } from '@components/common/TextInput';

<TextInput
  label="Username"
  placeholder="Enter your username"
  iconName="account"
  required={true}
  error="This field is required"
  onChangeText={(text) => console.log(text)}
  onFocus={() => console.log('Focused')}
/>
```

### Props

| Prop         | Type     | Description                                                                 | Default Value  |
| ------------ | -------- | --------------------------------------------------------------------------- | -------------- |
| `label`      | String   | The label text for the input field                                           | `''`           |
| `labelColor` | String   | Color of the label text                                                      | `COLORS.black` |
| `iconName`   | String   | The name of the icon to display next to the input field                      | `null`         |
| `error`      | String   | Error message to display when validation fails                               | `''`           |
| `onPress`    | Function | Function to call when the input field is pressed                             | `null`         |
| `password`   | Boolean  | If true, enables password hiding functionality                               | `false`        |
| `dropIcon`   | String   | The name of the drop-down icon to display                                    | `null`         |
| `login`      | Boolean  | If true, applies a specific login style                                      | `false`        |
| `validate`   | Boolean  | If true, enables validation state (displays error icon)                      | `false`        |
| `column`     | Boolean  | If true, aligns the label and input vertically; if false, aligns them horizontally | `true`      |
| `required`   | Boolean  | If true, displays a red asterisk next to the label for required fields        | `false`        |
| `onFocus`    | Function | Callback function when the input is focused                                  | `() => {}`     |
| `...props`   | Various  | Passes additional props to the underlying `RNTextInput`                      | `null`         |

---

#### Features

- **Label with Asterisk**: Displays an optional asterisk next to the label for required fields.
- **Password Toggle**: Allows the user to show or hide the password in the input field using an eye icon.
- **Error Handling**: Displays error messages and highlights the input border in red if validation fails.
- **Icons**: Supports icons on the right side of the input field, including a password toggle and error icon.

---

#### Component Breakdown

- **Label**: Displays a text label above or beside the input field.
- **TextInput**: A styled `TextInput` from React Native, which handles the input behavior.
- **Error Handling**: Shows an error message if the `error` prop is passed.
- **Password Visibility**: A toggle button (eye icon) for showing or hiding passwords when `password` prop is true.
- **Validation Icon**: An alert icon if `validate` is true and validation fails.

## 4. Store Documentation

The `stores` folder contains Zustand-based state management files that help manage various global states across the application. These stores provide centralized data handling and are organized into specific modules: `auth`, `box`, `currency`, and `product`.

#### 4.1 `auth` Folder

**File**: `useAuthStore.js`

This store manages the authentication status of users.

- **State Variables**:
  - `isLoggedIn`: Tracks the login status (`boolean`).
  - `user`: Stores the currently logged-in user’s details.
- **Actions**:
  - `login(userData)`: Updates the state to reflect a logged-in user with the provided `userData`.
  - `logout()`: Resets the authentication state, logging out the user.

#### 4.2 `box` Folder

**File**: `useInspectionStore.js`

This store tracks the inspection status of boxes.

- **State Variables**:
  - `inspectedIds`: Stores an array of IDs of the inspected boxes.
- **Actions**:
  - `addInspectedId(id)`: Adds a new box ID to the inspected list.
  - `resetInspectedIds()`: Resets the inspection state by clearing all inspected IDs.

#### 4.3 `currency` Folder

**File**: `useCurrencyStore.js`

This store handles currency selection based on the user's package.

- **State Variables**:
  - `currency`: Tracks the selected currency (default: AED).
- **Actions**:
  - `setCurrency(packageName)`: Dynamically sets the currency based on the package name, switching between AED and OMR depending on the environment variable `EXPO_PUBLIC_PACKAGE_NAME_OMAN`.

#### 4.4 `product` Folder

**File**: `useProductStore.js`

This store manages the products added to the application.

- **State Variables**:
  - `products`: Stores an array of product objects.
- **Actions**:
  - `addProduct(product)`: Adds a product if it doesn't already exist or updates an existing product with new quantity and price information.
  - `removeProduct(productId)`: Removes a product from the store by its ID.
  - `clearProducts()`: Clears all products from the store.

## 5. **API Documentation**

The API folder contains several subfolders that organize the API configuration, details, dropdowns, endpoints, and services for the 369ai application. The structure and usage of each section are documented below:


### 5.1 **Folder Structure**
- `config/`  
  Contains the base API configuration for the application.

- `details/`  
  Handles API calls related to fetching detailed information, such as invoice details, vendor details, etc.

- `dropdowns/`  
  Manages dropdown data used in forms and selection lists across the application.

- `endpoints/`  
  Holds the API endpoint constants for various sections of the application.

- `services/`  
  Contains utility functions for common API operations (like GET, POST, PUT, etc.) and error handling.

---

### **1. Configuration: `config/apiconfig.js`**

This file sets the base URL for the API, which is used in all API requests.

```js
// src/api/config.js
const API_BASE_URL = 'https://test.369ai.biz:3016'; // backend test environment
export default API_BASE_URL;
```

**Purpose:**  
This provides a centralized point for the base URL of the API, making it easy to switch between different environments (e.g., development, staging, production).

---

### **2. Details: `details/detailapi.js`**

This file contains functions to fetch detailed information about various entities like invoices, vendors, and more. It uses a common `get` method for sending HTTP GET requests and handles errors using a utility function.

#### Key Functions:

1. **`fetchAuditDetails(endpoint, sequenceNo)`**  
   Fetches audit details by sequence number.

   ```js
   const fetchAuditDetails = async (endpoint, sequenceNo) => {
     const response = await get(`${endpoint}?sequence_no=${sequenceNo}`);
     return response.data;
   };
   ```

2. **`fetchDetails(endpoint, detailId)`**  
   Fetches details for a specific entity using a detail ID.

   ```js
   const fetchDetails = async (endpoint, detailId) => {
     const response = await get(`${endpoint}/${detailId}`);
     return response.data;
   };
   ```

3. **`fetchDetailBySearch(endpoint, search, warehouseId)`**  
   Fetches details based on search criteria and warehouse ID.

   ```js
   const fetchDetailBySearch = async (endpoint, search, warehouseId) => {
     const response = await get(`${endpoint}?name=${search}&warehouse_id=${warehouseId}`);
     return response.data;
   };
   ```

---

### **3. Dropdowns: `dropdowns/dropdownApi.js`**

The `dropdownApi.js` file is responsible for fetching data for various dropdown lists in the application, such as customer names, products, and currencies.

#### Key Functions:

1. **`fetchInvoiceDropdown()`**  
   Fetches the invoice dropdown options.

   ```js
   export const fetchInvoiceDropdown = async () => {
     return fetchData(DROP_DOWN_API_ENDPOINTS.INVOICE);
   };
   ```

2. **`fetchProductsDropdown()`**  
   Fetches the product options.

   ```js
   export const fetchProductsDropdown = async () => {
     return fetchData(DROP_DOWN_API_ENDPOINTS.PRODUCTS);
   };
   ```

3. **`fetchCountryDropdown()`**  
   Fetches the list of countries.

   ```js
   export const fetchCountryDropdown = async () => {
     return fetchData(DROP_DOWN_API_ENDPOINTS.VIEW_COUNTRY);
   };
   ```

---

### **4. Endpoints: `endpoints/endpoints.js`**

This file centralizes all the API endpoint URLs, making it easy to reference them across the application. This promotes consistency and maintainability.

```js
// src/api/endpoints/endpoints.js
export const DETAIL_API_ENDPOINTS = {
  GET_INVOICE_DETAILS: `${API_BASE_URL}/invoice/details`,
  GET_VENDOR_DETAILS: `${API_BASE_URL}/vendor/details`,
  // Add other endpoints as needed
};

export const DROP_DOWN_API_ENDPOINTS = {
  INVOICE: `${API_BASE_URL}/dropdown/invoices`,
  PRODUCTS: `${API_BASE_URL}/dropdown/products`,
  VIEW_COUNTRY: `${API_BASE_URL}/dropdown/countries`,
  // Add other dropdown endpoints as needed
};
```

---

### **5. Services: `services/utils.js`**

This file includes utility functions that facilitate the API calls, including GET and POST methods. These utility functions help to reduce repetition and centralize common logic.

```js
// src/api/services/utils.js
import axios from "axios";
import handleApiError from "@api/utils/handleApiError";

// Common GET request
export const get = async (url, params = {}) => {
  try {
    const response = await axios.get(url, { params });
    return response;
  } catch (error) {
    handleApiError(error);
    throw error;
  }
};

// Common POST request
export const post = async (url, data) => {
  try {
    const response = await axios.post(url, data);
    return response;
  } catch (error) {
    handleApiError(error);
    throw error;
  }
};
```

---

### **Error Handling: `utils/handleApiError.js`**

This utility handles API errors and logs them or displays user-friendly error messages.

```js
// src/api/utils/handleApiError.js
export default function handleApiError(error) {
  if (error.response) {
    console.error("API Error:", error.response.data);
  } else if (error.request) {
    console.error("No response received:", error.request);
  } else {
    console.error("Error setting up request:", error.message);
  }
}
```

---

### **Example API Call: Fetch Invoice Details**

Below is an example of how to use the API to fetch invoice details using the `fetchBills.invoiceDetails` function.

```js
import { fetchBills } from '@api/details/detailapi';

const fetchInvoiceDetailsExample = async (sequenceNo) => {
  try {
    const invoiceDetails = await fetchBills.invoiceDetails(sequenceNo);
    console.log('Invoice Details:', invoiceDetails);
  } catch (error) {
    console.error('Error fetching invoice details:', error);
  }
};

fetchInvoiceDetailsExample(12345);
```

## 6. Hooks Documentation

The `hooks/` folder contains custom hooks that enhance the functionality of the 369ai project by managing state, optimizing data fetching, debouncing, and handling loaders. These hooks abstract common logic, making the components more maintainable and reusable.

---

### 6.1 **Folder Structure**
- `useDataFetching.js`  
  Provides a hook for handling data fetching with pagination.

- `useDebouncedSearch.js`  
  Manages search functionality with debouncing to optimize performance by limiting the frequency of API calls.

- `useLoader.js`  
  Controls loader display logic, ensuring a smooth user experience by maintaining a minimum display time for loading indicators.

---

### **1. `useDataFetching.js`**

The `useDataFetching` hook abstracts the logic for fetching paginated data and handling the loading state.

#### **Parameters:**
- `fetchDataCallback` (function): The callback function to fetch data. It accepts parameters such as `offset`, `limit`, and any additional filters.

#### **States:**
- **`data`** (array): Holds the fetched data.
- **`loading`** (boolean): Indicates whether data is currently being fetched.
- **`allDataLoaded`** (boolean): Flags whether all data has been fetched (used to prevent unnecessary additional API calls).
- **`offset`** (number): Tracks the current pagination offset.

#### **Key Functions:**

1. **`fetchData(newFilters)`**  
   Fetches the initial data set with the given filters.

   ```js
   const fetchData = useCallback(async (newFilters = {}) => {
     startLoading();
     try {
       const params = { offset: 0, limit: 20, ...newFilters };
       const fetchedData = await fetchDataCallback(params);
       setData(fetchedData);
       setAllDataLoaded(fetchedData.length === 0);
     } catch (error) {
       console.error('Error fetching data:', error);
     } finally {
       stopLoading();
     }
   }, [fetchDataCallback, startLoading, stopLoading]);
   ```

2. **`fetchMoreData(newFilters)`**  
   Loads more data as the user scrolls, appending it to the existing data.

   ```js
   const fetchMoreData = async (newFilters = {}) => {
     if (loading || allDataLoaded) return;
     startLoading();
     try {
       const params = { offset: offset + 1, limit: 20, ...newFilters };
       const fetchedData = await fetchDataCallback(params);
       if (fetchedData.length === 0) {
         setAllDataLoaded(true);
       } else {
         setData((prevData) => [...prevData, ...fetchedData]);
         setOffset((prevOffset) => prevOffset + 1);
       }
     } catch (error) {
       console.error('Error fetching more data:', error);
     } finally {
       stopLoading();
     }
   };
   ```

3. **`handleSearchTextChange(text)`**  
   Uses `debounce` to delay API calls while typing in search text, reducing the number of requests sent.

   ```js
   const handleSearchTextChange = debounce((text) => {
     fetchData(text);
   }, 1000);
   ```

#### **Return Values:**
- `data`: Fetched data.
- `loading`: Loading state.
- `fetchData`: Function to fetch initial data.
- `fetchMoreData`: Function to fetch more data.
- `handleSearchTextChange`: Function to handle search input changes with debouncing.

---

### **2. `useDebouncedSearch.js`**

The `useDebouncedSearch` hook provides a mechanism to delay search input processing, reducing unnecessary API calls or heavy computations by debouncing the user input.

#### **Parameters:**
- `callback` (function): The function to call when the debounced search input changes.
- `delay` (number): The delay (in milliseconds) to wait before invoking the callback after the user stops typing. Default is 1000ms.

#### **States:**
- **`searchText`** (string): The current value of the search input.

#### **Key Functions:**

1. **`debouncedSearch(text)`**  
   Uses lodash's `debounce` to call the `callback` function only after the user stops typing for the specified delay.

   ```js
   const debouncedSearch = useCallback(
     debounce((text) => {
       setSearchText(text);
       callback(text);
     }, delay),
     []
   );
   ```

2. **`handleSearchTextChange(text)`**  
   Handles the input changes and triggers the debounced search.

   ```js
   const handleSearchTextChange = (text) => {
     debouncedSearch(text);
   };
   ```

#### **Return Values:**
- `searchText`: The current search input value.
- `handleSearchTextChange`: Function to handle changes in the search input field.

---

### **3. `useLoader.js`**

The `useLoader` hook manages the loading state of components. It ensures that loaders are displayed for a minimum amount of time to enhance user experience.

#### **Parameters:**
- `initialLoading` (boolean): The initial loading state. Default is `false`.

#### **States:**
- **`loading`** (boolean): Represents whether the loader is active or not.
- **`startTime`** (useRef): Tracks when the loader started.

#### **Key Functions:**

1. **`startLoading()`**  
   Starts the loader and records the start time.

   ```js
   const startLoading = () => {
     startTime.current = Date.now();
     setLoading(true);
   };
   ```

2. **`stopLoading()`**  
   Stops the loader after ensuring it has been displayed for at least the minimum time specified by `MINIMUM_LOADER_TIME`.

   ```js
   const stopLoading = () => {
     const elapsed = Date.now() - startTime.current;
     if (elapsed < MINIMUM_LOADER_TIME) {
       setTimeout(() => {
         setLoading(false);
       }, MINIMUM_LOADER_TIME - elapsed);
     } else {
       setLoading(false);
     }
   };
   ```

#### **Return Values:**
- `loading`: The current loading state.
- `startLoading`: Function to trigger the loader.
- `stopLoading`: Function to stop the loader.

---

### **Example Usage**

```js
import { useDataFetching } from '@hooks';
import { useDebouncedSearch } from '@hooks';

const MyComponent = () => {
  const { data, loading, fetchData, fetchMoreData, handleSearchTextChange } = useDataFetching(fetchMyDataApi);
  const { searchText, handleSearchTextChange } = useDebouncedSearch((text) => fetchData({ searchText: text }));


  useEffect(() => {
    fetchData(); // Fetch initial data on mount
  }, []);

  return (
    <View>
      <TextInput onChangeText={handleSearchTextChange} placeholder="Search..." />
      {loading ? <Loader /> : <DataList data={data} />}
      <Button title="Load More" onPress={fetchMoreData} />
    </View>
  );
};
```

## 7. Navigation Documentation

### 7.1 Structure
The app leverages **React Navigation** to manage navigation flows between screens. It employs a combination of stack and tab navigators to create a structured and user-friendly navigation experience.

---

### 7.2 Navigators

#### 1. **`AppNavigator.js`**
This is the main navigator that manages the overall tab navigation structure within the application. It is the entry point for the bottom tab navigation.

- **Purpose**:  
  Defines and configures the bottom tab navigation structure, providing access to various sections of the app via tabs.

- **Example Tabs**:
  - **Home**
  - **Categories**
  - **Cart**
  - **Orders**
  - **Profile**


- **Key Dependencies**:
  - `@react-navigation/bottom-tabs`: For creating bottom tab navigators.
  
- **Sample Implementation**:
  ```js
  import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
  import HomeScreen from '@screens/HomeScreen';
  import ProfileScreen from '@screens/ProfileScreen';

  const Tab = createBottomTabNavigator();

  const AppNavigator = () => {
    return (
      <Tab.Navigator>
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Profile" component={ProfileScreen} />
      </Tab.Navigator>
    );
  };

  export default AppNavigator;
  ```

---

#### 2. **`StackNavigator.js`**
This handles navigation between different screens of the application, primarily using a stack-based approach.

- **Purpose**:  
  Manages stack-based navigation, handling transitions between screens such as forms, details, and other workflows that require hierarchical navigation.

- **Key Dependencies**:
  - `@react-navigation/stack`: For creating a stack-based navigation flow.

- **Sample Implementation**:
  ```js
  import { createStackNavigator } from '@react-navigation/stack';
  import HomeScreen from '@screens/HomeScreen';
  import DetailsScreen from '@screens/DetailsScreen';

  const Stack = createStackNavigator();

  const StackNavigator = () => {
    return (
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Details" component={DetailsScreen} />
      </Stack.Navigator>
    );
  };

  export default StackNavigator;
  ```

---

### 7.3 Navigation Flow

The navigation system relies on both stack and tab navigators. **`AppNavigator.js`** manages the bottom tab bar, allowing users to navigate between major sections of the app, while **`StackNavigator.js`** is responsible for handling screen transitions within each section.

- **Navigation Flow Example**:
  1. **AppNavigator.js**: Manages overall app navigation with tabs (e.g., Home, Profile, Orders).
  2. **StackNavigator.js**: Handles detailed navigation within individual sections, allowing users to drill down into specific screens such as viewing details or forms.

---

### 7.4 Key Features

- **Deep Linking**: Supports deep linking to handle external URLs and navigate to specific app screens.
- **Screen Transition Options**: Provides smooth transitions between screens, with custom animations for an enhanced user experience.

## 8. Utils Documentation

### 8.1 Overview
The `utils` folder contains helper functions, configuration, data formatters, and validation logic that is shared across various parts of the application. It is organized into subfolders for better modularity and code reuse.

### 8.2 Folder Structure
- **`common`**: Contains common utility functions and helpers used throughout the app.
  - **`stringUtils.js`**: Contains string manipulation utilities like truncation.
  - **`toastUtils.js`**: Provides toast message functionality using `react-native-toast-message`.
  - **`date/`**: Contains date-related utilities.
    - **`formatDate.js`**: Formats date strings.
    - **`formatDateTime.js`**: Formats date-time strings.

- **`config`**: Contains configuration utilities.
  - **`getConfig.js`**: Provides app-specific configurations based on environment variables.

- **`formatter`**: Contains data formatting utilities.
  - **`formatData.js`**: Formats data into a structure suitable for display in grids or lists.

- **`validation`**: Contains validation utilities used for form and data validation.
  - **`validation.js`**: Provides functions to validate form fields.
  - **`validationFunctions.js`**: Contains individual validation logic like email and phone number validation.
  - **`validationRules.js`**: Defines reusable validation rules for various form fields.

---

### 8.3 Common Utilities

####  `stringUtils.js`
This file provides utility functions for manipulating strings:
- **`truncateString(str, maxLength)`**: Trims the string to the specified length and appends ellipses (`...`) if necessary.
  ```js
  export const truncateString = (str, maxLength) => {
      return str.length > maxLength ? str?.trim().slice(0, maxLength) + '...' : str.trim();
  };
  ```

####  `toastUtils.js`
Handles displaying toast messages:
- **`showToast({ type, title, message })`**: Displays a toast notification at the bottom of the screen.
  ```js
  export const showToast = ({ type, title, message }) => {
    Toast.show({
      type,
      text1: title,
      text2: message,
      position: "bottom",
    });
  };
  ```

#### Date Utilities (`date/formatDate.js` and `date/formatDateTime.js`)
- **`formatDate(date, formatString)`**: Formats the given date into a human-readable string using `date-fns`.
- **`formatDateTime(date, formatString)`**: Formats both date and time.
  ```js
  export const formatDate = (date = new Date(), formatString = 'dd MMMM yyyy') => {
    return date ? format(new Date(date), formatString) : '';
  };
  ```

---

### 8.4 Config Utilities

####  `getConfig.js`
Retrieves the app's specific configurations based on environment variables:
- **`getConfig(appName)`**: Returns app-specific config data for UAE or Oman projects.
  ```js
  export const getConfig = (appName) => {
    const configs = {
      [process.env.EXPO_PUBLIC_APP_NAME_UAE]: {
        appName: process.env.EXPO_PUBLIC_APP_NAME_UAE,
        packageName: process.env.EXPO_PUBLIC_PACKAGE_NAME_UAE,
        projectId: process.env.EXPO_PUBLIC_PROJECT_ID_UAE,
      },
      [process.env.EXPO_PUBLIC_APP_NAME_OMAN]: {
        appName: process.env.EXPO_PUBLIC_APP_NAME_OMAN,
        packageName: process.env.EXPO_PUBLIC_PACKAGE_NAME_OMAN,
        projectId: process.env.EXPO_PUBLIC_PROJECT_ID_OMAN,
      },
    };
    return configs[appName] || {};
  };
  ```

---

### 8.5 Formatter Utilities

####  `formatData.js`
Formats a list of data into rows and columns, filling in empty spaces where necessary:
- **`formatData(dataList, numColumns)`**: Organizes data into a grid format with a specified number of columns.
  ```js
  export const formatData = (dataList, numColumns) => {
      const totalRows = Math.ceil(dataList.length / numColumns);
      const totalItems = totalRows * numColumns;
      const formattedData = [...dataList];
      if (dataList.length < totalItems) {
          const emptyItemCount = totalItems - dataList.length;
          for (let i = 0; i < emptyItemCount; i++) {
              formattedData.push({ key: 'blank', empty: true });
          }
      }
      return formattedData;
  };
  ```

---

### 8.6 Validation Utilities

#### `validation.js`
Handles validation for multiple form fields:
- **`validateFields(formData, fieldsToValidate)`**: Validates form data against predefined rules.
  ```js
  export const validateFields = (formData, fieldsToValidate) => {
    const errors = {};
    let isValid = true;
    fieldsToValidate.forEach(field => {
      const rule = allValidationRules[field];
      if (rule && !rule.validate(formData[field])) {
        errors[field] = rule.message;
        isValid = false;
      }
    });
    return { isValid, errors };
  };
  ```

#### `validationFunctions.js`
Defines individual validation logic for different input types:
- **`validateRequired(value)`**: Checks if a value is present.
- **`validateEmail(email)`**: Validates email format.
- **`validatePhoneNumber(number)`**: Validates a 10-digit phone number.
  ```js
  export const validateRequired = value => !!value;
  export const validateEmail = email => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
  export const validatePhoneNumber = number => /^[0-9]{10}$/.test(number);
  ```

#### `validationRules.js`
Provides reusable validation rules for different fields. Each rule has a message and a validation function:
- **`allValidationRules`**: Contains validation rules for fields like `name`, `phoneNumber`, `emailAddress`, and more.
  ```js
  export const allValidationRules = {
    name: { message: 'Please enter the Name', validate: validateRequired },
    phoneNumber: { message: 'Please enter a valid phone number', validate: value => validateRequired(value) && validatePhoneNumber(value) },
    emailAddress: { message: 'Please enter a valid email address', validate: value => validateRequired(value) && validateEmail(value) },
    // Additional rules here...
  };
  ```

### 8.7 Usage Examples

#### 1. **String Utilities**

```javascript
import { truncateString } from '@utils/common';

const longText = 'This is a very long string that needs to be truncated.';
const shortText = truncateString(longText, 20);
console.log(shortText);  // Output: 'This is a very long...'
```

#### 2. **Toast Utility**

```javascript
import { showToast } from '@utils/common';

showToast({
  type: 'success',
  title: 'Success',
  message: 'Operation completed successfully!',
});
```

#### 3. **Date Formatting**

```javascript
import { formatDate, formatDateTime } from '@utils/common/date';

const formattedDate = formatDate(new Date());
console.log(formattedDate); // Output: '12 September 2024'

const formattedDateTime = formatDateTime(new Date());
console.log(formattedDateTime); // Output: '12 September 2024 14:35:12'
```

#### 4. **Get Config**

```javascript
import { getConfig } from '@utils/config';

const appConfig = getConfig('myAppName');
console.log(appConfig); 
// Output: { appName: 'myAppName', packageName: 'com.example.myapp', projectId: '123456' }
```

#### 5. **Data Formatting**

```javascript
import { formatData } from '@utils/formatters';

const dataList = [{ id: 1 }, { id: 2 }, { id: 3 }];
const formattedList = formatData(dataList, 2);
console.log(formattedList); 
// Output: Formatted array with rows/columns structure and filled empty items if necessary
```

#### 6. **Field Validation**

```javascript
import { validateFields } from '@utils/validation';

const formData = {
  name: '',
  emailAddress: 'invalid-email',
  phoneNumber: '1234567890',
};

const fieldsToValidate = ['name', 'emailAddress', 'phoneNumber'];

const { isValid, errors } = validateFields(formData, fieldsToValidate);
console.log(isValid);  // Output: false
console.log(errors);   
/* Output:
{
  name: 'Please enter the Name',
  emailAddress: 'Please enter a valid email address',
}
*/
```

#### 7. **Validation Functions**

```javascript
import { validateEmail, validateRequired } from '@utils/validation/validationFunction';

const isNameValid = validateRequired('John');
console.log(isNameValid);  // Output: true

const isEmailValid = validateEmail('test@example.com');
console.log(isEmailValid);  // Output: true
```

## 9. Step-by-Step Guide for Dynamically Building an Expo App with Different Currencies and Project Name/ID

This guide outlines how to dynamically build your Expo app with different configurations such as currencies, project names, and IDs. It also includes building locally and on the server using **EAS Build**.

---

### 1. **Expo Development Setup**

Before starting the build process, make sure you're logged into both **Expo** and **EAS**:

1. Open your terminal.
2. Log in to **Expo Dev** and **EAS** by running the following command:

    ```bash
    eas login
    ```

   For project access, you will find the credentials in the repository’s README (ensure you have permission to access this information):
   [Project Access Guide](https://github.com/ingointo/369ai-latest/blob/main/README.md)
   
   - **Username**: **********  
   - **Password**: **********  

> Note: Do not share these credentials publicly.
### 2. **Local and Server Builds**

You can build your app either locally or on the server:

- **Local Build**:
  
  Run the following command to create a local build for Android:

  ```bash
  eas build -p android --profile preview --local
  ```

- **Server Build**:
  
  To generate a server build for Android:

  ```bash
  eas build -p android --profile preview
  ```

---

### 3. **Configuration for Project Name, Project ID, and Currencies**

Follow these steps to dynamically configure the Expo app for different currencies and project names:

#### 3.1 **Update the `.env` File**

1. Open the `.env` file in your project.
2. Update the following variable to match the desired app (for example, **369aiOman** or **369aiUAE**):

    ```bash
    APP_NAME=369aiUAE  # or 369aiOman
    ```

#### 3.2 **Update Expo Profile**

1. Open the `app.json` or `app.config.js` file.
2. Ensure that the app name matches the `APP_NAME` value from your `.env` file.

#### 3.3 **Modify `package.json`**

1. Open the `package.json` file.
2. Add the following key-value pair:

    ```json
    "type": "module"
    ```

    This is required to ensure compatibility with modern JavaScript.

---

### 4. **Generate the `app.json` File**

1. Run the following command to generate the `app.json` file with the appropriate project ID, package name, and other details:

    ```bash
    npm run generate-app-json
    ```

    This script will generate the required values based on the app name specified in the `.env` file.

#### 4.1 **Ensure Correct Scripts in `package.json`**

In your `package.json`, include the following script to handle the generation of `app.json`:

```json
"scripts": {
  "generate-app-json": "node scripts/generateAppJson.js"
}
```

Your `generateAppJson.js` script should read from the `.env` file and update `app.json` accordingly.

---

### 5. **Revert `package.json` to CommonJS**

Once you have successfully generated the `app.json` file, revert the `"type": "module"` change in `package.json` back to `"commonjs"` to avoid errors during the build.

Your `package.json` should now look like this:

```json
{
  "type": "commonjs"
}
```

---

### 6. **Build the Expo App**

Once everything is configured, build your app:

1. For regular Expo CLI builds:

    ```bash
    expo build:android
    ```

2. For EAS builds:

    ```bash
    eas build -p android --profile preview
    ```

---

### Additional Notes:

- Always double-check the configuration in your `app.json` to make sure it aligns with your desired settings.
- Ensure that the `generateAppJson.js` script correctly reads the `.env` file and updates the `app.json` file dynamically based on the app name, project ID, package name, etc.
