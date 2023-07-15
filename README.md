# Queue-Using-Array1
//Queue Using Array
//SOURCE CODE
import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Queue q=new Queue();
        Scanner sc= new Scanner(System.in);
        int n=sc.nextInt();        
        int val;
        for(int i=0;i<n;i++){
            val=sc.nextInt();
            q.enqueue(val);
        }
        q.display();
    }
}
class Queue{
    int front,rear, len=0;
    int arr[]=new int[100];
    Queue(){
        front=-1;
        rear=-1;        
    }
    public void enqueue(int val){
        if(rear==-1)
            front++;
        arr[++rear]=val;
        len++;
    }
    public void display(){
        for (int i=0;i<len;i++)
            System.out.print(arr[i]+" ");
    }
}
