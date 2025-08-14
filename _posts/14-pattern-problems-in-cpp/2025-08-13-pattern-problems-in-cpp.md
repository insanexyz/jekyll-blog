---
layout: post
title: Pattern problems in C++
date: 2025-08-13
categories: cpp patterns
author: insane
permalink: /posts/pattern-problems-in-cpp/
tags:
  - cpp
  - patterns
  - algorithms
  - dsa
  - post-14
---

![Thumbnail for the post](/assets/pattern-problems-in-cpp/thumbnail.webp)

<br>

Patterns problems in C++ archive here. I will probably keep on updating it as I solve more similar problems.

Problems found from YT videos, websites, or who knows from where. And yea I really did solve them instead of just copying. Pls trust. Pls. No lie me. Me good.

**Read it maybe?** : These are mostly solved just using for loops. Their are many ways to so solve one pattern, for example some will start i from 1 some from 0, some will use <= to end the loop while some <, some will use some other mathematical formula or view the pattern grid differently, etc. Some problems have more than one method to solve it, showcasing my 900+ IQ. Lol.

<br>

---

<br>

Pattern 1 -

```
* * * *
* * * *
* * * *
* * * *
```

```cpp
void print_pattern_01(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cout << "* ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 2 -

```
*
* *
* * *
* * * *
* * * * *
```

```cpp
void print_pattern_02(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i + 1; j++) {
            cout << "* ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 3 -

```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

```cpp
void print_pattern_03(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 1; j < i + 1; j++) {
            cout << j << " ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 4 -

```
1
2 2
3 3 3
4 4 4 4
5 5 5 5 5
```

```cpp
void print_pattern_04(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 1; j < i + 1; j++) {
            cout << i + 1  << " ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 5 -

```
* * * *
* * *
* *
*
```

```cpp
void print_pattern_05(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i; j++) {
            cout << "* ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

```
1 2 3 4 5
1 2 3 4
1 2 3
1 2
1
```

```cpp
void print_pattern_06(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 1; j < n + 1 - i; j++) {
            cout << j << " ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 7 -
```
    *
   ***
  *****
 *******
*********
```

```cpp
void print_pattern_07(int n) {
    for (int i = 0; i < n; i++) {
    
        // Prints first half
        //     *
        //    **
        //   ***
        //  ****
        // *****
        for (int j = 0; j < n; j++) {
            if (j < n - i - 1)
                cout << " ";
            else
                cout << "*";
        }
        
        // Prints second half -
        //
        //      *
        //      **
        //      ***
        //      ****
        for (int k = 0; k < i; k++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_07(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 8 -
```
*********
 *******
  *****
   ***
    *
```

```cpp
void print_pattern_08(int n) {
    for (int i = 0; i < n; i++) {
        // Prints first half -
        // *****
        //  ****
        //   ***
        //    **
        //     *
        for (int j = 0; j < n; j++) {
            if (j < i)
                cout << " ";
            else
                cout << "*";
        }
        
        // Prints second half -
        //      ****
        //      ***
        //      **
        //      *
        //
        for (int k = 0; k < n - i - 1; k++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_08(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i; j++) {
            cout << " ";
        }
        
        for (int j = 0; j < 2 * (n - i) - 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 9 -
```
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

```cpp
void print_pattern_09(int n)
{
    // For n = 5
    
    // Prints first part -
    //     *
    //    ***
    //   *****
    //  *******
    // *********
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    
    // Prints second half -
    // *******
    //  *****
    //   ***
    //    *
    for (int i = 1; i < n; i++) {
        for (int j = 0; j < i; j++) {
            cout << " ";
        }
        
        for (int j = 0; j < 2 * (n - i) - 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

```

<br>

---

<br>

Pattern 10 -
```
*
**
***
****
*****
****
***
**
*
```

```cpp
void print_pattern_10(int n) {
    // Considering n as till the row with maximum stars
    // Therefore n = 5

    // Prints first half -
    // *
    // **
    // ***
    // ****
    // *****
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }

    // Prints second half -
    // ****
    // ***
    // **
    // *
    for (int i = 1; i < n; i++) {
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_10(int n) {
    // Here we consider n = total number of rows
    // Therefore n = 9
    
    for (int i = 0; i < 2 * n - 1; i++) {
        int stars = i + 1;
        if (i > n - 1) stars = ((2 * n) - (i + 1));
        for (int j = 0; j < stars; j++) {
            cout << "*";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 11 -
```
1
0 1
1 0 1
0 1 0 1
1 0 1 0 1
```

```cpp
void print_pattern_11(int n) {
    short flip = 1;
    for (int i = 0; i < n; i++) {
        if (i % 2 == 0) flip = 1;
        else flip = 0;
        for (int j = 0; j < i + 1; j++) {
            cout << flip << " ";
            flip = 1 - flip;
        }
        cout << endl;
    }
}

```

<br>

---

<br>

Pattern 12 -
```
1        1
12      21
123    321
1234  4321
1234554321
```

```cpp
void print_pattern_12(int n) {
    for (int i = 0; i < n; i++) {
        // first half
        for (int j = 0; j < i + 1; j++) {
            cout << j + 1;
        }
        
        // spaces
        for (int j = 0; j < 2 * (n - i - 1); j++) {
            cout << " ";
        }
        
        // second half
        for (int j = i + 1; j > 0; j--) {
            cout << j;
        }
        
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 13 -
```
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

```cpp
void print_pattern_13(int n) {
    int x = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i + 1; j++) {
            cout << x++ << " ";
        }
        cout << endl;
    }
}

```

<br>

---

<br>

Pattern 14 -
```
A
AB
ABC
ABCD
ABCDE
```

```cpp
void print_pattern_14(int n) {
    for (int i = 0; i < n; i++) {
        char x = 'A';
        for (int j = 0; j < i + 1; j++) {
            cout << x;
            x = x + 1;
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_14(int n) {
    for (char i = 'A'; i < 'A' + n; i++) {
        for (char j = 'A'; j < i + 1; j++) {
            cout << j;
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_14(int n) {
    for (int i = 0; i < n; i++) {
        for (char j = 'A'; j < 'A' + i + 1; j++) {
            cout << j;
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 15 -
```
ABCDE
ABCD
ABC
AB
A
```

```cpp
void print_pattern_15(int n) {
    for (int i = 0; i < n; i++) {
        char x = 'A';
        for (int j = 0; j < n - i; j++) {
            cout << x;
            x = x + 1;
        }
        cout << endl;
    }
}
```

```cpp
void print_pattern_15(int n) {
    for (int i = 0; i < n; i++) {
        for (char j = 'A'; j < 'A' + (n - i); j++) {
            cout << j;
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 16 -
```
A
BB
CCC
DDDD
EEEEE
```

```cpp
void print_pattern_16(int n) {
    char ch = 'A';
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i + 1; j++) {
            cout << ch;
        }
        ch++;
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 17 -
```
   A
  ABA
 ABCBA
ABCDCBA
```

```cpp
void print_pattern_17(int n) {
    for (int i = 0; i < n; i++) {
        // space
        for (int j = 0; j < (n - i - 1); j++) {
            cout << ' ';
        }
        
        // chars
        char ch = 'A';
        for (int j = 0; j < i + 1; j++) {
            cout << ch++;
        }
        
        ch = ch - 2;
        for (int j = 0; j < i; j++) {
            cout << ch--;
        }
        
        cout << endl;
    }
    // No need to print the end spaces for each row.
    // Save computation yay!
}

```

```cpp
void print_pattern_17(int n) {
    for (int i = 0; i < n; i++) {
        // space
        for (int j = 0; j < (n - i - 1); j++) {
            cout << ' ';
        }
        
        // chars
        char ch = 'A';
        for (int j = 0; j < 2 * i + 1; j++) {
            if (j < i) {
                cout << ch++;
            } else {
                cout <<  ch--;
            }
        }
        
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 18 -
```
E
D E
C D E
B C D E
A B C D E
```

```cpp
void print_pattern_18(int n) {
    char ch = 'E';
    for (int i = 0; i < n; i++) {
        char start_char = ch;
        for (int j = 0; j < i + 1; j++) {
            cout << ch++ << " ";
        }
        ch = start_char - 1;
        cout << endl;
    }
}

```

```cpp
void print_pattern_18(int n) {
    for (int i = 0; i < n; i++) {
        for (char ch = 'E' - i; ch < 'E' + 1; ch++) {
            cout << ch << " ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 19 -
```
**********
****  ****
***    ***
**      **
*        *
*        *
**      **
***    ***
****  ****
**********
```

**An attempt to explain my approach to solve these problems through this pattern 19**

Method 1 approach -

Idea is to first divide entire pattern into two halves A and B -
![Pattern problems in C++ illustration for pattern 19 method 1](/assets/pattern-problems-in-cpp/first-half-second-half.webp)

Then subdivide the halves A and B into its quadrants (I, II, III, IV) -
![Pattern problems in C++ illustration for pattern 19 method 1](/assets/pattern-problems-in-cpp/quadrants.webp)

Take half A and print its two quadrants (I and II) lines simultaneously -
![Pattern problems in C++ illustration for pattern 19 method 1](/assets/pattern-problems-in-cpp/print-simul.webp)

For this just write the code to print pattern in quadrant II, then write the code to print pattern in quadrant I and then put a ``cout << endl`` in the end.

Do the same for second half B.

```cpp

void print_pattern_19(int n) {

    // First half
    for (int i = 0; i < n; i++) {
    
        /////////////////////
        // Second quadrant //
        /////////////////////
        // stars
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        // spaces
        for (int j = 0; j < i; j++) {
            cout << " ";
        }
        
        ////////////////////
        // First quadrant //
        ////////////////////
        // spaces
        for (int j = 0; j < i; j++) {
            cout << " ";
        }
        
        // stars
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
    
    // Second half
    for (int i = 0; i < n; i++) {
    
        ////////////////////
        // Third quadrant //
        ////////////////////
        
        // stars
        for (int j = 0; j < i + 1; j++) {
            cout << "*";
        }
        
        // spaces
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        
        /////////////////////
        // Fourth quadrant //
        /////////////////////
        
        // spaces
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        
        // stars
        for (int j = 0; j < i + 1; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
}
```

<br>

Method 2 approach -

Divide the pattern into two halves A and B -
![Pattern problems in C++ illustration for pattern 19 method 2](/assets/pattern-problems-in-cpp/first-half-second-half-02.webp)

See the following pattern and then simply write the code for stars, then spaces and then again stars for both halves (first half shown here)
![Pattern problems in C++ illustration for pattern 19 method 2](/assets/pattern-problems-in-cpp/method-02.webp)

Another way to visualize (left side is code from method 1 and right side is code from method 2) -
![Pattern problems in C++ illustration for pattern 19 method 2](/assets/pattern-problems-in-cpp/first-half-spaces-combined.webp) 

![Pattern problems in C++ illustration for pattern 19 method 2](/assets/pattern-problems-in-cpp/second-half-spaces-combined.webp)

See how ``j < i condition was written two times in half A`` which got combined to ``j < 2 * i``. Same for half B.

```cpp
void print_pattern_19(int n) {
    // First half
    for (int i = 0; i < n; i++) {
        // stars
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        // spaces
        for (int j = 0; j < 2*i; j++) {
            cout << " ";
        }
        
        // stars
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
    
    // Second half
    for (int i = 0; i < n; i++) {
        // stars
        for (int j = 0; j < i + 1; j++) {
             cout << "*";
        }
        
        // spaces
        for (int j = 0; j < 2 * (n - i - 1); j++) {
            cout << " ";
        }
        
        // stars
        for (int j = 0; j < i + 1; j++) {
             cout << "*";
        }
        
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 20 -
```
*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *
```

```cpp

void print_pattern_20(int n) {
    // First half
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < i + 1; j++) {
            cout << "*";
        }
        
        for (int j = 0; j < 2 * (n - i - 1); j++) {
            cout << " ";
        }
        
        for (int j = 0; j < i + 1; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
    
    // Second half
    // i = 1 so we can skip i = 0 line printing twice
    for (int i = 1; i < n; i++) {
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        for (int j = 0; j < 2 * i; j++) {
            cout << " ";
        }
        
        for (int j = 0; j < n - i; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
}
```

```cpp
void print_pattern_20(int n) {
    int spaces = 2 * n;
    int stars = 0;
    for (int i = 0; i < 2 * n - 1; i++) {
    
        if (i >= n) {
            stars = 2 * n - i - 1;
            spaces += 2;
        } else {
            stars = i + 1;
            spaces -= 2;
        }
        
        // Stars
        for (int j = 0; j < stars; j++) {
            cout << "*";
        }
        
        // Spaces
        for (int j = 0; j < spaces; j++) {
            cout << " ";
        }
        
        // Stars
        for (int j = 0; j < stars; j++) {
            cout << "*";
        }
        
        cout << endl;
    }
}

```

<br>

---

<br>

Pattern 21 -
```
* * * * *
*       *
*       *
*       *
* * * * *
```

```cpp
void print_pattern_21(int n) {
    for (int i = 0; i < n; i++) {
        // First and last row
        if ((i == 0) || (i == n - 1)) {
            for (int j = 0; j < n; j++) {
                cout << "* ";
            }
            cout << endl;
        } else {
            cout << "* ";
            for (int j = 0; j < n - 2; j++) {
                cout << "  ";
            }
            cout << "*" << endl;
        }
    }
}
```

```cpp
void print_pattern_21(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            // Fill with stars only if i or j is in boundary
            if (i == 0 || i == n - 1 || j == 0 || j == n - 1) {
                cout << "* ";
            } else {
                cout << "  ";
            }
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 22 -
```
5 5 5 5 5 5 5 5 5
5 4 4 4 4 4 4 4 5
5 4 3 3 3 3 3 4 5
5 4 3 2 2 2 3 4 5
5 4 3 2 1 2 3 4 5
5 4 3 2 2 2 3 4 5
5 4 3 3 3 3 3 4 5
5 4 4 4 4 4 4 4 5
5 5 5 5 5 5 5 5 5
```

```cpp
void print_pattern_22(int n) {
    for (int i = 0; i < 2 * n - 1; i++) {
        for (int j = 0; j < 2 * n - 1; j++) {
            // Calculate distances
            int top_dist = i;
            int bottom_dist = (2 * n - 1) - i - 1;
            int left_dist = j;
            int right_dist = (2 * n  - 1) - j - 1;
            
            // For
            // n = 2 -> max dist - 0
            // n = 3 -> max dist - 1
            // n = 4 -> max dist - 2
            // n = 5 -> max dist - 3
            // n = n -> max dist - (n - 2)
            cout << max(max(top_dist, bottom_dist), max(left_dist, right_dist)) - (n - 2) << " ";
        }
        cout << endl;
    }
}
```

<br>

---

<br>

Pattern 23 -
```
    *
   * *
  * * *
 * * * *
* * * * *
```

```cpp
void print_pattern_23(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (j < n - i - 1)
                cout << " ";
            else
                cout << "* ";
        }
        cout << endl;
    }
}
```