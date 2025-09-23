1. Odd or Even
```
	public static boolean oddOrEven(int n) {
	return n % 2 == 0 ? even : odd;
}
```

2. Count digits in a number

```
	public static int countDigits(int n) {
		int count = 0;
		while(n > 0) {
			n 
		}
	}
```

3. pyramid Pattern:
```
 public static void pyramidPattern(int n) {  
    for(int i = 1; i <= n; i++) {  
        for(int j = 0; j < i; j++) {  
            System.out.print(j+1 + " ");  // System.out.print("* ")
        }  
        System.out.println();  
    }  
}
```

```
Output:
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5 
```

- You can change the sout line to print star also

4. Box Pattern

```
public static void boxPattern(int n) {  
    for(int i = 0; i < n; i++) {  
  
        for(int j = 0; j < n; j++) {  
            if(i==0 || j == 0 || i == n -1 || j == n-1) {  
                System.out.print("* ");  
            }  
            else {  
                System.out.print("  ");  
            }  
  
        }  
        System.out.println();  
    }  
}
```

```
Output:
* * * * * 
*       * 
*       * 
*       * 
* * * * * 
 
```

5. Reverse Pyramid Pattern Right

```
public static void reversePyramidPatternRight(int n) {  
    for(int i = 1; i <= n; i++) {  
        for(int j = n; j >= i; j--) {  
            System.out.print(j + " ");  
        }  
        System.out.println();  
    }  
}
```

```
Output:
5 4 3 2 1 
5 4 3 2 
5 4 3 
5 4 
5
```

6. Reverse Number
```
public static int reverseNumber(int n) {  
    int rev = 0;  
    while (n > 0) {  
        int rem = n % 10;  
        n = n / 10;  
        rev = (rev * 10) + rem;  
    }  
    return rev;  
}
```

7. Palindrome Number

```
public static String isPalindrome(int n) {  
    int rev = 0;  
    int temp = n;  
    while (temp > 0) {  
        int rem = temp % 10;  
        temp = temp / 10;  
        rev = (rev * 10) + rem;  
    }  
    System.out.println("Reverse: " + rev);  
    System.out.println("Original: " + n);  
    return rev == n ? "Palindrome Number" : "Not a Palindrome Number";  
}
```

```
Output:

Reverse: 27829
Original: 92872
Not a Palindrome Number
```

8. Sum Of Digits
```
public static int sumOfDigits(int n) {  
    int count = 0;  
    while(n > 0) {  
        n = n / 10;  
        count++;  
    }  
    return count;  
}
```

9. Armstrong Number
     ##### Convert to String and do the work
```
public static boolean isArmstrong(int n) {  
    String str = String.valueOf(n);  
    int armstrong = 0;  
    int count = 0;  
    int temp = n;  
    while(temp > 0) {  
        temp = temp / 10;  
        count++;  
    }  
    for(int i = 0; i < str.length(); i++) {  
        armstrong += (int) Math.pow(Integer.parseInt(String.valueOf(str.charAt(i))),count);  
    }  
    return n == armstrong;  
}
```
##### Use reverse number + sum of digit logic
```
public static boolean isArmstrong(int n) {  
    int count = 0;  
    int res = 0;  
    int temp = n;  
    while(temp > 0) {  
        temp = temp / 10;  
        count++;  
    }  
    temp = n;  
    while (temp > 0) {  
        int rem = temp % 10;  
        res  += (int) Math.pow(rem,count);  
        temp = temp / 10;  
    }  
    return res == n;  
}
```
10. Fibonacci
```
public static void fibonacci(int n) {  
    int n1 = 0;  
    int n2 = 1;  
    if (n >= 1) System.out.print(n1 + " ");  
    if (n >= 2) System.out.print(n2 + " ");  
    for(int i = 3; i <= n; i++) {  
        int n3 = n1+n2;  
        System.out.print( n3 + " ");  
        n1 = n2;  
        n2 = n3;  
    }  
}
```

```
Output:
fibonacci(5) → 0 1 1 2 3
```
