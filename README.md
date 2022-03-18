count = 0
for i in range(1, 10):
    if i % 2 != 0:
        count += 1
        print(i)
print(f"we have {count} even number")
#-----------------------------------------------

def greet(firstName, lastName):
    print(f"Hi {firstName} {lastName}")


greet("Alex", "Kavanagh")


def calculator(x, y):
    return x + y


# x = input("x:")

# y = input("y:")


total = calculator(2, 1)
print(total)

#------------------------------------
# Fizz Buzz


def fizz_buzz(input):
    if input % 3 == 0 and input % 5 == 0:
        return "FizzBuzz"
    if input % 3 == 0:
        return "Fizz"
    if input % 5 == 0:
        return "Buzz"
    return input


val = " "
while val:
    val = input("Enter number: ")
    if val.lower() == "quit":
        break
    print(fizz_buzz(int(val)))


import requests
from time import ctime
from pathlib import Path
from collections import namedtuple
from collections import deque
from email.policy import default
import numbers
from pyclbr import Class
import queue
from timeit import timeit
from unittest import result
letters = ["a", "b", "c"]

# ADD into a List
letters.append("d") #add at the end of a list
letters.insert(0, "-")  # add at the end of a list

# Remove into a List
letters.pop() #remove last element in a list
letters.pop(1) #remove specific element in a list
del letters[0:2]# delete range of letter
letters.clear() # clear all elements in a list


print(letters.index("c")) #print index of specific element
print(letters.count("c")) # print how many C are in the list

# Start
items = [
    ("Product1", 10),
    ("Product2", 9),
    ("Product3", 12),
]


# def sort_item(item):
#     return item[1]


# items.sort(key=sort_item, reverse=True)
# print(items)


# numbers = [3, 51, 2, 8, 6]
# print(sorted(numbers))


# sort using lambda function
# lamba you do not need to use
# a function   such as : def


# items.sort(key=lambda item: item[1])
# print(items)

# x = list(map(lambda item: item[1], items))
# print(sorted(x))


# filter a list
items = [
    ("Product1", 10),
    ("Product2", 9),
    ("Product3", 12),
]


# x = list(filter(lambda item: item[1] >= 10, items))
# print(x)


# list comprehension
# this is to map through an list
# prices = [items[1] for item in items]
# print(prices)

# this is to filter through a list
# prices = [item for item in items if item[1] >= 10]
# print(prices)


# zip
# zip allow to
list1 = [1, 2, 3]
list2 = [10, 20, 30]


#print(list(zip(list1, list2)))
# result will be [(1, 10), (2, 20), (3, 30)]


# queues first in and first out

# queue = deque([])
# queue.append(1)
# queue.append(2)
# queue.append(3)
# queue.append(4)
# queue.popleft()  # poplest for deque
# print(queue)
# if not queue:
#     print("Empty")


# tuples
# tuples cannot be modified

# (1,2,3) this is an example fo tuple
# to convert a list to tuple tuple([1,2,3])
# list3 = []
# x = tuple(list1)
# print(x[:2])
# using tuple we can swap item easily

# x = 10
# y = 11


# y, x = (x, y)
# print(f"x:{x} y:{y}")


# set
# does not support index arr[3]
# you need to convert it to a list
# set is used for unique number
# list = [1, 1, 3, 4, 6, 6, 3]
# unique = set(list)
# #{1, 3, 4, 6}

# second = {1, 4}
# second.add(5)
# second.remove(1)
# length = len(second)
# print(length)
# # union of two set
# print(unique | second)
# #{1, 3, 4, 5, 6}
# print(unique & second)
# # {4} exist in both set
# print(unique - second)
# # {1, 3, 6} this is the difference
# print(unique ^ second)
# # print that are not in both
# #{1, 3, 5, 6}


# Dictionnaires
# collection of key value pair


# point = dict(x=1, y=2)
# point["x"] = 10
# del point["x"]
# point["z"] = 3
# point["w"] = 4
# print(point)

# for key, value in point.items():
#     print(key, value)
#     print(key+str(value))

# sentence = "this is a common interview question"

# unique = set(sentence)
# #new_sentence = [character for character in sentence]
# dictionary = {}
# for char in unique:
#     if char != " ":
#         dictionary[char] = sentence.count(char)

# #result = sorted(dictionary.items(), key=lambda x: x[1], reverse=True)
# result = sorted(dictionary.items(), key=lambda x: x[1])
# print(result[0])


# ----------------------------------------------------------
# Exception


# numbers = [1, 2]
# print(numbers[3])

# try:
#     file = open(app.py)  # open a file
#     age = int(input("age:"))
#     xfactor = 10/age
# except (ValueError, ZeroDivisionError):
#     print("you did not enter a valid age ")
# finally:
#     file.close()  # close a file


# code1 = """
# def calculateX(age):
#     if age <= 0:
#         return None
#     return 10/age


# val=calculateX(-1)
# if val==None:
#     pass
# """
# print("code= ", timeit(code1, number=10000))

# ------------------------------------------------------
#                          Classes
#        it is a blueprint to create new object

# objects is a instance of a class

# example:    class:Human     objects: John,Mary, Jack


class Point:
    default_color = "red"  # class default attribute

    def __init__(self, x, y):  # this is a constructor
        self.x = x
        self.y = y

    # def __add__(self, other):   #to combined point and other
    #     return (self.x + other.x, self.y+other.y)
        # def __eq__(self, other):  #equal
        #     return self.x == other.x and self.y == other.y

        # def draw(self):
        #     print(f" point {self.x}  , {self.y}")


# point = Point(1, 2)  # this is an instance of Point
# other = Point(1, 2)
# combined = point+other
# # point.draw()
# print(combined)


# -----------------------------------------------------------------------------------
        # inheritance
        # inherit from the from the parent
        # prevent duplicate code
# class Animal:\
#     def __init__(self):
#         self.age = 1

#     def eat(self):
#         print("eat")


# class mammal(Animal):  # mammal inerhit from animal

#     def __init__(self):
#         super().__init__()  # without the init it is a method overriding
#         self.weight = 2

#     def walk(self):
#         print("walk")


# class Fish(Animal):
#     def swim(self):
#         print("swim")


# m = mammal()
# s = m.weight
# print(s)


# -------------------------------
#              namedtuple
# once create we cannot modified


# Point = namedtuple("Point", ['x', 'y'])
# p1 = Point[1, 2]  # that is  the only add an element into a namedtuplet
# p2 = Point[2, 2]
# print(p1 == p2)  # only equal  not less ot greater or less or equal


# -------------------------------------
#               create a module
# module is some file that  contain some python code
# inside  a module  we can have a class  and function


# ----------------------------------------
#               python Standard library


response = requests.get("http://google.com")

print(response)
