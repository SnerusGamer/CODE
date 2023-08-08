/* 
LAB TASK 1 
QUESTION: 1a- Write a C program to implement Towers of Hanoi

Test case:
Input = 3
Output = 
Move disk -1 from pole A to c
Move disk -2 from pole A to B
Move disk -1 from pole C to B
Move disk -3 from pole A to c
Move disk -1 from pole B to A
Move disk -2 from pole B to C
Move disk -1 from pole A to C

*/
//Start writing program from here
#include <stdio.h>

void toh(int n,char p, char q, char r){
    if(n>0){
    toh(n-1,p,r,q);
    printf("Move disk %d from pole %c to %c\n",n,p,q);
    toh(n-1,r,q,p);
    }
}


int main(){
    int n ;
    scanf("%d",&n);
    toh(n,'A','C','B');
    return 0;
}

/*1b. Write a C program to implement STACK operations using array

Test Cases:
example 1:
input = 1 
12 
1 
21 
1 
45 
3 
4
output = 45 21 12

example 2:
case = t2
input = 2 4
output = stack is empty */

//start writing program from next line
#include <stdio.h>
#include <stdlib.h>

int top = -1, stack[100];
void push();
void pop();
void display();
int count=0;

int main(){
    int a;
    int b = 1;
    int choice;
    while(count!=01
    ){
        scanf("%d",&choice);
        switch(choice){
            case 1:
            push();
            break;
            
            case 2: 
            pop();
            break;
            
            case 3:
            display();
            break;
            
            case 7:
            printf("invalid choice");
            
            default:
                count++;
                break;
                
                
        }
    }
    return 0;
}

void push(){
    int n;
    if (top==2){
        printf("Stack is full\n");
        count++;
    }
    else{
        scanf("%d",&n);
        top = top + 1;
        stack[top] = n;
    }
}

void pop(){
    if(top==-1){
        printf("stack is empty\n");
        count++;
    }
    else{
        printf("%d is popped from stack\n",stack[top]);
        top = top -1;
    }
}

void display(){
    if(top==-1){
        printf("Stack overflow\n");
        count++;
    }
    else{
        for(int i=top;i>=0;i--){
            printf("%d ",stack[i]);
        }
        
    }
}

/*1c. Write a C program to implement QUEUE operations using array

Test Cases:
example 1:
input = 1 
12 
1 
21 
1 
45 
3 
4
output = 12 21 45

example 2:
case = t2
input = 2 4
output = queue is empty
*/
//Start writing program from here
#include <stdio.h>
#include <stdlib.h>
#define queue_size 4

int queue[4];
int front = -1;
int rear = -1;

void enqueue (int element);
void dequeue ();
void display ();

void main(){
    int choice,element;
    while(1){
        scanf("%d",&choice);
        
        switch(choice){
            case 1:
            scanf("%d",&element);
            enqueue(element);
            break;
            
            case 2:
            dequeue();
            break;
            
            case 3:
            display();
            break;
            
            case 4:
            exit(0);
            
            default:
            printf("Invalid choice");
        }
    }
}

void enqueue(int element){
    if(rear == 2){
        printf("queue is full\n");
    }
    else{
        rear = rear + 1;
        queue[rear] = element;
    }
}

void dequeue(){
    if(front==rear){
        printf("queue is empty\n");
    }
    else{
        front = front + 1;
        int delement;
        delement = queue[front];
        printf("%d is deleted from queue\n",delement);
        if(front==rear){
            front = -1;
            rear = -1;
        }
    }
}

void display(){
    if(front==rear){
        printf("queue is empty\n");
    }
    else{
        for(int i = front + 1;i<=rear;i++){
            printf("%3d",queue[i]);
        }
        printf("\n");
    }
}

/*2a. Write a C program to evaluation postfix expression.

Test Case example:

Input=982+-
Output=
enter any postfix number expression(eg.98+):
value of the postfix expression=-1.00
*/
//Start writing program from here
#include <stdio.h>
#include <math.h>
#include <ctype.h>

#define stacksize 100
float stack[stacksize];
int top=-1;
void push(char element);
int pop();



int main(){
    char postfix[50],ch;
    int i=0,oper1,oper2;
    printf("enter any postfix number expression(eg.98+):\n");
    scanf("%s",postfix);
    
    while((ch=postfix[i++])!='\0'){
        if(isdigit(ch)){
            push(ch-'0');
        }
        else{
            oper2 = pop();
            oper1 = pop();
            
            switch(ch){
                
                case '+':
                push(oper1+oper2);
                break;
                
                case '-':
                push(oper1-oper2);
                break;
                
                case '*':
                push(oper1*oper2);
                break;
                
                case '/':
                push(oper1/oper2);
                break;
                
                case '^':
                push(pow(oper1,oper2));
                break;
                
                default:
                 printf("invalid operator");
                 break;
            }
        }
    }
    
    printf("value of the postfix expression= %.2f \n",stack[top]);
    return 0;
}

void push(char element){
    top = top + 1;
    stack[top] = element;
}

int pop (){
    int delement;
    delement = stack[top];
    top = top -1;
    return (delement);
}

/*
TASK 3C. Write a C program to implement CIRCULAR QUEUE operations using arrays.

Test Cases:
case=t4
input=
1
20
1
30
1
40
1
50
3
2
1
50
1
60
3
4
output=
Circular Queue overflow
20	30	40	
rear=2 pointing at 40
front=0 pointing at 20
Deleted Element is 20
Circular Queue overflow
50	30	40	
rear=0 pointing at 50
front=1 pointing at 30
*/
//Start writing program from here


#include <stdio.h>
#include <stdlib.h>
#define queuesize 3

int queue[queuesize];
int front = -1;
int rear = -1;

void enqueue(int element);
void dequeue();
void display();

void main(){
    int choice,element;
    while(1){
        scanf("%d",&choice);
        
        switch(choice){
            
            case 1:
            scanf("%d",&element);
            enqueue(element);
            break;
            
            case 2:
            dequeue();
            break;
            
            case 3:
            display();
            break;
            
            case 4:
            exit(0);
            break;
            
            default:
            printf("invalid option");
        }
    }
}

void enqueue(int element){
    if(((rear==queuesize-1)&&(front==-1))||((rear==front)&&(front!=-1))){
        printf("Circular Queue overflow\n");
    }
    else if((rear==queuesize-1)&&(front!=-1)){
        rear = 0;
        queue[rear] = element;
    }
    else{
        rear = rear + 1;
        queue[rear] = element;
    }
}

void dequeue(){
    if (rear == -1 && front == -1){
        printf("Circular Queue underflow\n");
    }
    else{
        if(front==queuesize-1){
            front = -1;
        }
        front = front + 1;
        printf("Deleted element is %d\n",queue[front]);
        
        if(front==rear){
            front = -1;
            rear = -1;
        }
    }
}

void display(){
    if((front==rear)&&(front==-1)){
        printf("Circular Queue is empty");
        return;
    }
    if(front<rear){
        for(int i=front+1;i<=rear;i++){
            printf("%d\t",queue[i]);
        }
        printf("\n");
        printf("rear=%d pointing at %d\n",rear,queue[rear]);
        printf("front=%d pointing at %d\n",front+1,queue[front+1]);
    }
    else{
        for(int i=0;i<=rear;i++){
            printf("%d\t",queue[i]);
        }
        for(int i=front+1;i<=queuesize-1;i++){
            printf("%d\t",queue[i]);
        }
        printf("\n");
        printf("rear=%d pointing at %d\n",rear,queue[rear]);
        printf("front=%d pointing at %d\n",front+1,queue[front+1]);
    }
}

/*Write a C program to implement reading, writing, and addition of polynomials.
test case example:
case=t2
input=3
2
1
4
6
3
1
2
3
4
output=
Addition result: 3X^3->3X^2->7X^1->10X^0->

in the above test case first value 3 indicates highest degree of 1st polynomial
followed by the coeffient values of degree 3,2,1,and 0 
simililary the second 3 value indicates the highest degree of 2nd polynomial
followed by coeffient values

try giving the different degree values of the polynomials and test the output
*/

//Start writing program from here
#include <stdio.h>                                                                                                                                                                                                                                                                                                                
#include <stdlib.h>

struct node{
    int coeff;
    int expo;
    struct node*next;
};

struct node* create(struct node*);
struct node* insert(struct node*,int,int);
void add(struct node*,struct node*);
void display(struct node*);
/*void main(){
    struct node *head1 = NULL;
    struct node *head2 = NULL;
    head1 = create(head1);
    head2 = create(head2);
    add(head1,head2);
}*/

struct node* create(struct node *head){
    int n,expo, coeff;
    scanf("%d",&n);
    expo = n;
    for(int i=0;i<n+1;i++){
        scanf("%d",&coeff);
        head = insert(head,coeff,expo--);
    }
    return head;
}

struct node* insert(struct node *head, int coeff, int expo){
    struct node *newnode, *ptr;
    newnode = (struct node *)malloc(sizeof(struct node));
    newnode->coeff = coeff;
    newnode->expo = expo;
    newnode->next = NULL;
    if(head==NULL){
        newnode->next =NULL;
        head = newnode;
    }
    else{
        ptr = head;
        while(ptr->next!=NULL){
            ptr = ptr->next;
        }
        ptr->next = newnode;
        newnode->next = NULL;
    }
    return head;
}

void add(struct node *head1, struct node *head2){
    struct node *ptr1 = head1;
    struct node *ptr2 = head2;
    struct node *head3 = NULL;
    while(ptr1!=NULL && ptr2!=NULL){
        if(ptr1->expo==ptr2->expo){
            head3 = insert(head3,ptr1->coeff+ptr2->coeff,ptr1->expo);
            ptr1 = ptr1 ->next;
            ptr2 = ptr2 -> next;
        }
        else if (ptr1->expo > ptr2->expo){
            head3 = insert(head3,ptr1->coeff,ptr1->expo);
            ptr1 = ptr1->next;
        }
        else if (ptr1->expo < ptr2->expo){
            head3 = insert(head3,ptr2->coeff,ptr2->expo);
            ptr2 = ptr2->next;
        }
    }
    while(ptr1!=NULL){
        head3 = insert(head3,ptr1->coeff,ptr1->expo);
        ptr1= ptr1->next;
    }
    while(ptr2!=NULL){
        head3 = insert(head3,ptr2->coeff,ptr1->expo);
        ptr2 = ptr2->next;
    }
    display(head3);
}

void display(struct node *head){
    if(head==NULL){
        printf("No Polynomial\n");
    }
    else{
        struct node* temp = head;
        printf("Addition result: ");
        while(temp!=NULL){
            printf("%dx^%d",temp->coeff,temp->expo);
            temp = temp->next;
            if(temp!=NULL){
                printf("->");
            }
            else{
                printf("\n");
            }
        }
    }
}

void main(){
    struct node* head1 = NULL;
    struct node* head2 = NULL;
    //printf("Enter 1st polynomial \n");
    head1 = create(head1);
    //printf("Enter 2nd polynomial \n");
    head2 = create(head2);
    add(head1,head2);
}

DLL

#include <stdio.h>
#include <stdlib.h>

struct node {
    struct node *prev,*next;
    int data;
};

void insert(int,int);
void deletion(int);
void display();
void find(int);

struct node *head = NULL;
int len = 0;

void main() {
    int choice, element, pos;
    while(1) {
        scanf("%d",&choice);
            switch(choice) {
                case 1 : scanf("%d%d",&element,&pos);
                        insert(element,pos);
                        break;
                
                case 2 : scanf("%d",&pos);
                        deletion(pos);
                        break;
                        
                case 3 : display();
                        break;
                        
                case 4 : scanf("%d",&element);
                        find(element);
                        break;
                        
                case 5 : exit(0);
                
                default : printf("Enter a valid choice\n");
                
            }
        }
    }        

void insert(int ele,int pos) {
    struct node *newnode;
    newnode = (struct node*)malloc(sizeof(struct node));
    newnode -> prev = NULL;
    newnode -> next = NULL;
    newnode -> data = ele;
    
    if(head == NULL) {
        head = newnode;
        len++;
    }
    else if (head->next == NULL) {
        if(pos>len && pos != 2) {
            printf("Enter a valid position\n");
        }
        else {
            struct node *ptr = head;
            ptr->next = newnode;
            newnode->prev = ptr;
            len++;
        }
    }
    else {
        struct node *ptr = head,*temp = head;
        if((pos>len) && (pos-len!=1)) {
            printf("Enter a valid position\n");
        }
        else if(pos==1) {
            newnode->prev = NULL;
            newnode->next = ptr;
            ptr->prev = newnode;
            head = newnode;
            len++;
        }
        else if(pos>1 && pos<=len) {
            for(int i = 1;i<pos;i++) {
                temp = ptr;
                ptr = ptr->next;
            }
            newnode->prev = temp;
            newnode->next = ptr;
            ptr->prev = newnode;
            temp->next = newnode;
            len++;
        }
        else {
            while(ptr->next!=NULL) {
                ptr = ptr->next;
            }
            ptr->next = newnode;
            newnode->prev = ptr;
            len++;
        }
    }
    
}

