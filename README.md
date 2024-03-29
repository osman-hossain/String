<!--writing a tutorial programme about string-->

_s_~~tr~~__i__`ng`

### string
---

<p>programme of string</p>

<ol>
<li>code</li>
<li>picture</li>
</ol>  

- [x] code  
- [x] picture  
- [] error

</br>



### string basic

```c
#include<stdio.h>
int main()
{
    char a[6];

    a[0]='O';
    a[1]='s';
    a[2]='m';
    a[3]='a';
    a[4]='n';

    printf(" a = %s",a);

    return 0;
}
```
<image src="./images/basic.png" width="500" title="basic"/> 

### different style

```c
#include<stdio.h>
int main()
{
    char a[6]={'O','s','m','a','n','\0'};

    printf("a = %s",a);

    return 0;
}
```

```c
#include<stdio.h>
int main()
{
    char a[]={'O','s','m','a','n','\0'};

    printf("a = %s",a);

    return 0;
}
```
![image](./images/basic.png)  

### type full name

---

```c
#include<stdio.h>
int main()
{
    char a[]="Osman Hossain";

    printf("a = %s",a);

    getchar();
}
```
<image src="./images/basicfullname.png" width="500" title="basic"/> 

```c
#include<stdio.h>
int main()
{
    char a[]="Osman Hossain \ Karam Khan";

    printf("a = %s",a);

    getch();
}
```
![double](./images/double.png)  

<!--scanf can't take space like "osman hossain" print will be "osman" so Use gets(); insted scanf(). printf will be "osman hossain" -->  

### input name and printf "gets()"

```c
#include<stdio.h>
int main()
{
    int a[100];

    printf("Enter the number : ");
    gets(a);

    printf("a = %s",a);
    return 0;
}
```  
![input](./images/inputname.png)  

</b>

### single alphabet output

```c
#include<stdio.h>
int main()
{
    char a[]="sareng"

    int i=0;

    while(a[i]!='\0')
    {
        printf("a[%d] = %c\n",i,a[i]);
        i++;
    }
    return 0;
}
```
<image src="./images/single.png" width="500" title="single"/>  

### "strlen()"  finding length of string

```c
#include<stdio.h>
int main()
{
    char a[]="dipraaj sareng";
    
    int len=strlen(a);
    printf("length = %d",len);

    getch();
}
```  
![strlen](./images/strlen.png)

</br>

### without strlen() size

```c
#include<stdio.h>
int main()
{
    char a[]="dipraz sareng";
    int i=0,len=0;

    while(a[i]!='\0')
    {
        i++;
        len++;
    }
    printf("Length = %d",len);

    getchar();
}
```
![size](./images/size.png)  


### strcpy

```c
#include<stdio.h>
int main()
{
    char source[]="sareng",target[30];

    strcpy(target,source);

    printf("source = %s\n",source);
    printf("target = %s\n",target);

    getchar();
}
```  
<image src="./images/strcpy.png" width="500" title="strcpy"/>  

### Concatation "strcat()"

_sum of two string_  

```c
#include<stdio.h>
int main()
{
    char str1[]="My name is ";
    char str2[]="sareng";

    strcat(str1,str2);

    printf("str1 = %s\n",str1);
    printf("str2 = %s\n",str2);

    getch();
}
```  
<image src="./images/strcat.png" width="500" title="strcat"/>  

another style

```c
#include<stdio.h>
int main()
{
    char str[]="My name is ";

    strcat(str,"sareng");

    printf("str = %s",str);

    getchar();
}
```  

<image src="./images/strcat2.png" width="500" title="strcat"/>  

### without strcat

```c
#include<stdio.h>
int main()
{
    char str1[30]="My name is ";
    char str2[]="sareng";

    int i=0,j=0,len=0;

    while(str1[i]!='\0')
    {
        i++;
        len++;
    }

    while(str2[j]!='\0')
    {
        str1[len+j]=str2[j];
        j++;
    }
    printf("str1 = %s",str1);
    getchar();
}
```

![withoutstrcat](./images/without.png)

### strcmp()

string compare using strcmp()

```c
#include<stdio.h>
int main()
{
    char str1[]="serang is a component";
    char str2[]="is it true";

    int c=strcmp(str1,str2);

    if(c==0)
    {
        printf("The strings are Equal.");
    }
    else
    {
        printf("The strings are not Equal.");
    }

    getchar();
}
```  

<image src="./images/equal.png" width="500" title="equal"/>  

### strcmp()  use with input

```c
#include<stdio.h>
int main()
{
    while(1)
    {
        char a[100],b[100];

        printf("Enter the firt sentence : ");
        gets(a);
        printf("Enter the second sentence : ");
        gets(b);

        int c=strcmp(a,b);

        if(c==0)
        {
            printf("The strings are Equal.");
        }
        else
        {
            printf("The strings are not Equal.");
        }
    }
    getchar();
}
```  
![different](./images/diff.png)   

