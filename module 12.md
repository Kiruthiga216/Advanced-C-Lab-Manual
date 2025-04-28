

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

```
#include <stdio.h> 
#include <stdlib.h> 
struct Node { 
    float data; 
    struct Node* next; 
}; 
void push(struct Node** top, float value) { 
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node)); 
    if (!newNode) { 
        printf("Memory allocation failed\n"); 
        return; 
    } 
    newNode->data = value; 
    newNode->next = *top; 
    *top = newNode; 
} 
 
void display(struct Node* top) { 
    struct Node* current = top; 
    while (current != NULL) { 
        printf("%.2f\n", current->data); 
        current = current->next; 
    } 
} 
 
int main() { 
    struct Node* head = NULL; 
 
    push(&head, 10.10f); 
    push(&head, 11.11f); 
    push(&head, 12.12f); 
 
    display(head); 
 
    return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/de962869-451e-40a6-a8fe-75acd4fba82c)



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```
#include <stdio.h> 
#include <stdlib.h> 
struct Node { 
    float data; 
    struct Node* next; 
}; 
void push(struct Node** top, float value) { 
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node)); 
    if (!newNode) { 
        printf("Memory allocation failed\n"); 
        return; 
    } 
    newNode->data = value; 
    newNode->next = *top; 
    *top = newNode; 
} 
void pop(struct Node** top) { 
    if (*top == NULL) { 
        printf("Stack is empty, nothing to pop.\n"); 
        return; 
    } 
    struct Node* temp = *top; 
    *top = (*top)->next; 
    free(temp); 
} 
void display(struct Node* top) { 
    struct Node* current = top; 
    printf("stack elements:"); 
    while (current != NULL) { 
        printf(" %.2f", current->data); 
        current = current->next; 
    } 
    printf("\n"); 
} 
int main() { 
    struct Node* head = NULL; 
 
    push(&head, 10.01f); 
    push(&head, 20.02f); 
    push(&head, 30.03f); 
 
    display(head); 
 
    pop(&head); 
     
    printf("after pop "); 
    display(head); 
 
    return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/ca495f2b-08c8-47d6-9a83-bd631da1ed81)




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```
#include <stdio.h> 
#include <stdlib.h> 
struct Node { 
    float data; 
    struct Node* next; 
}; 
void enqueue(struct Node** front, struct Node** rear, float value) { 
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node)); 
    if (!newNode) { 
        printf("Memory allocation failed\n"); 
        return; 
    } 
    newNode->data = value; 
    newNode->next = NULL; 
 
    if (*rear == NULL) { 
        *front = *rear = newNode; 
    } else { 
        (*rear)->next = newNode; 
        *rear = newNode; 
    } 
} 
void display(struct Node* front) { 
    struct Node* current = front; 
    printf("queue elements:\n"); 
    while (current != NULL) { 
        printf("%.2f\n", current->data); 
        current = current->next; 
    } 
} 
int main() { 
    struct Node* front = NULL; 
    struct Node* rear = NULL; 
 
    enqueue(&front, &rear, 5.11f); 
    enqueue(&front, &rear, 10.22f); 
    enqueue(&front, &rear, 15.33f); 
 
    display(front); 
 
    return 0; 
} 
 

```

Output:

![image](https://github.com/user-attachments/assets/916fec4c-afdd-4ab5-97a1-240e0f8e2183)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
#include <stdio.h> 
#include <stdlib.h> 
struct Node { 
    float data; 
    struct Node* next; 
}; 
void enqueue(struct Node** front, struct Node** rear, float value) { 
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node)); 
    if (!newNode) { 
        printf("Memory allocation failed\n"); 
        return; 
    } 
    newNode->data = value; 
    newNode->next = NULL; 
 
    if (*rear == NULL) { 
        *front = *rear = newNode; 
    } else { 
        (*rear)->next = newNode; 
        *rear = newNode; 
    } 
} 
void display(struct Node* front) { 
    struct Node* current = front; 
    printf("queue elements:\n"); 
    while (current != NULL) { 
        printf("%.2f\n", current->data); 
        current = current->next; 
    } 
} 
int main() { 
    struct Node* front = NULL; 
    struct Node* rear = NULL; 
 
    enqueue(&front, &rear, 1.1f); 
    enqueue(&front, &rear, 2.2f); 
    enqueue(&front, &rear, 3.3f); 
 
    display(front); 
 
return 0; 
}
```

Output:

![image](https://github.com/user-attachments/assets/c52cb529-e036-41be-b6f1-e3c3255d7ae7)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
#include <stdio.h> 
#include <stdlib.h> 
struct Node { 
int data; 
struct Node* next; 
}; 
void enqueue(struct Node** front, struct Node** rear, int value) { 
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node)); 
    if (!newNode) { 
        printf("Memory allocation failed\n"); 
        return; 
    } 
    newNode->data = value; 
    newNode->next = NULL; 
 
    if (*rear == NULL) { 
        *front = *rear = newNode; 
    } else { 
        (*rear)->next = newNode; 
        *rear = newNode; 
    } 
} 
 
void peek(struct Node* front) { 
    if (front == NULL) { 
        printf("Queue is empty\n"); 
    } else { 
        printf("%d\n", front->data); 
    } 
} 
int main() { 
    struct Node* front = NULL; 
    struct Node* rear = NULL; 
 
    enqueue(&front, &rear, 10); 
    enqueue(&front, &rear, 20); 
    enqueue(&front, &rear, 30); 
 
    peek(front);   
 
    return 0; 
} 

```

Output:

![image](https://github.com/user-attachments/assets/d75fe401-f21e-48b9-9f95-cb693d411fc6)




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


