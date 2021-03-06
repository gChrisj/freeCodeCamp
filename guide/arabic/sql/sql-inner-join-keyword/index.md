---
title: SQL Inner Join Keyword
localeTitle: SQL الداخلية الانضمام إلى الكلمات الرئيسية
---
## SQL الداخلية الانضمام إلى الكلمات الرئيسية

### مثال على الاستخدام

لهذا الدليل سنناقش انضمام SQL (INNER)

### انضم (مثل الانضمام إلى Inner)

سيكون جدول الطالب في جملة FROM بحيث يكون جدول بدء أو يسار.

سننضم إلى جدول جهات اتصال الطلاب أو جدول RIGHT. سترى أن جميع الطلاب يظهرون أن ALSO في جدول الاتصال. كما هو موضح في الجداول أدناه ، فإن studentID 9 موجود في جدول الطالب ولكن ليس في جدول جهات الاتصال ، لذا لن يظهر في أحد الروابط.

بيان SQL

 ``SELECT a.studentID, a.FullName, a.programOfStudy, 
 b.`student-phone-cell`, b.`student-US-zipcode` 
 FROM student AS a 
 INNER JOIN `student-contact-info` AS b ON a.studentID = b.studentID; 
`` 

"انضم" البيانات \`\` \`النص + ----------- + ------------------------ + ------------ ------ + -------------------- + -------------------- + | studentID | FullName | programOfStudy | خلية هاتف الطالب student-US-zipcode | + ----------- + ------------------------ + ------------ ------ + -------------------- + -------------------- + | 1 | مونيك ديفيز الأدب | 555-555-5551 | 97111 | | 2 | تيري جوتيريز | برمجة | 555-555-5552 | 97112 | | 3 | سبنسر باوتير | برمجة | 555-555-5553 | 97113 | | 4 | لويس رمزي برمجة | 555-555-5554 | 97114 | | 5 | ألفين غرين | برمجة | 555-555-5555 | 97115 | | 6 | صوفي فريمان برمجة | 555-555-5556 | 97116 | | 7 | إدغار فرانك "تيد" كود علوم الكمبيوتر | 555-555-5557 | 97117 | | 8 | دونالد د. شامبرلين علوم الكمبيوتر | 555-555-5558 | 97118 | + ----------- + ------------------------ + ------------ ------ + -------------------- + -------------------- +

 `### Complete table listings for reference 
 
 Student table SQL 
` 

مزود SELECT a.studentID، a.FullName، sat\_score، a.programOfStudy، schoolEmailAdr من الطالب AS

 `student or LEFT table 
` 

نص + ----------- + ------------------------ + ----------- + ------------------ + ------------------------ + | studentID | FullName | sat\_score | programOfStudy | schoolEmailAdr | + ----------- + ------------------------ + ----------- + ------------------ + ------------------------ + | 1 | مونيك ديفيز 400 | الأدب | Monique@someSchool.edu | | 2 | تيري جوتيريز | 800 | برمجة | Teri@someSchool.edu | | 3 | سبنسر باوتير | 1000 | برمجة | Spencer@someSchool.edu | | 4 | لويس رمزي 1200 | برمجة | Louis@someSchool.edu | | 5 | ألفين غرين | 1200 | برمجة | Alvin@someSchool.edu | | 6 | صوفي فريمان 1200 | برمجة | Sophie@someSchool.edu | | 7 | إدغار فرانك "تيد" كود 2400 | علوم الكمبيوتر | Edgar@someSchool.edu | | 8 | دونالد د. شامبرلين 2400 | علوم الكمبيوتر | Donald@someSchool.edu | | 9 | ريمون ف. بويس 2400 | علوم الكمبيوتر | Raymond@someSchool.edu | + ----------- + ------------------------ + ----------- + ------------------ + ------------------------ + 9 صفوف في مجموعة (0.00 ثانية)

 ``SELECT * FROM `student-contact-info` AS b; 
`` 

جدول الاتصال الطالب أو الجدول الأيمن `text +-----------+----------------------------------+--------------------+--------------------+ | studentID | studentEmailAddr | student-phone-cell | student-US-zipcode | +-----------+----------------------------------+--------------------+--------------------+ | 1 | Monique.Davis@freeCodeCamp.org | 555-555-5551 | 97111 | | 2 | Teri.Gutierrez@freeCodeCamp.org | 555-555-5552 | 97112 | | 3 | Spencer.Pautier@freeCodeCamp.org | 555-555-5553 | 97113 | | 4 | Louis.Ramsey@freeCodeCamp.org | 555-555-5554 | 97114 | | 5 | Alvin.Green@freeCodeCamp.org | 555-555-5555 | 97115 | | 6 | Sophie.Freeman@freeCodeCamp.org | 555-555-5556 | 97116 | | 7 | Maximo.Smith@freeCodeCamp.org | 555-555-5557 | 97117 | | 8 | Michael.Roach@freeCodeCamp.ort | 555-555-5558 | 97118 | +-----------+----------------------------------+--------------------+--------------------+ 8 rows in set (0.00 sec)`

### استنتاج

كما هو الحال مع كل هذه الأشياء SQL هناك أكثر من ذلك بكثير من ما هو موجود في هذا الدليل التمهيدي.

آمل أن يمنحك هذا على الأقل ما يكفي للبدء.

يرجى الاطلاع على دليل مدير قاعدة البيانات الخاص بك والمتعة محاولة خيارات مختلفة بنفسك.