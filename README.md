# Практика 5 Столяров Даниил Шикхарович 22T0318
## Тема: приложение для парикмахерской.
## Текст задания
Усовершенствовать приложение из предыдущей практики. 
<ul>
  <li>Изменить способ отображения услуг на экране, вместо ListView использовать GridView с двумя столбцами.</li>
  <li>Добавить нижнюю навигационную панель (BottomNavigationBar), разделив приложение на 3 страницы: Каталог, Избранное и Профиль</li>
  <li>В Избранном должны находиться товары, отмеченные пользователем</li>
  <li>В профиле должна быть статичная страница-заглушка</li>
</ul>

## Порядок выполнения
### Шаг 1.
<p>Поместим услуги в 2 столбца, чтобы эффективнее использовать доступное пространство экрана.</p>
<p>Для этого используем GridView.builder()</p>

![изображение](https://github.com/user-attachments/assets/dc7b799a-cae8-4ec1-a3d0-a16f8798d6b8)

### Шаг 2.
При работе с Избранным, у меня возникла проблема: необходимо как-то изменять состояние списка избранных услуг, находясь в компоненте просмотра отдельной услуги. (Кнопка "добавить в Избранное", "Убрать из Избранного").
Поэтому вынесем список услуг и список избранных услуг в отдельный класс и будем использовать глобальный объект (и заодно напишем функцию, чтобы проверять, является ли произвольно взятая улсуга Избранной)

![изображение](https://github.com/user-attachments/assets/e83346f4-76b8-4dec-9d85-674ff6a5a570)

### Шаг 3.
Изменим содержимое страницы <i>item_view.dart</i>: добавим кнопку "добавить в Избранное", которая будет менять цвет и текст в зависимости от того, является ли данная услуга Избранной.

![изображение](https://github.com/user-attachments/assets/5ec32246-070c-4eb6-9058-348c098f90ab) 

![изображение](https://github.com/user-attachments/assets/0dd37268-e2a1-4bb8-a89d-f72b45cc902a)

![изображение](https://github.com/user-attachments/assets/442128d4-2460-46d2-9613-532cdc0b33e5)


### Шаг 4.
Добавим страницу с профилем пользователя.

![изображение](https://github.com/user-attachments/assets/1250ba44-6299-4863-a9d0-da8cd7d456c6)

### Шаг 5.
Добавим страницу со списком Избранное - по аналогии с каталогом, но с небольшими правками.

![изображение](https://github.com/user-attachments/assets/668a1084-afd1-492e-b6e4-eac97d957018)

### Шаг 6. Добавим Bottom Navigation Bar, куда подключим 3 страницы

![изображение](https://github.com/user-attachments/assets/59097220-748c-4243-9576-2bdb2bc21739)

