  ***ALGORITHM***
Step 1: Start
Step 2: Create Node Structure

Each node contains:

Roll Number
Category
Base Fee
Bus Fee
CDP Fee
Paid Fee
Pointer to next node
Step 3: Initialize
Set head = NULL
Step 4: Display Menu

Repeat until user exits:

Add Student
Search Student
Display All
Exit
🔷 Option 1: Add Student
Step 5: Input Data
Read roll_number
Read paid_fee, bus_fee, cdp_fee
Step 6: Determine Category
IF roll starts with "PMSR"
    category = PMSR
ELSE IF roll starts with "PMS"
    category = PMS
ELSE IF roll starts with "MGMT"
    category = Management
ELSE
    category = Non-PMS
Step 7: Assign Base Fee
IF category = PMS      → base_fee = 50000
IF category = PMSR     → base_fee = 30000
IF category = Management → base_fee = 80000
IF category = Non-PMS  → base_fee = 60000
Step 8: Create New Node
Allocate memory
Store all values
Set next = NULL
Step 9: Insert into Linked List
IF head == NULL
    head = new node
ELSE
    traverse to last node
    last->next = new node
🔷 Option 2: Search Student
Step 10: Input Roll Number
Step 11: Traverse Linked List
temp = head
WHILE temp != NULL
    IF temp->roll == input_roll
        GO TO Step 12
    temp = temp->next
IF not found
    PRINT "Student not found"
Step 12: Calculate Fee Details
total_fee = base_fee + bus_fee + cdp_fee
due = total_fee - paid_fee
Step 13: Display Details
Roll Number
Category
Fees (Base, Bus, CDP, Total)
Paid Fee
Due Amount
Step 14: Display Status
IF due <= 0
    PRINT "Fully Paid"
ELSE
    PRINT "Pending"
🔷 Option 3: Display All Students
Step 15: Traverse List
temp = head
WHILE temp != NULL
    PRINT temp->roll
    temp = temp->next
Step 16: Stop
*****FLOW CHART****
<img width="1024" height="1536" alt="Image" src="https://github.com/user-attachments/assets/d8a31f4d-2778-4c9c-ac72-365d3563b50f" />
 **methodology**

The program is developed to manage student fee records efficiently using a singly linked list, which enables dynamic memory allocation and easy insertion of records without requiring a fixed size. At the beginning, the head pointer is initialized to NULL, indicating that no student data is present. The program follows a menu-driven approach, allowing the user to repeatedly choose operations such as adding a new student, searching for an existing student, displaying all student records, or exiting the system.

When the user selects the add student option, the program collects essential details such as roll number, paid fee, bus fee, and CDP fee. Based on the prefix of the roll number, the student is categorized into groups like PMS, PMSR, Management, or Non-PMS. Each category is associated with a predefined base fee. After determining the category and base fee, a new node is created to store all the student details. This node is then inserted at the end of the linked list by traversing from the head to the last node, ensuring that the order of insertion is maintained.

For the search operation, the program asks the user to enter a roll number and then traverses the linked list sequentially to find a matching record. If the student is found, the program calculates the total fee by summing the base fee, bus fee, and CDP fee. It then computes the due amount by subtracting the paid fee from the total fee. Based on the due value, the program determines whether the student has fully paid the fees or still has a pending balance. All relevant details, including roll number, category, fee structure, total fee, paid amount, due amount, and payment status, are displayed clearly to the user. If the student is not found in the list, an appropriate message is displayed.


In the display operation, the program traverses the entire linked list from the head node to the last node and prints the roll numbers (or details) of all students, showing the structure of the list. This helps the user view all stored records at once. The program continues to execute these operations in a loop, allowing multiple actions until the user selects the exit option. Once the exit option is chosen, the program terminates, completing the execution. This methodology ensures efficient data handling, easy searching, and flexible storage using linked list concepts.


