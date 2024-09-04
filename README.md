# LinkedList-inserting
Inserting an element in LinkedList from starting
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None
        
        
class LinkedList:
    def __init__(self):
        self.head = None
        self.tail = None
        self.length = 0
        
        
    def append(self, value):
        new_node = Node(value)
        if self.head is None:
            self.head = new_node
            self.tail = new_node
        else:
            self.tail.next = new_node
            self.tail = new_node
        self.length += 1
    
    
    def __str__(self):
        temp_node = self.head
        result = " "
        while temp_node is not None:
            result += str(temp_node.value)
            if temp_node.next is not None:
                result += " --> "
            temp_node = temp_node.next
        return result
          
          
new_linked_list = LinkedList()
new_linked_list.append(11)
new_linked_list.append(22)
new_linked_list.append(77)
new_linked_list.append(66)
new_linked_list.append(55)
new_linked_list.append(44)
new_linked_list.append(33)
print(new_linked_list)
        


  output ==
  11 --> 22 --> 77 --> 66 --> 55 --> 44 --> 33
  
