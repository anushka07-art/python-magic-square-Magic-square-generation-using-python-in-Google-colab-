# python-magic-square-Magic-square-generation-using-python-in-Google-colab-

Magic Square Generation Using Python

About the Project

This project generates a magic square using Python. A magic square is a square matrix in which the sum of every row, column, and main diagonal is equal.

Objective

To generate an odd-order magic square using a Python program.

Technology Used

- Python
- Google Colab

code 

n = int(input("Enter an odd number: "))

magic = [[0 for i in range(n)] for j in range(n)]

i = 0
j = n // 2

for num in range(1, n * n + 1):
    magic[i][j] = num

    new_i = (i - 1) % n
    new_j = (j + 1) % n

    if magic[new_i][new_j] != 0:
        i = (i + 1) % n
    else:
        i = new_i
        j = new_j

print("Magic Square:")

for row in magic:
    print(row)

Example Output

For a 3 × 3 magic square:

8 1 6
3 5 7
4 9 2

The sum of each row, column, and main diagonal is 15.

Conclusion

This project demonstrates the use of lists, loops, and conditional statements in Python.