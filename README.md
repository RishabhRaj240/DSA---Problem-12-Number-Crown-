# Number Crown Pattern in C++

A beginner-friendly C++ program that demonstrates pattern printing using nested loops.

This project generates the **Number Crown Pattern**, where numbers increase from left to right, followed by spaces, and then decrease symmetrically. It is a popular pattern-printing problem from Striver's A2Z DSA Sheet and helps improve understanding of nested loops, spacing, and symmetry.

---

## 📌 Features

* Prints the Number Crown Pattern
* Uses nested `for` loops
* Demonstrates dynamic spacing and number sequences
* Beginner-friendly implementation
* Helps develop logical thinking and pattern recognition skills

---

## 🛠️ Technologies Used

* C++
* Standard Input/Output (`iostream`)

---

## 📂 Problem Statement

Given an integer `N`, print the Number Crown Pattern.

### Example

For:

```txt id="u6k8tw"
N = 5
```

Output:

```txt id="h2jhks"
1                 1
1 2             2 1
1 2 3         3 2 1
1 2 3 4     4 3 2 1
1 2 3 4 5 5 4 3 2 1
```

> **Note:** The spacing shown above is for illustration. The exact alignment depends on your console or editor font.

---

## 📸 Screenshot

<img width="1206" height="791" alt="Screenshot 2026-06-30 104025" src="https://github.com/user-attachments/assets/4da5f80e-675b-4456-b38b-8b08afc034b3" />

Example folder structure:

```txt id="n1atxt"
project-folder/
│
├── main.cpp
├── README.md
└── screenshots/
    └── output.png
```

---

## 💻 Source Code

```cpp id="6lvewy"
void numberCrown(int n) {

    int space = 2 * (n - 1);

    for (int i = 1; i <= n; i++) {

        // Left Numbers
        for (int j = 1; j <= i; j++) {
            cout << j << " ";
        }

        // Middle Spaces
        for (int j = 1; j <= space; j++) {
            cout << " ";
        }

        // Right Numbers
        for (int j = i; j >= 1; j--) {
            cout << j << " ";
        }

        cout << endl;

        space -= 2;
    }
}
```

---

## ▶️ How to Run

1. Compile the program:

```bash id="4ax0tt"
g++ main.cpp -o main
```

2. Run the executable:

```bash id="5zjlwm"
./main
```

3. Enter the value of `N`.

---

## 📸 Example Output

### Input

```txt id="x9gwxf"
4
```

### Output

```txt id="6g6nkl"
1           1
1 2       2 1
1 2 3   3 2 1
1 2 3 4 4 3 2 1
```

---

## 📖 Learning Concepts

This project helps beginners understand:

* Nested loops
* Pattern printing
* Number sequences
* Symmetric patterns
* Dynamic spacing
* Algorithmic thinking

---

## 🔍 Pattern Explanation

The pattern is built in three parts for every row:

### 1. Left Number Sequence

Prints numbers from `1` to the current row number.

```cpp id="g64gmb"
for (int j = 1; j <= i; j++)
```

### 2. Middle Spaces

Prints a decreasing number of spaces after each row.

```cpp id="yc1g5r"
space = 2 * (n - 1);
```

The value of `space` decreases by `2` after every iteration.

### 3. Right Number Sequence

Prints numbers in reverse order from the current row number back to `1`.

```cpp id="8n2upj"
for (int j = i; j >= 1; j--)
```

Combining these three sections creates the symmetric Number Crown Pattern.

---

## ⏱️ Complexity Analysis

### Time Complexity

```txt id="qnmj8w"
O(N²)
```

The nested loops execute approximately `N²` iterations.

### Space Complexity

```txt id="72otgk"
O(1)
```

Only a few integer variables are used.

---

## 👨‍💻 Author

Developed as a beginner-friendly C++ practice project for learning nested loops, pattern printing, and algorithmic problem-solving.
