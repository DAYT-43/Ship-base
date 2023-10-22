# Ship-base
Проект по сбору информации о всех кораблях построенных и находящихся в стадии стротельства в России, для получения реестра кораблей интересных компании

# “Реестр Судостроения для ОР”

Время ознакомления с проектом: 9 - 12 минут

<aside>
⚠️ Данная статья является кратким изложение проекта, без углубления в детали.

</aside>

## Содержание:

**Предисловие и краткое описание проекта**: 

**Профиль компании**

**Проблема**: 

**Обзор проекта**

**График и бюджет**

**Перспективы и развитие проекта**

**Отчет о проделанной работе по проекту**

## **Предисловие и краткое описание проекта**:

Для отдела была разработана большая база данных по контролированию строительства кораблей интересных для компании, с присвоенным названием **"Реестр Судостроения"**. 

База создана с использованием парсинга карточек и новостных статей на Python, WebScraper и Excel. 

Визуализация данных была осуществлена с помощью сводных таблиц в Excel. Начальный датасет содержал около 70 тысяч строк, а финальная база данных состоит из 400 строк (Кораблей) и содержит 100 параметров. 

Парсинг для исходной базы производился из двух сайтов, позже собрали 94 источника информации о строительстве кораблей.

Для выявления актуальных стадий строительства завода по нескольким заводам провел парсинг статей за 15 лет, а это сотни тысяч новостей (строк).

- *Скрины выгрузки статей для выявления стадий строительства корабля*
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/9676cdc6-1f9f-4ff3-b4b5-28bec190fa28/Untitled.png)
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/b22d36bc-9e55-49ea-945f-3025810fcbff/Untitled.png)
    

### **Итоги работ:**

- Руководитель всегда имеет быстрый отчет о текущем состоянии кораблей. Если готовить подобный отчет с нуля, на один завод уходит 2 часа, а с реестром максимум 10 мин;
- Руководитель всегда имеет под рукой отчет со всей хронологией сделок для предоставления высшему руководству;

### **Польза для меня:**

- Приобрел ценные навыки в области парсинга на Python;
- Повысил скорость сбора информации в интернете разы;
- Отточил навыки подготовки “сырых” данных к аналитике на реальном проекте;
- *Основная рабочая область реестра*
    
    ![Screenshot_2.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/f1fc8158-0b20-4324-9c6a-878dae9f3c3e/Screenshot_2.png)
    
    Дополнительные листы 
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/a3bfae15-73d4-4e98-adce-122dfcb4a88a/Untitled.png)
    
- *Общий дашборд*
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/8e1ee8f6-2cdf-4257-95bd-1a098c3563be/Untitled.png)
    

## **Профиль компании:**

**Русская Теплоизоляционная Компания** - Единственное в России производственное предприятие полного цикла по производству технической теплоизоляции из вспененного синтетического каучука (трубки, рулоны, ленты и др.), все этапы технологического процесса которого осуществляются в России по программе импортозамещения. Компания ведет работу через дистрибьюторов, но при необходимости сама принимает участие в важных тендерах

## **Проблема**:

**Проблема №1: Отсутствие готовых решений.**

Отдел работает в нефтегазовой и судостроительной сферах. Если для нефтегаза существуют готовые онлайн платформы для получения всей необходимой информации, то для судостроения дела обстоят намного хуже. Возникла задача понять, какое количество интересных кораблей сейчас находятся в необходимом статусе, чтобы успеть вовремя отработать и совершить поставку. 

**Проблема №2: Ограниченность информации и разрозненность.**

Для сбора полноценной информации о судах необходимо использовать различные источники, которых более сотни, но для нашего случая достаточно около 7-10.

## **Обзор проекта:**

Сейчас данный реестр состоит из нескольких блоков и нескольких листов и является рабочим инструментом для контроля всех текущих строящихся кораблей. 

Поскольку  у компании есть свои дистрибьюторы, которые также ведут работу по направлению судостроения, их сделки также фиксируются в данном реестре. 

После появления информации о проработке менеджером определенного корабля, информация по кораблю заноситься в CRM Битрикс 24, как Объект и сделка.

### Функции проекта ****“Реестр Судостроения”

1. Позволяет быстро получать информацию о необходимых кораблях, с помощью фильтров Excel;
2. Аккумулирует информацию  и распределяет по блокам;
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/154edecc-79b9-4c25-8372-b1dd9cd11092/Untitled.png)
    
3. Фиксирует продажи дистрибьюторов и компании в “блоке продаж”;
4. С помощью формул Excel:
    1. Высчитывает даты строительства кораблей;
    2. Сигнализирует, когда требуется обратить внимание на корабль;
    3. Распределяет информацию на другие листы, к примеру информацию по заводам.

### **Стек технологий** :

Прототипирование и дизайн: Microsoft Excel

