# DSA


# Why do perf-test cases fail?

# Do you understand the issue?
 Perf-test cases fail if the required performance is not met, in some cases if you unlock and run these you might also get the right output. 

# Where is the issue occurring?

# If Only performance test cases are failing either the time complexity of your code is not meeting the requirements or you’re not using the right data types to store the value. Can you look at the code and check what is the time complexity of it?

# Why do you think you are seeing this issue? What might be causing it?

 There are mainly 2 reasons why you would perf-test cases:

You’re not using the right data type, for example you might need a long variable to store values but you might be using int.

You’re not using the optimized approach, you might be implementing an O(N^2) but the problem can be solved in O(N)

How to Debug this? To debug this issue, I would recommend the following steps:

You can follow these steps to find and solve this issue: 

Take a look at the input constraints of the problem.

Identify what should be the time complexity of the solution based on the provided input constraints.

Optimize your solution (use of different data structure or reduction of loops etc.) to reduce the time complexity. 



# Why am I getting a timeout error?
# Do you understand the error?

We get a timeout error if we have a never ending loop in your code.

# Where is the error occurring?

# This will happen in the loops that are defined in your code, can we check the loops and their conditions?

# Why do you think you are seeing this error? What might be causing it?

If the loop condition is never met, the loop will continue running infinitely and running your code will result in a timeout error.

How to Debug this? To debug this issue, I would recommend the following steps:

Try to check the iterator in your loop and what is the condition where it should break. If the condition is never met, the loop will never break.

Add print statements or log messages to your code to track the progress of the loop. This can help you see where the loop is getting stuck. You can also do a dry run of your code with different test cases to see where it may fail.

Example of a never ending loop:

i = 1 

while(i > 0){

//statements

i = i+1

}



# What causes an Array Index Out Of Bounds Exception?
# Do you understand the error?

As the name says, we have an index that tries to access an element in an array that does not exist.

# Where is the error occurring?

Can you check the places you’re trying to access the array? This could be anywhere in the code, if you have a loop or recursive calls where the array is being indexed, check them as well. 

# Why do you think you are seeing this error? What might be causing it?

If in any case your index goes out of range of 0 to n-1, where n is the length of the array you would get the exception saying the index is out of bounds.

# How to Debug this? To debug this issue, I would recommend the following steps:

Dry run with an example and check what array values you’re trying to index.

The error code would look like this:

arr = {1, 2, 3}

val = arr[3]

Here the array only has values from index 0 to 2 but we’re trying to access the array with index 3. This would give you an error. To fix this, you would need to analyze why your code is trying to access an index that it shouldn’t. This could be happening in a loop, you would need to check the loop conditions and see that they are within expected range.
As an example:

for(i=0; i <= arr.length; i++) //gives error as i goes from 0 -> 3

for(i=0; i < arr.length; i++) //does not give error as i goes from 0 -> 2  //Approved



# Why am I getting an undefined error?
# Do you understand the error?

When writing code in JavaScript, any variable that does not have a value assigned to it is called undefined.

# Where is the error occurring?

# Error could be occurring at any variable that does not have a value assigned to it, can we run and check what variable the output/error is showing undefined?

# Why do you think you are seeing this error? What might be causing it?

Once you find the variable, you can see that you are doing something that is not syntactically right, like trying to find its length or trying to access a value that is not assigned. 

How to Debug this? To debug this issue, I would recommend the following steps:

If you’re getting “undefined”, check the variable initializations. It is also suggested to check the array indexes your code is trying to access.

For ex : -

arr = [1, 2, 3]

console.log(arr[3]) //gives undefined 

console.log(arr[2]) //gives 3 



 If you’re accessing elements in a map, it is also suggested to check them. 

Example:

mp = {‘a’ = 1}

console.log(mp[‘a’]) // gives 1

console.log(mp[‘b’]) // gives undefined as there is no key for ‘b’ in mp  



The below code will give an error, as the a is undefined:

let a

console.log(a.length)



Why is my Base test failing?
Do you understand the error?

Base tests fail if our code is not checking for all the different inputs that need to be handled.

Where is the error occurring?

Error is in the logic of the code, can we re-read the problem statement and check if all the possible input cases are covered?

Why do you think you are seeing this error? What might be causing it?

Can we unlock the failing test case and run it, this will help us understand what is the input, expected output and actual output for the failing test case. We can dry run on this if needed to find the issue with the logic in our code.

How to Debug this? To debug this issue, I would recommend the following steps:

To avoid this, it is recommended that you write a few test cases even before you start writing the code. This will help you write most of the logic initially so major changes need not be done after hitting the submit button. Even if you have already written the code, the same steps need to be followed to find and fix the issue.

write test cases that exercise the base cases that you have identified. These test cases should include a variety of different scenarios, both expected and unexpected, to test the full range of your code's capabilities. 

For example, let's say we are asked to capitalize the first character of every word in a string, and there are no special characters in the string, we can write test cases like below initially to test:

learn by doing

learn By Doing

Learn by       doing

LEARN BY DOING

learn      by      doing

Now once we find where the logic is failing, we can update our code so our code passes these test cases.



# Why is my Edge test failing?
# Do you understand the error?

Edge tests fail if our code is not checking for the weak points on the inputs.

# Where is the error occurring?

Error is in the logic of the code, where we are not checking for the edge inputs. Can we look at the constraints of the problem and check if we are covering all the possible inputs?

# Why do you think you are seeing this error? What might be causing it?

Can we unlock the failing test case and run it, this will help us understand what is the input, expected output and actual output for the failing test case. We can dry run on this if needed to find the issue with the logic in our code.

How to Debug this? To debug this issue, I would recommend the following steps:

To avoid this, it is recommended that you write a few test cases even before you start writing the code. This will save your debugging time and help you write better logic.

We can write a few test cases and check how those input values are handled by the code. For example let’s say we are asked to find the middle character of give string, the possible edge test cases we would test for are:

What if the input string is empty?

What if the input string only had one char?

What if the input string is of even length?

What if the input string is of odd length?

Now once we find where the logic is failing, we can update our code so our code passes these test cases.

Resource: How to come up with edge cases


