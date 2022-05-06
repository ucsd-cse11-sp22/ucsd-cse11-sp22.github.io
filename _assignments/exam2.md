---
layout: with-sidebar
index: 7
name: Exam 2
released-on: "2022-05-06"
---
# Exam 2

### Release: 11am Friday May 6, 2022
### Due: 11am Sunday May 8, 2022

**Note that this is released after class Friday, and is due on Sunday. We will not accept late submissions.**

This page details a take-home exam that you will complete over the next few
days. You can’t communicate with anyone about the content of the assignment
until the exam has concluded. **DO NOT** post clarification or other similar questions as staff will not be answering these types of questions during this time period. If there are broken links or otherwise strange parts of the writeup, you may post these concerns on piazza. If you have technical trouble creating a screencast (detailed below) feel free to reach out for assistance.

Do not use any online service (such as Discord) other than Piazza to ask questions about the
assignment. Do not search for, solicit, or use solutions to the problems that
you find elsewhere for the exam. These are all violations of academic integrity
that students have committed on exams like this in the past.

You can make use of any course notes, online resources about Java and its
libraries, Java tools, and so on to complete the exam, including re-using code
from class notes.

You can review the grading policy for exams in the [syllabus](/syllabus.html).
You will complete the programming task below and submit your work to the `Exam2` Gradescope assignment.

Starter code is available here:

