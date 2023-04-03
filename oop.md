```python

from random import choice,randrange
from time import sleep 

class Car:
    def __init__(self,brand_name,model,type):
        self.brand_name=brand_name
        self.model=model
        self.type=type
        self.fuel_tank= 50
        self.current_fuel=50
        self.__license = self.__set_license_plate()
            
        '''Attributes:
              brand_name: string value of brand of car
              model: string value of car model 
              type: string value of type of vechile'''            
            
    def __set_license_plate(self):
        get_licence_plate=input("Enter your licence plate: ")
        print(f'Thank you, we are using your licence plate to connect to your {self.type} to help monitor its functionality!')  
        return get_licence_plate
        
    def driving(self,km_driven):
        self.km_driven=km_driven
        if self.current_fuel ==0:
            print(f'Your {self.type} is out of gas, you cannot go anywhere')
        else:
            print(f'Today in your {self.type} you have driven {self.km_driven} kilometers ')
            for i in range(1,self.km_driven,2):
                if self.current_fuel !=0:
                    self.current_fuel-=2
            print(f'Your fuel tank is now at {self.current_fuel} liters')     
            
        '''Arugs:
              km_driven: integer input of how many km you trvalled'''
              
    def refuel(self):
        self.current_fuel == self.fuel_tank
        print(f'Your {self.type} is ready to roll!!')

    def add_more_fuel(self,amount):
        if self.current_fuel + amount > self.fuel_tank:
            print(f'Your {self.type}s tank cannot take this much fuel.')
        else:
            self.current_fuel+=amount
            print(f'Current fuel: {self.current_fuel}')
        '''Arugs:
              amount: integer input of how much fuel you want to add to vechile'''
              
    def speeding(self,speed):
        speed_limit=randrange(30,120,10)
        police_following=choice([True,False])
        speeding_fine=randrange(50,350,10)
        if speed_limit<speed and police_following:
            print(f'You were over the speed limit and a police officer caught you! You got a ${speeding_fine} fine')
        elif speed_limit<speed:
            print('You were over the speed limit but no police officer saw you!')
        else:
            print(f'The limit was {speed_limit} km/hr, you were at/under the limit')
      '''Arugs:
              speed: integer value of your car's currrent speed'''
              
    def __str__(self):
        return f'Cool {self.type}! I like your {self.brand_name} {self.model}!!'
    def __repr__(self):
        return __str__

class Electric_Car(Car):
    def __init__(self,brand_name,model,type):
        super().__init__(brand_name,model,type)
        '''Attributes:
              brand_name: string value of brand of car
              model: string value of car model 
              type: string value of type of vechile ''' 
      
    def add_more_fuel(self,amount):
        print(f"{self.brand_name}'s do not need fuel! Find a charging port") 
         '''Arugs:
              amount: integer input of how much fuel you want to add to car'''
        
    def refuel(self):
        battery=Battery()
        print(f'Okay your {self.brand_name} {self.model} is charging...')
        battery.recharge()
        
    def inventory(self):
        self.inventory=[]
        adding_more=True 
        while adding_more:
            stuff=input("Item: ")
            self.inventory.append(stuff)
            question=input('want to add more? (y/n) ')
            if question in "Nn":
                adding_more=False
        print(f'You have {self.inventory} in your car')       
        
class Battery:
    def __init__(self):
        self.full_battery=100
    def recharge(self):
        sleep(4)
        print(f'Okay, your vechile is back to {self.full_battery}% battery')
```
