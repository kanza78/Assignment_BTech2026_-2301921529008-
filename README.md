

### Problem statement

Reverse Integer
Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0

Course Schedule IV

### Coding Platform used
LEETCODE

###	Approach and solution explanation.

Initialization:
Create a variable ans and initialize it to 0. This variable will hold the reversed number.
Processing Each Digit:
Use a while loop to iterate as long as x is not zero. In each iteration:
Extract the last digit of x using x % 10 and store it in the variable digit.
Check if appending the digit to ans would cause overflow or underflow. This is done by comparing ans with INT_MAX / 10 and INT_MIN / 10.
If ans is greater than INT_MAX / 10, multiplying it by 10 and adding any digit would exceed INT_MAX.
Similarly, if ans is less than INT_MIN / 10, multiplying it by 10 and adding any digit would go below INT_MIN.
If the overflow or underflow condition is detected, return 0.
Update ans by multiplying it by 10 and adding the digit.
Remove the last digit from x by performing integer division x / 10.
Return Result:
