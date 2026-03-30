# Day 8 - POTD

## Problem Name:
Reverse Linked List

## Approach:
- Step 1: Initialize three pointers: prev = NULL, curr = head
- Step 2: Traverse the list
- Step 3: Store next node
- Step 4: Reverse current node's link
- Step 5: Move prev and curr forward
- Step 6: Repeat until curr becomes NULL
- Step 7: Return prev (new head)

## Code:
```cpp
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node* next;
};

Node* reverseList(Node* head) {
    Node* prev = NULL;
    Node* curr = head;

    while(curr != NULL) {
        Node* nextNode = curr->next; // store next
        curr->next = prev;           // reverse link
        prev = curr;                 // move prev
        curr = nextNode;             // move curr
    }

    return prev;
}

void printList(Node* head) {
    Node* temp = head;
    while(temp != NULL) {
        cout << temp->data << " -> ";
        temp = temp->next;
    }
    cout << "NULL";
}

int main() {
    Node* head = new Node{1, NULL};
    head->next = new Node{2, NULL};
    head->next->next = new Node{3, NULL};

    head = reverseList(head);

    printList(head);

    return 0;
}
