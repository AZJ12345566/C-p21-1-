# C-p21-1-
C语言学习笔记 p21 初识指针(1)
int main()
{
    int a=10;
    int* p=&a;//指针变量
    return 0;
}

int main()
{
    printf("$d\n",sizeof(char*));
    printf("$d\n",sizeof(short*));
    printf("$d\n",sizeof(int*));
    printf("$d\n",sizeof(double*));
    return 0;
}//输出都是4

int main()
{
    int a=0x11223344;
    int* pa=&a;
    char* pc=&a;
    printf("%p\n",pa);
    printf("%p\n",pc);
    return 0;
}//输出两个地址一模一样

int main()
{
    int a=0x11223344
    char* pc=&a;
    *pc=0;
    return 0;
}//指针类型决定了指针进行解引用的时候，能够访问空间的大小
//int* p;* p能够访问4个字节
//char* p；* p能够访问1个字节

int main()
{
    int a=0x11223344;
    int* pa=&a;
    char* pc=&a;
    printf("%d\n,pa);
    printf("%d\n,pa+1);
    printf("%d\n,pc);
    printf("%d\n,pc+1);
    return 0;
}//指针类型决定了指针走一步走多远

//野指针的成因：
//1.指针未初始化
//2.指针越界访问
//3.指针指向的那块内存空间释放了
int* test()
{
    int a=10;
    return &a;
}//a出来就直接被销毁了
int main()
{
    test();
    return 0;
}





