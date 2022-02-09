#include <stdio.h>
unsigned short int reverse_bits(unsigned short int n){
    unsigned short int a=0;
    for(int i=0;i<16;i++){
  
  a = a<<1;
    a= a|(n&1);
    n = n>>1;
    
    }
    return a;
}
void binary(unsigned short int a){
    int array[16];
    for(int x=0;x<16;x++){
        array[x]=a%2;
        a=a/2;
    }
    for(int j=15;j>=0;j--){
        printf("%d",array[j]);
    }
    
}
int main() {
    printf("Enter number\n");
    unsigned short int num;
    scanf("%hu",&num);
    printf("%hu\n",num);
    
    binary(num);
   unsigned short int c = reverse_bits(num);
    printf("\n%hu\n",c);
    binary(c);
    return 0;
}
