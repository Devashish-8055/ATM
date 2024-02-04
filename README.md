class Atm:
    def __init__(self):
        self.pin=''
        self.balance=0
        self.menu()
    def menu(self):
        i =int(input('''
                Hello how would you like to proceed
                1. Enter 1 for pin generation
                2. Enter 2 for balance check
                3. Enter 3 for cash withdraw
                4. Enter 4 for cash deposit
                5. Enter 5 for Exit
'''))
        if i==1:
            self.create_pin()
        elif i==2:
            self.balance_check()
        elif i==3:
            self.cash_withdraw()
        elif i==4:
            self.cash_deposit()
        elif i==5:
            self.exit()
        else:
            print("wrong choice")
    def create_pin(self):
        self.pin=int(input("Enter your pin"))
        print('pin generated successfully')
    def balance_check(self):
        test=int(input("Enter your pin"))
        if test==self.pin:
            print(self.balance)
        else:
            print('sorry wrong pin entered')
    def cash_withdraw(self):
        test=int(input("Enter your pin"))
        if test==self.pin:
            amt=int(input('Enter the amount you want to withdraw'))
            if self.balance<=0:
                print("You don't have the sufficient balance")
            else:
                self.balance=self.balance-amt
                print('Cash withdrawn successfully')
        else:
            print('Sorry wring pin entered')
    def cash_deposit(self):
        test=int(input("Enter your pin"))
        if test==self.pin:
            amt=int(input('Enter the amount you want to deposit'))
            self.balance=self.balance+amt
            print('Cash deposited successfully')
        else:
            print('sorry wrong pin entered')
    def exit(self):
        print('Thanks for coming')


        

'''First create an object using
SBI=Atm()
You can also create mulitple objects using
HDFC=Atm()
BOB=Atm()

After this the code inside the constructor will work and you can access all the methods.
''' 



