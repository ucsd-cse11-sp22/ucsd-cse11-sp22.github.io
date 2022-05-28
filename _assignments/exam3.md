---
layout: with-sidebar
index: 11
name: Exam 3
released-on: "2022-5-27"
---
# Exam 3

### Release: 11am Friday May 27, 2022
### Due: 11am Sunday May 29, 2022

**Note that this is released after class Friday, and is due Sunday morning. We will not accept late submissions.**


This page details a take-home exam that you will complete over the next few
days. You can’t communicate with anyone about the content of the assignment
until you receive your grade. You can message us privately on Piazza, but the
course staff will not give programming advice or answer most questions, including clarifications, about the
problems. If you have technical trouble creating a screencast (detailed below)
feel free to reach out for assistance.

Do not use any online service other than Piazza to ask questions about the
assignment. Do not search for, solicit, or use solutions to the problems that
you find elsewhere for the exam. These are all violations of academic integrity
that students have committed on exams like this in the past.

You can make use of any course notes, online resources about Java and its
libraries, Java tools, and so on to complete the exam, including re-using code
from class notes.

You can review the grading policy for exams in the [syllabus](/syllabus.html).
You will complete the programming task below and submit your work to the `Exam3` Gradescope assignment.

Starter code is available here:

[https://github.com/ucsd-cse11-sp22/cse11-exam3-starter](https://github.com/ucsd-cse11-sp22/cse11-exam3-starter)

Submission checklist (see long descriptions below for full details):

- [ ] `ComparatorStack.java`
- [ ] `CSVTool.java`
- [ ] `video.*` (`*` means whatever extension you have; we *really* prefer `mp4`, which is what Zoom produces. If you use an extension other than mp4, check that it plays in Gradescope!)

The starter code has been marked with the following annotation:

```java
// Task #.#: [Title]
// Your code here
```
You will only need to add code where you see this annotation.

Make sure to look at your Gradescope submission after submitting to see if all the required files are there.


### **Task 1 will be autograded. Task 2 will be both autograded and manually graded. Task 3 will be manually graded.** 

Make sure that your submission passes the autograder for your code to be properly graded. 

If you are having issues with getting the autograder to run successfully, you may find it helpful to consult the [Developing with the Gradescope Autograder in Mind](https://docs.google.com/document/d/1IKSDkG4kHC0gb2FyqdeOWJOAbQr6UCvYZSToIBopfVs/edit?usp=sharing) guide.

If your submission passes the autograder, then you should see output similar to:

<img src="exam2_success.png">{:width="100%"}

Be aware that the Sanity check does not check for code correctness, but rather that your code compiles. 

Your submission will be graded **after** the deadline. You should test thoroughly yourself to make sure your program works as expected.

## Clarifications

**Can I use a Java feature/library/method that we haven't covered in class?**

Yes, just make sure it doesn't break the autograder. The course staff is not responsible for fixing any submissions that fail the autograder during or after the exam. 

**Can we write more methods than specified?**

Yes, you can write additional helper methods.

**Can I use previous code that I wrote for a PA in my exam?**	

Yes.


## Task 1 – Generics and Exceptions
You will be writing your code in `ComparatorStack.java`. You will create a new generic class called `Stack` that will take 2 arguments for its constructor. `Stack` will have 2 fields: A generic `List<E>` object called `contents` and a `Comparator<E>` object called `comp`. These two fields will be set by its constructor. All imports have already been done for you.

Note: If you do not name these fields exactly, you will fail the autograder.

### Task 1.1
In the `Stack` class, you will use the design recipe to write a method called `push` that returns `void` and takes an argument of type `E` and adds it to the Stack. `Push` should add each element such that the element added to the top of the stack (i.e index '0'). 

### Task 1.2
In the `Stack` class, you will use the design recipe to write a method called `pop` that returns an element of type `E` and takes no arguments.  `Pop` should remove the top element in the stack (i.e index '0'). 

### Task 1.3
In the `Stack` class, you will use the design recipe to write a method called `findElements​​` that takes an argument of type `E` and returns an `int` representing the number of times that element is in the`Stack`. If the element is not found (i.e the element 'E' is not in the 'Stack' or the number of elements in the 'Stack' is not greater or equal to 1) you will return `0'. 'FindElements' should use the given 'Comparator' to determine if two elements are equal. 


### Task 1.4
In the `Stack` class, you will use the design recipe to write a method called `removeElements` that returns `boolean` and takes two arguments: one of type `E` and another of type 'int'.  This method removes all instances of the first argument from `Stack` up to the limit provided in the second argument. If the argument for 'E' does not exist in `Stack`, then you will throw a `NoSuchElementException` with no message. If the argument does exist, then you will return `true` if the removal was successful and `false` if the removal was unsuccessful. If there are less elements in the stack than the limit, remove all existing elements and return true. If there are more elements than the limit, remove up to the limit and return false (i.e if the second argument is 1 and there are three elements in the Stack, remove one element and return false). 'removeElements' should use the given 'Comparator' to determine if two elements are equal. 



Here is an incomplete list of basic tests to get you started that you can use as you like (and to help make sure we agree on how these methods work). These tests have been provided in `Sanity.java` for your convenience.


``` java
import tester.*;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Comparator;

class ProvidedStackTests_Sanity {
    void testPush(Tester t) {
        ArrayList<Integer> test_array = new ArrayList(Arrays.asList(1,3,3,8));
        Stack<Integer> q = new Stack(test_array, new IntCompare_Sanity());
       
        q.push(1);
    }

 void testPop(Tester t) {
        ArrayList<Integer> test_array = new ArrayList(Arrays.asList(1,3,3,8));
        Stack<Integer> q = new Stack(test_array, new IntCompare_Sanity());
        q.push(2);
        q.push(1);
        
        t.checkExpect(q.pop(), 1);
        t.checkExpect(q.pop(), 2);
    }

    void testFindElements(Tester t) {
        ArrayList<Integer> test_array = new ArrayList(Arrays.asList(1,3,3,8));
        Stack<Integer> q = new Stack(test_array, new IntCompare_Sanity());
        q.push(1);

        t.checkExpect(q.findElements(1),2);
        t.checkExpect(q.findElements(9), 0);
    }
    
      void testRemoveElements(Tester t) {
        ArrayList<Integer> test_array = new ArrayList(Arrays.asList(1,3,3,8));
        Stack<Integer> q = new Stack(test_array, new IntCompare_Sanity());
        q.push(3);
        q.push(3);
        q.push(1);
        

        t.checkExpect(q.removeElements(3,3), true);
        t.checkExpect(q.removeElements(8,0), false);
        //t.checkExpect(q.removeElements(5,2), false);
    }


}


class IntCompare_Sanity implements Comparator<Integer> {
    public int compare(Integer a, Integer b) {
        return a - b;
    }
}
```

## Task 2 – Command Line and String Parsing

You will be writing your code in a file called `CSVTool.java`. All imports have already been done for you. You should use [Hashmaps](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html) and [Set](https://docs.oracle.com/javase/8/docs/api/java/util/Set.html) in this task, but you are not required to. You may additionally import Hashmaps and Set if you use them.

Given a command line in the form of: 

```java
java CSVTool <query file> <data file 1> <data file 2> ... <data file n>
```

You will be printing out the results of CSVTool to the console. CSVTool will always be given at least 2 arguments, the first argument will always be the query file and the arguments that follow will always be CSV files. 

The query file will not contain duplicates. The individual data files will not contain duplicates, but duplicates will exist across multiple data files. 

The query file will be a list of query terms separated by a new line. For each term in the query file, we want to find all words in the data files that are "analogous" to those query words.

For each line in the data file, there are a list of words separated by commas that are analogous to each other. Such as in data_1.csv, the first line: 'train, trolley, cart, subway' means that all four of those words are analogous to each other. And since in our query file one of our queries is 'train', all words analogous to train in this case are 'trolley, cart, subway'. 

We have included some files of each type for you to inspect. Your task is to print all analogous terms for each query item. Hence, for each query item print out the following on one line:

'query: [word1, word2 … wordN]'

There may be analogous words across CSV files. Hence, if 'crisp' is analogous to 'snappy' and both belong to data_1.csv, and 'cool' is analogous to 'crisp' and both belong to data_2.csv,  then 'snappy' is analogous to 'crisp'. If the query word 'cold' is in the same line as 'crisp' and thereby analogous, the query for 'cold' should have '[crisp,snappy,cool]' printed. 

There will always be a continuity across csv files for the query words and their analogous terms. This means that you only have to read the CSV files in order once. You will never have a case where an analogous word is in data_1.csv and data_3.csv, and you need to read data_2.csv to connect words from data_3.csv. 

If you implement this correctly, then you should match the output below exactly. The order of your analogous list should be sorted and not contain the query term (if you use a Set, consider converting the Set to a [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html) in order to sort). You may find [Collections.sort()](https://docs.oracle.com/javase/7/docs/api/java/util/Collections.html#sort(java.util.List,%20java.util.Comparator)) useful for this Task. The order of the queries printed should match the order in the query file. Returned words for each query should only contain quique words without any duplicates. 

```java
$ java CSVTool queries_1.txt data_1.csv
car: [automobile, motorcar]
phone: []
cold: [crisp, freezing]
mug: [cup, goblet, teacup]
train: [cart, subway, trolley]



$ java CSVTool queries_1.txt data_1.csv data_2.csv
car: [automobile, motorcar]
phone: [cellphone]
cold: [chilly, crisp, freezing, frigid, icy, nippy, snappy]
mug: [chalice, cup, glass, goblet, teacup]
train: [cart, motorcade, subway, trolley]
```



Task 2 will also be manually graded.

## Video Task

You will record a short video of no more than 5 minutes. 

Tip: If you find yourself running out of time, you might be explaining your code too much. If the task does not ask you to directly explain your code, you don't need to explain it. 

Include:

- Show only your face and a picture ID (your student ID is preferred but any
picture ID with your name on it will work) for a few seconds at the beginning.
You don’t have to be on camera the whole time, though it’s fine if you are. Just
a brief confirmation that it’s you creating the video/doing the work attached to
the work itself is what we want. If you do not have a webcam, take a picture of
yourself (and your picture ID) with your phone and display that picture at the
start of your screen share.
- Write a test that causes an `NoSuchElementException` in `removeElements`. This test must not already be pre-written prior to the video. You may use checkExpect or checkException. 

  Show that the code causes an exception, then scroll to and make a comment at *each line of your code* that was evaluating on the **stack** when the exception was thrown. 
  
  Additionally, type out the *stack trace* at the moment the exception was thrown from the `removeElements` method. 

  Include only stack frames for methods in your code (not in libraries).

  Show the stack trace in the format below (table). You may prepare the table before the video, but you must fill it in during the video. Ignore the this reference and Tester parameter for tester methods in your trace.

  For objects and references, you can use any reference numbers that are consistent (see that the this parameter and the n local variable are the same below), and don't include the contents of the heap.

```java
class Numbers {
  List<Integer> values;
  Numbers(List<Integer> values) { this.values = values; }
  int addAll() {
    int total = 0;
    for(Integer i: this.values) {
      total += i;
      throw new RuntimeException(); // This line on the stack
    }
    return total;
  }
}
class ExamplesNumbers {
  void testNumbers(Tester t) {
    List<Integer> is = Arrays.asList(1, 2, 3)
    Numbers n = new Numbers(is);
    int total = n.addAll(); // This line on the stack
  }
}
/*
class             method        this reference      other variables
ExamplesNumbers   testNumbers   <ignore>            is = :1; n = :2
Numbers           addAll        :2                  total = 1; i = 1
*/
```
- There is no video task associated with Task 2.


