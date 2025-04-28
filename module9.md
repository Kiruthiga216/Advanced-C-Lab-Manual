EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
#include <stdio.h> 
#define SIZE 100   
 
char stack[SIZE]; 
int top = -1; 
void push(char item) { 
    if (top >= SIZE - 1) { 
        printf("Stack Overflow\n"); 
    } else { 
        top++; 
        stack[top] = item; 
    } 
} 
void display() { 
    if (top == -1) { 
        printf("Stack is empty.\n"); 
    } else { 
        for (int i = top; i >= 0; i--) { 
            printf("%c\n", stack[i]); 
        } 
    } 
} 
 
int main() { 
 
    top = -1; 
    push('A'); 
    push('B'); 
    push('C'); 
    display(); 
 
    return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/6b9e336f-e5d1-4ba2-97b8-d883020585da)




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
#include <stdio.h> 
#define SIZE 100   
 
float stack[SIZE]; 
int top = -1;   
void push(float item) { 
    if (top >= SIZE - 1) { 
        printf("Stack Overflow\n"); 
    } else { 
        stack[++top] = item; 
    } 
} 
void display() { 
    if (top == -1) { 
        printf("stack is empty\n"); 
    } else { 
        for (int i = top; i >= 0; i--) { 
            printf("%.1f ", stack[i]); 
        } 
        printf("\n"); 
} 
} 
int main() { 
top = -1; 
push(10.5); 
push(20.5); 
push(30.5); 
display(); 
return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/958fff4b-2049-48a9-be0a-2a11136befb7)





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h> 
#define SIZE 100 
char queue[SIZE]; 
int front = -1, rear = -1; 
void enqueue(char item) { 
    if (rear >= SIZE - 1) { 
        printf("Queue Overflow\n"); 
    } else { 
        if (front == -1) front = 0;  
        queue[++rear] = item; 
    } 
} 
void display() { 
    if (front == -1 || front > rear) { 
        printf("No elements to display\n"); 
    } else { 
        for (int i = front; i <= rear; i++) { 
            printf("%c\n", queue[i]); 
        } 
    } 
} 
int main() { 
    rear = -1; 
    front = -1; 
    enqueue('A'); 
    enqueue('B'); 
    enqueue('C'); 
    display(); 
 
    return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/ad691e52-376c-46de-8c8f-89ab733d0229)



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h> 
#define SIZE 100 
 
char queue[SIZE]; 
int front = -1, rear = -1; 
void enqueue(char item) { 
    if (rear >= SIZE - 1) { 
        printf("Queue Overflow\n"); 
    } else { 
        if (front == -1) front = 0;  
        queue[++rear] = item; 
    } 
} 
void display() { 
    if (front == -1 || front > rear) { 
        printf("No elements to display\n"); 
    } else { 
        for (int i = front; i <= rear; i++) { 
            printf("%c\n", queue[i]); 
        } 
    } 
} 
int main() { 
    rear = -1; 
    front = -1; 
    enqueue('a'); 
    enqueue('b'); 
    enqueue('c'); 
    display(); 
 
    return 0; 
} 
```

Output:
![image](https://github.com/user-attachments/assets/074464d0-af35-4699-aeee-4640f8100eb5)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
#include <stdio.h> 
#define SIZE 100 
char queue[SIZE]; 
int front = -1, rear = -1; 
void enqueue(char item) { 
if (rear >= SIZE - 1) { 
printf("Queue Overflow\n"); 
} else { 
if (front == -1) front = 0; 
queue[++rear] = item; 
} 
} 
void dequeue() { 
    if (front == -1 || front > rear) { 
        printf("Queue Underflow\n"); 
    } else { 
        front++; 
        if (front > rear) { 
            front = -1; 
            rear = -1; 
        } 
    } 
} 
void display() { 
    if (front == -1 || front > rear) { 
        printf("No elements to display\n"); 
    } else { 
        for (int i = front; i <= rear; i++) { 
            printf("%c\n", queue[i]); 
        } 
    } 
} 
int main() { 
    enqueue('X'); 
    enqueue('Y'); 
    enqueue('Z'); 
    display(); 
    dequeue(); 
    display(); 
 
 
    return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/ea174888-8e1d-4f6d-adf3-3379e31e4eab)



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
