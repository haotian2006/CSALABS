# Some tips that may be helpful

## Web-CAT Style Checker (if enabled)
webcat's style checking can be annoying so here are some tips on what you can do 

What you can do first is click on the `Full Printable Report` Button

![Keybinds.pdf](https://github.com/haotian2006/CSALABS/blob/main/Images/index/PrintReportButton.png?raw=true)

What it does is bring you to a page which shows you all the parts where your style is wrong

![Alt text](https://github.com/haotian2006/CSALABS/blob/main/Images/index/ErrorsIdk.png?raw=true)

This will allow you to see why exactly you are not getting your style points

Here is some style that webcat likes/dislikes

#### Closing brackets
???+Failure "Wrong"
    ```java
    if (condition){
        
    }

    if (condition) // webcat doesn't like this syntax
        return;

    class myClass
        {

    }
    ```
    Make sure that you have your starting { be below the Statements and Indented properly 

???+Success "Correct"
    ```java
    if (condition)
    {

    }

    if (condition)
    {
        return;
    }

    class myClass
    {

    }
    ```

#### Spaces between operators and Single lines

???+Failure "Wrong"
    ```java
    int sum=x+x;

    private Stack<Integer> backStk,forwardStk;

    System.out.println("Hello");System.out.println("World");
    ```

???+Success "Correct"
    ```java
    int sum = x + x;

    private Stack<Integer> backStk;
    private Stack<Integer> forwardStk;

    System.out.println("Hello");
    System.out.println("World");
    ```

#### Lines longer then 70 characters

???+Failure "Wrong"
    ```java
    // This is a line that will be more then 70 characters and will cause webcat to mark points off
    ```

???+Success "Correct"
    ```java
    // This is how you can avoid it
    // By using multiple lines
    // this can apply to java doc and code
    ```

#### Improper Indenting

???+Failure "Wrong"
    ```java
    if (condition)  
        {
    System.out.println("Hello World")
        }
    ```

???+Success "Correct"
    ```java
    if (condition)  
    {
        System.out.println("Hello World")
    }
    ```
    you can use an auto formatter to format your code as well

#### Improper Java Docs or missing

???+Failure "Wrong"
    ```java
    /**
    *  //description is missing 
    *  @author  //author is not filled out
    *  @version //version is not filled out ...
    *  @author  
    *  @author  
    *
    *  @author  
    */
    public class Integer
    { 
        private int x;

        //missing java docs
        public Integer(int x)
        {
            this.x = x;
        }

        /**
         * getX is missing a description @return
         * @return
         */
        public int getX()
        {
            return x
        }

        /**
         * setX is missing @param
         */
        public void setX(int x)
        {
            this.x = x;
        }

    }
    ```
???+Success "Correct"
    ```java
    /**
    *  A Integer wrapper class that encapsulates an int value
    *  @author  you
    *  @version Jan 1,1970
    *  @author  Period 1
    *  @author  Assignment: JMCH0
    *
    *  @author  Sources: none
    */
    public class Integer
    { 
        private int x;

        
        /**
        * Constructs an Integer object and initializes its value.
        * @param x The integer value to be stored
        */
        public IntegerWrapper(int x) {
            this.x = x;
        }

        /**
        * Retrieves the stored integer value.
        * @return The stored integer value
        */
        public int getValue() {
            return x;
        }

        /**
        * Updates the stored integer value.
        * @param x The new integer value to be stored
        */
        public void setValue(int x) {
            this.x = x;
        }

    }
    ```
    Remember to make sure that your java docs don't pass 70 characters and if it does you can move some to the next line

There is more checks that webcat does but these are the most basic ones



## Keybinds
![Keybinds.pdf](https://github.com/haotian2006/CSALABS/blob/main/Images/index/keyboard-shortcuts-macos.jpg?raw=true)

## Java Version is different  
If your java workspace is different then your Java version and it causes an error here is what you can do.

1. Go to EXPLORER (should be the first icon)
2. Go down to JAVA PROJECTS
3. Click on the 3 horizontal dots 
4. Press Clean Workspace

![cleanWorkspace.pdf](https://github.com/haotian2006/CSALABS/blob/main/Images/tips/CleanWorkspace.png?raw=true)

## AutoFill
There are a few statements that java will auto fill for you for example typing just sys will show you options such as `sysout`,`syserr`, etc... Pressing on those are way faster then just typing `System.out.println()`
