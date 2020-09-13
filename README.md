# Programming

You don't want nouns in function names: `TestableHtml`.

They should be verbs, because **functions do things**: `renderPageWithSetupsAndTeardowns`.

Every line of a function, should be at the same level of abstraction and that level should be one below the name.

First write code to get things done, BUT ALWAYS FIX THEM AFTERWARDS. **CLEAN THEM UP.**

**Getting code to read like well written pose:**
```
bool isTestPage = pageData.hasAttribute("Test");
if (isTestPage)
```
*If it is test page.*

---

## Functions should be ONE thing

A function is ONE thing, if you can't meaningfully extract another function from it.

Functions should not be 100 lines long.

Functions should HARDLY ever be 20 lines long.

**First rule of functions:**
They should be small.

**Second rule:**
They should be smaller than that.

Functions should not be large enough to hold "nested" structures. Therefore the indent level of a function should **not be greater than one or two.**

**Don't pass booleans into function arguments.**

A function should NOT have more than 3 arguments.

A set of functions that manipulate a set of variables is called a "Class".

Code that makes you double take, is rude: **Make sure that your code is not surprising.**

Avoid switch statements.

**Polymorphism:** Handlers, like BeFriendlier-Bot's handlers. **Every statement/case should come from a base class and have their own invocation functions.**

**Treat programming like science.** Test things!
Prove your software is not incorrect by surrounding it with tests.

"Why would you write code and then not test it?"

## Comments

### What is the purpose of a comment

To explain code that the code cannot explain.

Do not make excuses in the comments.

**Comments are chaotic neutral.**

Comments should be used to compensate for failures of expressing ourselves in code.

Comments do not make up for bad code.
<img src="https://i.imgur.com/y5utY56.png">

**Legal comments are allowed:**

```
// Copyright ...
```

### Informative comments

<img src="https://i.imgur.com/lZzetej.png">

*Second comment is lying. It matches way too much because of the "\*".*

**Todo comments should not be pushed to git, they should be DONE BEFORE committing otherwise they turn into "DON'T DO".**

Don't mumble in your comments, your code should explain itself.

DO NOT comment out code, **JUST DELETE IT**, before committing.

When writing comments, do not write about code that is somewhere else, make sure it is about the code adjacent to it.

## Naming

### Names of variable.

* Reveal intent:

  NOT "int d;"

  BUT "int elapsedTimeInDays;"

*How long should a variable name be?*

**Huge scopes need long names.**

What's a huge scope?

**A global variable:**
It better have a long name.

### Names of functions & classes

The opposite of a name of a variable. **The larger the scope, the shorter the name because it's going to be called all over the codebase.**

**Example:**

NOT `openFileOrThrowException()`,

BUT `open()`.

If the function is in a large scope it must be **abstracted**, therefore it must be shorter.

So in some instances, `int d;` is fine if the scope is tiny and more precise.

----

**Do not use noise words like "data", "info".**

Make sure your names are pronounceable.

---

## Expectations

* Do not ship shit.

Does all code need to have bugs?

* You will know your code works.

* Your code has the highest quality you can put out.

* Customers EXPECT that the code works, otherwise they will COMPLAIN BITTERLY.

* You will always be ready.

* If you do AGILE: You **must** be ready to deploy after a sprint, example: every 1-2 weeks.

* Stable productivity.
New product features shouldn't take longer and longer to code.

* Inexpensive adaptability.
Software means changeable product: To change behaviour of a machine. Your software must be **EASILY** (SOFT) CHANGEABLE PRODUCT.

* Continuous improvement.
Of the system, of the code. The code should be getting better with time.

* Fearless competence.
Do not be afraid of code! Clean the code!
DO NOT FOLLOW "If it ain't broke, don't fix it". Leave that to the wusses.
Do small changes to the function, keep checking if it still works (Run the tests) AND FIX THE MESS.
**"Commit the code a little bit better than when you found it."**

* You will not dump on QA...
**Do not use QA to find bugs on the system.**

* ...Because QA is not supposed to find anything.
The DEVELOPERS are the ones who are supposed to find bugs.
QA is always under HELLISH pressure. QA does NOT belong at the end of the process, they should be at the beginning because QA is NOT supposed to find anything.

**AUTOMATE YOUR TESTS: If a computer can do it, it should do it.**

* Honest estimates.
"I don't know" is THE MOST honest estimate but it doesn't contain enough information.
Define what we don't know: P.U.R.T. (Project Evaluation in Real Time) Don't give an estimate of one number, give an estimate of 3 numbers.

  1. The best case: If everything goes RIGHT. (Probably 1 week)
  2. The nominal case: If everything goes the usual way. (Probably 3 weeks)
  3. The worst case: If everything goes wrong. (Probably 8 weeks)

**I can't give you 1 number, you have to give 3 numbers: DO NOT LIE.**
