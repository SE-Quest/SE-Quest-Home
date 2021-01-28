# TEC_01

```c
#include <stdio.h>

int main() {
    char str[50];
    char alpha = 0;
    int num = 0,i,j;
    printf("Enter a String: ");
    scanf("%s",str);
    for (i=0; str[i]; i++){
        
        if ((str[i] >= 'A' && str[i] <= 'Z')||(str[i] >= 'a' && str[i] <= 'z')){
            if (alpha != 0){
                //Final output
                for (j=0; j<num; j++){
                    printf("%c",alpha);
                }
            num = 0;
            }
            alpha = str[i];
        }
        
        if (str[i] >= '0' && str[i] <= '9'){
            num = num*10+str[i]-48;
        }
        
        
    }
    //Last character will not be printed if you didn't give the below statement
    for (j=0; j<num; j++){
            printf("%c",alpha);
    }
    
    return 0;
}
```
