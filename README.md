# אלינה · פתיחת החנות

רשימת משימות משותפת לפתיחת החנות. כל מי שיש לו את הקישור יכול להוסיף משימות,
לשבץ את עצמו, לסמן בוצע ולכתוב הערות. הכל מסתנכרן בזמן אמת.

## הקמה (פעם אחת)

### 1. Firebase (מאגר המידע המשותף, חינם)
1. נכנסים ל-https://console.firebase.google.com ולוחצים **Create a project**. שם: `alina`. את Google Analytics אפשר לכבות.
2. בתפריט: **Build ← Firestore Database ← Create database**. מיקום: `eur3 (europe-west)`. בוחרים **production mode**.
3. בלשונית **Rules** מוחקים הכל, מדביקים את התוכן של `firestore.rules` ולוחצים **Publish**.
4. גלגל השיניים ← **Project settings** ← למטה **Your apps** ← הסמל `</>` (Web). שם: `alina`, ולוחצים **Register app**.
5. מעתיקים את הערכים מתוך `firebaseConfig` לקובץ `firebase-config.js`.

### 2. GitHub Pages (האתר עצמו)
**Settings ← Pages ← Build and deployment**: Source = **Deploy from a branch**,
בוחרים את הענף `main` ואת התיקייה `/ (root)`, ולוחצים **Save**.
הכתובת תהיה: `https://3368499-blip.github.io/alina/`

## קבצים
- `index.html` — האפליקציה
- `firebase-config.js` — פרטי החיבור ל-Firebase. בלי הפרטים האפליקציה עובדת במצב הדגמה ושומרת רק במכשיר.
- `firestore.rules` — ההרשאות: כל אחד קורא וכותב, רק לרשימת המשימות.
- `logo.png`, `icon-*.png`, `manifest.webmanifest` — לוגו וסמל להוספה למסך הבית.
