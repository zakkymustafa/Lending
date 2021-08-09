# Lending

Write a function that takes two arguments, you can call them whatever you want but
we'll refer to them here as transactions_csv_file_path & n. The first argument,
transactions_csv_file_path, is a string indicating the location of a csv file
containing transaction data. There are three examples of transaction data files in
this directory. The second argument, n, is an integer.

Your function should return the ids of the n best customers from the transaction data.
For this excercise we say that the best customer is the one that has the longest period
of consecutive daily payments, the second best is the one with the second longest
period, etc. 

Notes:
	- When we say consecutive daily payments, we mean that there is at least one
		transaction per consecutive calendar day.
	- When we say longest period of consecutive daily payments, we mean the period
		that contains the greatest number of consecutive calendar days.
	- If you need to break ties, you should choose account numbers that come first
		alphabetically.


Test cases:

Input:
	- transactions_csv_file_path: 'transaction_data_1.csv'
	- n: 1
Expected output:
	- ['ACC2']
  
  Input:
	- transactions_csv_file_path: 'transaction_data_2.csv'
	- n: 2
Expected output:
	- ['ACC1', 'ACC4']

Input:
	- transactions_csv_file_path: 'transaction_data_3.csv'
	- n: 3
Expected output:
	- ['ACC143', 'ACC214', 'ACC312']
