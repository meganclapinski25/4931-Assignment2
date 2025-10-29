# Debug Log

**Explain how you used the the techniques covered (Trace Forward, Trace Backward, Divide & Conquer) to uncover the bugs in each exercise. Be specific!**

In your explanations, you may want to answer:

- What is the expected vs. actual output?
- If there is a stack trace, what useful information does it contain?
- Which technique did you use, on which line numbers?
- What assumptions did you have about each line of code, and which ones were proven to be wrong?

_Example: I noticed that the program should show pizza orders once a new order is made, and that it wasn't showing any. So, I used the trace forward technique starting on line 13. I discovered the bug on line 27 was caused by a typo of 'pzza' instead of 'pizza'._

_Then I noticed another bug ..._

## Exercise 1

[[The first error I got was that the toppings was invalid keyword argument. I decided to use the trace forward technique starting on line40 where the PizzaTopping class starts, discovered that we were using the toppings from the Pizza class but asking for the PizzaTopping class on line 79. Then after that I ran into a route bug, showing that fulfull was not the correct route on   ]]

## Exercise 2

[[Your answer goes here!]]

## Exercise 3

[[Your answer goes here!]]
