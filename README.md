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