void deletion(int pos) {
    struct node *dptr = head,*postdptr = head;
    if(head  == NULL) {
        printf("no elements to delete\n");
    }
    else {
        if(pos>len) {
            printf("Enter a valid position\n");
        }
        else if(pos==1) {
            postdptr = dptr->next;
            postdptr->prev = NULL;
            head = postdptr;
            free(dptr);
            len--;
        }
        else if(pos==len) {
            while(postdptr->next!=NULL) {
                dptr = postdptr;
                postdptr = postdptr->next;
            }
            dptr->next = NULL;
            free(postdptr);
            len--;
        }
        else {
            struct node *dptr = head;
            for (int i = 1;i<pos;i++) {
                dptr = dptr->next;
            }
            (dptr->prev)->next = dptr->next;
            (dptr->next)->prev = dptr->prev;
            free(dptr);
            len--;
        }
    }
}

void display() {
    if(head==NULL) {
        printf("DLL is empty\n");
    }
    else {
        struct node *ptr1 = head, *ptr2 = head;
        printf("FORWARD Traversal: ");
        while(ptr1->next!=NULL) {
            printf("%d ",ptr1->data);
            ptr1=ptr1->next;
        }
        printf("%d \n",ptr1->data);
        while(ptr2->next!=NULL) {
            ptr2=ptr2->next;
        }
        printf("BACKWARD Traversal: ");
        while(ptr2->prev!=NULL) {
            printf("%d ",ptr2->data);
            ptr2=ptr2->prev;
        }
        printf("%d \n",ptr2->data);
    }
}

void find(int ele) {
    if (head==NULL) {
        printf("DLL is empty\n");
    }
    else {
        struct node *temp1 = head;
        int cnt = 1;
        while(temp1->next!=NULL) {
            if(temp1->data==ele) {
                break;
            }
            temp1 = temp1->next;
            cnt++;
        }
        if(temp1->next==NULL && temp1->data!=ele) {
            printf("element not found\n");
        }
        else {
            printf("%d found at position %d\n",ele,cnt);
        }
    }
}


/* 
LAB TASK 5
QUESTION: 5- Implement the following operations on Binary Search Tree
 i. create  ii. search iii. delete. 

Test cases:
case = t1
input=
1
35
1
13
1
56
1
12
1
27
2
13
4
5
output=
12->27->56->35->

*/
//Start writing program from here
#include <stdio.h>
#include <stdlib.h>
struct bstnode
{
    struct bstnode *left ;
    int data ;
    struct bstnode *right ;
};
typedef struct bstnode node ;
node *root = NULL ;
int flag = 0 ;
node* cre_bst(node*,int);
node* ins_bst(node*,int);
node* del_bst(node*,int);
node* sea_bst(node*,int);
void display(node*);
int findMin(node*);
void main()
{
    int choice , element ;
    node *temp ;
    while(1)
    {
        scanf("%d",&choice);
        switch(choice)
        {
            case 1 : scanf("%d",&element);
                     root = ins_bst(root,element); 
                     break;
                     
            case 2 : scanf("%d",&element);
                     root = del_bst(root,element);
                     break;
                     
            case 3 : scanf("%d",&element);
                     temp = sea_bst(root,element);
                     if(temp!=NULL)
                     printf("%d element found\n",element);
                     else
                     printf("%d element not found\n",element);
                     break; 
                     
            case 4 : if(root==NULL)
                     printf("BST is empty\n");
                     else
                     {
                        display(root); 
                        break;
                     }
                     
            case 5 : exit(0);
            
            default : printf("Enter a valid choice\n");
        }
    }
}
node* cre_bst(node *root, int ele)
{
    node *newnode ;
    newnode = (node *)malloc(sizeof(node));
    newnode->data = ele ;
    newnode->left = newnode->right = NULL ;
    return newnode ;
}
node* ins_bst(node *root,int ele)
{
    if(root==NULL)
        root = cre_bst(root,ele) ;
    else if(ele < root->data)
        root->left = ins_bst(root->left,ele);
    else
        root->right = ins_bst(root->right,ele);
    return root ;
}
node* del_bst(node *root,int ele)
{
    node *temp ;
    if(root==NULL)
    {
        flag = 1 ;
        return NULL ;
    }
    if(ele > root->data)
        root->right = del_bst(root->right,ele);
    else if(ele < root->data)
        root->left = del_bst(root->left,ele);
    else
    {
        flag = 0 ;
        if(root->left==NULL && root->right==NULL)
        {
            temp = root ;
            free(temp) ;
            root = NULL ;
        }
        else if(root->left==NULL)
        {
            temp = root ;
            root = root->right ;
            free(temp) ;
        }
        else if(root->right==NULL)
        {
            temp = root ;
            root = root->left ;
            free(temp) ;
        }
        else
        {
            int rightMin = findMin(root->right) ;
            root->data = rightMin ;
            root->right = del_bst(root->right,rightMin);
        }
    }
    return root ;
}
node* sea_bst(node *root,int ele)
{
    if(root==NULL)
        return NULL ;
    if(root->data==ele)
        return root ;
    if(ele > root->data)
        return sea_bst(root->right,ele) ;
    else if(ele < root->data)
        return sea_bst(root->left,ele) ;
}
void display(node *root)
{
    if(root!=NULL)
    {
        display(root->left);
        display(root->right);
        printf("%d->",root->data);
    }
}
int findMin(node *root)
{
    node *temp = root ;
    while(temp->left!=NULL)
        temp = temp->left ;
    return temp->data ;
}


