# c-module-10
# EXP NO:16
C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
# Aim: 
To write a C program to search a given element in the given linked list.

# Algorithm:

1.Define the structure for a node in a linked list.

2.Define the search function to find a specific character in the linked list.

3.Initialize the head of the linked list as needed.

4.Call the search function and perform other linked list operations as needed.
# Program:
```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data)
{
    struct Node *p=head;
    int found=0;
    int i=0;
    if(p==NULL)
    {
        printf("Empty list\n");
        return ;
    }
    while(p!=NULL)
    {
        i++;
        if(p->data==data)
        {
            printf("item %c found at location %d\n",data,i);
            found=1;
            break;
        }
        p=p->next;
    }
    if(!found)
    {
        printf("Item not found\n");
    }
 
 
 
 
 
}
```
# Output:

![image](https://github.com/user-attachments/assets/2165c3c3-6a31-45ae-bf86-6c3332d6f711)


Result: Thus, the program to search a given element in the given linked list is verified successfully.

# EXP NO:17
PROGRAM TO INSERT A NODE IN A LINKED LIST. 
# Aim:
To write a C program to insert a node in a linked list. 
# Algorithm:

1.Define the structure for a node in a linked list

2.Define the insert function to insert a new node with character data at the end of the linked list.

3.Initialize the head of the linked list as needed.

4.Call the insert function and perform other linked list operations as needed.
# Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;
void insert(char data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
        head=n;
        head->data=data;
        n->next=NULL;
        return;
    }
    temp=head;
    while(temp->next!=NULL)
    {
        temp=temp->next;
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;
    
    
}
```

# Output:
![image](https://github.com/user-attachments/assets/dec1437d-80f1-4572-8a27-31f6acd46959)


Result: Thus, the program to insert a node in a linked list is verified successfully.

# EXP NO:18
C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST 
# Aim:
To write a C program to traverse a doubly linked list.

# Algorithm:

1.Initialize a temporary pointer (temp) to the head of the list.

2.Use a while loop to traverse the list until the end (temp == NULL) is reached.

3.Inside the loop, print the data of the current node.

4.Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
# Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    
    struct Node* temp=head;
    while(temp!=NULL)
    {
        printf("%.2f\n",temp->data);
        temp=temp->next;
    }
    
    
    
}
```

# Output:

![image](https://github.com/user-attachments/assets/fd162bcb-88e1-443d-bdee-0b8ac9d42c8f)


Result: Thus, the program to traverse a doubly linked list is verified successfully.

# EXP NO:19
C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST 
# Aim:
To write a C program to insert an element in doubly linked list

# Algorithm:

1.Create a new node (newNode) and allocate memory for it.

2.Set the data of the new node to the provided value.

3.If the list is empty, set the new node as the head.

4.If the list is not empty, traverse the list to find the last node.

5.Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
# Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    n->data=data;
    n->next=NULL;
    n->prev=NULL;
    struct Node *temp=head;
    if(head==NULL)
    {
        head=n;
    }
    else
    {
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        temp->next=n;
        n->prev=temp;
    }
    
    
    
    
}
```
# Output:

![image](https://github.com/user-attachments/assets/73470362-ab82-4df4-b8cf-c636326bbb89)


Result: Thus, the program to insert an element in doubly linked list is verified successfully.

# EXP NO:20 
C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

# Aim:
To write a C function that deletes a given element from a linked list.

# Algorithm:

1.Check if the Linked List is Empty: o If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.

2.Traverse the Linked List: o Start from the head node and iterate through the list to find the node that contains the given element (data).

3.Handle Deletion of the First Node: o If the element to be deleted is found in the head node:  Update the head of the linked list to point to the next node (i.e., head = head->next).  Free the memory allocated to the node to be deleted.  Exit the function.

4.Traverse and Delete from the Middle or End: o If the element is not in the head node, continue traversing the list by checking each node’s next pointer. o When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next). o Free the memory allocated to the node to be deleted.

5.Handle the Case when the Element is Not Found: o If the element is not found in any node, print a message indicating the element is not present in the list.

6.End the Function.
# Program:
```
struct Node{
    int data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *p;
    p = head;
    if (p==NULL)
    {
        printf ("List is empty\n");
    }
    else
    {
        head = p->next;
        printf ("Node deleted from the begining ...\n");
    }
}
```
# Output:

![image](https://github.com/user-attachments/assets/36d7208f-1f65-4681-a907-13c3d6ff254c)


Result: Thus, the function that deletes a given element from a linked list is verified successfully
