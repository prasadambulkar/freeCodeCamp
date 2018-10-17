---
title: Using Browsec for Securing Your Connection to Freecodecampcom
localeTitle: باستخدام Browsec لتأمين الاتصال الخاص بك إلى Freecodecampcom
---
### لماذا أحتاج إلى مكون إضافي أو إضافة؟

بدأت بعض المعسكرات في الآونة الأخيرة بمواجهة مشاكل غريبة ، وهي "تعديل المحتوى" من قِبل بعض مزودي خدمة الإنترنت (ISP) ، مما أدى إلى كسر موقع الويب الخاص بـ [FreeCodeCamp.com](http://freecodecamp.com) (FCC) أحيانًا.

وقد ظهر ذلك مع بعض المشكلات التي سجلها المعسكر:

*   [\# 5999: إعلانات الحقن الهندية لمزودي خدمة الإنترنت تكسر الموقع](https://github.com/FreeCodeCamp/FreeCodeCamp/issues/5999)
*   [\# 6122: مشكلة خطيرة باستخدام IDE FCC ، وحدة التحكم تظهر الخطأ ...](https://github.com/FreeCodeCamp/FreeCodeCamp/issues/6122)
*   [\# 6381: غير قادر على عرض محرر التعليمات البرمجية في المستعرض](https://github.com/FreeCodeCamp/FreeCodeCamp/issues/6381)

## TL ؛ DR: ما الخطأ ، مرة أخرى؟

حسنا ، بالنسبة لبعض المعسكر ، هذه هي حالة كلاسيكية من [الرجل في الهجوم الأوسط](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) .

على سبيل المثال ، كما هو موضح في المسألة رقم 5999 ، يعمد مزودو خدمة الإنترنت من بعض المعسكرات من الهند عن قصد إدخال الإعلانات في مواقع الويب التي يزورها المستخدم والتي تتسبب في حدوث مشكلات.

وفي بعض الأحيان ، يستخدم مزودو خدمات الإنترنت أحيانًا استراتيجية مماثلة لتخزين مواقع الويب التي زارها المستهلكون ، حتى يتمكنوا من عرض المحتوى المخبأ على المستهلكين الآخرين الذين يزورون مواقع الويب نفسها ، مما يوفر لهم تكاليف النطاق الترددي ، في الوقت الذي توفر فيه مواقع الويب أسرع.

ولكن عندما لا يتم ذلك بشكل صحيح (أو يتم بشكل ضار كما هو الحال في الحالة الأولى) ، فإن هذا يعدل المحتوى الأساسي لمواقع الويب ، ويمنعها من العمل بشكل صحيح.

## ما هو الإصلاح ، إذن؟

بسيطة ، نحن بحاجة إلى تشفير اتصالنا إلى موقع FCC. من خلال تشفير حركة المرور لدينا ، نتجاوز قدرة مزود خدمة الإنترنت على تعديل المحتوى أو تخزينه مؤقتًا أثناء مروره عبر البنية الأساسية.

يمكن القيام بذلك من خلال وظيفة إضافية مفيدة للمتصفح تُسمى [Browsec](https://browsec.com/en/) .

### كيف تعمل الوظيفة الإضافية؟

تقوم الوظيفة الإضافية بإنشاء اتصال VPN بين جهازك والعالم الخارجي. أي ، السيد Peeping Tom (ISP) ، لا يمكنه العبث باتصالك بموقع FCC على الويب. من الناحية الفنية نفسها كما لو لم تكن في منزلك ، ولكن الوصول إلى موقع لجنة الاتصالات الفدرالية على شبكة الإنترنت من الولايات المتحدة أو هولندا أو أماكن أخرى مشابهة.

_وراء الكواليس فإنه يشفر نقل البيانات ، ويخفي IP الخاص بك._

## أنا بيعت ، أرني الخطوات.

ها أنت ذا!

### لـ Google Chrome:

#### الخطوة 1: تثبيت ملحق browsec.

يمكنك [تنزيل وتثبيت المكوّن الإضافي browsec](https://chrome.google.com/webstore/detail/browsec/omghfjlpggmjjaagoclmmobgdodcjboh) لـ Chrome من WebStore الرسمي.

![صورة لـ "Browsec على Google Chrome WebStore"](//discourse-user-assets.s3.amazonaws.com/original/2X/6/61bd52ed78c56369e62ca376b6dd9e56abcb6363.png)

#### الخطوة 2: مسح ملفات تعريف الارتباط وذاكرة التخزين المؤقت للمتصفح (اختياري).

إنه أمر جيد إذا قمت بمسح ذاكرة التخزين المؤقت للمتصفح للمرة الأولى التي ستستخدم فيها المتصفح ، بحيث يقوم المتصفح بتحميل كافة الملفات من البداية.

#### الخطوة 3: إعادة تشغيل المستعرض الخاص بك ، وزيارة [FreeCodeCamp.com](http://freecodecamp.com)

ما عليك سوى إغلاق المتصفح وإعادة تشغيله. تحقق من الامتداد الخاص بـ browsec ، للتعرف على الموقع النهائي المطلوب.

### بالنسبة إلى Mozilla Firefox:

قم بتنزيل إصدار Firefox محمول ، مع إضافة مجمعة ، من [موقع ويب Browsec](https://browsec.com/en/dashboard/main) .

![صورة لـ "Browsec على Google Chrome WebStore"](//discourse-user-assets.s3.amazonaws.com/original/2X/b/b30fbf3bade330044e18b3c37409f2437a3810c1.png)

هذا هو! الترميز سعيدة! إذا نجح ذلك ، فأخبرنا في [دردشة المساعدة](https://gitter.im/FreeCodeCamp/Help)

## أسئلة وأجوبة

### كيف أعرف ، إذا واجهت هجوم "رجل في المنتصف"؟

عند زيارة موقع FCC على الويب ، أو القيام بالتحديات ، إذا نظرت إلى وحدة تحكم مطور البرامج في المستعرض (اضغط على F12> علامة التبويب Console) ، من المفترض أن ترى أخطاءً مماثلة مثل أدناه.

![صورة لـ "خطأ"](//discourse-user-assets.s3.amazonaws.com/original/2X/4/4949599e3143f454fc5a7174a81e65fa68d04c77.png)

![صورة لـ "خطأ"](//discourse-user-assets.s3.amazonaws.com/original/2X/0/039acb319bae57f31ebd78aa3c8987f324a37f84.png)

![صورة لـ "خطأ"](//discourse-user-assets.s3.amazonaws.com/original/2X/2/25dcc04ecddc422fb7ba113ddac3378d5decd905.png)

هذه هي الحالات الكلاسيكية لهذه القضية.

### انتظر لحظة ، هل يمكنني استخدام أي آلية بديلة ، إلى Browsec؟

نعم ، لم لا ، يمكنك استخدام أي عملاء VPN متاحين في السوق ، ولكن ضع في اعتبارك أن Browsec مجاني ويعمل بشكل رائع!

### ماذا عن المتصفحات الأخرى ، إنترنت إكسبلورر ، سفاري ، وما إلى ذلك؟

همم ، ابحث عن أي إضافات VPN يمكنك العثور عليها لهذه المتصفحات ، [تور](https://www.torproject.org/) ، هو أحد هذه الأجهزة ، ولكنه يأتي مع اشتراكات مدفوعة الأجر ، يمكنك بشكل أساسي استخدام أي شخص مجهول الهوية ، ولكن يتم اختبار واختبار Chrome و Browsec و عملت لمعظم المعسكر في الماضي.

### هل يمكنني استخدام anonymizer لاستخدام المواقع بخلاف FCC؟

بكل تأكيد نعم. لما لا؟ لكن تذكر أن هذا لا يجعلك غير مرئيًا للقانون ، لذا كن حذراً مما تقوم به! ![:wink:](//forum.freecodecamp.com/images/emoji/emoji_one/wink.png?v=2 ":غمزة:")

### ماذا لو لم يعمل هذا بالنسبة لي؟

الرجاء إخبارنا في " [مساعدة الدردشة"](https://gitter.im/FreeCodeCamp/Help) ، سنحاول قصارى جهدنا لإيجاد حل بديل.

#### _تنصل_

**_لا يعتمد FreeCodeCamp أيًا من البرامج المذكورة في هذه المقالة ، يرجى استخدامها وفقًا لتقديرك الخاص. قد يتتبع بعض عملاء VPN نشاطك ، كما قد تكون هناك آثار جانبية مثل السرعة البطيئة أو تأخير تحميل الصفحة._**