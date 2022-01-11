# Игра "Жизнь"

Проект подготовлен в качестве вступительного испытания на курс "Машинное обучение" от "Тинькоф Образование". Язык реализации - Python 3.7. 

Условия игры:
 - «Жизнь» разыгрывается на бесконечном клеточном поле.
 - У каждой клетки 8 соседних клеток.
 - В каждой клетке может жить существо.
 - Существо с двумя или тремя соседями выживает в следующем поколении, иначе погибает от одиночества или перенаселённости.
 - В пустой клетке с тремя соседями в следующем поколении рождается существо.
 
 Задача реализована в соответствии с принципами Объекто-ориентированного программирования. Все функции и объекты реализованы в качестве классов, за исключением:
 - клеток поля - связано с тем, что автор пошел по не самом очевидному пути решения задачи, но заметно превосходящему по скорости исполнения. Грубо говоря, поле это numpy массив, где клетками являются его элементы, такой подход позволяет удобно и быстро получать количество соседей путем складывания срезов расширенного массива со сдвигом, а также удобно отфильтровывывать все элементы массива по условию, а не обрабатывать каждую клетку в цикле по отдельности, плюс не приходится рассматривать краевые случаи на гранях и углах поля.
 - совсем очевидных и коротких функций по типу сравнение на равенства массива нулевому или предыдущему, к таким функциям написаны комментарии в коде.
 
Бесконечность поля реализована тем, что его размеры можно запросто изменить в коде или подать на вход в качестве параметров функций.

# Файлы репозитория

### main.py

Основной файл, весь код программы находится здесь. Файл через консоль запускается на любых условиях. Для чтения на операционных системах MAC, следует запускать через sudo python main.py так как требуется чтение клавиш.

Программа выполняется до тех пор, пока поле не будет стационарным (следующий шаг не меняет положения клеток), пока клетки полностью не исчезнут или же пока пользователь принудительно не прекратит программу нажатием клавиши.

### visualisation_example.ipynb

Файл имеет говорящее название: в нем содержится пример с отображением состояния поля на цветном графике, а не печати массива из 0 и 1. В остальном код не отличается от того, что находится в файле *main.py*.
