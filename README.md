# ROLL-NUMBER-SORTING-SYSTEM-USING-BUBBLE-SORT
/*
Roll number sorting system using bubble sort
Roll No : CO2080
*/
#include <stdio.h>
int main()
{
 int n,i,choice,arr[101],j,temp;
 printf("Enter number of students: ");
 scanf("%d", &n);
  do
   {
    printf("==== Roll Number Sorting System ====");
   printf("\n1.Accept roll numbers from user\n2. Display roll numbers\n3. Display sorted roll numbers and intermediate pass\n4.Exit");
    printf("\nEnter your choice: ");
    scanf("%d", &choice);
    switch (choice)
    {
      case 1:
           printf("\nAdd roll numbers of students:\n");
            for(i=0;i<n;i++)
                {
                  scanf("%d", &arr[i]);
                }
                break;
      case 2:
          printf("\nRoll numbers of students are:\n");
          for(i=0;i<n;i++)
                {
                  printf("\n%d ", arr[i]);
                }
                printf("\n");
                break;
       case 3:
            for(i=0;i<n-1;i++)
             {
              for(j=0;j<n-i-1;j++)
                {
                 if (arr[j]>arr[j+1])
                  {
                    temp = arr[j];
                     arr[j] = arr[j+1];
                      arr[j+1] = temp;
                  }
                }
                printf("\nPASS %d : ",i+1);
                for(j=0;j<n;j++)
                {
                 printf("\t%d",arr[j]);
                 }
                 printf("\n");
              }
              printf("\nSorted roll numbers are:\n");
              for(i=0;i<n;i++)
               {
                 printf("\n%d ", arr[i]);
              }
              printf("\n");
              break;
      case 4:
           printf("\nExit");
                break;
            default:
                printf("\nINVALID CHOICE");
        }
    } while(choice != 4);
    return 0;
}

