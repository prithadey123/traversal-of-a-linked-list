 Overview
This project demonstrates how to create and traverse a **Singly Linked List** in C programming.

A linked list is a linear data structure where elements (nodes) are connected using pointers. Each node contains:
- Data
- A pointer to the next node

In this program, three nodes are created manually using dynamic memory allocation and then traversed to display their values.

---
 Source Code

```c
#include <stdio.h>
#include <stdlib.h>

// Define structure
struct Node {
    int data;
    struct Node* next;
};

int main() {
    // Creating nodes manually
    struct Node* head = NULL;
    struct Node* second = NULL;
    struct Node* third = NULL;

    // Allocate memory
    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));

    // Assign data and link nodes
    head->data = 10;
    head->next = second;

    second->data = 20;
    second->next = third;

    third->data = 30;
    third->next = NULL;

    // Traversal
    struct Node* temp = head;
    printf("Linked List Elements: ");
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
}
```

---

 Explanation

- `struct Node` → Defines a node with `data` and a pointer `next`.
- `malloc()` → Dynamically allocates memory for each node.
- Nodes are linked using `next` pointers.
- Traversal is done using a temporary pointer `temp`.
- Loop continues until `temp == NULL`.

---

 Sample Output

```
Linked List Elements: 10 20 30
```

---

 How to Compile and Run

 Compile:
```
gcc linked_list.c -o list
```

 Run:
```
./list
```

---

 Concepts Used
- Structures in C
- Pointers
- Dynamic Memory Allocation (`malloc`)
- Linked List Creation
- Linked List Traversal

---

Time Complexity
- Traversal: **O(n)**
