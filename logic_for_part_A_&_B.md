Logic to the Problem Statement :
The problem statement is to calculate the total combinations that are possible by rolling the dice , distribution of all possible combinations that can be obtained when rolling both Die A and Die B together and the Probability of all Possible Sums occurring among the number of combinations from (2).
1) The total number of combinations can be calculated by using the formula:
                = (Number of faces of a die)^(Number of dice used)
The logic for the first question can be given as ,first initialize the value of number of faces as” x=6”. Get the number of dice used as user input from the user. Using pow function calculate the number of combinations using the formula “pow(6,n)” and store it in a variable “total”. Print the variable “total”.So the number of combination is given as 36 since the number of dice used is 2.
2)	Calculate and display the distribution of all possible combinations that can be obtained when rolling both Die A and Die B together.
The logic for this second question is that ,here I used two for loops control structures to print the 36 combinations of the two dices. The for loop iteration starts from “1” and ends with “6”(7-1) since the for loop takes one value lesser than the end value. So the iteration runs 36  times and the combinations are printed.
3)	Calculating Probability of all Possible Sums occurring among the number of combinations from (2).
The logic for the third question is, here I created an empty list and using two for loop control structures, the sum of two dice values are found by adding the “I” and “j” value(i+j). The sum of i+j is appended to the empty list “a” . Using count method the sum of each dice value is counted and the probability distribution is printed by dividing the count by total number of combination that is 36. 
Logic for part-B:
●	If we look at the problem’s combinations for the lowest value that is 2 and the highest value that is 12,
●	Number of occurences of 2 = 1 time = [1,1] Number of occurences of 12 = 1 time = [4,8]
●	Since 2 comes only once with a combination of [1,1] both the new dice values New_Die_A and New_Die_B must contain value 1 . Also the sum 12 occurs only once with a combination of 4+8=12 that is [4,8]. Therefore the New_Die_A must contain 4 only once and New_Die_B must contain 8 only once. 4 must be present in New_Die_A only once because if there are more than one 4 in New_Die_A then the occurrence of sum 12 will occur more than one time. Also 8 must be present in New_Die_B only once because if there are more than one 8 in New_Die_B then the occurrence of sum 12 will occur more than one time. So the initial dice values are
●	New_Die_A = [1, 4, a1, a2, a3, a4] New_Die_B = [1, 8, b1, b2, b3, b4]
●	We need to find the values of a1 , a2 , a3 , a4 and b1 , b2 , b3 , b4 by combinations method.
●	The variables a1 , a2 , a3 , a4 will be repetitive combinations of 2 and 3 . That is a1 , a2 , a3 , a4 will be either 2 or 3.
●	So the combinations for this variables a1 , a2 , a3 , a4 are given as : 2,2,2,2
●	3,2,2,2
●	3,3,2,2
●	3,3,3,2
●	3,3,3,3
 
●	Also b1 ,b2 , b3 , b4 will be a combinations of any four values within 2,3,4,5,6,7 because the New_Die_B will have elements which are distinct . So totally there will be only 15 combinations. Eg : [4,5,6,7]….
●	Trying out the 15 combinations with the above 5 combinations may lead to 75 different combinations.
●	So therefore upcoming repetitive iterations using for loop…the combination 2,2,3,3 for a1, a2, a3, a4 with the combination 3,4,5,6 for b1 ,b2, b3, b4 will be the perfect answer for this problem
●	Therefore the answer is :
●	New_Die_A	=	[1,2,2,3,3,4]
●	New_Die_B = [1,3,4,5,6,8]
●	Logic for the code :
●	First get the Dice values from the users as user input for both the variables Die_A
●	and Die_B using a for loop .
●	Then create two user defined functions def calculate_sums(die_a, die_b) and
●	def undoom_dice(Die_A, Die_B) .
●	The calculate_sums() function is used to calculate the sum of combinations of the dice values i.e [2,3,4,5,6,7,8,9,10,11,12] with repetition.
●	The original_sums variables is used to take only the unique sum values.
●	Create a dictionary named as original_probabilities to store the probabilities with the sum as the key and probability distribution as the key value.
●	Now the New_Die_A and New_Die_B are to be calculated with combinations . As we said New_Die_A will have only one 1 and only one 4 in it for sure and New_Die_B will contain 1 once and 8 once. The remaining four values of both New_Die_A and New_Die_B must be found .
●	First New_Die_A is found using these five combinations [2,2,2,2], [3,2,2,2],[3,3,2,2],[3,3,3,2],[3,3,3,3] for those four variables a1,a2,a3,a4 using nested for loops .
●	The New_Die_B is found by checking the each probabilistic values with 15 more combinations . Likewise the loops are run for 75 times and checked with the probabilistic distribution variable original_probability which finally detects the values as
●	New_Die_A = [1, 2, 2, 3, 3, 4]
●	New_Die_B = [1, 3, 4, 5, 6, 8]

