## Recursion in Java

Recursion in java is a process in which a method calls itself continuously. A method in java that calls itself is called recursive method.

It makes the code compact but complex to understand.

Syntax:

```
    returntype methodname(){  
    //code to be executed  
    methodname();//calling same method  
    }  
```

### Java Recursion Example 1: Infinite times

```
    public class RecursionExample1 {  
    static void p(){  
    System.out.println("hello");  
    p();  
    }  
      
    public static void main(String[] args) {  
    p();  
    }  
    }  
```

output

```
hello
hello
...
java.lang.StackOverflowError
```

### Java Recursion Example 2: Finite times

```
    public class RecursionExample2 {  
    static int count=0;  
    static void p(){  
    count++;  
    if(count<=5){  
    System.out.println("hello "+count);  
    p();  
    }  
    }  
    public static void main(String[] args) {  
    p();  
    }  
    }  
```

output

    hello 1
    hello 2
    hello 3
    hello 4
    hello 5


### Java Recursion Example 3: Factorial Number

```
    public class RecursionExample3 {  
        static int factorial(int n){      
              if (n == 1)      
                return 1;      
              else      
                return(n * factorial(n-1));      
        }      
      
    public static void main(String[] args) {  
    System.out.println("Factorial of 5 is: "+factorial(5));  
    }  
    }  
```

output Factorial of 5 is: 120

#### Working of above program:

```
factorial(5) 
   factorial(4) 
      factorial(3) 
         factorial(2) 
            factorial(1) 
               return 1 
            return 2*1 = 2 
         return 3*2 = 6 
      return 4*6 = 24 
   return 5*24 = 120
```

### Java Recursion Example 4: Fibonacci Series

```
    public class RecursionExample4 {  
        static int n1=0,n2=1,n3=0;      
         static void printFibo(int count){      
            if(count>0){      
                 n3 = n1 + n2;      
                 n1 = n2;      
                 n2 = n3;      
                 System.out.print(" "+n3);     
                 printFibo(count-1);      
             }      
         }        
      
    public static void main(String[] args) {  
        int count=15;      
          System.out.print(n1+" "+n2);//printing 0 and 1      
          printFibo(count-2);//n-2 because 2 numbers are already printed     
    }  
    }  
```

output:

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377




