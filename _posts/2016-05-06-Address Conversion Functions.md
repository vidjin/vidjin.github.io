## Implementing address conversion functions

Some functions are used in network programming to convert the IP addresses to human readable form and back. 

inet_ntop() & inet_ntoa():These functions convert a network address in a struct in_addr to a dots-and-numbers format string.

inet_pton(), inet_aton() & inet_addr :This functions convert a dots-and-numbers string  to struct in_addr format.

inet_ntoa, inet_aton and inet_addr are deprecated because they are incompatible with IPv6 addresses. Functions like inet_pton and inet_ntop can be used with both IPv4 and IPv6 addresses. 
```
Code:

#include<stdio.h> 
#include<sys/socket.h> 
#include<stdlib.h> 
#include<arpa/inet.h> 
#define SERV_PORT 9002  
int main() 
{  
   char str[INET_ADDRSTRLEN],*str1,*str2; 
   struct sockaddr_in server; 
  
   printf("Testing inet_pton and inet inet_ntop\n"); 
   inet_pton(AF_INET, "192.0.2.33", &(server.sin_addr)); 
   inet_ntop(AF_INET, &(server.sin_addr), str, INET_ADDRSTRLEN); 
   printf("%s\n", str); // prints "192.0.2.33" 
    
   bzero(&str1,sizeof(str1)); 
   bzero(&server,sizeof(server)); 
  
   printf("Testing inet_ntoa and inet_aton\n"); 
   inet_aton("192.168.1.1",&(server.sin_addr)); 
   str1=inet_ntoa(server.sin_addr); 
   printf("%s\n",str1); 
  
   bzero(&str1,sizeof(str1)); 
   bzero(&server,sizeof(server)); 
  
   printf("Testing inet_addr\n"); 
   server.sin_addr.s_addr=inet_addr("192.2.2.2"); 
   str2=inet_ntoa(server.sin_addr); 
   printf("%s\n",str2); 
}  
```
![Output](images/Address-conversion-1.png "Output Screenshot")

Thanks!
