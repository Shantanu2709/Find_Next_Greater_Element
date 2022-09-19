# Find_Next_Greater_Element
Find_Next_Greater_Element using stack in Linear Time complexity...O(n)

// # Code
import java.util.*;
class HelloWorld {
    public static void main(String[] args) {
        int arr[]={6,8,0,1,3};
        int n=arr.length;
        Stack<Integer> s= new Stack<>();
        int nextgreater[] = new int[arr.length];
        for(int i=n-1; i>=0; i--)
        {
            while(!s.isEmpty() && arr[s.peek()] <=arr[i])
            {
                s.pop();
            }
                if(s.isEmpty())
                {
                    nextgreater[i]=-1;
                }
                else
                {
                    nextgreater[i]=arr[s.peek()];
                }
            
            s.push(i);
        }
        for(int i=0; i<arr.length; i++)
        {
            System.out.print(nextgreater[i]+" ");
        }
    }
}
