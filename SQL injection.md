# SQL injection 

## what is SQL injection, and how it effects, how to protect it 

## how do you identify that SQL can occur  
enter `'` in any search bar or anywhere you can get response 
![[Pasted image 20251128081714.png]]
we entered `'` here and the response was an error which has shown bellow 


![[Pasted image 20251128081640.png]]
and thats how we know that there is an vulnerability in this area 

## how many columns are returned 
we type a special code to see how many columns are there
`a' union select "1","2";-- -  
![[Screenshot_2025-11-28_08_55_04.png]]
 how do we know that there are only two columns ? because if we enter the code with only one it doesn't give us any response and neither with three . 


### now once you have identified that where to inject the code and how many columns are there you start the main code injection  

# perform SQL injection 

## all  the tables in current data base 
