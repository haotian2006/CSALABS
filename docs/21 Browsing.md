# 21 Lab: Browsing

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
![Alt text](ttps://github.com/haotian2006/CSALABS/blob/main/Images/Browsing/Stack.png?raw=true)