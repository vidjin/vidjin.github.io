Think of computer memory as cells which are 1 byte long. In order to store 2 byte hex-data (90AB), there are two possibilities: 

1. Big endian: In this, you store the most significant byte in the smallest address. Examples include Motorola 68000 series, Xilinx Microblaze, SuperH, IBM z/Architecture or Atmel AVR32. 

| Address value |     Data |
| :------------ | --------:|
|  1001         |        90|
|  1002         |        AB|


2. Little endian: In this, you store the least significant byte in the smallest address.
Example is Intel x86 and x86-64 series of processors, that's why it is also known as Intel Convention.

| Address value |     Data |
| :------------ | --------:|
|  1001         |        AB|
|  1002         |        90|

Program to check whether data in your system is stored in little endian format or big endian format.

Here's the code to test your machine's endianness:
```
#include<stdio.h>
#include<stdlib.h>
#define CPU_VENDOR_OS "intel-gnu-linux"
int main()
{          union
            {
                   short s;
                   char c[sizeof(short)];
            }un1;
            un1.s=0x0102;
            printf("%s\n",CPU_VENDOR_OS);
            if(sizeof(short)==2)
           {
                  if(un.c[0]==1 && un.c[1]==2)
                  {
                         printf("Big endian\n");
                   }
                   else if(un.c[0]==2 && un.c[1]==1)
                   {
                        printf("Little endian\n");
                   }
                  else
                  {
                       printf("Unknown\n");
                  }
          }
         return 0;
}
```

Output: Intel processor, so output is little endian.

![Output](images/LittleEndian.png)
