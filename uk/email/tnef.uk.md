{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ТНЕФ",
  "description":"Дізнайтеся про формат файлу TNEF та API, які можуть створювати та відкривати файли TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл TNEF?

Transport Neutral Encapsulation Format (TNEF) є власністю Microsoft для інкапсуляції вкладень електронної пошти на основі програмного інтерфейсу обміну повідомленнями (**MAPI**). Microsoft Outlook і Microsoft Exchange Server повністю підтримують TNEF, а пізніше декодують TNEF у MAPI та відображають відформатовані листи. Вкладення електронної пошти з кодуванням TNEF має тип MIME MS-TNEF і зберігається як winmail/win.dat. Вкладення у winmail .dat містить таку інформацію:


|Повідомлення|Об'єкти OLE|Функції Outlook
---|---|---|
|<ul><li> Оригінальні вкладення до повідомлень</li><li> Оригінальна відформатована версія</li><li> шрифти, розмір тексту та кольори тексту</li></ul> |<ul><li> вбудовані картинки</li><li> вбудовані документи Office</li></ul> |<ul><li> нестандартні форми</li><li> кнопки голосування</li><li> запити на зустрічі</li></ul>


Інші служби електронної пошти, які не підтримують TNEF, представляють звичайний текст для повідомлень у форматі TNEF. Outlook вбудовує розширений формат повідомлення у файли TNEF (OLE) або певні функції Outlook (форми, кнопки опитування та запрошення на конференцію). Дозволити явне кодування TNEF у поштовому клієнті Outlook неможливо, однак вибір формату RTF для надсилання електронної пошти неявно полегшує кодування TNEF.

## Формат файлу TNEF

Алгоритм даних TNEF створює згладжену структуру з розширених ієрархічних властивостей повідомлень. Потім ці згладжені структури використовуються для представлення послідовного потоку даних, що складається з певних властивостей.

У деяких ситуаціях, коли властивості зустрічаються в групах або мають кілька значень, потік може містити підрахунки та відступи для забезпечення певного вирівнювання даних. Особливою ситуацією, коли використання цього алгоритму є вигідним, є непідтримуване середовище обміну повідомленнями. У таких середовищах властивість розширеного повідомлення кодується в послідовний потік даних за допомогою TNEF Writer. Крім того, властивості, які не належать до основного TNEF, можуть бути інкапсульовані під час передачі. Потім ці інкапсульовані властивості стають доступними шляхом декодування через TNEF, щоб гарантувати доступність усіх властивостей вихідного повідомлення клієнтській програмі.

У TNEF усі типи числових даних мають порядковий порядок байтів, а їхній розмір перевищує один байт. Обробка цих числових значень на платформах без порядкового порядку вимагає виконання відповідних перетворень, щоб отримати правильні значення. Рядкові значення представлено у форматі доповненої форми Бекуса-Наура (ABNF) відповідно до специфікацій [RFC5234]. Коли рядок закінчується нульовим символом, він також включається; наприклад, `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="Формат файлу TNEF" >}}

## Атрибути TNEF і правила обробки ##

Потік даних у TNEF починається з номера старої версії, підпису, значення примітивного ключа та атрибута, що представляє кодову сторінку. Ця кодова сторінка створюється, коли кодувальник записує атрибути та властивості ANSI. Після цього потік перетворився на серію атрибутів, у якій спочатку вишикувалися атрибути повідомлення, а потім – атрибути вкладення. Різні характеристики повідомлень і вкладень містяться в спеціальних атрибутах, таких як attMsgProps, attAttachment і attRecipTable. Атрибути, які з’являються в потоці TNEF, містять структуру, властивості повідомлення та перетворення, необхідні для взаємодії з властивостями повідомлення. Кожен атрибут складається з ідентифікатора, розміру та даних атрибута, контрольної суми та рівня відповідно до його застосування.

## Відношення до протоколів та інших алгоритмів ##

Системи, які мають поганий механізм відображення формату розширеного повідомлення, потребують алгоритму даних TNEF для транспортування. Використовуючи тип медіа ms-TNEF, вихід алгоритму складається з файлу вкладення (winmail.dat) і основної частини MIME, зазначеної в [RFC2045]. Тіло звичайного текстового повідомлення передається за допомогою UUENCODE відповідно до специфікації [MSDN-UAF], і це тіло повідомлення або еквівалентний метод декодується на стороні одержувача. Крім того, TNEF може передавати дані повідомлень за допомогою різних інтернет-протоколів, таких як SMTP, POP3, IMAP4, а також протоколів MIME відповідно до стандарту RFC2045.

## Заява про застосовність ##

На додаток до простої передачі повідомлень, початкова програма TNEF мала бути створена для використання класів повідомлень і підтримки додаткових функцій, які не мають вихідної підтримки в транспортному протоколі. Цю програму було додатково вдосконалено для передачі розширених властивостей повідомлень і іменованих властивостей, які сучасні клієнти обміну повідомленнями використовують зараз. Для відповідності оригінальній реалізації оригінальний синтаксис атрибута зберігається, а спеціальний атрибут зберігає нові властивості повідомлення окремо.

## Список літератури

* [Формат транспортної нейтральної інкапсуляції](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Адреси електронної пошти та адресні книги в Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: алгоритм даних транспортного нейтрального формату інкапсуляції (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

