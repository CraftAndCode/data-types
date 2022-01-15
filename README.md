# Text variables and data types

```package
core
radio
microphone
```

```template
basic.forever(function () {
})
```

```blocks
basic.forever(function () {
})
```

## Step 0 @showDialog
Hello! Today we'll use text variables to make a device that stores information about you!

## Step 1 @showDialog
### Data types

As we've learned, variables are containers in the device's memory that have names and store data inside. What we don't know yet is that data isn't limited to just numbers. With MakeCode, we can store strings of text, too!
  
When a variable's value is set for the first time, it is also given a data type. Possible variable data types are:
- `Number`, for storing numeric data. We used these in a previous lesson.
- `Text`, for storing letters, words or phrases using any characters on your keyboard. You can store numbers in thee variables too, but the program will treat them as characters, not digits, and won't be able to use them for calculations.
- `Boolean`, for storing `true` or `false` answers to yes-or-no questions.
  
We can't use a number variable to store text or a text variable to store numbers, as these will result in an error.
  
## Step 2
### Creating a variable
Let's make the Micro:bit remember your name. We'll need a new variable.
Click the `|Make a Variable|` button. Let the variable name be `My name`.

## Step 3 @showHint
### Changing variable type
We have a variable now, but if we use a ``||variables.set||`` block to change its value, we'll need a ``||text." "||`` block from the new ``||text.text||`` category in your toolbox to input text instead of a number.
```hint
A numerical variable:
```
```blocks
let My_name = 0
```
A text variable:
```blocks
let My_name = ""
```

## Step 4 @showHint
### What's your name?
Now we're ready. Type your name in quotes. Let's also add some code to display the name on the screen.
```blocks
let My_name = "Alice"
```
```blocks
basic.forever(function () {

    basic.showString(My_name)

})
```

## Step 5 @showHint
### Name changer
We've displayed names on screen before using much simpler methods. Why do we need to use variables? 
  
Variables enable us to change the text inside at a later time. Say we want to make a name badge that can be used by two different people. We can write a program that will change the displayed name with the press of a button. Let's add some example code to ours!
```blocks
input.onButtonPressed(Button.A, function () {
    My_name = "Bob"
})
```

## Step 6
### Now it's your turn!
There is one thing that we've left for you to do. Update your program to switch the name back when the other button is pressed.

## Step 7 @showHint
### More information!
Now, let's consolidate our knowledge. Create two more variables to represent your last name and your age.

```blocks
let My_name = "Alice"
let My_lastname = "Smith"
let My_age = "10"
```

## Step 8 @showHint
### Presenting information
Now, let's present this information clearly! Use a ``||text.join||`` block to join different words and form a sentence. Make ure to include spaces! What does your Micro:bit tell you now?
```blocks
basic.forever(function () {
    basic.showString("Hi, I am " + My_name + " " + My_lastname + " and I am " + My_age + " years old. "    )
})
```

## Step 7 @showHint
### Challenge: Identity change
Now, let's make another information change with the press of a button. We've shown you how to switch from Alice to Bob, but now it's up to you to write more code to change it back again. Good luck!
```blocks
input.onButtonPressed(Button.A, function () {
    My_name = "Bob"
    My_lastname = "Johnson"
    My_age = "9"
})
```
## @showDialog

### Answers: Now it's your turn!
This is the code to be added to the program.
```blocks
input.onButtonPressed(Button.B, function () {
    My_name = "Alice"
})
```
### Answers: Identity change
This is the code to be added to the program.
```blocks
input.onButtonPressed(Button.A, function () {
    My_name = "Alice"
    My_lastname = "Smith"
    My_age = "10"
})
```

## Step 9
Today we've learned about different data types. Now we know how to store and modify text data inside the Micro:bit's memory. Cool!
