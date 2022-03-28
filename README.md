# tech-isbn

The ISBN-10 verification process is used to validate book identification numbers. These normally contain dashes and look like: 3-598-21508-8 

 

The ISBN-10 format is 9 digits (0 to 9) plus one check character (either a digit or an X only). In the case the check character is an X, this represents the value '10'.  

 

Part 1 

 

The following is an ISBN verification algorithm: 

From the last digit moving backwards, multiply each digit by its index, starting from 1  

Sum all the values 

If the remainder after dividing by 11 is zero, then the number is a valid ISBN number 

 

Test cases  

3598215088 true  

3598215089 false 

 

Part 2 – adds an additional feature (see step 2) 

 

The following is an ISBN verification algorithm: 

From the last digit moving backwards, multiply each digit by its index, starting from 1  

If the digit is the letter X then it should be treated as the number 10 

Sum all the values 

If the remainder after dividing by 11 is zero, then the number is a valid ISBN number 

 

Test cases  

359821507X true 

359821515X false 
