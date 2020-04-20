# Animations with Spring

This lesson explains how to make animations using react-springs

**Learning objectives**

- TNTs will be able to add animations to a component
- TNTs will understand how to create their own custom animations

**Time required and pace**

Total time: 1 hour

- 20 minutes - explain: How to add spring animations to an element.
- 20 minutes - Explore spring properties
- 20 minutes - evaluate: create an animated component

**Background / review**

- Function components/Class Components
- Props, state, Render

**Lesson details**

**Add react-springs to a function (20 minutes)**

1. 1)Yarn add react-springs
2. 2)As a table, TNTs draw what they&#39;ve learned so far about the app architecture
  - Display app architecture with labels, no descriptions
  - TNT groups talk through the function of the different parts and how they connect
3. 3)Re-group and walk through architecture thus far together - HTML, CSS, React, Node, React...

**How To Use Springs (20 minutes)**

Springs are used by assigning the style property of an element to a &#39;spring&#39; object. This can be done with a spring component or a spring hook in a function component.

1. 1)Spring Component in a class component:

A spring component expects a function returning a JSX element. The function will get a spring object that can be assigned to its style. As the spring changes the style object will be updated.

    class AnimatedView extends React.Component {
      render() {
        return (
          <Spring from={{ opacity: 0 }} to={{ opacity: 1 }}/>;
            {props => <div style={props}>hello</div>
          </Spring>;
        );
      }
    }

1. 2)Spring hooks in a function Component

Spring hooks are used by calling useSpring with an object containing the basic spring properties. The object returned can then be assigned to a JSX element&#39;s style property

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

**Core Properties (20 minutes)**

1. From: Object of type CssProperties, specifying the initial style of the animation.
2. To: Object of type CssPoperties specifying the end style of the animation
3. Delay: Time before animation starts
4. Immediate: Stops animation from running if set to true
5. Reset: Runs animation again
6. Reverse: Runs animation in reverse
7. OnStart: Function called at the start of an the animation
8. OnRest: Function called when the animation stops
9. OnFrame: Function called on each frame of the animation
10. Config: Takes in arguments to specify the physical properties of the animation(velocity, duration, etc)

**Animation Activity (20min)**

Create a function component that takes in a JSX Element as a property and renders it with an animation

**Stretch**

Name three differences between spring components and spring hooks
