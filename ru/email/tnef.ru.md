{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ТНЭФ",
  "description":"Узнайте о формате файлов TNEF и API-интерфейсах, которые могут создавать и открывать файлы TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .TNEF вариант №

Transport Neutral Encapsulation Format (TNEF) — это собственный формат Microsoft для инкапсуляции вложений электронной почты на основе интерфейса программирования приложений для обмена сообщениями (**MAPI**). Microsoft Outlook и Microsoft Exchange Server полностью поддерживают TNEF, а затем декодируют TNEF в MAPI и отображают отформатированные письма. Вложение электронной почты с кодировкой TNEF имеет тип MIME MS-TNEF и сохраняется как winmail/win.dat. Вложение в winmail .dat содержит следующую информацию:


|Сообщение|OLE-объекты|Функции Outlook
---|---|---|
|<ul><li> Вложения исходного сообщения</li><li> Оригинальная отформатированная версия</li><li> шрифты, размеры текста и цвета текста</li></ul> |<ul><li> встроенные картинки</li><li> встроенные офисные документы</li></ul> |<ul><li> пользовательские формы</li><li> кнопки голосования</li><li> запросы на встречи</li></ul>


Другие службы электронной почты, не поддерживающие TNEF, представляют обычный текст для сообщений в формате TNEF. Outlook встраивает расширенный формат сообщения в файлы TNEF (OLE) или определенные функции Outlook (формы, кнопки опроса и приглашения на конференцию). Санкционирование явного кодирования TNEF в почтовом клиенте Outlook невозможно, однако выбор формата RTF для отправки электронной почты неявно облегчает кодирование TNEF.

## Формат файла TNEF

Алгоритм данных TNEF устанавливает плоскую структуру на основе богатых иерархических свойств сообщения. Эти плоские структуры затем используются для представления последовательного потока данных, состоящего из определенных свойств.

В некоторых ситуациях, когда свойства встречаются в группах или имеют несколько значений, поток может включать счетчики и отступы для обеспечения определенного выравнивания данных. Отличительной ситуацией, когда использование этого алгоритма выгодно, является неподдерживающая среда обмена сообщениями. В таких средах расширенное свойство сообщения кодируется в последовательный поток данных модулем записи TNEF. Кроме того, свойства, не принадлежащие базовому TNEF, могут быть инкапсулированы во время передачи. Затем эти инкапсулированные свойства становятся доступными путем декодирования через TNEF, чтобы обеспечить доступность всех свойств исходного сообщения для клиентского приложения.

В TNEF все числовые типы данных имеют обратный порядок байтов и их размер больше одного байта. Обработка этих числовых значений на платформах, отличных от прямого порядка байтов, требует выполнения соответствующих преобразований для получения правильных значений. Строковые значения представлены в расширенном формате Бэкуса-Наура (ABNF) в соответствии со спецификациями [RFC5234]. Когда строка заканчивается нулевым символом, она также включается; например, `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="Формат файла TNEF" >}}

## Атрибуты TNEF и правила обработки ##

Поток данных в TNEF начинается с устаревшего номера версии, подписи, значения примитивного ключа и атрибута, представляющего кодовую страницу. Эта кодовая страница создается, когда кодировщик записывает атрибуты и свойства ANSI. После этого поток стал серией атрибутов, в которой сначала выстроились атрибуты сообщения, а затем атрибуты вложения. Различные характеристики сообщений и вложений содержатся в специальных атрибутах, таких как attMsgProps, attAttachment и attRecipTable. Атрибуты, отображаемые в потоке TNEF, содержат структуру, свойства сообщения и преобразования, необходимые для взаимодействия со свойствами сообщения. Каждый атрибут состоит из идентификатора, размера и данных атрибута, контрольной суммы и уровня в соответствии с его применением.

## Связь с протоколами и другими алгоритмами ##

Системы, которые имеют плохой механизм для отображения расширенного формата сообщений, изначально нуждаются в алгоритме данных TNEF для передачи. При использовании типа носителя ms-TNEF выходные данные алгоритма состоят из файла вложения (winmail.dat) и части тела MIME, указанной в [RFC2045]. Тело текстового сообщения передается с использованием UUENCODE в соответствии со спецификацией [MSDN-UAF], и это тело сообщения или эквивалентный метод декодируется на стороне получателя. Кроме того, TNEF может передавать данные сообщений с использованием различных интернет-протоколов, таких как SMTP, POP3, IMAP4, а также тех, которые интегрируют MIME в соответствии со стандартом RFC2045.

## Заявление о применимости ##

В дополнение к простой передаче сообщений исходное приложение TNEF должно было быть создано для использования классов сообщений и поддержки дополнительных функций, которые не имеют исходной поддержки в транспортном протоколе. Это приложение было дополнительно усовершенствовано для передачи расширенных свойств сообщений и именованных свойств, которые сегодня используют современные клиенты обмена сообщениями. Для соответствия оригинальной реализации поддерживается исходный синтаксис атрибута, а специальный атрибут отдельно содержит свойства нового сообщения.

## использованная литература

* [Формат нейтральной инкапсуляции транспорта](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Адреса электронной почты и адресные книги в Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: алгоритм данных транспортного нейтрального формата инкапсуляции (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

