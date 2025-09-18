
1) In a circular queue, what happens when rear is at end and space is at front?
	a)  Queue is full
	==b) Rear is incremented circularly==
	c) Underﬂow
	d) Skip
	
2) In AVL trees, a single Le rota on is performed in which case?
	a) LL case 
	==b) RR case==
	c) RL case
	d) LR case
	
3) Output-restricted deque allow dele on at:
	a) Rear
	==b) Front==
	c) Both
	d) Middle
	
4) The height of an AVL tree with 7 nodes is atleast:
	==a) 3==
	b) 2
	c) 1
	d) 4
	
5) If a queue is implemented using an array of size 10, and front=8, 
    rear = 3:how many elements are present?
	(a) 7
	(b) 5
	(c) 4
	==(d) 6==

	Fill-in-the-Blank Questions
	
6) Consider the following code:
	push(5),push(8),pop,push(2),push(5),pop,push(1),pop
	The output of the above snippet is .  ==Stack = [5,2]==
7) Inﬁx: A - (B + (C * D) / E) → Postfix:   ==A B C D * + E / -==
8) Inﬁx: (A + B) ^ (C + (D * E)) → Preﬁx:    ==^ + A B + C * D E==
9) Preﬁx: / * + A B C - D E → Postfix:    ==A B + C * D E - /==
10) Postfix: A B C * - D E F + / + → Preﬁx:    ==+ - A * B C / D + E F==
11) Postfix: 7 5 2 * 6 / 4 + 3 - 8 *   ==Mistake qus  Bonus==
12) Preﬁx: * + - 9 1 + * 5 2 / 6 3 8   ==180==
13) Queue size = 5, Insert: 5, 15, 25, 35, 45, Delete: 2 elements.
    Find Front and Rear indexes.   ==Final queue: [25,35,45];    2 & 4==
14) Circular Queue size = 6,Insert: 12, 24, 36, 48, 60,Delete: 3 elements. Insert: 72, 84.
	  Find Front and Rear indexes.   ==Answer: Front = 3, Rear = 0==
15) In a priority queue using an array, insert:
	(15,2), (25,4), (35,3), (45,1). Then delete the highest priority element.
	What is the new front and rear index?   ==Answer: Front = 0, Rear = 2==
16) What is Circular queue full logic

		class Node {
		    int data;
		    Node next;
		}
		
		class CircularQueue {
		    Node front = null, rear = null;
		
		    void enqueue(int value) {
		        Node newNode = new Node();
		        newNode.data = value;
		
		        if (front == null) {
		            front = rear = newNode;
		            rear.next = front;  // Circular link
		        } else {
		            rear.next = newNode;
		            rear = newNode;
		            rear.next = front;
		        }
		    }
		
		    void dequeue() {
		        if (front == null) {
		            System.out.println("Queue is empty");
		            return;
		        }
		
		        if (front == rear) {
		            System.out.println("Deleted: " + front.data);
		            front = rear = null;
		        } else {
		            System.out.println("Deleted: " + front.data);
		            front = front.next;
		            rear.next = front;
		        }
		    }
		
		    void display() {
		        if (front == null) {
		            System.out.println("Queue is empty");
		            return;
		        }
		
		        Node temp = front;
		        do {
		            System.out.print(temp.data + " ");
		            temp = temp.next;
		        } while (temp != front);
		        System.out.println();
		    }
		}

17) What is priority queue full logic
	   class PNode {
		    int data;
		    int priority;
		    PNode next;
		 }
		
		class PriorityQueueLL {
		    PNode head = null;
		
	    void enqueue(int data, int priority) {
	        PNode newNode = new PNode();
	        newNode.data = data;
	        newNode.priority = priority;
	
	        if (head == null || priority < head.priority) {
	            newNode.next = head;
	            head = newNode;
	        } else {
	            PNode temp = head;
	            while (temp.next != null && temp.next.priority <= priority) {
	                temp = temp.next;
	            }
	            newNode.next = temp.next;
	            temp.next = newNode;
	        }
	    }
	
	    void dequeue() {
	        if (head == null) {
	            System.out.println("Queue is empty");
	        } else {
	            System.out.println("Deleted: " + head.data);
	            head = head.next;
	        }
	    }
	
	    void display() {
	        PNode temp = head;
	        while (temp != null) {
	            System.out.println("Data: " + temp.data + ", Priority: " + 
	            temp.priority);
	            temp = temp.next;
	        }
	    }
	   }

18) Double ended queue full logic

			class DNode {
		    int data;
		    DNode next, prev;
		
		    DNode(int data) {
		        this.data = data;
		    }
		}
		
		class Deque {
		    DNode front = null, rear = null;
		
		    void insertFront(int data) {
		        DNode newNode = new DNode(data);
		        if (front == null) {
		            front = rear = newNode;
		        } else {
		            newNode.next = front;
		            front.prev = newNode;
		            front = newNode;
		        }
		    }
		
		    void insertRear(int data) {
		        DNode newNode = new DNode(data);
		        if (rear == null) {
		            front = rear = newNode;
		        } else {
		            rear.next = newNode;
		            newNode.prev = rear;
		            rear = newNode;
		        }
		    }
		
		    void deleteFront() {
		        if (front == null) {
		            System.out.println("Deque is empty");
		            return;
		        }
		        System.out.println("Deleted from front: " + front.data);
		        front = front.next;
		        if (front == null) rear = null;
		        else front.prev = null;
		    }
		
		    void deleteRear() {
		        if (rear == null) {
		            System.out.println("Deque is empty");
		            return;
		        }
		        System.out.println("Deleted from rear: " + rear.data);
		        rear = rear.prev;
		        if (rear == null) front = null;
		        else rear.next = null;
		    }
		
		    void display() {
		        DNode temp = front;
		        System.out.print("Deque: ");
		        while (temp != null) {
		            System.out.print(temp.data + " ");
		            temp = temp.next;
		        }
		        System.out.println();
		    }
		}

19) OUTPUT Restricted DEQUE,Size = 5,
	Operations: enqueueRear(10), enqueueRear(20)
	enqueueFront(35), dequeueFront(), dequeueRear(),
	Q:Final elements? Value of front and rear?  
	 - ==**Final elements:** [10, 20]==
	==**Front index:** 0 **Rear index:** 1==

20) ![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626033751.png)
		 ==q ancestor nodes = j, d, a==
		 ==f descendant nodes = l, m, f==

21) 
	- ==What is Height of tree = 5==
	- ==What is depth of d  = 1== 
	- ==what is height of c = 4==
	- ==Degree of j = 3==




22) Write tree for Strictly binary tree  ==Any strict binary tree example==

23) ![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626033948.png)

	- Preorder = 2 → 7 → 2 → 6 → 5 → 11 → 5 → 9 → 4  
	- Postorder = 6 → 5 → 2 → 11 → 7 → 4 → 9 → 5 → 2
	- Inorder = 6 → 2 → 5 → 7 → 11 → 2 → 4 → 9 → 5
	
24) Construct a Binary Tree from Traversal Results
	Inorder Traversal: [4, 1, 7, 5, 6, 3, 2]
	Postorder Traversal: [4, 3, 2, 5, 7, 6, 1]
		==Error in qus Bonus==

25) ![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626034108.png)
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626043443.png)
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626043540.png)
    

26) ![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250626034143.png)