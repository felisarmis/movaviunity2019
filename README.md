# Movavi Unity3D 2019/2020
Учебные пособия и материалы для самостоятельного изучения для курса Movavi School по разработке игр на Unity3D за 2019/2020 год.


## Содержание

### Проекты
* [Arkanoid](#arkanoid)

### Занятия
* [Урок 01](#урок-01)
* [Урок 02](#урок-02)

### Самостоятельное изучение
* [Документация по Unity](#документация-по-unity)
* [Видео уроки](#видео-уроки)
* [Текстовые уроки](#текстовые-уроки)
* [Платные видеокурсы и книги](#платные-видеокурсы-и-книги)
* [Game design](#game-design)
* [Инди-игры](#инди-игры)
* [Инди-game-сообщества](#инди-game-сообщества)

---

## Проекты

### Arkanoid

__Arkanoid__ — видеоигра для игровых автоматов, разработанная компанией Taito в 1986 году. Игра основана на играх серии __Breakout__ фирмы Atari. Именно её название стало нарицательным для класса подобных игр.

Игрок контролирует небольшую платформу-ракетку, которую можно передвигать горизонтально от одной стенки до другой, подставляя её под шарик, предотвращая его падение вниз. Удар шарика по кирпичу приводит к разрушению кирпича. После того как все кирпичи на данном уровне уничтожены, происходит переход на следующий уровень, с новым набором кирпичей. Есть и некоторое разнообразие: определённые кирпичи нужно ударять несколько раз, иногда появляются летающие враги, от которых отталкивается шарик, удар по некоторым кирпичам приводит к выпаданию из них капсул-призов — приз активируется, если поймать такую капсулу ракеткой.

[Статья в Википедии](https://ru.wikipedia.org/wiki/Arkanoid)  
[Полное описание всех уровней оригинальной игры](https://arcadeclassics.net/80s-game-videos/arkanoid/)  
[Статья по гейм-дизайну и истории Breakout-like игр](https://www.gamasutra.com/view/feature/1630/breaking_down_breakout_system_and_.php?print=1)

---

## Занятия

### Урок 01

[Ассеты для первого урока](https://drive.google.com/open?id=1RutbCKuZoJ7GvpjKGVUZcl4bRQFdkCiH)  
[Готовый проект первого урока](https://drive.google.com/open?id=1yxAPA8qwG-PNlEk1EpV2Rb0WOV_YUi1l)

1. Создание проекта.  
   Нужен 2D проект, крайне желательно работать сразу на флешке.

2. Импорт ассетов изображений из папки - фон, шарик, платформа, блоки разных видов.

3. Настройка размеров ассетов через параметр __Pixels per unit__.  
   Для фона выбрали 120.  
   Для шарика - 256.  
   Для платформы - 128.  

4. Настройка pivot для ассета фона.  
   Для фона через __Sprite Editor__ надо поместить pivot в нижний левый угол.

5. Настройка камеры.  
   Для камеры надо выбрать соотношение сторон 16 / 9.
   Установить размер камеры на 6.

6. Нужно переместить фон в начало координат (чтобы нижний левый угол как раз совпадал с началом координат), камеру разместить так, чтобы она закрывала весь фон (нижние левые углы совпадали с фоном).

7. Разместить объекты в пространстве по оси Z.  
   Камеру отодвинуть назад на -100.  
   Шарик и платформа - 0.  
   Фон подвинуть назад на +10.  

8. Назначить шарику коллайдер типа __Circle Collider 2D__.  
   Платформе назначить коллайдер типа __Polygon Collider 2D__.

9. Создать скрипт для платформы, чтобы она следовала за мышью.

10. Добавить шарику компонент __Rigidbody__.

11. Создать физический материал и добавить его всем коллайдерам.  
    В физическом материале __Friction__ - 0, а __Bounciness__ - 1.

12. Создать стены: левую, правую и верхнюю из пустых объектов, назначить им коллайдеры типа __Box Collider 2D__, отредактировать размер коллайдеров, чтобы закрывали всю границу экрана, добавить им физический материал.

13. Отредактировать скрипт платформы так, чтобы платформа не выходила за границы экрана (через __Mathf.Clamp__).

14. Создать скрипт для шарика, чтобы он следовал за платформой на заданном изначально расстоянии.


### Урок 02

[Ассеты для второго урока](https://drive.google.com/open?id=1yN7JlBp5GGdfvQF4x6VkKaMmn7BSTw9d)  

1. Поведение шарика  
   Написать скрипт поведения шарика - в начале игры следует за платформой, после нажатия мыши получает ускорение вверх, затем не подчиняется прямому управлению

2. Создание нижнего коллайдера для перезагрузки сцены при проигрыше  
   Написание скрипта для перезагрузки сцены при проигрыше  
   Не забыть про включение __SceneManager__

3. Добавление блока  
   Настройка ассета блока  
   Добавление коллайдера и физического материала

4. Создание скрипта для разрушения блока

5. Создание префаба из блока

6. Проигрывание случайного звука при столкновении шарика

7. Проигрывание звука при разрушении блока

8. Создание своего уровня из блоков разного цвета

---

## Самостоятельное изучение

### Документация по Unity
* https://docs.unity3d.com/Manual/index.html 
* https://forum.unity.com/ 
* https://answers.unity.com/index.html 
* https://stackoverflow.com/questions/tagged/unity3d 

### Видео уроки:
* https://learn.unity.com/ 
* https://www.youtube.com/channel/UCG08EqOAXJk_YXPDsAvReSg 
* https://www.youtube.com/channel/UCYbK_tjZ2OrIZFBvU6CCMiA 
* https://www.youtube.com/user/SykooTV 
* https://www.youtube.com/user/Cercopithecan 
* https://www.youtube.com/channel/UCHM37DnT_QGJT5Zyl4EmqcA/featured 
* https://www.youtube.com/playlist?list=PLGp0Y-yHLA-_PGtqama4XP1CGgXwlqsX9
* https://www.youtube.com/channel/UC7P6olyswpgJlElZA6RXUNQ

### Текстовые уроки:
* https://catlikecoding.com/unity/tutorials/ 
* https://www.alanzucconi.com/tutorials/ 

### Платные видеокурсы и книги:
* https://www.udemy.com/unitycourse/ 
* https://www.udemy.com/unitycourse2/ 
* https://www.ozon.ru/context/detail/id/34792570/ 
* https://www.ozon.ru/context/detail/id/149333515/ 

### Game design:
* https://www.youtube.com/channel/UC0JB7TSe49lg56u6qH8y_MQ 
* https://www.youtube.com/playlist?list=PLBmERAe8ffebQIbaFc6WqahtWsOIHoAMz 
* http://narratorika.com/ 
* https://www.youtube.com/channel/UCqJ-Xo29CKyLTjn6z2XwYAw 
* https://www.youtube.com/channel/UC0fDG3byEcMtbOqPMymDNbw 
* https://dtf.ru/gamedev 
* https://www.ozon.ru/context/detail/id/151117665/ 
* https://www.coursera.org/specializations/game-development
* https://www.coursera.org/specializations/game-design
* http://aushestov.ru/
* http://level-design.ru/
* https://www.youtube.com/user/ExtraCreditz/videos

### Инди-игры:
* https://itch.io/ 
* https://gamejolt.com/ 
* https://www.indiegamewebsite.com/ 
* https://www.indiegamewebsite.com/2019/06/24/the-100-best-indie-pc-games/ 
* https://www.indiegamewebsite.com/2018/05/11/the-100-best-indie-games-of-all-time/ 
* https://www.rockpapershotgun.com/ 
* https://www.youtube.com/channel/UCylVqS5Hk_i175AyCeYKT2w 

### Инди-game-сообщества:
* https://vk.com/last_indie_standing 
* https://vk.com/ggdev 
* https://vk.com/igrologia_vk 
* https://vk.com/mooshigames   
* https://vk.com/gdcuffs 
