
Но компьютерная математика чуть более интересная.

Остаток от деления.
Операция остатка от деления -- это операция получения наименьшего целого положительного числа r, которое выполняет условие: a = (b * q) + r при том, что a, b, q -- это целые числа и a не равно b и 0 <= r < |b|, где a -- это делимое число, b -- это делитель и r -- это остаток от деления, q -- это неполный частный остаток, но нам это пока не надо. Это абсолютно правильное определение (о котором создатели JavaScript очевидно не знают по причине тотальной безграмотности и невежества), но достаточно запутанное. Есть и более простое: Остаток от деления a на b это некоторое число r, которое надо отнять от a чтобы оно делилось на b без остатка. 

Например:
Остаток от деления 10 на 2 будет 0 поскольку 10 делится на 2 без остатка.
Остаток от деления 5 на 2 будет 1, поскольку 5 на 2 не делится нацело и надо отнять 1, чтобы делилось без остатка.
Остаток от деления двух чисел в Python можно найти при помощи оператора %. Например 10 % 5 вернет 0 или 5 % 2 вернёт 1.
При помощи интерпретатора Python найдите остатки от деления для таких пар чисел:
28, 7 (0)
100, 13 (9)
-215, 26 (26)
3, 2 (1)
162531625361 384756384 (164431313)


Деление.


Типы данных:
Мы с вами привыкли и оперируем реальными данными.
Мы запоминаем числа, буквы, слова, образы, решения
Компьютер также имеет свои типы данных: числа, строки, булев тип.

К счастью - пайтон их сам идентифицирует.

Но у каждого типа есть свои особенности работы:


Основные типы данных и операторы для них:
Целые числа: 1, 2, 2343, 10
Вещественные (числа с дробной частью) 1.0, 3.14, 2.44
Строки: ‘hello world’
Булев тип: True, False

Создайте два числа x, y, оба равные единице, но сделайте это так, чтобы x было целым, а y -- число с дробной частью.
Ответ: 
x = 1
y = 1.0

Для того, чтобы понимать то, как работает программа, тем более, искать в ней ошибки, необходимо понимать как действия в программе происходят.

"Поток выполнения" - действия выполняются сверху вниз последовательно


x = “hello”
print(x) # Вернёт ‘hello’

x = x + “ world”
print(x) #  Теперь вернет “hello word”


Арифметические действия выполняются точно так же, как и в математике.
Последовательность действий.
Упражнения на устный счет.


Математические функции.
В математике мы привыкли к функциям: синусы и косинусы.
Программирование их использует


Пример на встроенные математические функции

from math import sin, cos, sqrt, pi
sin(pi/2) # 1
cos(pi) # -1
sqrt(16) # 4

Обобщить: связь с их софтами.
Померять их доходы, расходы по сферам - сделать расчет в Пайтоне.
Сделать аналогичную схему по времени и стремлениям.


Неизменяемые переменные (константы).

Примеры по неизменяемым переменным.




Результат первого занятия: калькулятор, т.е. можем ввести данные и вывести результат вычислений.

Далее - практика так, чтобы это было привычным.

По сути сам интерпретатор Python -- это мощный продвинутый калькулятор. Предлагаю дать решить задачу:
Вам дано список чисел n, найдите остаток от деления наибольшего числа из n на наименьшее.
n = [13.580561604444451, 20.84387403771435, 72.25470578556231, 85.67213261111209, 37.63172346290232, 87.59428903919381, 35.2069084488854, 11.872987522885925, 32.76366191400453, 17.732945429869275, 96.7309657452768, 65.55036893111621, 68.19357703500117, 49.30127265132532, 33.66856439791127, 70.37272824419965, 62.685743003227756, 65.66554999592876, 53.02899512238653, 83.4254067771523, 57.05372596821685, 31.384397763493045, 70.19881200300306, 34.585602649196524, 89.40962101698108, 41.70949991272782, 12.768633608367008, 26.957511129962132, 26.337480885175868, 2.792417623779875, 7.647398372796155, 33.11465572361385, 23.504591617701564, 97.93633792417958, 72.27966212804138, 2.3302201961702074, 8.901858684281027, 53.217851853788325, 80.19918712606075, 23.675618303622425, 98.4430999662397, 79.75244876328351, 59.60445383836137, 13.676498361230284, 7.653387239382569, 73.27791656834985, 36.96937831516113, 21.85355611788429, 44.07060622809963, 12.84131455889761, 85.68356873050216, 3.9274188988804193, 2.0771060536838193, 29.382265352963234, 17.332360343464337, 71.33786945984669, 67.71433210791545, 22.162772375332086, 68.00878511207273, 22.542119784199954, 21.904860728548726, 81.56980784532612, 2.679885219810929, 73.66385550041936, 49.69397274790778, 0.41649942211824387, 16.604499778091785, 36.531997857917666, 36.222106642365446, 26.345459831193775, 52.905902474950096, 59.66456232080196, 78.13792583883506, 24.72068378204131, 50.319628062010736, 1.642637021099902, 45.45937363642767, 38.749512362842566, 25.921955279002685, 41.13807598927538, 86.98964415554339, 37.727914978876775, 61.64297244943357, 10.92296698459274, 97.96852951340489, 2.846216918628963, 93.80185968303478, 36.98099085630794, 54.56262731111825, 23.523696758589818, 29.50227089337375, 94.17319617194153, 83.69155785782891, 79.33462618224726, 22.543286690533314, 72.13918218970043, 22.91380017248451, 38.67506953273517, 40.999419975587934, 61.18038184220948]

Правильный ответ 0.14923634633414729
Чтобы его получить надо выполнить: max(n) % min(n)