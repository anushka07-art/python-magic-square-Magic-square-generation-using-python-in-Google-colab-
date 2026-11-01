# python-magic-square-Magic-square-generation-using-python-in-Google-colab-

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