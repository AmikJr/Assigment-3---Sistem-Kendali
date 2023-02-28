import numpy as np

def value_polynomial():
    n = int(input("Input value of a polynomial (degree): "))
    coeffs = []
    for i in range(n, -1, -1):
        coeff = float(input(f"Input the coefficient of x^{i}: "))
        coeffs.append(coeff)
    return coeffs

def routh(coeffs, K):
    n = len(coeffs)
    M = np.zeros((n+1, n//2+1))
    if n % 2 == 0:
        M[0][0], M[0][1] = coeffs[0], coeffs[2]
        M[1][0], M[1][1] = coeffs[1], coeffs[3]
        coeffs = coeffs[4:]
    else:
        M[0][0] = coeffs[0]
        M[1][0] = coeffs[1]
        coeffs = coeffs[2:]
    for i in range(2, n+1):
        j = 0
        for k in range(0, n-i+1, 2):
            try:
                a = M[i-2][j+1] * M[i-1][j]
                b = M[i-2][j] * M[i-1][j+1]
                c = M[i-1][j] * K
                M[i][j] = (c - a) / b
            except ZeroDivisionError:
                M[i][j] = 0.0001
            j += 1
    return M

def check_stability(table):
    num_sign_changes = 0
    for i in range(table.shape[0]-1):
        if np.sign(table[i, 0]) != np.sign(table[i+1, 0]):
            num_sign_changes += 1
    return num_sign_changes

def print_routh(table):
    for i in range(table.shape[0]):
        for j in range(table.shape[1]):
            if table[i, j] != 0:
                print(table[i, j], end="\t")
            else:
                print("0.0001", end="\t")
        print()

# Get the polynomial coefficients from the user
coeffs = value_polynomial()

# Get the value of K from the user
K = float(input("Input value of K: "))

# Calculate the Routh table
table = routh(coeffs, K)

# Print the Routh table
print("Routh :")
print_routh(table)

# Check the stability of the system
num_sign_changes = check_stability(table)
if num_sign_changes == 0:
    print("System is stable")
else:
    print(f"System is unstable. Number of sign changes = {num_sign_changes}")
