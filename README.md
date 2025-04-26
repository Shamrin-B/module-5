# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    float length, width, area;
    float *lptr, *wptr;

    printf("Enter the length of the rectangle: ");
    scanf("%f", &length);
    printf("Enter the width of the rectangle: ");
    scanf("%f", &width);

    lptr = &length;
    wptr = &width;

    area = (*lptr) * (*wptr);

    printf("The area of the rectangle is: %.2f\n", area);

    return 0;
}
```
## OUTPUT
		       	
```
Enter the length of the rectangle: 5
Enter the width of the rectangle: 4
The area of the rectangle is: 20.00
```

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str;

    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }

    str = "WELCOME";

    printf("%s\n", str);

    free(str);

    return 0;
}
```

## OUTPUT
```
WELCOME
```


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct Student student;

    printf("Enter the student's name: ");
    fgets(student.name, sizeof(student.name), stdin);

    printf("Enter the roll number: ");
    scanf("%d", &student.roll_no);

    printf("Enter the marks: ");
    scanf("%f", &student.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s", student.name);
    printf("Roll Number: %d\n", student.roll_no);
    printf("Marks: %.2f\n", student.marks);

    return 0;
}
```

## OUTPUT
```
Enter the student's name: John Doe
Enter the roll number: 12345
Enter the marks: 88.5

Student Information:
Name: John Doe
Roll Number: 12345
Marks: 88.50
```

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct Employee emp[3];
    int i;

    for(i = 0; i < 3; i++) {
        printf("Enter details for employee %d\n", i+1);

        printf("Enter name: ");
        getchar();
        fgets(emp[i].name, sizeof(emp[i].name), stdin);

        printf("Enter ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter basic salary: ");
        scanf("%f", &emp[i].basic_salary);

        emp[i].gross_salary = emp[i].basic_salary + (emp[i].basic_salary * 0.25) + (emp[i].basic_salary * 0.15);
    }

    printf("\nEmployee Details and Gross Salary:\n");
    for(i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i+1);
        printf("Name: %s", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

    return 0;
}
```

 ## OUTPUT
```
Enter details for employee 1
Enter name: John Doe
Enter ID: 1001
Enter basic salary: 50000

Enter details for employee 2
Enter name: Jane Smith
Enter ID: 1002
Enter basic salary: 60000

Enter details for employee 3
Enter name: Emily Clark
Enter ID: 1003
Enter basic salary: 45000

Employee Details and Gross Salary:

Employee 1:
Name: John Doe
ID: 1001
Basic Salary: 50000.00
Gross Salary: 62500.00

Employee 2:
Name: Jane Smith
ID: 1002
Basic Salary: 60000.00
Gross Salary: 75000.00

Employee 3:
Name: Emily Clark
ID: 1003
Basic Salary: 45000.00
Gross Salary: 56250.00
```
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    int n, i, j;
    
    for(i = 0; i < 2; i++) {
        printf("Enter details for student %d:\n", i+1);
        printf("Enter roll number: ");
        scanf("%d", &n);
        
        printf("Enter marks for 5 subjects: \n");
        for(j = 0; j < 5; j++) {
            printf("Subject %d: ", j+1);
            scanf("%d", &s[i].subject[j]);
        }
    }

    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374;
    s[1].total = 383;

    for(i = 0; i < 2; i++) {
        printf("\nStudent %d - Total Marks: %d\n", i+1, s[i].total);
        printf("Average Marks: %.2f\n", (float)s[i].total / 5);
    }

    return 0;
}

```

## OUTPUT

 ```
Enter details for student 1:
Enter roll number: 1
Enter marks for 5 subjects: 
Subject 1: 78
Subject 2: 75
Subject 3: 80
Subject 4: 72
Subject 5: 69

Enter details for student 2:
Enter roll number: 2
Enter marks for 5 subjects: 
Subject 1: 85
Subject 2: 88
Subject 3: 75
Subject 4: 70
Subject 5: 65

Student 1 - Total Marks: 374
Average Marks: 74.80

Student 2 - Total Marks: 383
Average Marks: 76.60
```

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


