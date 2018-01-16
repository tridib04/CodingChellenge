# CodingChallenge

Problem:

Given a collection of 5-digit ZIP code ranges (each range includes both their upper and lower bounds), 
provide an algorithm that produces the minimum number of ranges required to represent the same restrictions as the input.


Project Structure:

1. Data package which contains the POJO to hold lowerBound and upperBound zip codes.
2. Main package which contains the runner class
3. Service package which contains main business logic
4. Util package which contains the validation class.
5. Exception package which contains a custom exception class.
6. Test package which contains the JUnit test class.

Assumptions:

Zip Code is valid only it is numeric characters, has a length of 5 and cannot be null. 
If neither is matched exception will be thrown.

Algorithm:

1. Create a new list L to hold the new merged list.
2. Valid data then proceed otherwise throw exception "Not a Valid Zip". (Validation includes length, null check and numeric values).
3. Check if the L is empty (intial first run case), then add the ZipRange object to the list. 
		Otherwise merge the range if it overlaps with the existing range.
4. flag = false
5. If the new range exists with the existing range no need to add, set flag to false.
6. If the new range doesn't exists with the existing range need to add, set flag to true.
7. If the range overlaps , merge them, set flag to true.
8. If toAdd flag is true, add the Object to the list		 
