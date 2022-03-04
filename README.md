# Юзер-Бот, що автоматизує репортування Телеграм каналів пропагандистів

Цей Телеграм Юзер-Бот використовується для автоматизації репорту пропагандистьских каналів. 

## Інсталяція 
1. По-перше, вам необхідно інсталювати Python3. Python можна завантажити за [посиланням](https://www.python.org/). Також треба [завантажити git](https://git-scm.com/download/win) (натискаємо на "Click here to download" зверху, під час встановлення декілька раз натискаємо Next. Далі перезавантажуємо комп'ютер).
2. Запустіть консоль. Для цього використовуйте комбінацію клавіш Win+R, у з'явившомуся вікні напишіть cmd та натисніть enter
3. Далі виконуємо наступні команди:
```
git clone https://github.com/Antcating/telegram_report_bot_ua
cd telegram_report_bot_ua
pip install -r requirements.txt
```
4. Переходимо за посиланням  https://my.telegram.org/, вводимо свій номер телефону та код авторизації
<br>Переходимо у вкладку API development tools, пишемо любий App title та Short name
<br>Нагорі отримуємо App api_id та App api_hash
<br>**ПЕРЕДАВАТИ КОМУСЬ `api_id` та `api_hash` НІ В ЯКОМУ РАЗІ НЕ МОЖНА!!! Вони дают можливіть контролювати вашу персональну сторінку у Телеграмі.**

## Використання 
1. Далі запускаємо бота:`python main.py`
2. По черзі вводимо:
- App api_id
- App api_hash
- Телефон вашого аккаунта у форматі +380ххххххххх
- Код автентифікації який прийде повідомленням у телеграм
3. Бот автоматично напише репорти на випадкові 150 каналів з файлу `telegram_db`.
<br>**Правильно налаштована програма буде відображати такий результат:**
<br><br>![image](https://user-images.githubusercontent.com/39994538/155859028-e83b5228-e711-4f21-bf4e-db9b1cfccb24.png)

Щоб використати інший аккаунт, треба видалили файл session_new.session у папці з програмою (або використати команду `del session_new.session`).

## Оновлення боту та бази каналів
Ми намагаємося періодично оновляти самого бота та базу пропагадистських каналів, тому рекомендуємо іноді перевіряти чи не додались нові канали. 
Якщо ви хочете оновити базу та/чи бота вам необхідно: 
1. Зайти у теку проекту
2. Відкрити консоль у цій теці 
3. Вписати команду 
``` 
git pull
```
4. База та бот оновлені, можете як вказано вище запускати бота та відсилати репорти на більшу кількість пропагандистів.


## Безпека телеграм-акаунту
Під час налаштування бота вам буде потрібно вказати одноразовий код на сайті my.telegram.org та у python модулі [telethon](https://github.com/LonamiWebs/Telethon). Перше - це офіційний сайт телеграму, друге - це дуже відомий модуль, код якого був перевірений досвідченими програмістами не один раз. Тож ваш акаунт не передається третім особам на протязі всього процесу налаштування та використання програми.
<br>Також програма емулює поведінку нового пристрою який використовує ваш акаунт. Ви можете побачити цей віртуальний пристрій в активних сеансах телеграму (Налаштування -> Приватність і безпека  -> Показати всі сеанси). Він матиме таку ж назву і тип які ви вкажете під час реєстрації на my.telegram.org. *Після виконання програми ви можете видалити цей девайс з активних сеансів.*

## Додаткова інформація
У теці проєкту знаходиться файл `telegram_db`, що містить у собі список пропагандистських каналів. Якщо ви маєте інформацію про інші канали, що не війшли у список, але заслуговують репорту - присилайте їх мені у [телеграм](https://www.t.me/Achating) або додавайте їх у реквестах на Github.


# English Version
# User-Bot, which automates the reporting of Telegrams of propagandist channels

This Usergram Bot-User is used to automate the reporting of propaganda channels.

## Installation
1. First, you need to install Python3. Python can be downloaded from [посиланням] (https://www.python.org/). You also need to [download git] (https://git-scm.com/download/win) (click on "Click here to download" at the top, click Next several times during installation. Then restart the computer).
4. If you don't have a Telegram Account, sign up for one
5. Start the console. To do this, use the key combination Win + R, in the window that appears, type cmd and press enter
6. Next, execute the following commands:
`` `
git clone https://github.com/Antcating/telegram_report_bot_ua
cd telegram_report_bot_ua
pip install -r requirements.txt
`` `
7. Follow the link https://my.telegram.org/, enter your phone number and authorization code [посиланням](https://my.telegram.org/auth)
<br> Go to the API development tools tab, write any App title and Short name and submit
<br> Above we get App api_id and App api_hash
<br> ** TRANSFER TO SOMEONE `api_id` and` api_hash` IT IS NOT POSSIBLE IN ANY WAY !!! They allow you to control your personal page in the Telegram. **

## Usage
1. Next, run the bot: `python main.py`
2. In turn, enter:
- App api_id
- App api_hash
- Phone of your account in the format + 380ххххххххх, use the phone number of your Telegram Account
- Authentication code that will be sent in a telegram
3. The bot will automatically write reports on random 150 channels from the file `telegram_db`.
<br> ** Properly configured program will display the following result: **
<br> <br>! [image] (https://user-images.githubusercontent.com/39994538/155859028-e83b5228-e711-4f21-bf4e-db9b1cfccb24.png)

To use another account, delete the session_new.session file in the program folder (or use the `del session_new.session` command).

## Update bot and channel database
We try to periodically update the bot itself and the database of propaganda channels, so we recommend that you sometimes check to see if new channels have been added.
If you want to update the database and / or bot you need:
1. Go to the project folder
2. Open the console in this folder
3. Enter the command
`` `
git pull
`` `
4. The database and bot have been updated, you can run the bot as above and send reports to more promoters.


## Telegram account security
When configuring the bot, you will need to enter a one-time code on my.telegram.org and in the python module [telethon] (https://github.com/LonamiWebs/Telethon). The first is the official site of the telegram, the second is a very well-known module, the code of which has been tested by experienced programmers more than once. Therefore, your account is not transferred to third parties during the entire process of setting up and using the program.
<br> The program also emulates the behavior of a new device that uses your account. You can see this virtual device in active telegram sessions (Settings -> Privacy & Security -> Show all sessions). It will have the same name and type that you specify when registering at my.telegram.org. * After running the program, you can remove this device from active sessions. *

## Additional Information
In the project folder there is a file `telegram_db`, which contains a list of advocacy channels. If you have information about other channels that are not included in the list, but deserve a report - send them to me in [telegram] (https://www.t.me/Achating) or add them in the requisites on Github.

