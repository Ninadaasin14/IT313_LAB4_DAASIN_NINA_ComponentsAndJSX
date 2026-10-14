# IT313 Laboratory 4 - React Components & JSX

## Student Roster Card Renderer

This project is a simple React Native application created using Expo. It displays a list of enrolled students using reusable React components and JSX.

## Problem

The application needs to display each student as a card. Each card shows the student's name, course, and units enrolled. A **Full Load** label is displayed only when the student's `isFullLoad` value is true.

The application also displays the total number of students based on the student array.

## Component Structure

### StudentCard

`StudentCard` is a functional component that represents one student.

It receives these props:

* `name`
* `course`
* `units`
* `isFullLoad`

The props are destructured in the function parameter.

It also uses conditional rendering with `&&` to display the **Full Load** label only when `isFullLoad` is true.

### StudentRoster

`StudentRoster` is the parent component. It contains the student data and uses `.map()` to render one `StudentCard` for every student.

Each card uses the student's unique ID as the React `key`.

```tsx
key={student.id}
```

The total number of students is also computed using:

```tsx
`${roster.length} students`
```

## React and JSX Concepts Used

* Functional Components
* Props
* Props Destructuring
* JSX Expressions
* Conditional Rendering
* `.map()`
* `key` Prop
* React Native `View`, `Text`, and `Button`

## How to Run the App

First, install the project dependencies:

```bash
npm install
```

Then start the Expo development server:

```bash
npx expo start
```

Open the application using Expo Go or an Android emulator.

## Key Experiment

For the required experiment, the `key` was temporarily changed from:

```tsx
key={student.id}
```

to:

```tsx
key={index}
```

The roster was then reversed using the Reverse Roster button.

The ID-based key was restored because a student's ID is a stable and unique identifier, while the array index represents only the current position of an item.

## Author

Daasin

IT313 - Mobile Programming
