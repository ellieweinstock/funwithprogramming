#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define QUEUE_MAX_SIZE 10 //change this
#define MAX_SIZE 500

void QUEUE_PUSH(int);
void QUEUE_POP();
void PRINTQUEUE();

int lo, hi, queuesize;
int q[QUEUE_MAX_SIZE+3];
char buff[MAX_SIZE+3];

int main()
{
    memset(q, -1, sizeof(q));

    while(1 < 2)
    {
        system("cls");
        printf("> ");
        scanf("%s", buff);

        if( !strcmp(buff, "push") )
        {
            int y;
            system("cls");
            printf("push: ");
            scanf("%d", &y);
            QUEUE_PUSH(y);
        }
        else if( !strcmp(buff, "pop") )
            QUEUE_POP();
        else if( !strcmp(buff, "print") )
            PRINTQUEUE();
        else if( !strcmp(buff, "exit") )
            return 0;
    }
    return 0;

}

void QUEUE_PUSH(int x)
{
    if(hi == QUEUE_MAX_SIZE)
        hi = 0;
    q[hi++] = x;
    ++queuesize;
}

void QUEUE_POP()
{
    if(!queuesize)
    {
        lo = hi = 0;
        return;
    }
    --queuesize;
    q[lo++] = -1;
    if(lo >= QUEUE_MAX_SIZE)
        lo = 0;
}

void PRINTQUEUE()
{
    int i;
    printf("\n\n*****************************************************************\n");
    printf("QUEUE status:\n");
    for(i = 0; i < QUEUE_MAX_SIZE; ++i)
        printf("%d ", q[i]);
    printf("\n*****************************************************************\n\n");
    printf("Press Enter to continue.\n");
    getchar(), getchar();
}
