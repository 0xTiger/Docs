---
date: 2020-08-12
keywords: פורמט קובץ jxr, .jxr, jxr, כיצד לפתוח קבצי jxr, סיומת .jxr, סיומת jxr
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ JXR
linktitle: JXR
description: "למד על פורמט קובץ JXR וממשקי API שיכולים ליצור ולפתוח קובצי JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## מהו קובץ JXR? ##

JPEG XR (טווח JPEG מורחב) הוא פורמט קובץ לתמונות צילום בטון רציף. זהו תקן דחיסת תמונות סטילס המבוסס על HD Photo שפותחה על ידי מיקרוסופט. הוא תומך בדחיסה חסרת אובדן כאחד.

## היסטוריה קצרה ##

Windows Media Photo הוכרזה לראשונה על ידי מיקרוסופט ב-WinHEC 2006. שמו שונה ל-HD Photo בנובמבר 2006. JPEG XR אושר כתקן בינלאומי ISO/IEC 29199-2 ב-19 ביוני 2009. ITU-T ו-ISO/IEC פרסמו הצעה מפרט פורמט (ITU-T T.833 | ISO/IEC 29199-3), ערכת בדיקות התאמה (ITU-T T.834 | ISO/IEC 29199-4), ותוכנת ייחוס (ITU-T T.835 | ISO /IEC 29199-5) עבור JPEG XR לאחר השלמת מפרט קידוד התמונה ב-2010. דוח טכני המתאר את ארכיטקטורת זרימת העבודה עבור JPEG XR פורסם ב-2011.

## עיצוב JPEG XR ##

בהשוואה ל-JPEG, JPEG XR מציע מספר שיפורים כולל:

- **דחיסה טובה יותר**: JPEG XR מציע יחסי דחיסה גבוהים יותר.
- **דחיסה ללא הפסדים**: JPEG XR תומך בדחיסה ללא הפסדים.
- **מבנה אריחים**: ניתן לפלח תמונת JPEG XR לאזורי אריחים שבהם ניתן לפענח כל אזור בנפרד.
- **דיוק צבע יותר**: JPEG XR כולל המרה פנימית למרחב הצבע YCoCg לתמיכה בתמונות באמצעות מרחב צבע RGB. JPEG XR תומך גם בדגם צבע CMYK של 16 סיביות לכל רכיב (64 סיביות לפיקסל). JPEG XR תומך בפורמט צבעוני של נקודה צפה RGBE משותפת עבור תמונות HDR. JPEG XR תומך גם בגווני אפור ובקידודי צבע רב-ערוציים.
- **מפת שקיפות**: JPEG XR תומך בערוץ האלפא לשקיפות.
- **שינוי תמונה בדומיין דחוס**: ניתן להמיר תמונות JPEG XR לקידוד אובדן, להפחית ברזולוציה, לחתוך, להפוך, לסובב, וניתן לשנות את מבנה האריחים ללא פענוח מלא של הקובץ.
- **תמיכה במטא נתונים**: קובץ תמונה JPEG XR עשוי להכיל פרופיל צבע ICC לייצוג צבע עקבי במספר מכשירים. הפורמט תומך גם בפורמטים של מטא נתונים של Exif ו-XMP.

## פורמט מיכל ##

ניתן לאחסן נתוני תמונה של JPEG XR בפורמט מיכל דמוי TIFF באמצעות טבלה של תגיות Image File Directory (IFT). קובץ JXR מכיל את הדברים הבאים בתגי IFD:

- נתוני תמונה: זהו נתוני תמונה עצמאיים רציפים.
- נתוני ערוץ אלפא אופציונליים: אם זה קיים, ניתן לדחוס את נתוני התמונה בנפרד מה שמאפשר תמיכה באפליקציות שאינן תומכות בשקיפות.
- מטא נתונים
- מטא נתונים אופציונליים של XMP
- מטא נתונים אופציונליים של Exif

מכיוון שהוא מבוסס על פורמט TIFF, הוא יורש את כל מגבלות פורמט TIFF כמו מגבלת גודל הקובץ של 4 GB.

## הפניות ##

- [JPEG XR - ויקיפדיה](https://en.wikipedia.org/wiki/JPEG_XR)

