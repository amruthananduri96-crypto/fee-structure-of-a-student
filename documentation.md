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
