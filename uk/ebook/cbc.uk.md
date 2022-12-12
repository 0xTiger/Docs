{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "розширення", "файл", "формат", "Книги коміксів", "Формат файлів коміксів", "електронна книга" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу CBC та API, які можуть створювати та відкривати файли CBC.",
  "title" :"CBC - формат файлу колекції коміксів",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Що таке файл CBC?

Файл із розширенням .cbc — це стиснена колекція файлів коміксів для електронних книг і містить файли [CBZ](/uk/ebook/cbz/) і [CBR](/uk/ebook/cbr/). Він використовується [Calibre](https://calibre-ebook.com/), додатком для перетворення електронних книг, який є кросплатформним менеджером електронних книг із відкритим кодом і дозволяє вам керувати своїми електронними книгами та конвертувати їх у різні формати . Файл CBC містить файл .txt, comics.txt, у якому перераховано інші файли, які є частиною архіву. Кілька програм доступні в Інтернеті, які можуть конвертувати файли CBC у [AZW3](/uk/ebook/azw3), [EPUB](/uk/ebook/epub/), [FB2](/uk/ebook/fb2/), [MOBI](/uk/ebook/ mobi/), [TXT](/uk/word-processing/txt/), [PDF](/uk/pdf/) та інші популярні формати файлів.

## Формат файлу CBC

Файли CBC — це стислі архіви, які містять CBZ, CBR і текстовий файл для переліку вмісту. Текстовий файл comics.txt має кодування UTF8 і містить список файлів CBC, які читачі можуть використовувати для впорядкування своїх колекцій. Файл CBC зазвичай має кілька атрибутів, які дозволяють організувати цю колекцію, наприклад комікс, категорія, видавець, серія, видання та виконавець.

Вміст зразка файлу CBC перераховано таким чином:

* comics.txt - текстовий файл, який містить список файлів CBR і CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Файл(и) CBZ

де файл comics.txt містить такий вміст:

* 1.cbz: Перша глава
* 2.cbz: Другий розділ
* 3.cbz: Третій розділ

Читачі обробляють файл comics.txt і генерують зміст на основі наданих даних.

## Список літератури

* [Калібр](https://calibre-ebook.com/)
