### Title: How to convert between binary and decimal
### Author: Kevin Pagan Maisonet
### Summary: 
This tutorial is to teach students the basics of binary numbers and their conversions. This means what a binary number is, how they relate to decimal numbers, and easy  algorithmic ways to manually convert a binary number to a decimal and vice versa.
### Target Audience: 
The tutorial is geared towards students, particularly very early students with little to know experience in anything IT related. This is why there are no mentions of the nuances to the "on and off" signals in computers, but dive deep into the values of each and every numbers place in both the binary and decimal systems.

<br><br>

# Binary and Decimal Conversions

Decimal refers to the number system we use daily where every single digit represents a number 1-10. For example, look at the number 157.

# <u>1</u> &nbsp;&nbsp;&nbsp;&nbsp; <u>5</u> &nbsp;&nbsp;&nbsp;&nbsp; <u>7</u>

1. In the far right is the 1's place where 7 represents seven 1s, or 7.

2. Then in the middle is the 10's place where *5* represents five 10's, or 50.

3. And finally in the far left is the 100's place. Where *1* represents one 100.<br>

And when you tally this entire number up, it will make 

### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1(100) + 5(10) + 7(1) =
### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;100 &nbsp; + &nbsp; 50 &nbsp; + &nbsp; 7 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = &nbsp; 157 

<br>

While this makes sense to us humans, partially because we normally have 10 fingers making this base easy to represent with our own bodies, **base-10.** But what if we were a computer? Computers don't have fingers, so instead of using these 10 non-existent fingers to count, they use 2 figurative ones. On and off, **base-2.**

Fundamentally, computers run off of electricity and an easy representation of a number would be a pulse, an on and an off. This is not an entirely new idea either as previous methods of communication, like Morse code, also relied on similar pulses.

# Binary Representation

Previously we saw how in the base-10 system, every single digit can can be 1 of 10 numbers. In binary though, each digit can only be 1 of *2* numbers. *And* instead of each place representing an exponent of 10 (*Ex: 10^0 = 1, 10^1 = 10, 10^3 = 100*), each place will represent an exponent of 2. Let's take a look at the binary number 101 as an example.

# <u>1</u> &nbsp;&nbsp;&nbsp;&nbsp; <u>0</u> &nbsp;&nbsp;&nbsp;&nbsp; <u>1</u>

1. The far right is going to be the 2^0, or 1's, place. So a 1 in this place represents one 1.

2. The middle is going to be the 2^1, or the 2's, place. So a 0 in this place represents zero 2s

3. And finally in the far left place is the 2^2, or the 4's, place. So a 1 in this place represents one 4.

And when you tally *this* entire number up, it will make 

### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1(4) + 0(2) + 1(1) =
### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4 &nbsp; + &nbsp; 0 &nbsp; + &nbsp; 1 &nbsp; &nbsp; &nbsp; &nbsp; = &nbsp; <u>5</u>

<br>

So 101 in binary is **5** in decimal. 

# From Binary to Decimal
The previous example is actually precisely how you convert from binary to decimal. We look at every single number and in which numbers place it is, add it up, and we will have the decimal value. 

Most binary numbers you will see though, will be 8 digits long. So let's try another more realistic example:

# 0101 1100

This number can be written as 01011100 or as 1011100, but it is much more readable to divide it into 2 parts of 4 and keep any leading 0's. Lets do the left half first:

### &nbsp;&nbsp;&nbsp;&nbsp; <u>0</u> &nbsp;            &nbsp;&nbsp;&nbsp; <u>1</u>                   &nbsp;&nbsp;&nbsp;&nbsp; <u>0</u>            &nbsp;&nbsp;&nbsp; <u>1</u>
 2^7 &nbsp; 2^6 &nbsp; 2^5 &nbsp; 2^4
 
 128 &nbsp; &nbsp; 64 &nbsp; &nbsp; 32 &nbsp; &nbsp; 16
 
 0(128) + 1(64) + 0(32) + 1(16)
 
 <br>
 Then do the right half
 
### &nbsp;&nbsp;&nbsp;&nbsp; <u>1</u> &nbsp;            &nbsp;&nbsp;&nbsp; <u>1</u>                   &nbsp;&nbsp;&nbsp;&nbsp; <u>0</u>            &nbsp;&nbsp;&nbsp; <u>0</u>
  2^3 &nbsp; 2^2 &nbsp; 2^1 &nbsp; 2^0
 
&nbsp; &nbsp;8 &nbsp; &nbsp; &nbsp; 4 &nbsp; &nbsp; &nbsp; 2 &nbsp; &nbsp; &nbsp; 1
 
 1(8) + 1(4) + 0(2) + 0 (1)
 
 <br>
 
 All of this equalling:
 
 64 + 16 + 8 + 4 = **92**
 
# From Decimal to Binary

This process can also be done in reverse. Let's take the number 151 as an example. When we went from binary to decimal, we *ADDED* all the digits values where there was a 1. Now to go from decimal to binary, we can simply reverse this and subtract everything. 

### &nbsp;&nbsp; &nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>          &nbsp; &nbsp; &nbsp; &nbsp;          <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u> 

We will represent each place as it's value if it were a 1.

### &nbsp;&nbsp;128 64 &nbsp;32 16 &nbsp; &nbsp; &nbsp; &nbsp; 8 &nbsp; &nbsp;4 &nbsp;&nbsp;&nbsp;2 &nbsp; &nbsp;1

And we will simply go down the line of places, looking for the first and biggest number we can possibly subtract our decimal by. 

So, in our example, the biggest number that 151 can be subtracted by is of course 128. And we will do so. 

151 - 128 = **23**

23 will now be the number we continue subtracting things from. And since we could take 128 from 151, we will mark that place as a 1. Our converted number for now looks like this:

### &nbsp;&nbsp; &nbsp; <u>1</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>          &nbsp; &nbsp; &nbsp; &nbsp;          <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u> 

The next two places, 64 and 32, are two big to subtract from 23. However, 16 isn't. So we will repeat the process

23 - 16 = **7**

And our converted now looks like this:

### &nbsp;&nbsp; &nbsp; <u>1</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>1</u>          &nbsp; &nbsp; &nbsp; &nbsp;          <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u> 

With zeroes still in the spots where we could not subtract from.

Now we continue. 

7 - 4 =  **3**

3 - 2 = **1**

1 - 1 = **0**

And the *FINAL* binary number is:

### &nbsp;&nbsp; &nbsp; <u>1</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>0</u>  &nbsp;&nbsp; <u>1</u>          &nbsp; &nbsp; &nbsp; &nbsp;          <u>0</u>  &nbsp;&nbsp; <u>1</u>  &nbsp;&nbsp; <u>1</u>  &nbsp;&nbsp; <u>1</u> 
