# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
1.2 [Бизнес-требования](#business_requirements)  
1.2.1 [Исходные данные](#initial_data)   
1.2.2 [Границы проекта](#project_boundary)  
1.3 [Обзор аналогов](#analogues) 
1.3.1 [Myth Defence](#Myth_Defence)
1.3.2 [Plants vs. Zombies](#PlantsVSZombies)
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)  
2.3.1 [Классы пользователей](#user_classes)  
2.3.2 [Аудитория приложения](#application_audience)  
2.3.2.1 [Целевая аудитория](#target_audience)  
2.3.2.1 [Побочная аудитория](#collateral_audience)  
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)
3.1 [Функциональные требования](#functional_requirements)  
3.1.1 [Основные функции](#main_functions)  
3.1.1.1 [Игровой процесс](#game_proccess)  
3.1.1.2 [Строительство башен](#build_tower)  
3.1.1.3 [Получение ресурсов](#gain_resources)  
3.1.1.4 [Потеря жизней](#lose_healthpoits)  
3.1.2 [Ограничения и исключения](#restrictions_and_exclusions)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.1.1 [Требования к удобству использования](#requirements_for_ease_of_use)  
3.2.1.2 [Требования к безопасности](#security_requirements)   
3.2.2 [Ограничения](#restrictions)

<a name="intro"/>

# 1 Введение

<a name="appointment"/>

## 1.1 Назначение
В этом документе описаны функциональные и нефункциональные требования к игровому приложению «Gnome Fortress» для ОС Windows. Этот документ предназначен для команды разработчиков, которая будет реализовывать и проверять корректность работы приложения.

<a name="business_requirements"/>

## 1.2 Бизнес-требования 

<a name="initial_data"/>

### 1.2.1 Исходные данные
Видеоигра – это специальная компьютерная программа или электронное устройство, реализующие игровой процесс. По всему миру в производство видеоигр вовлечены миллионы людей самых разных специальностей: художники, программисты, дизайнеры, издатели, продавцы, промышленники и многие другие. Ежегодная прибыль рассматриваемого сектора экономики варьируется в пределах 10-15 миллиардов долларов. Игры жанра "Tower defence" предоставляют прекрасную возможность отдохнуть физически и развлечься интеллектуально. 

<a name="project_boundary"/>

### 1.2.2 Границы проекта
Игра должна иметь графический интерфейс, для того, чтобы обеспечить взаимодействие игрока с компьютером, в ней должны быть реализованы стандартные правила игры, такие как: постройка защитных сооружений, автоматически истребляющих находящихся в зоне поражения врагов, генерация полчищ врагов, движущихся к определённой позиции, уничтожения противника, застройка и создание проходов (лабиринтов) для врагов, поиск противниками оптимального кратчайшего пути до определенной точки (далее «Замка»), лучшение зданий и их характеристик, проигрыш в случае достижения определённым количеством противников «Замка». 

<a name="analogues"/>

## 1.3 Обзор аналогов

<a name="Myth_Defence"/>

### 1.3.1 «Myth Defence»
«Myth Defense» - классический игра жанра Tower Defense: игроку предлагают строить башни, которые уничтожают выходящие из определенной точки карты силы противника. Для победы нужно пережить определенное число волн с противниками. Изначально у игрок имеет 20 жизней, как только один из вражеских юнитов проходит всю карту живым и невредимым, игрок теряете одну жизнь. Потеря всех жизней – проигрыш. В игре есть несколько различных карт, отличающихся между собой не только оформлением, местностью и разбросанными препятствиями, но и количеством точек выхода вражеских юнитов. На самой простой карте враги выходят с одного конца карты и движутся к другому, а на самых сложных может быть до трех выходов и трех входов, что серьезно осложняет игру. 

<a name="PlantsVSZombies"/>

### 1.3.2 «Plants vs. Zombies»
«Plants vs. Zombies» -  стратегия в жанре Tower Defense, в которой задачей игрока является защита дома от зомби. Игровое поле разделено на сетку из пяти или шести горизонтальных рядов и девяти столбцов, и, как правило, стилизовано под лужайку дома. Игрок размещает различные типы растений и грибов на отдельных клетках сетки. Каждое растение имеет свою уникальную способность, которая активируется при использовании. Некоторые типы зомби также имеют свои способности, против которых могут быть более эффективны те или иные растения. 

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы
Продукт должен являться игровым приложением для OC Windows и иметь простой интерфейс пользователя. Приложение должно быть реализовано с помощью библиотеки SFML и написано на языке программирования С++. 

<a name="user_interface"/>

## 2.2 Интерфейс пользователя

<a name="user_specifications"/>

## 2.3 Характеристики пользователей

Для данного приложения не предусмотрены особые виды пользователей, т.к. он не имеет каких-либо ограничений.

<a name="user_classes"/>

### 2.3.1 Классы пользователей

| Класс пользователей | Описание |
|:---|:---|
| Стандартный пользователь | Пользователи, которые могут играть в данное приложение |

<a name="application_audience"/>

### 2.3.2 Аудитория приложения
Люди любой возрастной категории, желающие скоротать времени за строительством башен.

<a name="target_audience"/>

#### 2.3.2.1 Целевая аудитория
Люди младшей и средней возрастной категории, которые проводят больше времени в ПК.

<a name="collateral_audience"/>

#### 2.3.2.2 Побочная аудитория
Люди любой возрастной категории.

<a name="assumptions_and_dependencies"/>

## 2.4 Предположения и зависимости
1. Приложение не может работать при отсутствии файлов msvcp140.dll и vcruntime140.dll, которых требует огромное количество игр, написанных на С++. Эти файлы должны поставляться вместе с приложением.

<a name="system_requirements"/>

# 3 Системные требования

<a name="functional_requirements"/>

## 3.1 Функциональные требования

<a name="main_functions"/>

### 3.1.1 Основные функции

<a name="game_proccess"/>

#### 3.1.1.1 Игровой процесс

*Описание.** Для выполнения игровых операций, используются следующие клавиши клавиатуры, а также компьютерная мышь.

| Клавиша | Выполняемая функция | 
|:---|:---|
| W/Up | Поворот блока по часовой срелке |
| A/Left | Смещение блока влево на 1 клетку, если действие возможно |
| D/Right | Смещение блока вправо на 1 клетку, если действие возможно |
| S/Down | Смещение блока вниз дополнительно на 1 клетку, если действие возможно |
| Прокрутка колёсика мыши | в зависимости от направления увеличивает или уменьшает масштаб |
| Space | Пауза, т.е. остановка игрового процесса, до повторного нажатия данной клавиши |
| Левая кнопка мыши | взаимодействие с объектом, над которым распологается курсор |

<a name="build_tower"/>

#### 3.1.1.2 Строительство башен.
**Описание.** При выборе типа башни для последующей постройки, игрок волен построить её.  
**Требования.** Наличии достаточного количества ресурсов, места для строительва (место не занято другой башней, врагом, элементами ландшафта), а также возможности пройти всем текущим и последующим противникам добраться до замка. 

<a name="gain_resources"/>

#### 3.1.1.3 Получение ресурсов.
**Описание.** При убийстве противников игрок получает определенное количество ресурсов.  
**Требования.** Различные виды врагов приносят своё значение ресурсов. Различные виды башен негативно или позитивно влияют на получаемые с врагов ресурсы. Ресурсы можно тратить на строительсво новых башен или улучшение имеющихся.  

<a name="lose_healthpoits"/>

#### 3.1.1.4 Потеря жизней.
**Описание.** При пересечении противником ворот замка отнимается определенное количество жизней.  
**Требования.** Разные виды врагов наносят свой урон замку. Если количество жизней оказывается равно нулю, то игрок проигрывает.

<a name="restrictions_and_exclusions"/>

### 3.1.2 Ограничения и исключения
1. Приложение выполняет весь функционал без наличия подключения к Интернету;
2. Для работы приложения должны присутствовать файлы msvcp140.dll и vcruntime140.dll, они должны поставляться вместе с игрой.

<a name="non-functional_requirements"/>

## 3.2 Нефункциональные требования

<a name="quality_attributes"/>

### 3.2.1 Атрибуты качества

<a name="requirements_for_ease_of_use"/>

#### 3.2.1.1 Требования к удобству использования
1. Понятность в управлении приложением используя компьютерную мышь;
2. Интуитивно понятный интерфейс.
3. Быстрый отклик приложения.

<a name="security_requirements"/>

#### 3.2.1.2 Требования к безопасности
Данное приложение является полностью безопасным, т.к. оно не собирает какую-либо информацию о пользователе и не имеет доступа в Интернет.

<a name="restrictions"/>

### 3.2.2 Ограничения
1. Приложение должно быть реализовано на языке C++14(либо выше);
2. Приложение должно использовать библиотеку SFML версии 2.4.1(либо выше) и выше, для обеспечения графческого интерфейса;
3. Приложение должно стабильно работать на Windows 7/10/11.
