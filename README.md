# Masters_Datascience_Assiagnment-4
Masters_Datascience_Assiagnment-4

#1) 1.1 Write a Python Program (with class concepts) to find the area of the triangle using the below formula.area = (s*(s-a)*(s-b)*(s-c)) ** 0.5 Function to take the length of the sides of triangle from user should be defined in the parent class and function to calculate the area should be defined in subclass.

class Shape:
    def __init__(self, sides):
        self.n = sides
        self.listsides = [0 for i in range(sides)]

    def readSides(self):
        self.listsides = [float(input("Enter side "+str(i+1)+" : ")) for i in range(self.n)]

class Triangle(Shape):
    def __init__(self):
        Shape.__init__(self,3)

    def findAreaTriangle(self): 
        a, b, c = self.listsides
        s = (a + b + c) / 2     
        area = (s*(s-a)*(s-b)*(s-c)) ** 0.5
        print('The area of the triangle is %0.2f' %area)

t = Triangle()
t.readSides()
t.findAreaTriangle()

#1) 1.2 Write a function filter_long_words() that takes a list of words and an integer n and returns the list of words that are longer than n.

def filter_long_words(liststr,n):
    new_list=[]
    for str in liststr:
        if len(str)>n:
            new_list.append(str)
    return new_list

words = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday"]
long_words = filter_long_words(words,6)
print(long_words)

#2) 2.1 Write a Python program using function concept that maps list of words into a list of integers representing the lengths of the corresponding words.

def lenstr(str):
    return len(str)

x_len = map(lenstr, ("Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday")) #mapping words to lengths

print(x_len)

print(list(x_len))

#2) 2.2 Write a Python function which takes a character (i.e. a string of length 1) and returns True if it is a vowel, False otherwise.
def isvowelchar(ch):
    if ch in('a','e','i','o','u'):
        return True
    else:
        return False

print(isvowelchar('p'))
print(isvowelchar('a'))

