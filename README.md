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

