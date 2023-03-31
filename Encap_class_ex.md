```python 
# On encap.py 
class User:
    def __init__(self,username):
        self.__username=username
        self.__password=self.__set_password() # we have a function called set_pwd which sets the password for us so we are using self. to call it here
        self.__logged_in=False
    
    def __set_password(self):
        get_password=input('enter a password: ')
        return get_password 

    def login(self,password):
        if password==self.__password:
            if self.__logged_in:
                print('You are already logged in ')
            else:
                self.__logged_in=True
                print(f'{self.__username} is successfully logged in!')
        else:
            print("Incorrect password")
            
    def logout(self):
        if self.__logged_in:
            self.__logged_in=False
            print(f'{self.__username} is successfully logged out')
        else:
            print(f'{self.__username} is already logged out')
            
    def __str__(self):
        # Base override of the string built-method
        return f'User: {self.__username}'
        
    def __repr__(self):
        return self.__str__()
        
     # end of User class
     
# on main.py
from encap import User

"""
user needs two attributes arugument: username and user status ( Alpha and Beta)
Methods: 
    login()
    logout()
    """
test=User('aroushsyed')
#test.login('lol')
#test.logout()

```