Сбор информации: Python (requests, BeautifulSoup)

Форматы файлов: html, csv, xlsx

## **График и бюджет**

На проект был выделен месяц и ресурсы одного специалиста. В итоге в рабочее состояние проект пришел через две недели, далее в рабочем режиме происходило заполнение информации по каждому кораблю.

## **Перспективы и развитие проекта**

- Можно создать пользовательский интерфейс, загрузить данные на сервер, разработать программу с автоматическими сборщиками данных и предварительно обученными моделями NLP, сделать быстрое формирование отчетности.

## Отчет о проделанной работе по проекту

Для большего понимания проделанной работы, ниже частично опишу размышления и решенные задачи.

Датасет собран из сайтов водный транспорт https://fleetphoto.ru/  и Корабел.ру https://www.korabel.ru/, затем заполнено вручную с сайтов Медиапалуба и др.

### Создание парсера сайта “Водный транспорт” на Python:

Необходимо, чтобы парсер скачивал информацию о всех проектах и делал страницу в Excel  файле с разбивкой по листам (по Судостроительным заводам)

Изначально план был такой, но…

Изучая структуру сайта Водный транспорт и Корабел.ру с целью понять что их связывает, найти общие ключи для данных, написал парсер, и получил список заводов с сайта Водный транспорт. Но чтобы получить необходимые данные быстрее, нашел и воспользовался решением из коробки, так называемым WebScraper и получил результат быстрее.

- Заметки из блокнота (исследование сайтов)
    
    Сайт [korabel.ru](http://korabel.ru) 
    
    - Скрины
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/566f6b99-726b-4017-87bf-699706847952/Untitled.png)
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/23af2585-60de-407c-9fa4-e27119347e7d/Untitled.png)
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42081a4a-6d6a-41bd-9032-71036f83daa4/Untitled.png)
        
    
    Требуемые судостроительные предприятия России находятся по адресу 
    
    https://fleetphoto.ru/entities/?rid=1
    
    [https://fleetphoto.ru/entities/?rid=](https://fleetphoto.ru/entities/?rid=1)2 если поставить цифру 2, то будут судостроительные предприятия Беларуссии, и т.д. (цифра отвечает за страну)
    
    С данной страницы нужно получить все ссылки на все судостроительные заводы, всего 8 страниц данных
    
    пагинация, каждая страница по 50 заводов 
    
    https://fleetphoto.ru/entities/?rid=1&st=350
    
    **rid:** 1 **st:** 350
    
    оффсет +50
    
- Код / Code Python
    
    ```python
    import requests
    import lxml
    from bs4 import BeautifulSoup
    from requests.api import head
    import csv
    from datetime import datetime
    
    # создаем словарь с заголовками запроса
    headers = {
        'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9',
        'user-agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.0.0 Safari/537.36'
    }
    
    def get_data(url):
        # отправим гет запрос на страницу, распечатаем результат, получим результат 200
        response = requests.get(url=url, headers=headers)
        print(response)
    
     
    def main():
        get_data(url='https://fleetphoto.ru/entities/?rid=1')
    
    if __name__ == '__main__':
        main()
    # Output <Response [200]>
    ```
    
    ```python
    import requests
    import lxml
    from bs4 import BeautifulSoup
    from requests.api import head
    import csv
    from datetime import datetime
    
    # создаем словарь с заголовками запроса
    headers = {
        'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9',
        'user-agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.0.0 Safari/537.36'
    }
    
    def get_data(url):
        response = requests.get(url=url, headers=headers)
        # print(response)
    # Записываем информацию в html файл
        with open(file='index3.html', mode='w', encoding='UTF-8') as file:
            file.write(response.text)
      
    def main():
        get_data(url='https://fleetphoto.ru/entities/?rid=1')
    
    if __name__ == '__main__':
        main()
    ```
    
    ```python
    import requests
    import lxml
    from bs4 import BeautifulSoup
    from requests.api import head
    import csv
    from datetime import datetime
    
    # создаем словарь с заголовками запроса
    headers = {
        'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9',
        'user-agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.0.0 Safari/537.36'
    }
    
    def get_data(url):
        response = requests.get(url=url, headers=headers)
        # print(response)
    # Комментирую код, чтобы не долбить сайт запросами
       # with open(file='index3.html', mode='w', encoding='UTF-8') as file:
        #    file.write(response.text)
      
    def main():
        get_data(url='https://fleetphoto.ru/entities/?rid=1')
    
    if __name__ == '__main__':
        main()
    ```
    
- Полученный список компаний с сайта
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/7e4285c8-c355-457c-86d7-9b6905c7adce/52fe8063-d1a4-482d-8e57-a3135a168bcd/Untitled.png)
    

### Сбор информации с помощью WebScraper:

