<h1> Recursion </h1>
Technique of a function calling itself.

<h2> Recursive Function </h2>
A function that calls itself repeatedly until a <b>condition is met</b>.
Three simple components: <br><br>
<ul>
  <li>call the method in itself</li>
  <li> have an exit statement </li>
  <li>reduce the input domain</li>
</ul>

<br><br>
When do we stop?
At a <b>base case </b>, or else you may face a <b>stack overflow error </b>.
<br>
Coming to a simple example of factorial of a number, we know that <br>
<code>5!= 5 * 4 * 3 * 2 * 1
4!= 4 * 3 * 2 * 1
5!= 5 * 4! or 
n! = n * (n-1)! or
factorial(n) = n * factorial(n-1)
</code>

<h4>What is the base case? When we do we stop finding factorial of a number?</h4>
When you reach 1.

```cpp
if(num==1){
        return 1;
    }
```

<img width="266" alt="image" src="https://github.com/user-attachments/assets/9d41d0cb-86ee-4d52-9110-8db2295488e2" /> ![image](https://github.com/user-attachments/assets/d1817e74-c282-4af7-9c61-c91bc3ad796c)

<b> Now do you see why the stack overflow occur may occur? This shows the need for a base condition. </b>
<br><br>
<h4>Can you model a similar base case and recursive case for Fiboncacci?</h4>

```cpp
Fib(n) = Fib(n-1) + Fib(n-2) -> recursive case
Fib(0)=0, Fib(1)=1 -> base case
```
<img width="599" alt="image" src="https://github.com/user-attachments/assets/2ad8816e-f56c-4cc9-b43e-cb2b98a80871" />
<br><br>
It's like a DFS traversal of this tree.
<br>
Try to code factorial and the Fibonacci series.

<h2>Recursion when there are "pending" statements</h2>

```cpp
#include <stdio.h>
  void display(int n)
  {
    if(n<1) return;
    else
      {
        printf("%d",n);
        display(n-1);
        printf("%d",n);
      }
  void main()
  {
    int n=3;
    display(3);
  }
}
```
![image](https://github.com/user-attachments/assets/970684e7-dfb7-47b0-9388-ccc3d4d05bd3)

Predict the output. 
    <details>
<summary>Show Answer</summary>
321123
</details>