### strrev() 

reverse text

```c
#include<stdio.h>
int main()
{
    char a[]="this is sareng";

    printf("a = %s\n",a);

    strrev(a);

    printf("a = %s",a);

    getch();
}
```
<image src="./images/reverse.png" width="500" title="strrev"/>  

### strrev(); without reverse

reverse without strrev tag.

```c
#include<stdio.h>
int main()
{
    char a[]="dipraj sareng";
    char b[14];
    int i=0,len=0,j;

    while(a[i]!='\0')
    {
        len++;
        i++;
    }

    for(j=0,i=len-1; i>=0; i--,j++)
    {
        b[j]=a[i];
    }
    b[j]='\0';
    printf("a = %s\n",a);
    printf("b = %s",b);
    getch();
}
```  

<image src="./images/strrev.png" width="500" title="without strrev"/>  

### palindrome

```c
#include<stdio.h>
int main()
{
    char a[]="madam";
    char b[30];
    int i=0,j;
    int len = strlen(a);
    printf("length = %d\n",len);
    for(j=0,i=len-1; i>=0; i--,j++)
    {
        b[j]=a[i];
        printf("b[%d] = a[%d] = %c\n",j,i,b[j]);
    }
    b[j]='\0';

    printf("\n a = %s\n",a);
    printf("\n b = %s\n",b);

    int c=strcmp(a,b);
    if(c==0)
        printf("\npalindrome\n");
    else
        printf("\nnot palindrome\n");
    return 0;
}
```  
<image src="./images/palindrome.png" width="500" title="palindrome"/>  

### swap 

```c
#include<stdio.h>
int main()
{
    char a[]="vutan";
    char b[]="bangladesh";
    char temp[20];

    printf("\n\nBefore Reverse\n");
    printf("a = %s\n",a);
    printf("b = %s\n",b);


    strcpy(temp,a);
    strcpy(a,b);
    strcpy(b,temp);
    printf("\n\nAfter reverse\n");
    printf("a = %s\n",a);
    printf("b = %s\n",b);

    getch();
}
```  

<image src="./images/swap.png" width="500" title="swap"/>  

### strupr() upper

```c
#include<stdio.h>
int main()
{
    char a[]="gooGle";

    printf("Input a = %s\n",a);

    strupr(a);

    printf("Upper a = %s",a);

    getchar;
}
```

<image src="./images/upper.png" width="500" title="upper"/>  

### strlwr() lower

```c
#include<stdio.h>
int main()
{
    char a[]="MY NaME IS SArEnG";

    printf("Input a = %s\n",a);

    strlwr(a);

    printf("Lower letter a = %s",a);

    getch();
}
```

<image src="./images/lower.png" width="500" title="lower"/>  

### count vowel consonant words digits and others

```c
#include<stdio.h>
int main()
{
    while(1)
    {
        char a[100],ch;
        int i,vowel,consonant,word,digit,other;

        printf("Enter the strings : ");
        gets(a);

        i=vowel=consonant=word=digit=other=0;

        while((ch=a[i])!='\0')
        {
            if(a[i]=='a' || a[i]=='e' || a[i]=='i' || a[i]=='o' || a[i]=='u' ||
                    a[i]=='A' || a[i]=='E' || a[i]=='I' || a[i]=='O' || a[i]=='U')
            {
                vowel++;
            }
            else if((ch>='a' && ch<='z') || (ch>='A' && ch<='Z'))
            {
                consonant++;
            }
            else if(ch>='0' && ch<='9')
            {
                digit++;
            }
            else if(ch==' ')
            {
                word++;
            }
            else
            {
                other++;
            }
            i++;
        }
        word++;

        printf("Vowel = %d\n",vowel);
        printf("Consonant = %d\n",consonant);
        printf("Words = %d\n",word);
        printf("Digits = %d\n",digit);
        printf("Others = %d\n",other);

    }
    getch();
}
```

![multiplecount](./images/multiple.png)  

### count capital small and digits

```c
#include<stdio.h>
int main()
{
    char a[100];
    int i,capital,small,digit;

    printf("Enter a string : ");
    gets(a);

    i=capital=small=digit=0;

    while(a[i]!='\0')
    {
        if(a[i]>=65 && a[i]<=90)
        capital++;
        else if(a[i]>=97 && a[i]<=122)
        small++;
        else if(a[i]>=48 && a[i]<=57)
        digit++;
        i++;
    }
    printf("Capital = %d\n",capital);
    printf("Small = %d\n",small);
    printf("digit = %d\n",digit);

    getch();
}
```  

![csd](./images/csd.png)
