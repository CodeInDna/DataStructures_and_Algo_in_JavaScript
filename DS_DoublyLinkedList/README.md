# DoublyLinkedList
Doubly Linked List with methods
----------------------------------------------------------------------------------------------------------------------------------------

Push pseudocode
•	Create a new node with the value passed to the function
•	If the head property is null set the head and tail to be the newly created node 
•	If not, set the next property on the tail to be that node
•	Set the previous property on the newly created node to be the tail
•	Set the tail to be the newly created node 
•	Increment the length 
•	Return the Doubly Linked List

-----------------------------------------------------------------------------------------------------------------------------------------

Pop pseudocode
•	If there is no head, return undefined
•	Store the current tail in a variable to return later
•	If the length is 1, set the head and tail to be null
•	Update the tail to be the previous Node
•	Set the newtail’s next to null
•	Decrement the length
•	Return the value removed

-----------------------------------------------------------------------------------------------------------------------------------------

Shift pseudocode
•	If the length is 0, return undefined
•	Store the current head property in a variable (we’ll call it old head)
•	If the length is one
  o	Set the head to be null
  o	Set the tail to be null
•	Update the head to be next of old head
•	Set the head’s prev propery to null
•	Set the old head’s next to null
•	Decrement the length

-----------------------------------------------------------------------------------------------------------------------------------------

Unshift pseudocode
•	Create a new node with the value passed to the function 
•	If the length is 0
  o	Set the head to be new node
  o	Set the tail to be new node
•	Otherwise 
  o	Set the prev property on the head of the list to be the new node
  o	Set the next property on the new node to be the head property
  o	Update the head to be the new node
•	Increment the length
•	Return the list

----------------------------------------------------------------------------------------------------------------------------------------

Get pseudocode
•	If the index is less than 0 or greater or equal to the length, return null
•	If the index is less than or equal to half the length of the list
  o	Loop through the list starting from the head and loop towards the middle
  o	Return the node once it is found
•	If the index is greater than half the length of the list
  o	Loop through the list starting from the tail and loop towards the middle
  o	Return the node once it is found
  
----------------------------------------------------------------------------------------------------------------------------------------

Set pseudocode
•	Create a variable which is the result of the get method at the index passed to the function
  o	If the get method returns a valid node, set the value of that node to be the value passed to the function
  o	Return true
•	Otherwise, return false

----------------------------------------------------------------------------------------------------------------------------------------

Insert pseudocode
•	If the index is less than or greater than the length return false
•	If the index is 0, unshift
•	If the index is same as the length, push
•	Use the get method to access the index -1
•	Set the next and prev properties on the correct nodes to link everything together
•	Increment the length
•	Return true

----------------------------------------------------------------------------------------------------------------------------------------

Remove pseudocode
•	If the index is less than or greater than or equal to the length return false
•	If the index is 0, shift
•	If the index is same as the length-1, pop
•	Use the get method to access the item to be removed
•	Update the next and prev properties to remove the found node from the list
•	Set next and previous to null on the found node
•	Decrement the length
•	Return the removed node

