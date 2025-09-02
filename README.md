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