[https://github.com/ucsd-cse11-sp22/cse11-exam2-starter](https://github.com/ucsd-cse11-sp22/cse11-exam2-starter)

Submission checklist (see long descriptions below for full details):

- [ ]`ExamplesArrays.java`
- [ ]`Numbers.java`
- [ ]`Tweets.java`
- [ ]`WordFilter.java`
- [ ]`video.*` (`*` means whatever extension you have; we *really* prefer `mp4`, which is what Zoom produces. If you use an extension other than mp4, check that it plays in Gradescope!)

The starter code has been marked with the following annotation:

```java
// Task #.#: [Title]
// Your code here
```
You will only need to add code where you see this annotation.

Make sure to look at your Gradescope submission after submitting to see if all the required files are there.


### **Task 1-3 will be autograded and will make up most of the Exam 2 score. Task 4 will be manually graded.** 

Make sure that your submission passes autograder for your code to be properly graded. 

If you are having issues with getting the autograder to run successfully, you may find it helpful to consult the [Developing with the Gradescope Autograder in Mind](https://docs.google.com/document/d/1IKSDkG4kHC0gb2FyqdeOWJOAbQr6UCvYZSToIBopfVs/edit?usp=sharing) guide.

If your submission passes the autograder, you should get full points (31/31 points) and you should see output similar to:

<img src="exam2_success.png">

Be aware that the Sanity check does not check for code correctness, but rather that your code compiles. 

Your submission will be graded **after** the deadline. You should test thoroughly yourself to make sure your program works as expected.

## Clarifications

**Can I use a Java feature/library/method that we haven't covered in class?**

Yes, just make sure it doesn't break the autograder. The course staff is not responsible for fixing any submissions that fail the autograder during or after the exam. 

**Can we write more methods than specified?**

Yes, you can write additional helper methods.

**Can I use previous code that I wrote for a PA in my exam?**

Yes.

**What does thread mean for Tweets?**

Use the definition in [PA4](https://ucsd-cse11-sp22.github.io/assignments/pa4.html)


## Task 1 – Arrays
You will be writing the majority of your code in `ExampleArrays.java`, however several tasks will require you to modify other files. For each task, we provided some basic test cases inside the Sanity.java file. You can just do ./run ProvidedArrayTests to run them. We commented out some of the test cases for other methods to make sure you won’t get any errors when trying to run the test case. Please uncomment them when you are finished implementing all the methods for Task 1. Feel free to use this file to test your code by adding more test cases. However, make sure that this file won’t crash the Autograder when you submit it to Gradescope.


### Task 1.1
In the `ExampleArrays` class, you will use the design recipe to write a method called `averageWithThreshold` that takes a `Number[]` (an array of Number objects) and `Number threshold` as two arguments and returns a `Number` that represents the average of all the elements in the `Number[]` that are bigger than the threshold. There are essentially two steps in this task, you need to find all the `Number` that are bigger than the threshold value, then you will need to find the average of all these numbers and return that average. 

If the input `Number[]` contains no numbers that are bigger than the threshold value, return a `Number` representing the integer `0`. If the input `Number[]` is empty, also return a `Number` representing the integer `0`. We will not test `Number` objects that represent negative numbers so you may ignore this case. The `Number[]` tested will not contain numbers that will cause an Integer overflow error. 

To assist you in your task, you will modify the `Number` interface, located inside `Numbers.java`. In addition to all the methods that were written in PA4 (which you can just copy from your PA4), you will add an additional method to the `Number` interface and modify the classes that implement `Number`. That method will be called `compare` and it will take a `Number` as an argument and will return an integer. 

Your `compare` method will behave as follows:
- Case 1: If `this` is numerically greater than `other`, then return `1`
- Case 2: If `this` is numerically lesser than `other`, then return `-1`
- Case 3: If `this` is numerically equal to `other`, then return `0`


### Task 1.2
In the file `ExampleArrays.java`, you will add a new class **OUTSIDE** the `ExampleArrays` class called `Pair`. It will have two fields of type int called `a` and `b`. Its constructor will initialize both fields to be the value as specified by the arguments given to the constructor.

In the `ExampleArrays` class, you will use the design recipe to write a method called 
`findGoodPairs` that will take a `Pair[]` as an argument and return `Pair[]`. Each element of the returned `Pair[]` will be a good pair. The requirement for a good pair is that its first number has to be smaller than the second number. For example, (1,3) is a good pair and (1,0) is not. If there is no good pair then you can return an empty array. 


### Task 1.3
In the `ExampleArrays` class, you will use the design recipe to write a method called `mergePairs` that will take 2 `Pair[]` p1, p2 and return a new `Pair[]`. Each pair in the returned `Pair[]` is “merged” together from elements in p1 and p2.  Say we have Pair[] p1 and Pair[] p2, we want to merge p1[i] and p2[i], with i being any index number, based on the following rules:
The first number of the merged pair is the smaller number between p1[i] and p2[i]
The second number of the merged pair is the bigger number between p1[i] and p2[i]

For example, if p1 = [(1,4), (4, 6)] and p2 = [(2,3), (1,5)], then the returned pair array is [(1, 4), (1,6)]. 

Notes: 
- If the 2 `Pair[]` p1 and p2 are of different lengths, then you will set the length of the returned `Pair[]` to be the length of the shortest Pair[]. You may safely ignore the remaining `Pair` objects of the longer `Pair[]`.
- For p1 and p2, assume that each pair inside these 2 arrays is always a good pair, meaning that the first number is smaller than the second number. 

There are some tests that have been provided in `Sanity.java` for your convenience.

``` java
class ProvidedArrayTests {
    ExampleArrays ea = new ExampleArrays();

    void testAverageWithThreshold(Tester t) {

        Number[] test1 = { new WholeNumber(1) , new Fraction(4, 2), new WholeNumber(3) };
        Number threshold = new WholeNumber(1);

        t.checkExpect(ea.averageWithThreshold(test1,threshold).toDouble(), 2.5);
	}

    void testFindGoodPairs(Tester t) {
        Pair[] p1 = {new Pair(1,2), new Pair(4,3), new Pair(5,6)};
        Pair[] p2 = {new Pair(2,2), new Pair(4,3), new Pair(7,6)};

        Pair[] expect_p1= {new Pair(1, 2), new Pair(5, 6)};
        Pair[] result_p1 = ea.findGoodPairs(p1);

        Pair[] expect_p2= {};
        Pair[] result_p2 = ea.findGoodPairs(p2);
        
        t.checkExpect(result_p1, expect_p1); // Basic test
        t.checkExpect(result_p2, expect_p2); // Empty test

    }

    void testMergePairs(Tester t) {
        Pair[] p1 = {new Pair(1,4), new Pair(4,6)};
        Pair[] p2 = {new Pair(2,3), new Pair(1,5)};        

        Pair[] expect_p1_p2 = {new Pair(1, 4), new Pair(1, 6)};
        Pair[] result_p1_p2 = ea.mergePairs(p1, p2);

        t.checkExpect(result_p1_p2, expect_p1_p2);
    }

    void testMergePairs2(Tester t) {
        Pair[] p1 = {new Pair(1,4), new Pair(10,15)};
        Pair[] p2 = {new Pair(5,6), new Pair(4,5)};        

        Pair[] expect_p1_p2 = {new Pair(1, 6), new Pair(4, 15)};
        Pair[] result_p1_p2 = ea.mergePairs(p1, p2);

        t.checkExpect(result_p1_p2, expect_p1_p2);
    }    
}
```

## Task 2 – Interfaces

We've provided code for `Tweet`, `ReplyTweet`, and `TextTweet` and several related classes that we've used for PAs in `Tweets.java`. Again, we provided some basic test cases inside the Sanity.java file. You can just do ./run ProvidedTweetTests to run them. We commented out this class so that you can run test cases for Task 1 without any compiling error. Please uncomment the ProvidedTweetTest inside Sanity.java before running it.  Feel free to use this file to test your code by adding more test cases. However, make sure that this file won’t crash the Autograder when you submit it to Gradescope. 


### Task 2.1
In `Tweets.java`, you will add a method called `latestTweetOnThread` to the `Tweet` interface and all implementing classes. `latestTweetOnThread` takes no arguments and returns a `Tweet` representing the latest date on the thread as determined by the date. If two tweets have the same years then use their months. Return the `Tweet` with the latest date. 

For `TextTweet`, return the `this` object itself. For `ReplyTweet`, follow the description above to return the Tweet with the latest date.

Note: 
- The date is a String in this format “MM-YYYY” so you need to do some string manipulation to get the value of month and year. You can safely assume that the date is always valid in this format.  
- If 2 tweets have the same date, then return the tweet that appears later on the thread, which is `this` object for ReplyTweet.


### Task 2.2
In `Tweets.java`, you will add a method called `longestUsernameOnThread` to the `Tweet` interface and all implementing classes. `longestUsernameOnThread` takes no arguments and returns a `User` representing the author with the longest username on the thread. If the usernames have the same length, then return the author that appears later on the thread (Note that you don’t need to compare dates for this).

For `TextTweet`, return the author of the tweet itself. For `ReplyTweet`, return the author with a longer username, as described above, with `this ReplyTweet` as the latest tweet in the thread. 

There are no specific test requirements for these methods other than the one listed in the video below; we will test them to ensure they are correct and you should test them thoroughly enough to be confident in their correctness.

There are some tests that have been provided in `Sanity.java` for your convenience.

```java
class ProvidedTweetTests {
    User u1 = new User("greg", "Greg", 12);
    User u2 = new User("greg2", "Greg2", 12);

    Tweet t1 = new TextTweet("We're already halfway through with the quarter", u1, 12, "05-28-2022");
    Tweet t2 = new ReplyTweet("Yeah, can you believe it. It still feel like the beginning of the quarter", u2, 13, "04-28-2021", t1);

    void testLatestTweetOnThread(Tester t) {
        t.checkExpect(t2.latestTweetOnThread(), t1);
    }

    void testLongestUsernameOnThread(Tester t) {
        t.checkExpect(t2.longestUsernameOnThread(), u2);
    }
}
```

## Task 3 – Main and Command-Line Arguments

Your task is to write a program in `WordFilter.java` that will filter palindrome words from an array of words. 

Palindrome words are words that read the same backward as forward. For example: “kayak” is a palindrome word. 

Notes:
If there are no words provided as command line arguments, print **Empty Array** .
Ignore the case with empty string, we won’t be testing those. 
If no word is a palindrome in the list, then don’t print anything.
Assume that all words in the array are lowercase. 

To test your program, you can do the following and the result should be the same as below. 

```
$ javac WordFilter.java
$ java WordFilter cat dog kayak level
kayak level
$ java WordFilter cse11 classes students 
$ java WordFilter
Empty Array
```

## Video Task

You will record a short video of no more than 6 minutes. 

Tip: If you find yourself running out of time, you might be explaining your code too much. If the task does not ask you to directly explain your code, you don't need to explain it. 

Include:

- Show only your face and a picture ID (your student ID is preferred but any
picture ID with your name on it will work) for a few seconds at the beginning.
You don’t have to be on camera the whole time, though it’s fine if you are. Just
a brief confirmation that it’s you creating the video/doing the work attached to
the work itself is what we want. If you do not have a webcam, take a picture of
yourself (and your picture ID) with your phone and display that picture at the
start of your screen share.
- `averageWithThreshold`
  - Choose an example of calling `averageWithThreshold` with an array of at least length 4 where there should be at least 1 number bigger than the threshold value.
  - Write down a table corresponding to **one** loop you wrote in the body of the method that shows, for **all** variable(s) involved in the loop, what its value is at the start and end of each loop iteration. Write your table in a comment next to the loop, as  shown in the example below. 
  - You may write the Number objects using their "toText()" representation. That means that you may write `WholeNumber` as `n` and `Fraction` in the form `n/d`. 
  - You may pre-write the header row of the table, but you **must** fill in the
  contents of the table on the video. As you fill in the “end” value for each
  variable, indicate which statement(s) in the program caused its value to
  change.
  - If a `return` statement happens in the loop, note that in the row as well.
  - If the word only has 1 character, then it is not a palindrome. 

  ```
  int a = 0;
  int z = 0;
  for(int i = 1; i < 6; i += 2) {
    z += i;
  }
  /*
  i start   i end   z start   z end
  1      	  3       0         1
  3         5       1         4		
  5         7       4         9
  */
  ```


- Choose a test that you wrote on your own for `latestTweetOnThread` where the thread has at least 2 `ReplyTweet`s and 1 `TextTweet`. You will need to write this test outside of your testing methods and store the result in a field. Run the program and show the output for that object, and the objects it references, at the terminal. Then, next to the example, describe the stack in a comment, where in each line you indicate:
  - The *class* of the method called
  - The *name* of the method called
  - The *reference* of the `this` parameter (the reference numbers do not need to be consistent with what `./run` gives, but they should be consistent with the order of the objects)
  - The *return value* of that method call. Use reference numbers here.

  Put the call that happens first on the last line of your stack trace (so it's
  at the bottom, as we've drawn in problem sessions and in the notes and
  videos). Only include calls to the `latestTweetOnThread` method. If you include any more methods, you will have points deducted. 

  You may prepare the table header (class, method, reference number, return value) prior to your video, but the table itself **must** be filled in during your video.

  You may abbreviate class names as long it is obvious what class the abbreviation is referring to.

  As an example, consider this program, output, and test:

  ```
  interface I { boolean m(); }
  class C { public boolean m() { return false; } }
  class D {
    I i;
    D(I i) { this.i = i; }
    public boolean m() { return !this.i.m(); }
  }
  class Examples {
    C c = new C();
    C c2 = new C();
    D d1 = new D(this.c);
    D d2 = new D(this.c2);
    D d3 = new D(this.d1);
    boolean ans1 = this.d2.m();
    boolean ans2 = this.d3.m();
    /*

    class	method  reference   return value
    C     m       :1          false
    D     m       :2          true
    D     m       :3          false
    */
  }
  $ ./run Examples
  Tester Library v.3.0
  -----------------------------------
  Tests defined in the class: Examples:
  ---------------------------
  Examples:
  ---------------
  new Examples:1(
   this.c = new C:2()
   this.c2 = new C:3()
   this.d1 = new D:4(
    this.i = C:2)
   this.d2 = new D:5(
    this.i = C:3)
   this.d3 = new D:6(
    this.i = D:4)
   this.ans1 = true
   this.ans2 = false)
  ---------------
  No test methods found.
  ```

