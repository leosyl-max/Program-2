#include <stdio.h>
#include <conio.h>

void reverse(int *arr, int size){
int *start= arr, *end= arr+size-1;
while (start<end){
    int temp= *start;
    *start= *end;
    *end= temp;
    start++;
    end--;
}
}
int main(){
int arr[]={1,2,3,4,5,6};
int size= sizeof(arr)/sizeof(arr[0]);
printf("Original array: \n");
for(int i=0; i<size; i++){
    printf("%d \n", arr[i]);
}
reverse(arr, size);
printf("Reverse array: \n");
for (int i=0; i<size; i++){
    printf("%d \n", arr[i]);
}
return 0;
}
