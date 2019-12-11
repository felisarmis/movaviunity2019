# Movavi Unity3D 2019/2020
Учебные пособия и материалы для самостоятельного изучения для курса Movavi School по разработке игр на Unity3D за 2019/2020 год.


## Содержание

### Arkanoid
* [Урок 01](#урок-01)
* [Урок 02](#урок-02)
* [Урок 03](#урок-03)
* [Урок 04](#урок-04)
* [Урок 05](#урок-05)
* [Урок 06](#урок-06)
* [Урок 07](#урок-07)
* [Урок 08](#урок-08)
* [Урок 09](#урок-09)
* [Урок 10](#урок-10)

### Ruby's Adventure

### Самостоятельное изучение
* [Документация по Unity](#документация-по-unity)
* [Видео уроки](#видео-уроки)
* [Текстовые уроки](#текстовые-уроки)
* [Платные видеокурсы и книги](#платные-видеокурсы-и-книги)
* [Game design](#game-design)
* [Инди-игры](#инди-игры)
* [Инди-game-сообщества](#инди-game-сообщества)

---

## Arkanoid

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
[Готовый проект второго урока](https://drive.google.com/open?id=1JY3jQKtsm2zU4vInaJE4XMGXbPJL4yl0)  

1. Поведение шарика  
   Написать скрипт поведения шарика - в начале игры следует за платформой, после нажатия мыши получает ускорение вверх, затем не подчиняется прямому управлению

2. Создание нижнего коллайдера для перезагрузки сцены при проигрыше  
   Написание скрипта для перезагрузки сцены при проигрыше  
   Не забыть про включение __SceneManager__

3. Добавление блока  
   Настройка ассета блока  
   Добавление коллайдера и физического материала

4. Создание скрипта для разрушения блока


### Урок 03

[Ассеты для третьего урока](https://drive.google.com/open?id=1qVtyxj8X7Y_iDraPrtBsGrQY02k3fD1K)  
[Готовый проект третьего урока](https://drive.google.com/open?id=1Z2U9pGru2KJNrNXidPXpCfyq0mMLGzGf)  

1. Воспроизведение случайного звука при столкновении шарика
2. Воспроизведение звука при разрушении блока
3. Работа с префабами
4. Создание префаба из блока
5. Создание первого уровня из блока-префаба


### Урок 04

[Ассеты для четвертого урока](https://drive.google.com/open?id=1li7RsfD7Qu3vAHsbmA-plj8Qn3eVrGwh)  
[Готовый проект четвертого урока](https://drive.google.com/open?id=1r9eqM1Pw6bGwR1RFkrDF555THXONKSYQ)  

1. Подсчет блоков на уровне
2. Загрузка следующего уровня после разрушения всех блоков
3. Создание префабов для всех необходимых объектов (камера, фон и стены, шар и платформа)
4. Создание второго уровня из префабов


### Урок 05

[Ассеты для пятого урока](https://drive.google.com/open?id=1xKZgHq8FbAqdnGVWwhUNZqNRd2bHQehF)  
[Готовый проект пятого урока](https://drive.google.com/open?id=1LixVkGUYl7ekq8fmMVGVZIpOMBkggW6p)  

1. Подсчет очков за разрушенные блоки.
2. Создание интерфейса для отображения заработанных очков.
3. Вывод очков на экран.
4. Перенесение очков из одного уровня в другой.  
   Singleton паттерн.
5. Исправление поведения при потере мяча.


### Урок 06

[Ассеты для шестого урока](https://drive.google.com/open?id=1q9LxvQ4-KpypU5NsDZFvSugpJkBu2omB)  
[Готовый проект шестого урока - Unity 2018.3](https://drive.google.com/open?id=1X6vIbZDfx01rPMqzh2AsU-zT40Y6QWJa)  
[Готовый проект шестого урока - Unity 2019.2](https://drive.google.com/open?id=1vxkSMCMUQh5piI8tIiA1a2qa4Q4rK1hN)  

1. Создание сцен начального меню и окончания игры.
2. Создание кнопок для начала игры и возврата на первый экран.
3. Навешивание событий загрузки уровней на кнопки.


### Урок 07

[Ассеты для седьмого урока](https://drive.google.com/open?id=1GHpnNqf6GTEhQfrwDIztX2DMGyBbQY07)  
[Готовый проект седьмого урока](https://drive.google.com/open?id=1ACygVbgZtkY1jzU6sHqTFLzXotfpAFeU)

1. Изменения поведение при потере всех жизней - загрузка последнего экрана.
2. Добавление частиц в проект.
3. Появление частиц при разрушении блока (Instansiate)
4. Префаб и поведение неразрушаемого блока
5. Префаб и поведение блока с несколькими уровнями разрушения.


### Урок 08

[Ассеты для восьмого урока](https://drive.google.com/open?id=1P7gNRQNtF8GxeJpetZ10uyjF5v1aFnZe)  
[Готовый проект восьмого урока](https://drive.google.com/open?id=1ywvQCTnPmc6YGa9ULL8F-FoV3lvXH2nZ)  

1. Загрузка ассетов для обозначения бонусов
2. Создание префабов блоков для разных видов бонусов с помощью SpriteMask
3. StartCoroutine и IEnumerator
4. Бонус увеличения ширины платформы
5. Бонус деактивации падения мяча


### Урок 09

[Готовый проект девятого урока](https://drive.google.com/open?id=12O3jHqll_2DsF63Ei4cLADu0AnRDGsHE)  

1. Бонус дублирования мяча
2. Бонус изменения скорости игры
3. Бонус супер мяча
4. Бонус прилипающего мяча


### Урок 10

Самостоятельная работа над проектом __Arkanoid__


---

## Ruby's Adventure

### Настройка проекта, главный герой, первый скрипт

1. Создать новый 2D проект.
2. Найти в Asset Store и импортировать __2D Beginner: Tutorial Resources__ (https://assetstore.unity.com/packages/essentials/asset-packs/2d-beginner-tutorial-resources-140167)
3. Создать новую сцену __MainScene__
4. Импортировать [ассет главного героя](https://connect-prd-cdn.unity.com/20190206/learn/images/7d1c06b8-7c73-44b4-8c41-3246b3ce8427_image4.png?_ga=2.217537814.1411910662.1575807073-1222847038.1575502921) в __Art > Sprites__
5. Создать игровой объект главного героя из ассета
6. Поставить координаты:  
   a. Для камеры - __0 по x и 0 по y__  
   b. Для героя __-2 по x и 0 по y__  
7. Создать новую папку __Scripts__, внутри создать скрипт __RubyController__
8. Посмотреть стандартные настройки управления в __Edit > Project Settings>Input__
9. [Написать скрипт](https://drive.google.com/open?id=1s30yEHP9E3kCaE6Q8qho_DyR55okB-kx) для движения главного героя


### Игровой мир и объекты

1. Создать __Tilemap__ через __2D Object > Tilemap__
2. Создать папку в __Assets > Art__, назвать ее __Tiles__, внутри нее создать новый __Tile__, назвать его __FirstTile__
3. Скачать [ассет первого тайла](https://connect-prd-cdn.unity.com/20190206/learn/images/9d150874-0668-448e-8eec-fc8d888adc1d_image11.png?_ga=2.155268155.1411910662.1575807073-1222847038.1575502921) и сохранить в папку __Art > Sprites__
4. Назначить скачанную картинку в поле __Sprite__ у созданного __FirstTile__
5. Открыть палитру тайлов через __Window > 2D > Tile palette__
6. Создать новую палитру через __Create New Palette__, задать ей имя и сохранить в папку __Tiles__
7. Перетащить __FirstTile__ на новую палитру
8. Настроить параметр __Pixel Per Unit__ у нового тайла на 64 (как размер самой картинки)
9. Настройка первого тайлсета:
   a. В папке __Art > Sprites > Environment__ выбрать тайлсет __FloorBricksToGrassCorner__  
   b. __Sprite Mode__ поменять на __Multiple__  
   c. __Pixel Per Unit__ поменять на 64  
   d. Открыть __Sprite Editor__ и в верхнем меню нажать __Slice__  
   e. Type поставить на __Grid by Cell Count__, количество колонок и строк (С и R) поставить на 3, нажать __Slice__, потом __Apply__  
   f. Теперь можно перетащить тайлсет в палитру и сохранить в папку __Tiles__  
10. Таким же образом сделлать с другими тайлсетами в папке __Art > Sprites > Environment__ (все с floor в названии)

> :art: Нарисовать первый уровень (немногим больше области обзора камеры)

11. Выделить в иерархии __Tilemap__ и у него установить в компоненте __Tilemap Renderer__ значение __Order in Layer__ на -10
12. Перетащить ассет __MetalCube__ из __Assets > Art > Sprites > Environment__ в сцену
13. Настройка порядка сортировки объектов:  
   a. Пойти в __Edit > Project Settings > Graphics__  
   b. В __Camera Settings__ изменить __Transparency Sort Mode__ на __Custom Axis__  
   c. __Transparency Sort Axis__ задать x = 0, y = 1, z = 0  
   d. В компонентах __Sprite Renderer__ у  __MetalCube__ и у героя поменять __Sprite Sort Point__ на __Pivot__  
   e. В настройках ассетов поменять __Pivot__ на __Bottom__ (или через __Sprite Editor__)  
14. Создать папку __Prefabs__ и сделать __MetalCube__ префабом

> :art: Добавить новых объектов из __Art > Sprites > Environment__, меняя Pivot, Pixel Per Unit, Order in Layer и создавая префабы


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
* https://www.youtube.com/channel/UCBDLWj5X5D9bvBa3JIMMTIQ
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
