{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על Age of Empires 2 Expansion Replay תבנית קובץ MGX וממשקי API שיכולים ליצור ולפתוח קבצי MGX.",
  "title" : "קובץ MII - פורמט קובץ Wii Virtual Avatar",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-he",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## מהו קובץ MII?

קובץ MII הוא פורמט קובץ אווטאר וירטואלי המשמש לאחסון אווטרים וירטואליים בקונסולת המשחקים של Nintendo Wii. קבצים אלה מכילים מידע כגון מראה האווטאר, תנועות והנפשות. ניתן להשתמש בהם במשחקים, ביישומי רשתות חברתיות ובתוכנות אחרות ב-Wii. קובץ MII מכיל גם תכונות אחרות על האווטאר כמו מין, צבע שיער, צבע עור, תווי פנים וסוג עיניים.

אתה יכול לפתוח קובץ MII באמצעות ה-[My Avatar Editor](https://rc24.xyz/goodies/mii/).

## פורמט קובץ MII

פורמט הקובץ MII מוגדר בפירוט ב-[Wii Brew](https://wiibrew.org/wiki/Mii_data). מחרוזות בקובץ MII מאוחסנות בפורמט Unicode (UTF-16), big-endian.

### בלוק MI

נתוני קובץ MII מאוחסנים ב-Wiimote בשני בלוקים. אורכו של כל בלוק 750 בתים, עם 2 בתים CRC, מה שהופך אותו לסך של 752 בתים. כל בלוק מתחיל בערך של 4 בתים ('RNCD') שנראה כמספר הקסום של פורמט הקובץ MII.

## כיצד ליצור קבצי MII?

ישנן מספר דרכים שונות ליצור אווטארים עבור ה-Nintendo Wii:

1. `שימוש בערוץ Mii המובנה ב-Wii:` ערוץ זה מאפשר לך ליצור אווטרים מותאמים אישית באמצעות מגוון כלים, כולל תווי פנים, מבנה גוף ולבוש. לאחר שיצרת את האווטאר שלך, תוכל לשמור אותו כקובץ Mii ולהשתמש בו במשחקים ובתוכנות אחרות ב-Wii.

1. `שימוש באפליקציית Mii Maker ב-Nintendo 3DS:` אפליקציית Mii Maker מאפשרת לך ליצור אווטרים מותאמים אישית באמצעות מסך המגע והמצלמה ב-Nintendo 3DS שלך. לאחר שיצרת את האווטאר שלך, תוכל לשמור אותו כקובץ Mii ולהעביר אותו ל-Wii שלך באמצעות חיבור אלחוטי.

1. `שימוש בתוכנת צד שלישי:` חלק מהמפתחים יצרו תוכנה המאפשרת לך ליצור אווטרים מותאמים אישית עבור ה-Wii. תוכנה זו מיועדת בדרך כלל לשימוש במחשב ועשויה לדרוש שלבים נוספים כדי להעביר את האווטאר ל-Wii שלך.

1. `שימוש באווטרים מוכנים מראש:` חלק מהמשחקים ותוכנות אחרות ב-Wii עשויים להגיע עם אווטרים מוכנים מראש שבהם תוכל להשתמש.

בכל המקרים, אתה צריך שיהיה לך חשבון נינטנדו כדי ליצור ולשמור את הדמות שלך ב-Wii.

## הפניות

* [עורך האווטאר שלי](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)

