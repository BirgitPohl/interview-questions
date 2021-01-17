# ReactJS Interview Questions

## What does controlled/uncontrolled component mean?
    The candidate should show the understanding that, in UI elements, like the fields, the data can be handled by the DOM or by React. The candidate would ideally say that in any regular case there is no need for uncontrolled component as it has lots of disadvantages and likely introduces need for hacks.

**Senior/Lead**
   
    A senior/lead could additionally mention that one justified use case is a third party libraries when "old world" is mixed with a React apps.


## What are props? What can they be used for?
    The candidate should mention that they can be used to introduce variability to a component, in same way like a function can take parameters. The candidate would ideally make it clear that functions and other components can and commonly are passed in props.

**Senior/Lead**
   
    For a candidate interviewing for a senior/lead not mentioning about passing of components for reusability can be bit of a red flag, especially if the interviewer asks, "what else for" in case that the candidate does not mention it self. So ideally the candidate says something like: Passing of components can be very useful in cases of reusable components. One example could be tables, where some functionality is common, but the rows for example could have their own components. It would be really nice if the candidate mentions in this context the usage of TypeScript types and draws a connection to dependency injection.


# Functional vs OOP in ReactJS

## Could a React component be seen as a pure function? What if it is class based?
    Ideally here the candidate says that yes, it can and it is encouraged. The fact that a component is class based does not change this. Candidate should say that the output in both cases can solely depend on the input. The candidate is likely to mention that the benefit is that the component is easier to debug and test.

## If you code a React component (UI, like button or a field) as a pure (as in pure function), but it still needs a state, how could you do it?
    This should lead to the candidate to mention about placing the state outside of the UI components. As an example: a form and its fields, the state of the fields could be stored in the form components state (or it's redux state).
    If the candidate suggests a pattern, where every UI component ( `Table`, `Dropdown` ...) has its own place in Redux state, this could be seen as an anti-pattern. It would be good to ask for more details in this case.

## Why did RreactJS introduced hooks and functions additionally to classes? What is the benefit here from your perspective?
    Additional features, backward compatibility is ensured when still using object-oriented writing.

    Under the hood, OOP had a functional nature. There is an output from the render() function.

    Immutability: You can read props, but not change them.

    Unidirectional data-flow.

    HOC and HOF allow re-usability

    States are being handles by the application, functional components avoid that. Component only depends on the props. You can isolate states in HOC and pass props to functional components.


-----------

## If this state depends on different parts of the app. What ways there are to access the other parts of the state?
    The states can be moved higher in component hierarchy, to common ancestors. So that the business logic can easily access the state of the other parts of the app. Ideally big portion of the business logic lives in actions, reducers, further away from the react containers and components.

## What is a Higher-Order Components (HOC)? Could you name any common HOC that you are using with redux or anything else if you are not using redux?
    HOC is a composition pattern that takes a component and returns an augmented version of that component. So it can add common features to a component.
    Good example from redux: `connect()` creates a HOC that is used to map state and the action creators to the component.

# State Management

## What is FLUX?
    Flux is the key architecture that facebook engineers spoke about when introducing React as a pattern to manage the state.
    The candidate should show the understanding of the unidirectional data flow. Components just render based on what is in the state, and various actions can change that state.

  
### Follow up question: Describe this in case that the user types text in a field.
    The candidate could say something like: The `onchange` of fields invokes a function that gets `event.target.value` that is passed to the state. That change in the state re-triggers a rerender, passing the latest value from the state through props to the input element's `value`.

## What would somebody want to use Redux or MobX?
    When the state gets big, these could provide a structure and useful utilities to keep things more structured and predictable. The candidate could mention here that they bring lots of boilerplate code, but still the benefits they offer should over weight the extra code, especially in non trivial applications.

## What are the alternatives to these state management libraries?
    Reacts own state and props drilling/context API.
    StateX - Turing machine inspired state management.

## What is common between the state of the app and functional programming term such as immutable value, pure function?
    The state is never mutated, we always reduce the new state using the existing state and the delta.

## What is the task of a reducer in Redux?
    They perform this specific definitions of how the resulting state will be, based on the existing state and the newly received delta.

## Why would somebody want to use a library for managing side effects?
    - By nature the the reduces are synchronous. Facebook's Flux description says _Where dependencies do occur between stores, they are kept in a strict hierarchy, with synchronous updates managed by the dispatcher._.

## How do you prefer to structure the state?
    This is pretty open ended an many answers can be debated. But in my opinion the ideal way is to follow these rules:
    - strictly no duplication, eliminate this by always moving higher in hierarchy.
    - State models more closely the App and the UI than the DTOs and entities. As likely less data transforming is needed (done as a part of fetching and not in containers).
    - Be structured and develop a convention regarding the deltas dispatched by actions.
    - Don't try to save code if it compromises predictability. This often times mean the templatation to start using containers state instead of redux. It is easy to miss a future need to interact with something in the state that is not available in container state and makes a hack or a refactoring required.

## Do you mix React state and state management library?
    The candidate would ideally mention saving coding and being lean but being aware that this brings the risk to miss a future need to interact with something in the state that is not available in container state and makes a hack or a refactoring required.

# Testing

## How do you test a React app?
    The candidate should explaining about testing components, snapshot testing, testing utils, testing actions and reducers. E2E testing by driving the browser. Demonstrate the understanding of need for mocking.

## What does open–closed principle mean? How does it relate to ReactJs?
    Making UI components very configurable.
    
    Passing components with props to allow more fine grained configurability.

## Can you give an example for Single Responsibility in ReactJS?
    # TODO Your expectations here