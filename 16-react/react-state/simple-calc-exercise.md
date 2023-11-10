# Lab: Simple Calc

Now, it's time for you to check back on everything! You will be building a calculator with React, and only minimal instructions have been provided for you to really think about what's happening.

At first, your calculator will just add 2 numbers together when they are typed in. For the bonus, you might decide to get more creative.

_there is a repofied version of this lab that can be found_ [_here_](https://github.com/WDI-SEA/react-simple-calc-lab/tree/main)

## Set Up

Like usual, use `create-react-app` to make a new project.

## Step 1

Create a Calculator component. Add the following JSX to your Calculator's `render()` function:

```jsx
            <div className="caclulator">
                <h1>Add with React!</h1>

                <form onSubmit={this.calculate}>
                    <input type="number" 
                        name="num1"
                        value={this.state.num1}
                        onChange={this.setNum}
                    />
                    <span>+</span>
                    <input type="number" 
                        name="num2"
                        value={this.state.num2}
                        onChange={this.setNum}
                    />
                    <button>=</button>
                    <h3>{this.state.sum}</h3>
                </form>
            </div>
```

## Step 2

Set up the initial state of your component. What state attributes will you need to track? What values should those state items start with? Where is that state displayed in the browser?

> Remember: You will only need one state object. That one state can hold as many key-value pairs as you need!

## Step 3

You will want to trigger a function when the values in your textboxes change. You can capture these values by setting a function on the onChange property. Let's say I have a textbox tracking my first number.

```jsx
<input type="number"
  name="num1"
  value={this.state.num1}
  onChange={this.setNum}
/>
```

I want to store this number as part of my state. Let's say I decided to call it `num1`. I could set my state like so:

```text
setNum = (e) => {
  this.setState({ [e.target.name]: e.target.value});
}
```

> Hint: The \[\] are there so we can use a dynamic key value! This value becomes `num1` or `num2` depending on what was clicked and sent to the function from `onChange`.

If you decided to use buttons for your calculator, you probably want to use `onClick` instead of `onChange`, but the concepts are the same! Here is some documentation to help you choose what you want to do and how to do it:

* [React form documentation](https://facebook.github.io/react/docs/forms.html)
* [A list of events React supports](https://facebook.github.io/react/docs/events.html#supported-events)

## Step 4

Once you've got your event handlers set up to capture the input, you'll need to create a method for your submit button. The method should accept the triggered event, get the input values from your state, add them together, and set part of the state to the new `sum`.

Hint: Where should this method go?

In the same component as it's being used - between the constructor and the render.

> Thought: How will you handle inputs that aren't numbers?

## Step 5

Once the state of the `sum` has been set, React will re-render the whole component. Make sure you have a place in your JSX that displays the result!

## Bonus

* Make the calculator work with any of the 4 basic arithmetic operations

  \(+, -, \*, /\). How will this change your `state` and your JSX?

