{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "розширення", "файл", "формат", "веб", "сертифікат", "мова" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - формат файлу сертифіката",
  "description":"Дізнайтеся про формат файлу CER та API, які можуть створювати та відкривати файли CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Що таке файл CER? ##

Файл із розширенням .cer відповідає за зберігання деякої інформації про сертифікат власника та конкретний відкритий ключ. Цей формат файлів не може зберігати закриті ключі та може зберігати лише один сертифікат x509. Спеціально захищені центри сертифікації належать до HTTPS, надійного та безпечного протоколу для перегляду
CER — це сертифікат вашого сервера. Зазвичай його отримує центр сертифікації для домену. CER здебільшого вважається таким самим, як [CRT](/uk/web/crt/), хоча обидва вони мають однаковий формат сертифіката SSL, але мають різні розширення імен файлів.
Їх можна використовувати в операційних системах, просто відкривши браузер і перевіривши безпеку браузера або веб-сайту, який використовується.

## Коротка історія ##

У 1995 році Thawte став першим органом із сертифікації для вирішення проблеми публічних сертифікатів SSL (захищеного сокета) у США. Після цього є серія таких органів влади, яка була заснована з 1995 по 2020 рік.

## Формат файлу CER ##

Ці файли можуть бути просто
* PKC S#7 містить кодування Base64 ASCII
* Його розширення файлів p7b або p7cZ
* Для двійкового вмісту сертифікатом буде DER або pkcs12/pfx.
Існує багато типів файлів сертифікатів з деякими унікальними характеристиками:
* .pem, коли організація usThawteificate зв’язує цей формат, добре відомо, що створює сертифікати
* .arm, коли метод отримання сертифіката допомагає самопідписаному, необхідний, указаний формат для цієї мети – .arm. Він представлений у кодуванні base-64 ASCII.
* .der, складається з двійкових даних. Це означає, що його можна використовувати лише для одного сертифіката
* .pfx (PKC512), складається з закритого ключа, що відповідає сертифікату, виданому ЦС, або самопідписаному сертифікату. Цей формат добре відомий для перетворення однієї реалізації SSL в іншу.


