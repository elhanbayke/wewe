def calculate():
    operation = input('''
Введите знак:
+ 
- 
* 
/ 
''')

    number_1 = int(input('Введите первое число: '))
    number_2 = int(input('Введите второе число: '))

    if operation == '+':
        print('{} + {} = '.format(number_1, number_2))
        print(number_1 + number_2)

    elif operation == '-':
        print('{} - {} = '.format(number_1, number_2))
        print(number_1 - number_2)

    elif operation == '*':
        print('{} * {} = '.format(number_1, number_2))
        print(number_1 * number_2)

    elif operation == '/':
        print('{} / {} = '.format(number_1, number_2))
        print(number_1 / number_2)

    else:
        print('Вы не ввели оператор, пожалуйста перезапустите программу.')

    # Add again() function to calculate() function
    again()

def again():
    calc_again = input('''
Вы хотите продолжить?
Если да введите Y. если нет N!
''')

    if calc_again.upper() == 'Y':
        calculate()
    elif calc_again.upper() == 'N':
        print('Все-го хо-ро-ше-го.')
    else:
        again()

calculate()
