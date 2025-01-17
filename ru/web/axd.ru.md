{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл AXD — формат файла веб-обработчика ASP.NET",
  "description" :"Узнайте, что такое файл AXD и API, с помощью которых можно создавать и открывать файлы AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## .AXD вариант №

Файл AXD — это файл веб-параметров, который используется для обработки и получения запросов встроенных ресурсов в ASP.NET. Он состоит из инструкций для получения встроенных ресурсов, таких как изображения, файлы JavaScript ([.JS](/ru/web/js/)) и файлы [.CSS](/ru/web/css/). Файлы AXD используются для внедрения ресурсов на клиентские страницы. Это позволяет клиентским страницам получать доступ к этим ресурсам на сервере стандартным способом.

## Формат файла AXD

Файлы AXD хранятся в виде двоичных файлов на стороне сервера. Это относится к файлу веб-обработчика в ASP.NET, который представляет собой компоненты, генерирующие ответы на определенные запросы к веб-серверу. Файлы AXD выполняют пользовательскую обработку перед генерацией ответа на основе запросов страниц на стороне клиента. Обычно они сохраняются как файлы **WebResource.axd**.

### Что такое файл WebResource.axd?

Большинство проектов ASP.NET сохраняют файлы AXD как файлы WebResource.axd, которые позволяют клиентским страницам загружать ресурсы, встроенные в сборку. Ваше приложение может столкнуться с низкой производительностью, если вы запустите его в режиме отладки, поскольку обработчик WebResources.axd не кэшируется.

## Рекомендации

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

