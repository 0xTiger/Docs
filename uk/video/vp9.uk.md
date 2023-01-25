{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Файл", "Розширення", "Формат файлу", "Формат відео", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 – відеофайл TrueMotion",
  "description":"Дізнайтеся про формат файлу VP9 та API, які можуть створювати та відкривати файли VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Що таке файл VP9?

Google розробив кодек VP9 як безкоштовний стандарт кодування відео з відкритим вихідним кодом як наступника VP8. Його спочатку було розроблено для стиснення вмісту Ultra HD на YouTube, оскільки він розширює та підвищує ефективність кодування свого попередника. Якщо говорити про оригінальні кодеки VPX, то вони прийшли від On2 Technologies, яка була асимільована Google у 2010 році. Пізніше Google відкрила кодек. Обидва формати VP8 і VP9 доступні за безкоштовною ліцензією BSD, яка дозволяє операторам організовувати навички кодування або декодування як ексклюзивного програмного забезпечення, так і програмного забезпечення з відкритим кодом, не розкриваючи вихідний код.

## Технічні характеристики VP9

* VP9 забезпечує максимальну роздільну здатність 8192x4352 зі швидкістю до 120 кадрів в секунду та кілька колірних просторів із Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 і sRGB.
* У цьому форматі повністю підтримується весь спектр варіантів використання в Інтернеті та на мобільних пристроях, від стиснення з низьким бітрейтом до високоякісного ультра-HD з додатковою підтримкою 10/12-бітного кодування та HDR.
* Він може зменшити бітрейт відео на цілих 50% порівняно з іншими
* Він підтримує адаптивне потокове передавання та використовується YouTube та іншими відомими постачальниками веб-відео
* Пристрої Chrome, Opera, Edge, Firefox і Android, а також мільйони смарт-телевізорів підтримують декодування цього кодека
* Роздільна здатність відео понад 1080p модифікується за допомогою VP9 і забезпечує стиснення без втрат
* Різні колірні простори, такі як Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 і sRGB підтримуються VP9
* HDR-відео з використанням Hybrid Log-Gamma та Perceptual Quantizer також може підтримуватися VP9


## Коротка історія

* Розробка відеокодека VP9 почалася в 2011 році, а його декодер було додано до веб-браузера Chromium у грудні 2012 року.
* Його перша версія веб-браузера Google Chrome була випущена в лютому 2013 року, і тоді було випущено декодування
* Google випустив Chrome 29.0.1547 із остаточною підтримкою VP9 у серпні 2013 року
* У жовтні 2013 року до FFmpeg було додано інтуїтивний декодер VP9
* Mozilla додала підтримку VP9 до Firefox у грудні 2013 року у версії 2, яка була випущена 18 березня 2014 року.
 

## Робота VP9

Зазвичай відео 4K покращує якість зображення, зменшуючи певні пікселі, а кодек VP9 і HEVC збільшують їх, щоб зменшити бітрейт і розмір файлу. Хоча це може здатися суперечливим, механізм кодування бере більші пікселі та змінює їх на кращу роздільну здатність. Вихідне відео, що містить відеокадри, кодується або стискається, щоб створити стислий бітовий потік відео. Кожен окремий кадр спочатку розбивається на блоки пікселів. Потім блоки ретельно перевіряються на тривимірні відхилення, а послідовні з’єднання між кадрами оцінюються, щоб скористатися областями, які не можна змінити. Вони кодуються за допомогою векторів руху, які забезпечують якість даного блоку в наступному кадрі. Залишкова інформація кодується за допомогою ефективного двійкового стиснення.

## Список літератури

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google%20video%20platform%20YouTube)
* [Веб-документи MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Кокос](https://www.coconut.co/)
