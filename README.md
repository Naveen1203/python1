# python1
# Nested Lists

# Given the names and grades for each student in a Physics class of  students, store them in a nested list and print the name(s) of any
# student(s) having the second lowest grade.

# Note: If there are multiple students with the same grade, order their names alphabetically and print each name on a new line.

# Input Format
# The first line contains an integer, N, the number of students. 
# The 2N subsequent lines describe each student over 2 lines; the first line contains a student's name, and the second line contains
# their grade.

# Constraints
# 2 <= N <= 5
# There will always be one or more students having the second lowest grade.

# Output Format
# Print the name(s) of any student(s) having the second lowest grade in Physics; if there are multiple students, order their names
# alphabetically and print each one on a new line.
#####################################
if __name__ == '__main__':
    num = []
    arr =[]
    for _ in range(int(input())):
        name = input()
        score = float(input())
        arr.append([name,score])
        num.append(score)
        
    x = sorted(arr)
    y = sorted(list(set(num)))

    for i in x:
        if i[1] == y[1]:
            print (i[0])
