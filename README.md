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

3. [Components Documentation](#3-components-documentation)  
   3.1 [Overview](#31-overview)  
   3.2 [Component Index](#32-component-index)  

4. [Usage](#4-usage)  
   4.1 [Running the Application](#41-running-the-application)  
   4.2 [Development Setup](#42-development-setup)

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


## 1. CalendarScreen

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

## 2. VerticalScrollableCalendar

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

## 3. DropdownSheet

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

## 4. MultiSelectDropdownSheet

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

## 5. Button

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

## 6. FABButton

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

## 7. LoadingButton

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

## 8. PressableInput

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
## 9. CheckBox

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

## 10. DetailCheckBox

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


## 11. SafeAreaView
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


## 12. SearchContainer
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

## 13. RoundedContainer
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

## 14. RoundedScrollContainer
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


## 15. BottomSheetHeader
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

## 16. NavigationHeader
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

## 17. AnimatedLoader
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

## 18. OverlayLoader
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

## 19. CustomTabBar
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

## 20. DetailField

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

## 21. TextInput
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

---
