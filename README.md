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
