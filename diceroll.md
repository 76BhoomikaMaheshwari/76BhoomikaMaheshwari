import random
def roll_a_dice(x):
    max_val = 6
    min_val = 1
    roll_again = 'yes'
    d = 0
    while roll_again == 'yes' or roll_again == 'y':
        a = int(input('enter a number between 1 & 6: '))
        print('rolling the dice...')
        b =  random.randint(min_val, max_val)
        print('the values are:', b)
        
        if a == b:
            d = d+1
            print('congrats you got a point')
            g = d
        else:
            print('better luck next time')
        roll_again = input('roll again?')
        
    else:
        c = input(('are you sure you want to exit(yes/no): '))
        if c == 'no' or c == 'n':
            print(roll_a_dice(x))
        else:
            print('your score is: ', g)

z = input('wanna roll the dice(yes/no): ')
if z == 'yes' or z == 'y':
    print(roll_a_dice(z))
else:
    print('come if you wanna play')
