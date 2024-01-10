# Some tips that may be helpful

## Web Cat Style Checker (if enabled)
webcat's style checking can be annoying so here are some tips on what you should do 

What you can do first is click on the `Full Printable Report` Button

![Keybinds.pdf](https://github.com/haotian2006/CSALABS/blob/main/Images/index/PrintReportButton.png?raw=true)

What it does is bring you to a page which shows you all the parts where your style is wrong

![Alt text](https://github.com/haotian2006/CSALABS/blob/main/Images/index/ErrorsIdk.png?raw=true)

This will allow you to see why exactly you are not getting your style points

Here is what you should do an not do

#### Closing brackets

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/x.png?raw=true" width= 15 height= 15>
```java
if (condition){
    
}

if (condition)
    return;

class myClass{

}
```

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/check.png?raw=true" width= 15 height= 15>
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

#### Spaces between operations and Multiline

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/x.png?raw=true" width= 15 height= 15>
```java
int sum=x+x;

private Stack<Integer> backStk,forwardStk;
```
<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/check.png?raw=true" width= 15 height= 15>

```java
int sum = x + x;

private Stack<Integer> backStk;
private Stack<Integer> forwardStk;
```

#### Lines longer then 70 characters

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/x.png?raw=true" width= 15 height= 15>
```java
// This is a line that will be more then 70 characters and will cause webcat to mark points off
```

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/check.png?raw=true" width= 15 height= 15>

```java
// This is how you can avoid it
// By using multiple lines
// this can apply to java doc and code
```

#### Improper Indenting

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/x.png?raw=true" width= 15 height= 15>
```java
if (condition)  
    {
System.out.println("Hello World")
    }
```

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/check.png?raw=true" width= 15 height= 15>

```java
if (condition)  
{
    System.out.println("Hello World")
}
```

#### Improper Java Docs or missing

<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/x.png?raw=true" width= 15 height= 15>
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
public class test
{ 
    private int x;

    //missing java docs
    public test(int x)
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
<img src="https://github.com/haotian2006/CSALABS/blob/main/Images/index/check.png?raw=true" width= 15 height= 15>
```java
/**
*  Stores a int x for testing
*  @author  you
*  @version Jan 1,1970
*  @author  Period 1
*  @author  Assignment: JMCH0
*
*  @author  Sources: none
*/
public class test
{ 
    private int x;

    
    /**
     * Creates and stores x
     * @param x The int being stored
     */
    public test(int x)
    {
        this.x = x;
    }

    /**
     * gets the stored value
     * @return the stored value
     */
    public int getX()
    {
        return x
    }

     /**
     * setX is missing @param
     * @param x Value being stored
     */
    public void setX(int x)
    {
        this.x = x;
    }

}
```

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
