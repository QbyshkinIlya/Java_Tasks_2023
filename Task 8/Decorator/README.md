# ПРАКТИЧЕСКАЯ РАБОТА №8
Реализация программы: <br>
![ОКНО](https://github.com/Je1rei/Java-Tasks/blob/main/Task%208/Decorator/IMG/star.png) 
![ОКНО](https://github.com/Je1rei/Java-Tasks/blob/main/Task%208/Decorator/IMG/Presents.png) 
![ОКНО](https://github.com/Je1rei/Java-Tasks/blob/main/Task%208/Decorator/IMG/Girlands.png) 
![ОКНО](https://github.com/Je1rei/Java-Tasks/blob/main/Task%208/Decorator/IMG/All.png)

Паттерн "Декоратор" (Decorator):
Программа реализует паттерн "Декоратор", который позволяет добавлять дополнительное поведение или функциональность к объектам без изменения их основной структуры. 

- HelloController:
- - initialize(): Этот метод выполняется при инициализации контроллера. Он создает объект класса ChristmasTreeImpl и вызывает метод draw(), отображая базовую елку.
- - addLights(ActionEvent actionEvent): Добавляет гирлянду к елке, создавая объект класса Girland, который декорирует базовую елку.
- - addPresents(ActionEvent actionEvent): Добавляет подарки к елке, создавая объект класса Presents, который декорирует базовую елку.
- - addStar(ActionEvent actionEvent): Добавляет звезду к елке, создавая объект класса Star, который декорирует базовую елку.
- - addAll(ActionEvent actionEvent): Добавляет все украшения к елке, включая подарки, гирлянду и звезду.
- - del(ActionEvent actionEvent): Удаляет все украшения с елки и отображает только базовую елку.
- - addSandG(ActionEvent actionEvent): Добавляет гирлянду и звезду к елке, декорируя ее сразу двумя украшениями.
- - ChristmasTree (Интерфейс):
- - draw(Pane pane): Этот метод определяет интерфейс для отрисовки рождественской елки. Все классы, реализующие этот интерфейс, должны предоставить свою реализацию отрисовки.

- ChristmasTreeImpl:
- - Этот класс реализует интерфейс ChristmasTree.
- - draw(Pane pane): Метод рисует базовую форму рождественской елки, состоящую из треугольника (кроны) и прямоугольника (ствола).

- TreeDecorator:
- - Этот класс представляет базовый класс для декораторов рождественской елки.
- - Содержит ссылку на объект типа ChristmasTree, который декорируется.
- - Реализует интерфейс ChristmasTree.
- - draw(Pane pane): Метод делегирует вызов методу draw() базового объекта ChristmasTree.

- Girland:
- - Декоратор для добавления гирлянды к рождественской елке.
- - drawGirland(Pane paneLight): Метод отрисовывает гирлянду, представленную круглыми элементами разных цветов, анимируя их мерцание.

- Presents:
- - Декоратор для добавления подарков к рождественской елке.
- - drawwithPresents(Pane panePresent): Метод отрисовывает подарки, представленные прямоугольными элементами разных цветов.

- Star:
- - Декоратор для добавления звезды к рождественской елке.
- - drawStar(Pane panestar): Метод отрисовывает звезду в виде пятиконечной звезды разного цвета.

