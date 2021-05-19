# Read : 10

## Stacks and Queues

### Stacks: 

- A stack is a data structure that consists of **Nodes**.

- Each **Node** references the next **Node** in the stack, but does not reference its previous.

1. **Push** - Nodes or items that are put into the stack are pushed.
   
2. **Pop** - Nodes or items that are removed from the stack are popped. 

3. **Top** - This is the top of the stack.

4. **Peek** - When you peek you will view the value of the top Node in the stack. 
   
5. **IsEmpty** - Returns true when stack is empty otherwise returns false.


- **FILO** : First In Last Out

    - This means that the first item added in the stack will be the last item popped out of the stack.

- **LIFO**: Last In First Out

    - This means that the last item added to the stack will be the first item popped out of the stack.


#### Example:

- Python's built-in List data structure comes bundled with methods to simulate both stack and queue operations.

- Let's consider a stack of letters:

```
letters = []
# Let's push some letters into our list
letters.append('c')
letters.append('a')
letters.append('t')
letters.append('g')
# Now let's pop letters, we should get 'g'
last_item = letters.pop()
print(last_item)
# If we pop again we'll get 't'
last_item = letters.pop()
print(last_item)
# 'c' and 'a' remain
print(letters) # ['c', 'a']
```


### Queues:

1. **Enqueue** - Nodes or items that are added to the queue.
   
2. **Dequeue** - Nodes or items that are removed from the queue. 
   
3. **Front** - This is the front/first Node of the queue.
   
4. **Rear** - This is the rear/last Node of the queue.
   
5. **Peek** - When you peek you will view the value of the front Node in the queue. 
   
6. **IsEmpty** - Returns true when queue is empty otherwise returns false.

- **FIFO** : First In First Out

    - This means that the first item in the queue will be the first item out of the queue.

- **LILO**: Last In Last Out

    - This means that the last item in the queue will be the last item out of the queue.

#### Example:

- Consider a "queue" of fruits:

```
fruits = []
# Let's enqueue some fruits into our list
fruits.append('banana')
fruits.append('grapes')
fruits.append('mango')
fruits.append('orange')
# Now let's dequeue our fruits, we should get 'banana'
first_item = fruits.pop(0)
print(first_item)
# If we dequeue again we'll get 'grapes'
first_item = fruits.pop(0)
print(first_item)
# 'mango' and 'orange' remain
print(fruits) # ['c', 'a']
```

##### [Go Back](code_401_reading_notes.md)