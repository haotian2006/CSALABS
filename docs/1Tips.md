# Some tips that may be helpful

## Web Cat Style Checker (if enabled)
webcat's style checking can be annoying so here are some tips on what you should do 

What you can do first is click on the `Full Printable Report` Button

![Keybinds.pdf](https://github.com/haotian2006/CSALABS/blob/main/Images/index/PrintReportButton.png?raw=true)

What it does is bring you to a page which shows you all the parts where your style is wrong

![Alt text](https://github.com/haotian2006/CSALABS/blob/main/Images/index/ErrorsIdk.png?raw=true)

This will allow you to see why exactly you are not getting your style points

Here is what you should do an not do

#### Make sure your closing brackets are below the if statement or class

![x](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.stockio.com%2Ffree-clipart%2Fx-icon&psig=AOvVaw08MSFFv18q0br7ejL-OX7H&ust=1704954656639000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCOC_kpuZ0oMDFQAAAAAdAAAAABAP)
```java
if (condition){

}

class myClass{

}
```
<span style="color:LightGreen">Allowed</span>
```java
if (condition)
{

}

class myClass
{

}
```

#### Spaces between operations

<span style="color:Red">Not Allowed</span>
```java
int sum=x+x;
```
<span style="color:LightGreen">Allowed</span>
```java
int sum = x + x;
```
```java
/**
*  Class Description here
*
*  @author  yourName
*  @version Date
*  @author  Period: Period
*  @author  Assignment: JMCh0_Test
*
*  @author  Sources: none
*/
public class test
{ 

}
```

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
