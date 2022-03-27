#include<stdio.h>
#include<string.h> 
    struct Student
    {
        char student_ID[17];
        int st1;
        int st2;
    }student[1000];
int main()
{
    struct Student stduent[1000] ;
    int Iint[1000];
    int i,j,m,a;
    printf("考生数为: \n");
    scanf("%d" ,&a);
    for(i=0;i<a;i++)
    {
        scanf("%s %d %d" ,&student[i].student_ID,&student[i].st1,&student[i].st2);
    }  
    printf("退至考生数:");
    scanf("%d",&m);
    for(j=0;j<m;j++)
    {
        printf("退至考生的座位号:");
        scanf("%d" ,&Iint[j]);
        for(i=0;i<a;i++)
        {
            if(Iint[j]==student[i].st1)
            {
                printf("考号:%s座位号:%d\n",student[i].student_ID,student[i].st2);
                break;
            }
        }
    }
    return 0;
}