/*6. Write a C program to implement BST TREE TRAVERSAL TECHNIQUES BFS(level-order) AND DFS (only inorder and preorder)

Test Case example:
case = t4
input=
1
100
1
23
1
150
1
5
2
3
4
output=
100->23->150->5->
Preorder Traversal is:100->23->5->150->
Inorder Traversal is:5->23->100->150->

*/
//Start writing program from here
#include<stdio.h>
#include<stdlib.h>

struct node{
    int data;
    struct node *left;
    struct node *right;
};

struct node *root=NULL;
int rear=-1;
int front=-1;
struct node *insert(struct node *root,int data);
void levelorder(struct node *root);
struct node *queue[100];
void enqueue(struct node *x);
void dequeue();
void inorder(struct node *root);
void preorder(struct node *root);

int main(){
    int ch,n;
    while(1){
        scanf("%d",&ch);
        switch(ch){
            case 1:scanf("%d",&n);
            root=insert(root,n);
            break;
            case 2:levelorder(root);
            break;
            case 3:
                   printf("\nPreorder Traversal is:");
                   preorder(root);
                   printf("\n");
                   printf("Inorder Traversal is:");
                   inorder(root);
                    break;
            case 4:exit(0);
            default : printf("invalid choice");
        }
    }
    return 0;
}

struct node *insert(struct node *root,int data){
    struct node *temp;
    if(root==NULL){
        temp=(struct node*)malloc(sizeof(struct node));
        temp->data=data;
        temp->left=temp->right=NULL;
        root=temp;
        return root;
    }
    else if(data<=root->data){
        root->left=insert(root->left,data);
    }
    else{
        root->right=insert(root->right,data);
    }
    return root;
}

void levelorder(struct node *root){
    struct node *temp;
    if(root==NULL){
        printf("Tree is empty");
        return;
    }
    else{
        enqueue(root);
        while(front!=rear){
            temp=queue[front+1];
            printf("%d->",temp->data);
            if(temp->left!=NULL)
            enqueue(temp->left);
            if(temp->right!=NULL)
            enqueue(temp->right);
            dequeue();
        }
    }
}
void enqueue(struct node *x){
    rear++;
    queue[rear]=x;
}
void dequeue(){
    front++;
}
void inorder(struct node *root){
    if(root!=NULL){
        inorder(root->left);
        printf("%d->",root->data);
        inorder(root->right);
    }
}
void preorder(struct node *root){
    if(root!=NULL){
        printf("%d->",root->data);
        preorder(root->left);
        preorder(root->right);
      }
}

/*7a. Write a C program to traverse the graph in BFS order.

Test Case example:
case = t1
input= 5
0 1 1 1 0     
1 0 0 0 1                           
1 0 0 0 1
1 0 0 0 1
0 1 1 1 0
3
output=
3 1 5 2 4


*/

