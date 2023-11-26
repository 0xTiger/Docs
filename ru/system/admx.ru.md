{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ADMX — формат файла административного шаблона групповой политики",
  "description":"Узнайте о формате файла ADMX и о том, как открыть файлы ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADMX вариант №

Файл ADMX — это файл конфигурации политики, используемый программным обеспечением групповой политики Microsoft Windows, которое управляет группой компьютеров в группе. Это файл административного шаблона на основе XML, который был представлен в пакете обновления 1 для Windows Vista. Файлы ADMX содержат параметры конфигурации для учетных записей пользователей, конфигурации операционной системы и приложений. Файлы ADMX используются для хранения и развертывания конфигураций централизованного управления многими компьютерными системами.

Вы можете создавать или редактировать файлы ADMX с помощью любого XML-совместимого, любого текстового редактора или редактора объектов групповой политики Microsoft.

## Формат файла ADMX – дополнительная информация

Файлы ADMX хранятся в универсальном формате файлов [XML](/ru/web/xml/), который удобен для чтения человеком. Это многоязычный формат файлов, который позволяет системным администраторам, говорящим на разных языках, работать с одними и теми же файлами ADMX. Файлы ADMX заменили старый формат файлов [ADM](/ru/system/adm/), который представляет собой формат текстовых файлов в формате Юникода. Файлы ADMX указывают разделы реестра, которые изменяются при изменении определенного параметра групповой политики.

### Что я могу сделать с файлом ADMX?

Файлы ADMX определяют, какие действия разрешены пользовательским компьютерам, входящим в группу. Групповая политика налагает правила, установленные в сочетании с программным обеспечением Active Directory. Файлы ADMX управляются из центрального хранилища в ОС Windows, которое является центральным расположением в домене.

Файл ADMX, развернутый в рабочей среде, может позволить администраторам реализовывать такие политики, как:

* Контролировать использование Интернета
* Загрузка определенных типов файлов
* Использование съемных устройств в системах

## Рекомендации

* [Файлы административных шаблонов — ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ — Управление файлами административных шаблонов] (https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)
