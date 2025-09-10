# python-ai-basic-training
This is basic training progam

31-08-2025:
============================

# Data structure 

# List : it is ordered ,mutable,allows duplicates

# Example :

# Storing students' scores
list_scores=[20,30,40,50]

# access

print(f"First Element {list_scores[0]}") # first element 20 
print(f"Last Element {list_scores[-1]}")  # 50 (last element)

# Update
list_scores.append(10)

print(f"Add at the end {list_scores}")

# Insert at index

list_scores.insert(0,5)

print(f"Add at the beginning {list_scores}")


# Remove element
list_scores.remove(30) 

print(f"it removes 30 from the list : {list_scores}")  # [5,20,40,50,10]

# Pop last element
list_scores.pop()  # removes 10

print(f"it removes last element in the list {list_scores}")# [5,20,40,50]


# Slice
slice_list=list_scores[1:3] # [5,20,40,50]

print(f"it slice the list {slice_list}")# [20,40]


# Practice 

list = [1, -2, 3, -4, 5, -6]

list.sort()

print(f" the re arranged list : {list}")

##########
list = [1, -2, 3, -4, 5, -6]
nl=[]
pl=[]
l=[]
for n in list:
    if n < 0:
        nl.append(n)
    else:
        pl.append(n)

res=nl+pl
print(f" the final list : {res}")

Day-2 : 01-09-2025
===============================================================

# reverse list

num=[10,30,2,4,5,90]

reverse=num[::-1]
print(f"original list  {num}")
print(f"reverse list  {reverse}")


# find the second largest number 
l=[10,30,2,4,5,90]
f=s=0
for n in l:
    if n>f: # 10>0
        s=f  # this swapping is important here 
        f=n
    elif n>s :
        s=n   
print(f"the first ax number is {f}") 
print(f"the second max number is {s}")  


# Tuple 
#prepare 

# A tuple is like a list, but immutable (cannot be changed after creation).

# Think of it as a read-only list.
# Examples
 
t = (1, 2, 3, 4)
print(t[0]) 
print(type(t))


t1 = (1, 2, 3)
t2 = 1, 2, 3   # without brackets
t3 = (5,) 

print(f"General syntax (1, 2, 3) : {t1}") 

print(f" syntax 1,2,3 : {t2}") 

print(f" dfferent (5,): {t3}")

# Packing 

person = ("John", 25, "Developer")  # packing

name,age,desi=person

print(f" Name  : {name}") 

print(f" Age: {age}")

print(f" designation : {desi}")

Day-3 02-09-2025
======================================================

# Tuple practice 

# we can return multiple values

def arithameticOperations(a,b):
    return a+b,a-b,a*b

sum,sub,mul=arithameticOperations(10,10)

print(f" add ,sub,mul:{sum},{sub},{mul}")

# Nested tuples 

matrix = ((1,2), (3,4), (5,6))
print(matrix[1][0]) # 3
print(matrix[0][0]) # 1
print(matrix[2][1]) # 6

# tuple functions -> len(),max(),min(),count(),index()

t = (1, 2, 2, 3, 4, 2,7,9)

print(f"length :{len(t)}") # 8

print(f" mix number :{max(t)}") # 9

print(f" min number :{min(t)}") # 1

print(f" min number :{t.count(2)}") # 3

print(f" index :{t.index(9)}") # 7

# store multiple objects 

t = (1, [2,3], 4,{'name':'masthan'})
t[1][0] = 99
print(t)   # (1, [99, 3], 4,{'name': 'masthan'})

# Tuple as Dictionary key

locations = {
    (17.385, 78.486): "Hyderabad",
    (28.704, 77.102): "Delhi"
}
print(locations[(17.385, 78.486)])  # Hyderabad


for cordi,city in locations.items():
    print(f"the cordinates: {cordi} and city :{city}")
    
Day -4 : 09-09-2025
============================================
#Set

#Unique elements, no duplicates

#Good for membership tests, mathematical set ops

list1 = [1, 2, 3, 4, 5, 6]
list2 = [4, 5, 6, 7, 8, 9]

common_elements= set(list1) & set(list2) # & 

print(f"common elements :{common_elements}")

# Remove Duplicates from a List

nums = [1, 2, 2, 3, 4, 4, 5]

uniquevales=set(nums)

uniquevalist=list(set(nums))

print(f"unique elements :{uniquevales}")

print(f"unique elements list:{uniquevalist}")

#Find Elements in List1 but not in List2 

a = [10, 20, 30, 40]
b = [30, 40, 50]

resul=set(a) - set(b)

print(f"list1 elements not in list 2 :{resul}")

# Check If Two Strings are Anagrams Using Sets

s1 = "listen"
s2 = "silent1"

is_anagram= set(s1) == set(s2)

print(f"anagram  :{is_anagram}")

# Count Unique Vowels in a String

text = "programming in python"
vowels = set("aeiou")

found = set(text) & vowels
print("Unique vowels found:", found)

Day 5: 10-09-2025
==========================================

What is NumPy?

NumPy (Numerical Python) is a Python library for working with numerical data.

It provides:

Multi-dimensional arrays (ndarray) → much faster than Python lists.

Mathematical functions to operate on arrays.

Linear algebra, statistics, random numbers → backbone of AI/ML.

👉 In short: Python lists = general purpose, NumPy arrays = scientific computing.

Why is NumPy Important?

Performance → NumPy is written in C under the hood, so operations are 50x–100x faster than normal Python loops.

Foundation of AI/ML → Libraries like Pandas, TensorFlow, PyTorch, Scikit-learn are built on top of NumPy.

Vectorized Operations → Instead of looping element by element, NumPy applies operations to the whole array at once (SIMD).

Memory Efficient → Stores elements in a compact format compared to Python lists.

Where is NumPy Used? (Potential Usages)

✅ 1. Data Analysis / Data Science

Handling large datasets efficiently.

Example: Stock prices, sensor data, customer behavior.

✅ 2. Machine Learning & Deep Learning

Representing feature matrices, training data, and weights of neural networks.

✅ 3. Image Processing

Images are just arrays of pixels (RGB values). NumPy handles them easily.

✅ 4. Scientific Computing

Physics simulations, weather prediction, genetics, astronomy → heavy on matrix computations.

✅ 5. Finance

Risk analysis, Monte Carlo simulations (randomness in predictions).    


