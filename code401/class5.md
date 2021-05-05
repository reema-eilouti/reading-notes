# Read : 05

## Linked Lists

- Like lists, Linked List is a linear data structure. Unlike lists, linked list elements are not stored at a adjacent locations; the elements are linked using pointers.

- **Why Linked List?**
  
  - In lists if we want to insert a new value, we need to maintain the sorted order, so we have to move all the elements less than or greater than the value.
  
  - Deletion is also expensive with lists. For example, to delete a value everything after/before that value  has to be moved.



- **Representation**

  - A linked list is represented by a pointer to the first node of the linked list. 

  - The first node is called the head. 

  - If the linked list is empty, then the value of the head is NULL.

  - Each node in a list consists of at least two parts:
    1. data
    2. Pointer *(Reference)* to the next node
  

- **Example:**
```
# Node class
class Node:
    # Function to initialize the node object
    def __init__(self, data):
        self.data = data  # Assign data
        self.next = None  # Initialize 
                          # next as null
# Linked List class
class LinkedList:
    # Function to initialize the Linked 
    # List object
    def __init__(self): 
        self.head = None
```
 
- **Tree Linked List Example:**
```
# Define a class for the tree node.
class Node:
    # Define your __init__() method.
    def __init__(self, data):
        self.left = None
        self.right = None
        self.data = data
```
```
# Instantiating a tree with the root node with value (10)
root = Node(10)
# Our tree look like this now
#        10
#      /    \
#    None   None
```
```
# Adding the left child of the root to 34
root.left = Node(24)
# Setting the right child of the root to 89
root.right = Node(42)
```

- **Tree Traversals:**
- Left - Parent - Right
```
    def print_inorder(self): #LPR
        if self.left != None:
            self.left.print_inorder()
        print(self.data)
        if self.right != None:
            self.right.print_inorder()
```
- Parent - Left - Right
```
    def print_preorder(self): #PLR
        print(self.data)
        if self.left != None:
            self.left.print_inorder()
        if self.right != None:
            self.right.print_inorder() 
```
- Left - Right - Parent
```
    def print_postorder(self): #LRP
        if self.left != None:
            self.left.print_postorder() 
        if self.right != None:
            self.right.print_postorder()
        print(self.data)
```


##### [Go Back](code_401_reading_notes.md)