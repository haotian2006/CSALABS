# 21 Lab: Browsing

>Difficulty: <span style="color:lightgreen">simple</span> (15 Minuets)
!!!warning
    This lab takes off points determining on your formatting. Make sure you have Java Doc comments and make sure your style follows what webcat wants.
    You can find out how to style properly [here](https://haotian2006.github.io/CSALABS/1Tips/#web-cat-style-checker-if-enabled)
!!!warning 
    Remember to Check `BrowserView.java` when submitting to webcat

## Instructions 
In this lab we will implement a toy browser called `LineCruiser`. Rather than
browsing web pages, our browser will “browse” several lines of text in the same file.
Figure 21-5 shows the classes that we have to write for this project. As usual, this is
a team effort: I’ll provide the `LineCruiser`, `BrowserMouseListener`,
`BrowserControlPanel`, and BrowserView classes, and you work on the
`BrowserModel` class.

Our browser has “Home,” “Back,” and “Forward” buttons, just like a real browser.
An important part of your task is to figure out how exactly these buttons work in a
real browser (such as Firefox or Internet Explorer). “Home,” “Back,” and “Forward”
in our browser should work the same way

Now let’s agree on more formal specifications.

My BrowserView class provides one method of interest to you:
```java
public void update(int n)
```
It displays several lines from the file, as many as fit in the display, with the n-th line
at the top of the display. Your class, BrowserModel, should call update as
necessary.

Your BrowserModel class should provide one constructor and six methods.

BrowserModel’s constructor takes one parameter:

```java
BrowserModel(BrowserView view)
```

Your constructor should save view to be able to call view’s update method later.
Don’t forget to call update from BrowserModel’s constructor to initialize view.
Four of BrowserModel’s methods are used for navigation:

```java
void back();
void forward();
void home();
void followLink(int n);
```

I call home, back, and forward methods when a corresponding button is clicked. I
call followLink(n) when a hyperlink pointing to the n-th line is clicked.

BrowserModel’s two remaining methods let me know whether the “Back” and/or
“Forward” buttons should be enabled or disabled: 

```java
boolean hasBack();
boolean hasForward();
```

The return true means enable; false, disable.
You’ll find the LineCruiser files in `JM\Ch21\Browser`. The `lines.html data` file
for testing our browser is in the same folder. Use `java.util.Stack<Integer>`
for the stacks. Write the BrowserModel class and test the program thoroughly. 

## Overview 
This lab introduces you to Stacks which is a data structure that is LIFO (Last In First Out) 

![Alt text](https://github.com/haotian2006/CSALABS/blob/main/Images/Browsing/Stack.png?raw=true)

This can be useful here as we just need the last Item added to the stack to keep track of the pages you went before

## BrowserModel
The class you will be working on.

### **---Fields---**
>By default, consider all fields private unless specified otherwise
### view `BrowserView`

Hold the BrowserView
!!!info 
    To update a BrowserView's page you need to use the method `BrowserView.update(page)`

### backStk `Stack<Integer>`
Holds the Stack for pages that you've been to

### forwardStk `Stack<Integer>`
Holds the Stack for pages to go after you go bacK

### topLine `int`
The current page you will be on


### **---Methods/Functions---**
>By default, consider all Methods public unless specified otherwise
### BrowserModel(`BrowserView view`) : `constructor`
Initialize all the fields 

### Home : `void`
Clears the stacks and goes to the home page (0)

### back : `void`
Updates `view` to the previous line from the back stack 
!!!info
    remember to update `forwardStk` and `topLine`.
    Also remember to check if `backStk` is empty

### forward : `void`
Similar to `back()` but moves forward instead.

### followLink(`int n`) : `void`

![Alt text](https://github.com/haotian2006/CSALABS/blob/main/Images/Browsing/link.png?raw=true)



