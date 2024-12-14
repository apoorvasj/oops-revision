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






