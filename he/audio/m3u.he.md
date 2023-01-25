---
date: 2019-12-13
keywords: m3u, פורמט קובץ m3u, סיומת .m3u, רשימת השמעה מולטימדיה m3u, פורמט רשימת השמעה m3u
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "למד על פורמט קובץ M3U וממשקי API שיכולים ליצור ולפתוח קבצי M3U."
title: פורמט קובץ M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## מהו קובץ M3U? ##

M3U (URL MP3) הוא קובץ רשימת השמעה אודיו המאוחסן עם סיומת .m3u. M3U אינו קובץ אודיו בפועל, הוא רק מצביע על קבצי אודיו ולפעמים וידאו. M3U פותח לשימוש עם תוכנת Winplay3 על ידי Fraunhofer. זה גם נתמך על ידי נגני מדיה ותוכנות שונות.

## פורמט קובץ M3U

אין מפרט רשמי לפורמט הקובץ M3U, זה תקן דה פקטו. M3U הוא קובץ טקסט פשוט המשתמש בסיומת .m3u אם הטקסט מקודד בקידוד ברירת המחדל שאינו Unicode של המערכת המקומית או עם סיומת .m3u8 אם הטקסט מקודד UTF-8. כל ערך בקובץ M3U יכול להיות אחד מהבאים:

- נתיב מוחלט לקובץ
- נתיב הקובץ ביחס לקובץ M3U.
- כתובת אתר

### M3U מורחב ###

ב-M3U המורחב מוצגות הנחיות נוספות שמתחילות ב-"#" ומסתיימות בנקודתיים(:) אם יש להן פרמטרים. להלן רשימה של הנחיות עבור M3U מורחב.

- **#EXTM3U** - זוהי כותרת הקובץ המציינת את M3U המורחבת וחייבת להיות השורה הראשונה של הקובץ.
- **#EXTENC:** - קידוד טקסט. זה חייב להיות השורה השנייה של הקובץ.
- **#EXTINF:** - משמש למידע על מסלול ומאפיינים נוספים אחרים.
- **#PLAYLIST:** - הכותרת של רשימת ההשמעה
- **#EXTGRP:** - התחל קיבוץ שמות
- **#EXTALB:** - מידע על אלבום
- **#EXTART:** - אמן האלבום
- **#EXTGENRE** - ז'אנר אלבומים
- **#EXTM3A** - רשימת השמעה של קובץ בודד עבור רצועות אלבומים או פרקים.
- **#EXTBYT:** - גודל הקובץ בבתים.
- **#EXTBIN:** - נתונים בינאריים בהמשך.
- **#EXTIMG:** - לוגו, כריכה או תמונות אחרות.

### HLS M3U ###

HLS (HTTP Live Streaming) נוצר על ידי אפל כדי להזרים אודיו ורדיו למכשירי iOS. הוא מבוסס על M3U המורחב המקודד UTF-8. זה תוקן כ-RFC 8216 בשנת 2017 על ידי IETF. התגים של רשימת ההשמעה של HLS מתחילים ב-"#EXT-X-". להלן רשימה של תגים עבור HLS

- **EXT-X-VERSION** - מציין את גרסת התאימות של הקובץ בהתבסס על המדיה והשרת שלו.
- **#EXT-X-START:** - מציין את נקודת ההתחלה המועדפת עבור רשימת ההשמעה.
- **#EXT-X-PLAYLIST-TYPE:** - מספק את סוג רשימת ההשמעה (EVENT או VOD).
- **#EXT-X-TARGETDURATION:** - הוא מציין את משך הפלח המרבי.
- **#EXT-X-MEDIA-SEQUENCE:** - זה מציין את מספר רצף המדיה.
- **#EXT-X-INDEPENDENT-SEGMENTS** - זה מציין שכל דגימות המדיה הן עצמאיות וניתנות לפענוח ללא מקטעים אחרים.
- **#EXT-X-MEDIA:** - הוא משמש לקשר בין רשימות השמעה של מדיה המכילות עיבודים חלופיים של אותו תוכן.
- **#EXT-X-STREAM-INF:** - הוא מציין זרם וריאנטי שהוא חלק מהעיבודים.
- **#EXT-X-BYTERANGE:** - מציין שקטע המדיה הוא תת-טווח של המשאב שזוהה על ידי ה-URI שלו.
- **#EXT-X-DISCONTINUITY** - מציין אי רציפות בין קטעי המדיה הקודמים והבאים.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - זה מאפשר סנכרון בין ביצועים שונים של אותו זרימת וריאציות או זרמים וריאנטים שונים.
- **#EXT-X-KEY:** - מציין כיצד לפענח פלחי מדיה.
- **#EXT-X-MAP:** - מציין כיצד להשיג את סעיף אתחול המדיה. יש צורך לנתח את פלחי המדיה הרלוונטיים.
- **#EXT-X-PROGRAM-DATE-TIME:** - הוא משייך את המדגם הראשון של פלח המדיה לתאריך ו/או שעה מוחלטים.
- **#EXT-X-DATERANGE:** - הוא משייך טווח נתונים.
- **#EXT-XI-FRAMES-ONLY** - מציין שכל פלח מדיה ברשימת ההשמעה מתאר I-frame בודד.
- **EXT-XI-FRAME-STREAM-INF** - זה מציין שקובץ הפלייליסט מכיל I-frames של מצגת מולטימדיה.
- **#EXT-X-SESSION-DATA:** - הוא מאפשר לנתוני הפעלה שרירותיים
נישא ברשימת השמעה מאסטר.
- **#EXT-X-SESSION-KEY:** - מאפשר מפתחות הצפנה. הלקוח יכול לטעון מראש מפתחות אלה מבלי לקרוא את רשימת ההשמעה תחילה.
- **#EXT-X-ENDLIST** - זה מציין שלא יתווספו עוד פלחי מדיה לקובץ.

להלן רשימה של סוגי מדיה באינטרנט המשמשים את M3U:

- **application/vnd.apple.mpegurl**: זהו סוג המדיה הרשום היחיד (רשום ב-2009) עבור M3U המשמש להתייחסות לרשימות ההשמעה ביישומי HLS.
- סוגי המדיה האינטרנטיים הבאים משמשים יישומים שאינם HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## דוגמה M3U ##

זוהי דוגמה לקובץ M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## הפניות ##

- [M3U - ויקיפדיה](https://en.wikipedia.org/wiki/M3U)
- [סטרימינג בשידור חי של HTTP](https://tools.ietf.org/html/rfc8216)
