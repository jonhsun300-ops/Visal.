# កម្មវិធីគ្រប់គ្រងពិន្ទុសិស្ស (អនុវិទ្យាល័យ)

## ឯកសារនៅក្នុង ZIP
- `index.html` — កម្មវិធីទាំងមូល (HTML/CSS/JavaScript)
- `firestore.rules` — ច្បាប់សុវត្ថិភាព Cloud Firestore

## ដំឡើង Firebase
1. ចូល https://console.firebase.google.com/ ហើយបង្កើត Project ថ្មី។
2. នៅក្នុង Project settings > Your apps បង្កើត Web app ហើយចម្លង `firebaseConfig`។
3. បើក `index.html` ដោយ text editor ហើយជំនួសតម្លៃ `PASTE_..._HERE` នៅក្នុង `firebaseConfig` ដោយតម្លៃពិតរបស់គម្រោង។
4. ក្នុង Firebase Console > Authentication > Sign-in method បើក `Email/Password`។
5. ក្នុង Firebase Console > Firestore Database បង្កើត database។
6. ចូល Firestore > Rules ហើយបញ្ចូលខ្លឹមសារពី `firestore.rules` រួច Publish។
7. បង្ហោះ `index.html` ទៅ hosting ដែលបម្រើ HTTPS (ឧ. Firebase Hosting)។ ការបើកឯកសារដោយផ្ទាល់ក្នុង file:// អាចមិនដំណើរការបានល្អ។
8. បើក URL របស់កម្មវិធី បង្កើតគណនីគ្រូមួយ ហើយចាប់ផ្ដើមបញ្ចូលសិស្ស និងពិន្ទុ។

## សុវត្ថិភាពសំខាន់
- កុំប្រើ Firestore Rules ដែលអនុញ្ញាតឱ្យមនុស្សគ្រប់គ្នាអាន/សរសេរទិន្នន័យ។
- កំណែនេះបែងចែកទិន្នន័យតាមគណនី Firebase UID នីមួយៗ។ គណនីគ្រូផ្សេងមិនឃើញទិន្នន័យរបស់គ្នាទេ។ បើចង់ឱ្យគ្រូច្រើននាក់ប្រើ database សាលារួម ត្រូវរចនាសិទ្ធិ Admin/Teacher បន្ថែម មិនត្រូវប្ដូរ Rules ឱ្យបើកចំហឡើយ។
- អ៊ីមែល/ពាក្យសម្ងាត់គឺគណនី Firebase Authentication។ កុំចែករំលែកពាក្យសម្ងាត់។
- `firebaseConfig` ជាព័ត៌មានកំណត់ Web app មិនមែនជាពាក្យសម្ងាត់ Database ទេ។ សុវត្ថិភាពសំខាន់គឺ Authentication និង Firestore Rules។
- កំណែគំរូនេះគណនាមធ្យមភាគពីកំណត់ត្រាពិន្ទុទាំងអស់ដែលត្រូវនឹងតម្រងថ្នាក់/មុខវិជ្ជា។ និទ្ទេស និងកម្រិតជាប់/ធ្លាក់គឺជាគំរូ បងត្រូវកែតាមបទបញ្ជារបស់សាលា។
- លុបសិស្សមិនលុបពិន្ទុរបស់សិស្សនោះដោយស្វ័យប្រវត្តិទេ។ សូមពិនិត្យពិន្ទុមុនពេលលុប។

## របៀបបង្ហោះទៅ Firebase Hosting (សង្ខេប)
ត្រូវដំឡើង Node.js និង Firebase CLI នៅលើកុំព្យូទ័រ។ ក្នុង folder របស់ project:
1. `npm install -g firebase-tools`
2. `firebase login`
3. `firebase init hosting` ហើយជ្រើស project និងថតដែលមាន `index.html`
4. `firebase deploy`

បើមិនធ្លាប់ប្រើ command line សូមធ្វើតាមជំហានក្នុង Firebase Console ឬស្នើឱ្យអ្នកដែលស្គាល់បច្ចេកទេសជួយបង្ហោះ។ មុនប្រើជាមួយទិន្នន័យសិស្សពិត សូមសាកល្បងជាមួយទិន្នន័យគំរូជាមុន។


មុខងារបន្ថែម៖ តារាងចំណាត់ថ្នាក់ក្នុងថ្នាក់ និងតារាងកិត្តិយសសម្រាប់មធ្យមភាគ >= 90 តាមឆ្នាំសិក្សា។ សូមជំនួស firebaseConfig ក្នុង index.html ដោយ config ពីគម្រោង Firebase របស់អ្នក មុនប្រើ។