Отчет руководству о проделанной работе с таймингом

В данном отчете не учитывается сбор статей, так как он проводился после создания базы.

- Скрин отчета:
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/aaf9c881-7288-4425-ac96-3464a42320a4/Untitled.png)
    

Учитывается “чистое” затраченное время, тоесть время без перерывов и переключений на другие задачи.

1. После нескольких часов тренировок понял логику работы парсера и его недостатки.
2. Сформировал парсеры для сайта водный транспорт, поставил парситься на выходные
3. Сформировал парсеры для сайта корабел, поставил парситься на выходные

| № | Задача | Кол-во минут | выгружено строк |
| --- | --- | --- | --- |
| 1 | Ознакомление сайтом, с которого будет забираться информация | 60 |  |
| 2 | Формирование парсера №1 - Сайт https://fleetphoto.ru/ Выгрузка судов с карточки завода | 180 |  |
| 3 | Работа парсера №1- Сайт https://fleetphoto.ru/ | 120 | 32988 |
| 4 | Формирование парсера №2- Сайт https://fleetphoto.ru/ Выгрузка карточек судов | 90 |  |
| 5 | Работа парсера №2 - Сайт https://fleetphoto.ru/ | 1980 | 58293 |
| 6 | Ознакомление сайтом, с которого будет забираться информация | 40 |  |
| 7 | Формирование парсера №3 - Сайт https://www.korabel.ru/ | 120 |  |
| 8 | Работа парсера №3 - Сайт https://www.korabel.ru/ | 240 | 2389 |
| 9 | Обработка таблицы №1 с сайта -  https://fleetphoto.ru/ | 30 |  |
| 10 | Обработка таблицы №2 с сайта -  https://fleetphoto.ru/ | 180 |  |
| 11 | Обработка таблицы №3 с сайта - https://www.korabel.ru/ | 60 |  |
| 12 | Создание реестра и заполнение, сначала данными с https://fleetphoto.ru/, потом с  https://www.korabel.ru/ | 120 |  |
| 13 | Ручная фильтрация и заполнение реестра текущими статусами кораблей | 100 |  |
| 14 | Проверка и довнесение военных кораблей, на которых нет карточек, путем сравнения таблицы 1 и 2 | 120 |  |
| 15 | Создание общей аналитики по реестру с (диаграммы, сводки) | 120 |  |
|  | Минут всего: | 3560 |  |
|  | Часов всего: | 59,33 |  |
|  | Рабочих дней, при 50% занятости на проекте (8 часов в рабочем дне): | 14,83 | по факту 12 суток |
|  | Часов на ознакомление с сайтами: | 1,7 |  |
|  | Часов на формирование парсеров: | 6,5 |  |
|  | Часов на работу парсеров: | 39 |  |
|  | Часов на работу с данными: | 12,2 |  |

Можно рассчитать приблизительное  количество времени работы парсера ссылаясь на то, что один переход на сайте занимает 2 секунды

---

Обработка таблиц в Excel. На обработку ушло много времени, поскольку **базы данных по судостроению имеют недостоверную информацию**, поэтому мы забирали из полученных таблиц суда, которые не сданы в эксплуатацию около 300 штук и обрабатывали каждый вручную

---

На двух сайтах, одни и те же данные написаны по разному, зацепиться почти не за что, поэтому **автоматизировать работу не удалось, приходилось проходится по каждой вкладке вручную**

---

По факту ушло ровно 12 суток до того момента, когда таблица приобрела вид, когда с ней может работать менеджер

---

Если писать парсер с нуля, на текущем уровне, на один парсер может уйти неделя (1500-2000 минут) но с каждым парсером будет ускоряться. **Парсер можно написать за 3-12 часов**

---

---

Выводы:

---

1. Мы точно знаем, что на разработку подобной базы, **по любому сегметну рынка уйдет меньше 11 суток** (при посвящении проекту не менее 40% времени в день)

---

2. Данный проект стоил своего времени, потому-что:

---

1) У нас **теперь есть 3 готовых парсера** на два сайта и если понадобиться сделать новые парсеры на сайт, это получиться сделать в 2-3 раза быстрее;

---

2) **Есть готовая база данных для создания аналитики и инфографики** для отделов продаж и маркетинга по судостроительному сегменту рынка;

---

3) **Базу данных можно актуализировать в любой момент**, выгрузив данные из раздела "Обновление базы данных" на сайте Водный транспорт, а также можно проверять данный раздел вручную, с целью актуализации БД;

---

4) Возвращаясь к вопросу о **скорости сбора данных**, если бы данную базу пришлось собирать специалисту вручную до текущего состояния, у него ушло бы больше 60 чистых часов механической работы только на создание реестра, а о базе всех 60000 строк и говорить не стоит, поскольку для базы лишь 400 потенциально полезных строк.
