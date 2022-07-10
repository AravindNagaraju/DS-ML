1.   
```
int a = 0, b = 0;
for (i = 0; i < N; i++) {  
a = a + rand();  
}  
for (j = 0; j < M; j++) {  
b = b + rand();  
}
```

Time Complexity: $O(N) + O(M)$  
Note: The for loops are executing one after the other and both are of order $N$ and $M$ respectively.  
  
  
2.  
``` 
int a = 0;
for (i = 0; i < N; i++) {
for (j = N; j > i; j--) {
a = a + i + j;
}
}
```

Time Complexity: $O(n^2)$  
Note: Nested loop. The first loop's complexity is $O(N)$. But the second `for` loop's runs $N$ times in the first iteration and the order decrements by 1 in each of the consecutive iterations.


3.   
```
int i, j, k = 0;
for (i = n / 2; i <= n; i++) {
for (j = 2; j <= n; j = j * 2) {
k = k + n / 2;
}
}
```

Time Complexity: $O(n * log(n))$  
Note: First `for` loop will have $O(n/2)$ and second loop has $O(logn)$ since increment is multiple of 2.


4.   
```
int a = 0, i = N;
while (i > 0) {
a += i;
i /= 2;
}
```

Time Complexity: $O(log(n))$  
Note: $N$ becomes $N/2$ in the next step and so on and so forth. 


5. 
```
for(var i=0;i<n;i++)
i*=k
```

Time Complexity: $O(logn)$  
Note: Each time, $i$ is being multiplied with $k$. $i$ approaches $n$ faster.


6.  
```
def fun(n):
if (n < 5):
print("GeeksforGeeks", end ="")
else:
for i in range(n):
print(i, end= " ")
```

Time Complexity: $O(n)$  
Note: only if `n < 5`, then $O(1)$. Else order will be $n$ 


7.  
```
def fun(a, b):
while (a != b):
if (a > b):
a = a - b
else:
b = b - a
```

Time Complexity: $O(1)$  
Note: since $a$ and $b$ will be defined in the function, and the program first checks if $a$ is not equal to $b$.


8. 
```
void fun(int n)
{
for(int i=0;i*i<n;i++)
cout<<"GeeksforGeeks";
}
```

Time Complexity: $O(\sqrt(n))$  
Note: Though $i$ is starting at 0 and increment is 1, condition is $i^2 < n$, $i^2 = n$ implies order will be $sqrt(n)$.


9.  
```
void fun(int n, int x)
{
for (int i = 1; i < n; i = i * x) //or for(int i = n; i >=1; i = i / x)
cout << "GeeksforGeeks";
}
```

Time Complexity: $O(log(n))$  
Note: Increment is $i*x$


10.  
```
void fun(int n)
{
for (int i = 0; i < n / 2; i++)
for (int j = 1; j + n / 2 <= n; j++)
for (int k = 1; k <= n; k = k * 2)
cout << "GeeksforGeeks";
}
```

Time Complexity: $O(n^2 log(n))$    
Note: First loop will have order $n$, second loop will have order $n$, since incerment is 1; third loop will have order $log(n)$ since increment is $k*2$


11.  
```
void fun(int n)
{
int i = 1;
while (i < n) {
int j = n;
while (j > 0) {
j = j / 2;
}
i = i * 2;
}
}
```

Time Complexity: $O(2 log(n))$  
Note: $i$ is incrementing by $i*2$ and approaching $n$ and $j$ is dencrementing by $j/2$ and approaching 0. And since this is a nested loop, $log(n) + log(n)$

