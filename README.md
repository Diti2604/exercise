#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n,m;
    scanf("%d %d", &n, &m);
    int num[n][m];

    for(int i=0; i<n; i++)
    {
        for(int j=0; j<m; j++)
        {
            scanf("%d", &num[i][j]);
        }
    }

    for(int i=0; i<n; i++)
    {
        int min=num[i][0];
        for(int j=0; j<m; j++)
        {
            if(num[i][j]<min)
            {
                min=num[i][j];
            }
        }

        for(int j=0; j<m; j++)
        {
            printf("%d ", num[i][j]-min);
        }
        printf("\n");
    }
    return 0;
}
