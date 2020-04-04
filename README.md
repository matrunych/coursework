Course-work for first year in course "Programming fundamentals".

# Призначення та коротка характеристика програми
Програма призначена для того, щоб допомогти користувачу з пошуком бюджетного житла для мінімізації витрат на харчування.
Вхідними даними користувача є місто, де він/вона хоче зупинитись та ціна за ніч за двох у готелі на яку розраховує.
Програма бере дані з сайту https://hotelscan.com/ru та Zomato. Результатом виконання програми є html карта, на якій позначені готелі на заклади харчування. Над готелями є надпис. а точніше: назва його, ціна та кількість ресторанів поблизу; над ресторанами - назва та середня ціна за трапезу для двох.

# Структура програми з коротким описом модулів, функцій, класів та методів.
Усі модулі у папці modules
Основним модулем при запуску програми є flask_hotel_search.py, у якому програма буде запущена на сервері. 
У модулі PARSE_hotelscen.py модуль parsing відбувається парсинг сайту з готелями та запис даних у словник. 
Модуль MAP_new.py функція create_map() обробляє словник, шукає дані у zomato та позначає рузьтати на карті. 
Функція main_creatir() запускає попередню функцію.
Модуль zomatp_1.py і клас Zomato використовуються для дістання інформації з сервісу zomato з ключем користувача.

# Коротка інструкція по користуванню програмою
Програма розроблена на фласку, після запуску файлу flask_hotel_search.py користувач перейде на посиланням. Там введе місто де зупиниться та ціну, якщо ціну не введено, будуть розглядатися усі готелі без обмежень за ціною. Після цього аналізуються отримані дані та виведено карту. Якщо місто, яке ввів користувач, відсутнє на Zomato, користувач буде повідомлений, якщо місто введено неправильно, доведеться ввести ще раз.

# Опис тестових прикладів для первірки працездатності програми.
Якщо введено неправильно місто, користувач повинен увести ще раз.
Якщо не введено ціну, обробляються усі готелі.
Якщо введено місто, яке відстутнє на сервісі Zomato , користувач буде повідомлений та запрошений увести місто ще раз
У разі введених правильно даних, здійснюється пошук, обробка та виведення карти для користувача.
