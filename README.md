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

balance = 5200 #assumption on user's balance
pin = int(input('Please Enter You 4 Digit Pin: ')) #to prompt the user to enter correct pin

#correct pin is assumed to be 123456
if pin == (123456):

#Challenge 1 only focusing on the cash withdrawal transaction
print('1) Check Balance\n')
print('2) Withdraw Cash\n')

#if the amount that is desired to be withdrawn is insufficient
elif withdraw >= balance:
            print ('Your transaction has been cancelled/ is unsuccessful due to insufficient balance')
            break
