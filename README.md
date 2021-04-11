# C2_CnC

challenge 1: 
[Challenge 1 CC Nur Fatinhieyah 1724044 (3).pdf](https://github.com/fatinhieyah/C2_CnC/files/6291387/Challenge.1.CC.Nur.Fatinhieyah.1724044.3.pdf)


CSC 4101 Section 1 – 2021 March
Challenge 1 – State Transition Testing

1. Chosen project title: ATM (Withdraw cash)

2. Identify a part of the project that relates with state transitions:
a) Valid card - the user needs a valid bank card in order to withdraw money
b) Correct pin – the user inserts correct pin to perform the transaction
c) Sufficient amount – the amount that need to be withdrawn is sufficient 

The user is assumed to have a valid card in this situation.

balance = 5200 #the user's balance is assumed
back = ('Y')
pin = int(input('Please Enter You 4 Digit Pin: ')) #to prompt user to enter their correct pin

if pin == (123456): #this is the assumed correct pin
  while back not in ('n','NO','no','N'):
      print('\nPlease choose the transaction to continue:\n') #Challenge 1 only focusing on the withdraw cash transaction
      print('1) Check Balance\n')
      print('2) Withdraw Cash\n')
      
      option = int(input('Choose the transaction to continue:\n'))
      if option == 1:
        print('Your Account Balance is RM',balance,'\n')
        back = input('Would you like to continue? ')
        if back in ('n','NO','no','N'):
          print('Thank you for using our service \n')
          break
          
      elif option == 2:
        withdraw = float(input('Choose/enter the amount: \n1) RM 100/2) RM 200/3) RM 300/4) RM 400/5) RM 500/6) RM 600 for other amount enter 7: '))
        if withdraw in [1, 2, 3, 4, 5, 6]:
          balance = balance - withdraw
          print ('\nYour current balance: RM ',balance)
          print ('\nPlease take the cash dispensed')
          print ('\nThank you for using our service')
          break

        elif withdraw == 7:
          withdraw = float(input('Please enter amount: RM '))
          if withdraw <= balance:
            balance = balance - withdraw
            print ('\nYour current balance: RM ',balance)
            print ('\nPlease take the cash dispensed')
            print ('\nThank you for using our service')
            break
          elif withdraw >= balance:
            print ('Your transaction has been cancelled/ is unsuccessful due to insufficient balance') #if the amount to be withdrawn is sufficient
            break

      else:
        print('Please enter a correct number. \n')
        back = ('y')
elif pin != (123456):
  print('Incorrect Pin!') #if the user entered incorrect pin


