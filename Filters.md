**Logic :** Client -> (Routing -> Controller -> Action Method) -> return to Client


2. Where we can Apply :
-----------------------
A. Globally

B. Controller 
Before execution
    |
(Controller)
  
  
C. Action 
Before execution
    |
(Action) - Execution Time
    |
After execution

3. How to Use :
---------------
We can use filter as Attribute 

4. 5 types of Filter :
----------------------
it execute this order type
1. Authentication
2. Authorization
3. Action
4. Result
5. Exception

We can make cutom filter all 5 types of.

5. PreDefined Filter :
----------------------
OutputCache
HandleError


