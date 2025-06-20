# Components vs Instances vs React Elements

1. Components:

- Description of UI
- function that retures react elements (element tree), in jsx

2. Component Instances:

- created when we use this components
- if 3 times then 3 instances
- calls component e.g Tab()
- has its own state, props and life cycle
- RETURNS REACT ELEMENTS

3. React Elements:

- JSX converted to react.createElement() calls
- result of the component calls
- information necessary to create DOM elements

NOTE: THEN THIS REACT ELEMENT WILL GET CONVERTED INTO THE DOM ELEMENT. Then the UI will be visible

Process:
COMPONENTS -> COMPONENT INSTANCES (A1,A2,A3) -> REACT ELEMENTS (for each instance) -> DOM ELEMENT (for each react elment) -> USER INTERFACE ON SCREEN

# How this react element is inside the DOM and displayed on the screen?

OVERVIEW:

1. RENDER IS TRIGGERED (by updating the state somewhere)

- TWO SITUATION THAT TRIGGERS RENDERS:

  1. INITIAL RENDER - of the application
  2. RE-RENDER - state updates in any component

2. RENDER PHASE - React calls components functions and figure out how DOM should be updated (doesnt update the DOM)

IN REACT, RENDERING IS NOT UPDATING THE DOM OR DISPLAYING THE ELEMENTS ON THE SCREEN. RENDERING ONLY HAPPENS INTERNALLY INSIDE REACT, IT DOES NOT PRODUCE ANY VISUAL CHANGES.

EXPLANATION IN IMG 01 TO 06

3. COMMIT PHASE - React actually writes to the DOM inserting, updating, deleting elements
   THIS DOM UPDATE IN THE COMMIT PHASE IS NOT DONE BY REACT LIBRARY OR BROWSER BUT BY REACTDOM LIBRARY
   BECASUE REACT CAN WORK WITH DIFFERENT HOSTS SUCH AS REACTNATIVE, REMOTION ETC....

EXPLANATION IN IMG 07 TO 09

4. VISUAL CHANGE
