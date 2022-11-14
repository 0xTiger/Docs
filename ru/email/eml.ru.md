{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML — сообщение электронной почты",
  "description":"Узнайте о формате файла EML и API-интерфейсах, которые могут создавать и открывать файлы EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## .EML вариант №

Формат файла EML представляет собой сообщения электронной почты, сохраненные с помощью Outlook и других соответствующих приложений. Почти все клиенты электронной почты поддерживают этот формат файла из-за его соответствия стандарту формата интернет-сообщений RFC-822. Microsoft Outlook — это программное обеспечение по умолчанию для открытия типов сообщений EML. Файлы EML можно использовать для сохранения на диск, а также для отправки получателям с использованием протоколов связи.

## Краткая история EML

Спецификации формата файла EML доступны в соответствии со стандартным форматом [RFC 822] (http://www.ietf.org/rfc/rfc0822.txt). До RFC-822 правила обмена сетевыми сообщениями регулировались RFC-733, пока в 1982 году первый не был создан как улучшение латерального путем установления стандартов ARPA. В то же время Microsoft создала собственные COM-модули для разработки собственного почтового клиента, т. е. Outlook Express. RFC-822 стал частным форматом, когда Microsoft отошла от открытого стандарта и создала формат файла [PST](/ru/email/pst/), в котором сообщения электронной почты сохраняются в высокоструктурированном формате базы данных. Это приводило к проблемам у пользователей почтовых клиентов сторонних производителей, когда электронные письма пересылались из Microsoft Outlook.

Это было в 2001 году, когда стандарт 822 был расширен до 2822 — формата интернет-сообщений, который в настоящее время используется для создания, чтения и отправки сообщений EML в формате MIME RFC-822.

## Спецификации формата файла EML

Файлы EML состоят из двух отдельных разделов:

* Заголовки — содержит информацию о заголовке сообщения.
* Тело сообщения — содержит серию информации, которая может включать содержимое сообщения, встроенные изображения и вложения.

### Информация о заголовках ###

Файл EML состоит из информации заголовков и, возможно, тела сообщения. Каждая строка заголовка в EML состоит из двух частей, разделенных двоеточием «:». Первый называется «Имя заголовка», а тот, что следует за двоеточием, — телом заголовка. Например, к таким заголовкам относятся:

* Адрес электронной почты отправителя
* Адрес электронной почты получателя
* Тема письма
* Отметка времени и даты сообщения

**Пример заголовка**

Из:<John@bmw.eml.light.com>

К:<Andy@fileformat.com>

Дата: Чт, 8 Мар 2018 10:43:37 +0100

Тема: bmw eml лайт

### Тело сообщения ###

Тело сообщения EML содержит основную информацию электронной почты в виде текста, гиперссылок и вложений. Тело письма может содержать простой читаемый текст, но это не обязательно. При этом тело сообщения может быть пустым или содержать зашифрованные данные вложений.

Содержимое тела сообщения описывается его Content-Type, который позволяет приложениям для чтения читать информацию в соответствующих форматах. Он фактически представляет характер и формат документа. Структура типа MIME или типа содержимого очень проста; он состоит из типа и подтипа, двух строк, разделенных '/'. Пространство не допускается. «Тип» представляет категорию и может быть дискретным или составным типом. «Подтип» специфичен для каждого типа. Список типов, подпадающих под категорию Content-Type, длинный, но некоторые важные типы контента следующие:


|**Тип**|**Описание**|**Пример подтипов**
---|---|---|
|text|Представляет формат, удобочитаемый для человека|text/plain, text/html, text/css, text/javascript
|image|Представляет изображение любого типа, кроме видео|image/bmp, image/png, image/jpg, image/gif
|audio|Представляет любой формат аудиофайла|audio/mdi, audio/wav
|application|Представляет любые двоичные данные|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Представление вложения в теле EML ###

Тело EML содержит границы для каждого типа содержимого, которое оно содержит. Вложение в теле сообщения идентифицируется его Content-Type и Content-Disposition, как показано в следующем примере:

Content-Type: текстовый/обычный; кодировка#"windows-1252"; имя#"apple store.txt"
Content-Disposition: вложение; имя_файла#"apple store.txt"
Контент-передача-кодирование: base64
Идентификатор X-вложения: f_jkhztmd02

Как видно, Content-Disposition, установленный на вложение, позволяет приложениям чтения получать информацию о вложении, такую как имя файла вложения и кодировку передачи. За информацией заголовка вложения следует закодированное содержимое вложения, которое должно быть прочитано.

#### Пример электронной таблицы в качестве вложения ####

Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; имя#"english_spodr.xlsx"
Content-Disposition: вложение; имя_файла#"english_spodr.xlsx"
Контент-передача-кодирование: base64
Идентификатор X-вложения: f_jkhztmd43

## использованная литература

* [RFC 822] (http://www.ietf.org/rfc/rfc0822.txt)
