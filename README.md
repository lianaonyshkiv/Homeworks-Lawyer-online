# Homeworks-Lawyer-online
Містить результати виконання домашніх завдань. 

![1.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/1.png)

# Project name: 
Lawyer-online
    
# Description: 
Проект має на меті автоматизацію юридичної консультації. Оскільки на виконання проекту
є обмежений час - 8 тижнів - на даний момент, програма працюватиме не досконало.
За описом ситуації підбиратиметься кілька ймовірних статтей, що могли б підходити під дану ситуацію, задля конкретики згодом
програма задаватиме додаткові запитання, яких потребуватиме для остаточного рішення. Інформацію про джерела можна знайти 
ось [тут](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/wiki). Детальнішу інформацію про мотивацію вибору такої
теми можна знайти за цим [посиланням](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/wiki/%D0%94%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D1%94-%D0%B7%D0%B0%D0%B2%D0%B4%D0%B0%D0%BD%D0%BD%D1%8F-%E2%84%960).
Юридичні рішення часто бувають суб'єктивними, оскільки застосовують людський ресурс, який так чи інакше зацікавлений
у одній із сторін. Автоматизація юридичних процесів мала б зробити ці процеси менш суб'єективними та справедливішими згодом.
Очевидно, що робота над цим проектом повинна тривати набагато довше. Проте за цей період часу точно можна функціоналом цієї 
програми спростити роботу в галузі юриспруденції, а саме класифікацією кримінальних ситуацій, а згодом вже покращувати.

Вхідні дані: ситуація від користувача
Вихідні: підбірка статтей кримінального кодексу України

# Structure:
*docs(усі текстові файли, що були необхідними для виконання дз):

    adt - опис АТД використаних при виконанні домашніх завдань
    analysis - аналіз результатів, що вийшли за час виконання циклу домашніх завдань
    api - функціональні можливості Natural Language API
    data - опис даних, що отримувались для досягнення результату та плану роботи над ними
    get_data_capacity - опис отриманих даних після виконання циклу домашніх завдань
    modules - можливості можулів, що використовуватимуться для аналізу даних
    posts - рецензії 3 дописів, що стосуються теми домашнього завдання та розділу комп'ютерних наук, зачіпленого в ньому
    proposition - опис того, що можна зробити за допомогою Natural Language API
    questions - відповіді на запитання для вибору теми
    requirements - функціональні та нефункціональні вимоги на систему
    
examples(приклади для роботи з модулями для обробки даних):

    kku.csv - файл із вмістом Кримінального кодексу України, що використовувався для зчитування
    modules_for_data.py - модуль з рикладами використання бібліотек для обробки даних
    
images(містить зображення, що використовувались для офомлення wiki та README):

    0.png
    1.png
    ...
    
modules(папка із модулями для реалізації запланованого у циклі домашніх завдань):

    kku(папка для роботи з файлом вмісту Кримінального кодексу України):
        trans - папка із вмістом реалізації перекладача
        article-adt_sample.py - модуль-приклад використання Article ADT
        articls_with_punkts.xlsx - результат обробки Кримінального кодексу
        chocing_relevant_information_in_articles.py - модуль із реалізацією Article ADT як класу Article(детальніше про роботу методів
            можна прочитати в docs.adt), цей модуль також підбирає важливі слова та синоніми до кожної статі за допомогою методу у цьому             класі
        creating_file_for_articles_with_punkts.py - модуль із реалізацією KKU ADT як клас KKU, аналогічно як вище, прочитати про методи 
            детальніше можна у названому файлі, цей модуль власне створює файл-результат обробки кримінального кодексу                               articles_with_punkts.xlsx.
        kku.csv - файл із вмістом Кримінального кодексу
        kku_adt_sample.py - модуль приклад використання KKU ADT
    pytextrank - папка із вмістом реалізації підбору важливих слів з речення
    samples_reading(папка із модулями для зчитуання ситуацій-прикладів):
        1.csv - файл з вмістом збірника задач з кримінального права
        2.csv - файл з вмісто збірника задач з кримінального права
        sample_adt_sample.py - модуль-пиклад використання Sample ADT
        samples.py - модуль для реалізації Sample ADT як клас Sample, детальніше про методи цього класу можна прочитати у файлі, 
            описаному вище, цей можуль створює файли-результати обробки збірників
        samles.xlsx - результат обробки збірника задач з кримінального права 1
        samles_2.xlsx - результат обробки збірника задач з кримінального права 2
    web_application(папка із вмістом усього необхідного для створення веб-застосунку та обробки користувацкого введення):
        my_app(папка із застосунком):
            reading_users_situation(папка для збереження усього пов'язаного із обробкою користувацьких ситуацій):
                persons(папка для збереження модулів для обробки дійових осіб у ситуації):
                    person.py - модуль для реалізації класу Person
                read_save_input.py - модуль для реалізації UsersSituaion ADT як класу UsersSituation, використовується для зчитування                       користувацьких даних та їх обробки(про методи детальніше у файлі описаному вижче)
            static(папка для збереження усіх файлів необхідних для оформлення веб-застосунку)
            template(папка для збереження html файлів для веб-застосунку):
            articles_with_punkts.xlsx - файл із статтями, пунктами та важливими словами до кожної статті
            result.xlsx - файл для запису ористувацтких даних
            run.py - модуль для запуску застосунку
            users_history.xlsx - файл для збереження користувацької історії
            
samples(папка із прикладами використання АТД):

    2.csv - файл із даними для Samples ADT 
    articles_adt_sample.py - модуль-приклад використання Articles ADT
    articles_with_punkts.xlsx - файл із даними для використання Articles ADT
    kku.csv - файл із даними для використання KKU ADT
    kku_adt_sample.py - модуль-приклад використання KKU ADT
    sample_adt_sample.py - модуль приклад використання Sample ADT
    

# Table of Contents: 
1. [Installation](#installation)
2. [Usage](#usage)
3. [Contributing](#contribution)
4. [Credits](#credits)
5. [License](#license)

# Installation:

Для використання достатньо просто 
<pre>
git clone https://github.com/lianaonyshkiv/Homeworks-Lawyer-online
</pre>

Після цього запустити run.py, що у my_app, та перейти за посиланням у терміналі
![8.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/8.png)

# Usage:

Після переходу на сайт побачите таке відображення
![9.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/9.png)
Гортаючи вниз, буде
![10.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/10.png)
![11.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/11.png)
![12.png](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/12.png)
На останньому зображенні видно, що є можливість увести свою ситуацію у спеціальновідведеному місці.
Введіть її та отримайте результат.
Працює лише українською мовою.
Заповнювати усі поля не обов'язково.

Наприклад після вводу "Шахрайство" результат виглядатиме так
![14.jpg](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/14.png)
![15.jpg](https://github.com/lianaonyshkiv/Homeworks-Lawyer-online/blob/master/images/15.png)

# Contribution:

Будь-ласка дотримуйтесь стилю при заванаженні версій. Загалом "fork-and-pull" Git workflow.

1) Fork the repo on GitHub
2) Clone the project to your own machine
3) Commit changes to your own branch
4) Push your work back up to your fork
5) Submit a Pull request so that we can review your changes

# Credits:

Тут можете бути Ви!

# License:
[MIT](https://choosealicense.com/licenses/mit/)