#include <stdio.h>


#define MAX_QUEUE_SIZE 100

int queue[MAX_QUEUE_SIZE];
int front = -1, rear = -1;

void enqueue(int vertex) {
    if (rear == MAX_QUEUE_SIZE - 1) {
        printf("Queue is full.\n");
        return;
    }
    if (front == -1)
        front = 0;
    queue[++rear] = vertex;
}

int dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
        return -1;
    }
    int vertex = queue[front++];
    return vertex;
}

int isQueueEmpty() {
    return front == -1 || front > rear;
}


void BFS(int graph[100][100], int n, int startVertex, int visited[100]) {
    enqueue(startVertex);
    visited[startVertex] = 1;

    while (!isQueueEmpty()) {
        int currentVertex = dequeue();
        printf("%d ", currentVertex + 1);

        for (int i = 0; i < n; i++) {
            if (graph[currentVertex][i] && !visited[i]) {
                enqueue(i);
                visited[i] = 1;
            }
        }
}}

int main() {
    int n, graph[100][100], sourceVertex, visited[100] = {0};

   
    scanf("%d", &n);

    
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &graph[i][j]);
        }
    }

    
    scanf("%d", &sourceVertex);

    BFS(graph, n, sourceVertex - 1, visited);

    printf("\n");

    return 0;
}

/*7b.Write a C program to implement traverse the graph in DFS order.

Test Case example:

input= 5
0 1 1 1 0     
1 0 0 0 1                           
1 0 0 0 1
1 0 0 0 1
0 1 1 1 0
1
output=
1 2 5 3 4


*/

#include <stdio.h>

void DFS(int graph[100][100], int n, int currentVertex, int visited[100]) {
    printf("%d ,", currentVertex+1);
    visited[currentVertex] = 1;

    for (int i = 0; i < n; i++) {
        if (graph[currentVertex][i] && !visited[i]) {
            DFS(graph, n, i, visited);
        }
    }
}

int main() {
    int n, graph[100][100], sourceVertex, visited[100] = {0};
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &graph[i][j]);
        }
    }
    scanf("%d", &sourceVertex);
    for (int i = 0; i < n; i++) {
        printf("VERTEX %d       ",i+1);
        for (int j = 0; j < n; j++) {
            printf("%d  ", graph[i][j]);
        }
        printf("\n");
    }
    if(n>0){
     printf("\n The DFS Traversal of Graph is :\n");
    DFS(graph, n, sourceVertex - 1, visited);
    printf("\n");
}
else{
    printf("Graph Empty - No DFS");
}
    return 0;
}

/*
8a. Write a C program to implement Sequential search.
Test Cases:
case = t1
input=
5
3 5 6 7 8
6
output=
Search is successful element is found at position 3 

case=t2
input=
7
3 1 5 7 8 4 3 
10
output=
Element not found


*/
//start program from next line......
#include <stdio.h>
#include <stdlib.h>

int main(){
    int n;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    int find;
    scanf("%d",&find);
    int zap = -1;
    for(int i=0;i<n;i++){
        if(find==arr[i]){
            zap = i;
            break;
        }
    }
    if(zap==-1){
        printf("Element not found");
    }
    else{
        printf("Search is successful element is found at position %d",zap+1);
    }
}

/*
8b. Write a C program to implement Binary search.
Test Cases:
case = t1
input=
5
3 5 6 7 8
6
output=
Search is successful element is found at position 3

case=t2
input=
7
3 1 5 7 8 4 3 
10
output=
Element not found

*/
//start program from next line......
#include <stdio.h>

int bin (int arr[],int find,int low,int high);
int bin(int arr[],int find, int low,int high){
    while(low<=high){
        int mid = low + (high-low)/2;
        
        if(arr[mid] == find){
            return mid;
        }
        if(arr[mid] < find){
            low = mid + 1;
        }
        else{
            high = mid-1;
        }
    }
    return -1;
}

