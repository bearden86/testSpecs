# testSpecs
block 18 workshop

we are going to implement Test Driven Development (TDD). There will be Unit test specs (low level, specific individual function or task), Functional test specs (functionality based on user interaction)

format for unit test specs:
- expect [action] to be [some result]
- example prompt: a function called addition that returns the sum of two input integers
- expect addition(2, 3) to be a number
- expect addition(2, 3) to equal 5
- expect addition('a', 3) to be an error

format for functional test specs:
- when a user clicks 'log in' without filling in any information, they should be shown an error and prompted to sign in
- when a user clicks 'log in' but has filled out credentials incorrectly, they should be shown an error and prompted to sign up if not already
- when a user clicks 'log in' and has filled in their login credentials correctly they should be taken to the dashboard


//PROMPTS// and //RESPONSES//

Unit Tests
1. A function called 'multiplication' that returns the product of the two input numbers
   - expect multiplication(num1, num2) to multiply num1 and num2 and return the product
   - expect multiplication(num1, num2) to return an integer
   - expect num1 and num2 to be integer parameters
   - expect any parameter other than an integer to cause an error
2. A function called 'concatOdds' takes two arrays of integers as arguments. it should return a single array that only contains the odd numbers, in ascending order, from both arrays.
   - example: concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1]) should result in [-1, 1, 3, 9, 15]
  
   - expect concatOdds([array1], [array2]) to return an array of odd numbers from values in given arrays
   - expect concatOdds([array1], [array2]) to only accept integer inputs, all others result in error
   - expect concatOdds([array1], [array2]) to compare values accepting only odd numbers and sort them in ascending order
   - expect concatOdds([array1], [array2]) to ignore multiple instances of the same odd number
  

Functional Tests
1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.
   - when a user clicks 'check out' and the cart is empty, they should receive an error that the cart is still empty
   - when a user has items in their cart and click 'check out', they should be prompted with two options, 'log in' or 'continue as guest'
   - when a user clicks 'continue as guest' they should be able to check out after providing the needed payment and shipping information
   - when a user clicks on their 'cart', they should see a clear summary of all items and prices, including subtotal
   - when a user logs in after clicking 'check out', any saved payment and shipping information should be preloaded for ease of use, but they should be prompted to review and ensure validity
   - when a user has completed cart, billing and shipping info, the final page should be a review before hitting final submit button for purchase
   - user should receive a confirmation page after successfully completing check out.
