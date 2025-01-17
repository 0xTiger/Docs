{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ملف TSX - ملف React TypeScript - ما هو ملف .tsx وكيفية فتحه?",
  "description":"تعرف على ملف TSX React TypeScript وكيفية فتحه.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-ar-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## ما هو ملف TSX؟

يرتبط امتداد الملف ".tsx" عادةً بملفات TypeScript التي تحتوي على كود **React**. **TypeScript عبارة عن مجموعة شاملة من JavaScript** تضيف كتابة ثابتة إلى اللغة، و**React عبارة عن مكتبة JavaScript لإنشاء واجهات المستخدم**. عند العمل مع React وTypeScript معًا، غالبًا ما يستخدم المطورون الامتداد ".tsx" لملفاتهم للإشارة إلى أنها تحتوي على كل من TypeScript وJSX (امتداد بناء جملة React لـ JavaScript).

## مثال ملف TSX

يتيح لك TypeScript تحديد أنواع المتغيرات ومعلمات الوظائف والمزيد. غالبًا ما ترى كود TypeScript في ملف ".tsx" يحدد أنواع الخاصيات والحالة والمتغيرات الأخرى المستخدمة في مكونات React.

```
// مثال: كود TypeScript في مكون React
واجهة MyComponentProps {
   الاسم: سلسلة؛
   العمر: العدد؛
}
const MyComponent: React.FC<MyComponentProps> = ({ الاسم، العمر }) => {
   // منطق المكون هنا
   إرجاع <div>{name} عمره {age} سنة.</div>;
};
```

## JSX (امتداد بناء جملة React)

JSX هو امتداد بناء جملة لـ JavaScript موصى به بواسطة React. يبدو مشابهًا لـ XML/HTML ويستخدم لوصف الشكل الذي يجب أن تبدو عليه واجهة المستخدم.

```
// مثال: JSX في مكون React
const MyComponent: React.FC<MyComponentProps> = ({ الاسم، العمر }) => {
   إرجاع <div>{name} عمره {age} سنة.</div>;
};
```

عادةً ما يحتوي الملف ".tsx" على تعريف مكون React باستخدام المكونات الوظيفية أو مكونات الفئة.

```
// مثال: تعريف مكون التفاعل في ملف ".tsx".
const MyComponent: React.FC = () => {
   إرجاع <div>مرحبًا، رد فعل!</div>;
};
```

سترى غالبًا عبارات الاستيراد في بداية الملف، مما يؤدي إلى جلب التبعيات والوحدات النمطية الضرورية.

```
// مثال: استيراد البيانات في ملف ".tsx".
استيراد رد فعل من "رد فعل"؛
```

## كيفية فتح ملف TSX؟

ملفات TSX هي ملفات نصية عادية لذا يمكنك فتحها في أي محرر نصوص، على سبيل المثال. المفكرة. ومع ذلك، فهذه ملفات ترميز ومن المفترض أن يتم فتحها بواسطة IDE، على سبيل المثال. كود الاستوديو المرئي.