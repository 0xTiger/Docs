---
date: 2021-07-05
keywords: spc, .spc, формат файлу spc, як відкрити файли spc, файл сертифіката видавця програмного забезпечення
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - файл сертифіката видавця програмного забезпечення
linktitle: SPC
description: "Дізнайтеся, що таке формат файлу SPC та API, які можуть створювати та відкривати файли SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Що таке файл SPC?

Файл із розширенням .spc — це файл цифрового сертифіката безпеки, створений у форматі PKCS #7. Деякі програми створюють ці файли сертифікатів для безпечного обміну інформацією. Кілька таких програм включають OpenSSL і програму Signcode.exe, що входить до складу Microsoft .NET Framework. Як і інші файли сертифікатів, такі як [.cer](/uk/web/cer/), [.p7c](/uk/web/p7c/) і [.ssp](/uk/web/ssp/), файли SPC містять відкритий ключ інформація, зашифрована за допомогою закритого ключа. Цим відкритим ключем можна поділитися з користувачами публічно, а закритий ключ залишається конфіденційним.

## Формат файлу SPC - Додаткова інформація

Файли SPC зберігаються на диску як двійкові файли, які можна відкрити в будь-якому текстовому редакторі, але не читаються людиною. Вони базуються на останній доступній версії PKCS # 7 [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Список літератури

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Довідка SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

