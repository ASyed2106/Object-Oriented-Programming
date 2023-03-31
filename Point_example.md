``` python
# on point.py

class Point:
    def __init__(self,x,y):
        self.x=x
        self.y=y
    def distance(self,other_point):
        #we assume other_point is a Point() object 
        diff_x=(self.x- other_point.x) ** 2
        diff_y=(self.y-other_point.y)**2
        result=(diff_x+diff_y)** 0.5
        return result 
    def __mul__(self,num):
        # this is the multiplication operato overider
        return Point(self.x*num, self.y*num)
        
    def __str__(self):
        return f"Point Object ({self.x},{self.y})"
    def __repr__(self):
        return self.__str__()
        
# on main.py
from point import Point

test1=Point(2,6)
test2=Point(-1,5)
orgin=Point(0,0)
test3=Point(5,0)
print(test1)
print(test2)
print('distance from orgin to (5,0) ', orgin.distance(test3))
print(orgin) ```