int main(){
    int n;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    int find;
    scanf("%d",&find);
    
//sorting the array
    int temp = 0;
    for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
            if(arr[i]>arr[j]){
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    
    int ans = bin(arr,find,0,n-1);
    
    if(ans>0){
        printf("Search is successful element is found at position %d",ans+1);
    }
    else{
        printf("Element not found");
    }
    
    
    return 0;
}

/* LAB TASK 9
QUESTION: 9a-Implement Insertion sort using a C program.

INPUT FORMAT:
FIRST LINE CONTAINS "n" NO OF ELEMENTS
SECOND LINE CONTAINS "n" integers seperated by a space

OUTPUT FORMAT:
DISPLAY UNSORTED LIST,SORTING METHOD NAME AND SORTED LIST AS PER THE TEST CASE

Test Cases:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
INSERTION SORT
Sorted List
-45	-8	-1	0	4	6
*/
//Start writing program from here
#include <stdio.h>

void ins(int arr[],int n);
void ins(int arr[],int n){
    int i,j,zap;
    for(i = 1;i<n;i++){
        zap = arr[i];
        j = i-1;
        while((arr[j]>zap)&&(j>=0)){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1] = zap;
    }
}

int main(){
    int n;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("Unsorted List\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    printf("\n");
    ins(arr,n);
    printf("INSERTION SORT\n");
    printf("Sorted List\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    
    return 0;
}

/* 9b.Write a C program to implement Selection Sort.
Test Case example:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
SELECTION SORT
Sorted List
-45	-8	-1	0	4	6	

*/
//Start writing program from here
#include <stdio.h>

void sel(int arr[],int n);
void sel(int arr[],int n){
    for(int i=0;i<n-1;i++){
        for(int j=i+1;j<n;j++){
            if(arr[j]<arr[i]){
                int temp;
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
    }
    }
}

int main(){
    int n;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("Unsorted List\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    printf("\n");
    sel(arr,n);
    printf("SELECTION SORT\n");
    printf("Sorted List\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    return 0;
}

/* 
LAB TASK 10
QUESTION: 10 a-Demonstrate shell sort using a C program.

INPUT FORMAT:
FIRST LINE CONTAINS "n" NO OF ELEMENTS
SECOND LINE CONTAINS "n" integers seperated by a space

OUTPUT FORMAT:
DISPLAY UNSORTED LIST,SORTING METHOD NAME AND SORTED LIST AS PER THE TEST CASE

Test Cases:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
SHELL SORT
Sorted List
-45	-8	-1	0	4	6
*/
//Start writing program from here
// Shell Sort in C programming

#include <stdio.h>

void shellSort(int arr[], int n) {
    int gap, i, j, temp;

    for (gap = n / 2; gap > 0; gap /= 2) {
        for (i = gap; i < n; i++) {
            temp = arr[i];
            for (j = i; j >= gap && arr[j - gap] > temp; j -= gap) {
                arr[j] = arr[j - gap];
            }
            arr[j] = temp;
        }
    }
}

int main() {
    int n, arr[100];


    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }


    printf("Unsorted List\n");
    for (int i = 0; i < n; i++) {
        printf("%d\t", arr[i]);
    }
    printf("\n");

    shellSort(arr, n);

    printf("SHELL SORT\n");
    printf("Sorted List\n");
    for (int i = 0; i < n; i++) {
        printf("%d\t", arr[i]);
    }
    printf("\n");

    return 0;
}

/* 
LAB TASK 10
QUESTION: 10B-Demonstrate Heap sort using a C program.

INPUT FORMAT:
FIRST LINE CONTAINS "n" NO OF ELEMENTS
SECOND LINE CONTAINS "n" integers seperated by a space

OUTPUT FORMAT:
DISPLAY UNSORTED LIST,SORTING METHOD NAME AND SORTED LIST AS PER THE TEST CASE

Test Cases:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
MERGE SORT
Sorted List
-45	-8	-1	0	4	6
*/
//Start writing program from here
#include <stdio.h>

void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

void heapify(int arr[], int n, int i) {
    int largest = i;
    int leftChild = 2 * i + 1;
    int rightChild = 2 * i + 2;

    if (leftChild < n && arr[leftChild] > arr[largest])
        largest = leftChild;

    if (rightChild < n && arr[rightChild] > arr[largest])
        largest = rightChild;

    if (largest != i) {
        swap(&arr[i], &arr[largest]);
        heapify(arr, n, largest);
    }
}


void heapSort(int arr[], int n) {
    for (int i = n / 2 - 1; i >= 0; i--)
        heapify(arr, n, i);

    for (int i = n - 1; i >= 0; i--) {
        swap(&arr[0], &arr[i]); 
        heapify(arr, i, 0);     
    }
}

int main() {
    int n, arr[100];


    scanf("%d", &n);


    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Unsorted List\n");
    for (int i = 0; i < n; i++) {
        printf("%d\t", arr[i]);
    }
    printf("\n");

    heapSort(arr, n);

    printf("HEAP SORT\n"); 
    printf("Sorted List\n");
    for (int i = 0; i < n; i++) {
        printf("%d\t", arr[i]);
    }
    printf("\n");

    return 0;
}


/* 
LAB TASK 11
QUESTION: 11a-Demonstrate Merge sort using a C program.

INPUT FORMAT:
FIRST LINE CONTAINS "n" NO OF ELEMENTS
SECOND LINE CONTAINS "n" integers seperated by a space

OUTPUT FORMAT:
DISPLAY UNSORTED LIST,SORTING METHOD NAME AND SORTED LIST AS PER THE TEST CASE

Test Cases:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
MERGE SORT
Sorted List
-45	-8	-1	0	4	6
*/
//Start writing program from here
#include <stdio.h>
#include <stdlib.h>
 

void merge(int arr[], int l, int m, int r)
{
    int i, j, k;
    int n1 = m - l + 1;
    int n2 = r - m;

    int L[n1], R[n2];
 

    for (i = 0; i < n1; i++)
        L[i] = arr[l + i];
    for (j = 0; j < n2; j++)
        R[j] = arr[m + 1 + j];
    i = 0;
    j = 0;
    k = l;
    while (i < n1 && j < n2) {
        if (L[i] <= R[j]) {
            arr[k] = L[i];
            i++;
        }
        else {
            arr[k] = R[j];
            j++;
        }
        k++;
    }
 
    
    while (i < n1) {
        arr[k] = L[i];
        i++;
        k++;
    }
    
    while(j<n2) {
        arr[k] = R[j];
        j++;
        k++;
    }
}
 
void mergeSort(int arr[], int l, int r)
{
    if (l < r) {
        int m = l + (r - l) / 2;
        mergeSort(arr, l, m);
        mergeSort(arr, m + 1, r);
 
        merge(arr, l, m, r);
    }
}
 

void printArray(int A[], int size)
{
    int i;
    for (i = 0; i < size; i++)
        printf("%d ", A[i]);
    printf("\n");
}
 

int main()
{
    int n;
    scanf("%d",&n);
    int arr[n];
    for (int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    int arr_size = sizeof(arr) / sizeof(arr[0]);
    printf("Unsorted List\n");
    printArray(arr, arr_size);
 
    mergeSort(arr, 0, arr_size - 1);
 
    printf("MERGE SORT\n");
    printf("Sorted List\n");
    printArray(arr, arr_size);
    return 0;
}


/* 
LAB TASK 11
QUESTION: 11b-Develop a C program for Quick sort.

INPUT FORMAT:
FIRST LINE CONTAINS "n" NO OF ELEMENTS
SECOND LINE CONTAINS "n" integers seperated by a space

OUTPUT FORMAT:
DISPLAY UNSORTED LIST,SORTING METHOD NAME AND SORTED LIST AS PER THE TEST CASE

Test Cases:
case = t1
input = 6
-1 6 -45 -8 0 4
output = 
Unsorted List
-1	6	-45	-8	0	4	
QUICK SORT
Sorted List
-45	-8	-1	0	4	6
*/
//Start writing program from here
// C code to implement quicksort
 
#include <stdio.h>

void swap(int* a, int* b)
{
    int t = *a;
    *a = *b;
    *b = t;
}

int partition(int arr[], int low, int high)
{
    int pivot = arr[high];
    int i = (low - 1);
 
    for (int j = low; j <= high - 1; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(&arr[i], &arr[j]);
        }
    }
    swap(&arr[i + 1], &arr[high]);
    return (i + 1);
}
void quickSort(int arr[], int low, int high)
{
    if (low < high) {
        int pi = partition(arr, low, high);
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}
int main()
{
    int N;
    scanf("%d",&N);
    int arr[N];
    for (int i=0;i<N;i++){
        scanf("%d",&arr[i]);
    }
    printf("Unsorted List\n");
    for (int i=0;i<N; i++)
        printf("%d ", arr[i]);

    quickSort(arr, 0, N - 1);
    printf("QUICK SORT\n");
    printf("Sorted List\n");
    for (int i = 0; i < N; i++)
        printf("%d ", arr[i]);
    return 0;
}
