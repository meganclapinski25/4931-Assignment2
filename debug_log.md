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

-- File "/Users/meganclapinski/Downloads/SPD-2.3-Debugging-Techniques-Lab-main/exercise-2/app.py", line 52, in results
    'city': result_json['name'],
-- File "/Users/meganclapinski/Downloads/SPD-2.3-Debugging-Techniques-Lab-main/exercise-2/app.py", line 54, in results
    'temp': result_json['main']['temperature'],
    KeyError: 'temperature' 


-- The first error I got was a KeyError : 'name' on line 52. I decided to trace backwards and work throguh ecah line of code before the error took place. I found that when requesting the city and units, that we were calling from an unknown variable. I changed those to match the name of the input. After that I still got the same error. So at this point I decided to look at the API docuimentation, check that params were correct in order to call the correct API calls. I saw that for cities the pararmeter used is q. So i changed 'place' to 'q' in the params. I then got another KeyError with 'temperature', I looked up the API documentation again and saw that the JSON calls temp and not temperature 

## Exercise 3

Errors: 
IndexError: list index out of range
TypeError: list indices must be integers or slices, not float


Answer : 
    - The error is from line 37 from utils.py saying list index out of range. I traced backwords and saw that we were satrting from the leftt index with I on the right side which would go out of bounds. My next error was TypeError: list indices must be integers or slices, not float. An integer is being sent as a flot. So I go from my error line and work backwards to see the math done before the arugment. I saw that we are using the division sign '/' which returns the value as a float. I changed that to floor division // 
