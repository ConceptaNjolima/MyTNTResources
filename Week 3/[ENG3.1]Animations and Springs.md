# Animations with Spring

This lesson explains how to make animations using react-springs

## Learning objectives

* TNTs will be able to add animations to a component
* TNTs will understand how to create their own custom animations

## Time required and pace

* Total time: 2 hours, 45 minutes

  - 45 minutes - **Pre-session**: background learning, research, and investigations
  - 60 minutes - **Instructional Session**
  - 60 minutes - **Post-session**:

## Background / review

* Function components/Class Components
* Props, state, Render

## Pre-session (45 minutes)

*Prepare for the session* [here](../../../wiki/[ENG2.2]View-component-layout)

## Session Details

### How To Use Springs (20 minutes)

Springs are used by assigning the style property of an element to a "spring" object. This can be done with a **Spring component** (within a class component) or a **Spring hook** (within a function component.)

#### Spring Component within a Class component

A spring component expects a function returning a JSX element. The function will get a spring object, often called `props`, that can be assigned to its style. As the spring changes the style object will be updated.

    class AnimatedView extends React.Component {
      render() {
        return (
          <Spring from={{ opacity: 0 }} to={{ opacity: 1 }}>
            {props => <div style={props}>hello</div>
          </Spring>
        )
      }
    }

#### Spring Hooks within a Function Component (only)

Spring hooks are used by calling `useSpring()` with an object containing the basic spring properties. The object returned can then be assigned to a JSX element's style property. The hook requires that you use an `animated` extentions for the containing JSX elements - create this [using the animated element](), like `<animated.div ... > ... </animated.div>`

    function AnimatiedFunc() {
      const springProps = useSpring({
        from: {
          opacity: 1
        },
        to: {
          opacity: 1
        }
      });
      return (
        <animated.div style={springProps}>
          <p>Hello</p>
        </animated.div>
      );
    }

### Core Properties (20 minutes)

1. From: Object of type CssProperties, specifying the initial style of the animation.
2. To: Object of type Css Poperties specifying the end style of the animation
3. Delay: Time before animation starts
4. Immediate: Stops animation from running if set to true
5. Reset: Runs animation again
6. Reverse: Runs animation in reverse
7. OnStart: Function called at the start of an the animation
8. OnRest: Function called when the animation stops
9. OnFrame: Function called on each frame of the animation
10. Config: Takes in arguments to specify the physical properties of the animation(velocity, duration, etc)

## Animation Activity (20min)

Create a function component that takes in a JSX Element as a property and renders it with an animation

## Stretch

Name three differences between spring components and spring hooks
