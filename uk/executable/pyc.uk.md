{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу PYC та API, які можуть створювати та відкривати файли PYC.",
  "title" :"Формат файлу PYC - скомпільований файл Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Що таке файл PYC?

Файл PYC — це скомпільований вихідний файл, створений із вихідного коду, написаного мовою програмування Python. Коли файл PY запускається за допомогою інтерпретатора Python, він перетворюється на байт-код для виконання. У той же час скомпільований байт-код також зберігається як файл .pyc для повторного використання з кешу пізніше, якщо це можливо.

## Структура формату файлу PYC

Файли PYC мають байт-код, і специфікації їхнього формату файлів недоступні для всіх. Проте дослідження деяких джерел показують, що [структура файлу PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) складається з:

* «Чотирибайтове магічне число» - просто два байти, які змінюються з кожною зміною коду сортування, а потім два байти 0d0a.
* `Чотирибайтова мітка часу модифікації` - мітка часу модифікації Unix вихідного файлу, який створив .pyc, щоб його можна було перекомпілювати, якщо джерело зміниться.
* `Об’єкт маршалованого коду` – вихід marshal.dump об’єкта коду, який є результатом компіляції вихідного файлу.

## Список літератури

* [Структура файлів .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)
