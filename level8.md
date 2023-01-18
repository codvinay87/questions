Q1 How do you implement a stack data structure in Python?

Solution
class Stack:
    def __init__(self):
        self.items = []
    
    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        if not self.is_empty():
            return self.items.pop()
    
    def peek(self):
        if not self.is_empty():
            return self.items[-1]
    
    def is_empty(self):
        return len(self.items) == 0

#Test Cases
s = Stack()
s.push(1)
s.push(2)
s.push(3)
print(s.pop()) Output: 3
print(s.peek()) Output: 2
print(s.is_empty())  Output: False

Q2 How do you implement a queue data structure in Python?
class Queue:
    def __init__(self):
        self.items = []
    
    def enqueue(self, item):
        self.items.append(item)
    
    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
    
    def peek(self):
        if not self.is_empty():
            return self.items[0]
    
    def is_empty(self):
        return len(self.items) == 0
# Test Cases
q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
print(q.dequeue()) Output: 1
print(q.peek())  Output: 2
print(q.is_empty()) Output: False

Q3How do you implement a linked list in Python?
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None
    
    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
    
    def insert_at_end(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            return
        last_node = self.head
        while last_node.next:
            last_node = last_node.next
        last_node.next = new_node
    
    def delete_by_value(self, data):
        if self.head is None:
            return
        if self.head.data == data:
            self.head = self.head.next
            return
        current_node = self.head
        while current_node.next:
            if current_node.next.data == data:
                current_node.next = current_node.next.next
                break
            current_node = current_node.next
    
    def print_list(self):
        current_node = self.head
        while current_node:
            print
 #TEST CASES
 insert_at_beginning(3)
ll.insert_at_beginning(2)
ll.insert_at_beginning

Q4 How do you implement a binary search tree in Python?

class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

class BST:
    def __init__(self):
        self.root = None

    def insert(self, data):
        new_node = Node(data)
        if self.root is None:
            self.root = new_node
            return
        current_node = self.root
        while True:
            if data < current_node.data:
                if current_node.left is None:
                    current_node.left = new_node
                    break
                current_node = current_node.left
            else:
                if current_node.right is None:
                    current_node.right = new_node
                    break
                current_node = current_node.right
    
    def search(self, data):
        current_node = self.root
        while current_node:
            if data == current_node.data:
                return True
            elif data < current_node.data:
                current_node = current_node.left
            else:
                current_node = current_node.right
        return False

# Test Cases
bst = BST()
bst.insert(5)
bst.insert(3)
bst.insert(7)
print(bst.search(5))  Output: True
print(bst.search(6))  Output: False



