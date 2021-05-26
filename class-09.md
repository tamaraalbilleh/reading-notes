# Stacks and Queues
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
## Common terminology for a stack :
* push : 
    * Nodes or items that are put into the stack are pushed
* pop : 
    * Nodes or items that are removed from the stack are popped. 
    * When you attempt to pop an empty stack an exception will be raised.
* top : 
    * the top of the stack
* peek 
    * When you peek you will view the value of the top Node in the stack
    * When you attempt to peek an empty stack an exception will be raised.
* isEmpty : 
    * returns true when stack is empty otherwise returns false.
## stack concepts :
### FILO 
first in last out : means that the first item added in the stack will be the last item popped out of the stack.
### LIFO : 
last in first out : means that the last item added to the stack will be the first item popped out of the stack.
### Stack Visualization
![stack](https://4cawmi2va33i3w6dek1d7y1m-wpengine.netdna-ssl.com/wp-content/uploads/2018/07/Computer-science-fundamentals_6.1.png)
### Push O(1)
you push it into the stack by assigning it as the new top, with its next property equal to the original top.
### Pop O(1)
* removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
* you would check isEmpty before conducting a pop. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.
### Peek O(1)
* you will only be inspecting the top Node of the stack.
* Typically, you would check isEmpty before conducting a peek.
### IsEmpty O(1)
* returns a boolean that indicates if a stack is empty or not.
## Queue
* Enqueue 
    * Nodes or items that are added to the queue.
* Dequeue 
    * Nodes or items that are removed from the queue. 
    * If called when the queue is empty an exception will be raised.
* Front  
    * This is the front/first Node of the queue.
* Rear 
    * This is the rear/last Node of the queue.
* Peek 
    * When you peek you will view the value of the front Node in the queue. 
    * If called when the queue is empty an exception will be raised.
* IsEmpty 
    * returns true when queue is empty otherwise returns false.
## Queues concepts :
### FIFO
First In First Out : the first item in the queue will be the first item out of the queue.

### LILO
Last In Last Out :the last item in the queue will be the last item out of the queue.
### Queue Visualization
![queue](https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Data_Queue.svg/1200px-Data_Queue.svg.png)
### Enqueue O(1)
add an item to a queue, you use the enqueue action. This is done with an O(1) operation in time because it does not matter how many other items live in the queue (n);
### Dequeue O(1)
remove an item from a queue, you use the dequeue action. This is done with an O(1) operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.
### Peek O(1)
* you will only be inspecting the front Node of the queue.

* Typically, you want to check isEmpty before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.
### IsEmpty O(1)
* returns a boolean that indicates if a queue is empty or not.