# Mini Interaktiv Sahifa — Boshlovchilar uchun Topshiriq

**Daraja:** Beginner



---

## 1. Loyiha tavsifi
Sizdan kichik bir web sahifa yaratish so‘raladi: bu sahifa bir nechta bo‘limlarga (section) bo‘lingan bo‘ladi. Har bir bo‘lim o‘ziga xos funksiya bajaradi:

- **Salomlashish:** foydalanuvchi ism kiritadi va tugma bosilganda "Salom, [ism]!" chiqadi.
- **Rang almashtirish:** kvadrat elementning rangi va ichidagi matni siz belgilagan ranglar bo‘ylab o‘zgaradi.
- **Matn o‘zgartirish:** bir matn paragrafiga tugma bosilganda boshqa matn chiqadi.
- **Bo‘limlarni almashtirish (tabs):** yuqoridagi tugmalar yordamida bo‘limlar orasida almashish.

Bu loyiha bir nechta kichik topshiriqlarni bir joyda mashq qilish uchun mo‘ljallangan.

---

## 2. Nimalar qilish kerak — Bosqichma-bosqich
Quyidagi bosqichlarni bajarish tavsiya etiladi. Har bir bosqichni yakunlaganingizda kodni tekshirib ko‘ring.

### 2.1. Fayllar tuzilmasi
Loyiha papkangiz quyidagi fayllardan iborat bo‘lsin:

```
mini-interaktiv-sahifa/
├─ index.html
├─ style.css
└─ script.js
```

> Eslatma: Hamma kodni bitta `index.html` ichida yozishingiz ham mumkin, lekin alohida fayllarga bo‘lish yaxshi amaliyot.

### 2.2. `index.html` — struktura
- `<header>` ichida loyihaning nomi.
- Navigation uchun 3 ta tugma: `Salomlashish`, `Rang`, `Matn`.
- Har bir bo‘lim uchun `<section id="..." class="section">` — boshlang‘ich faqat bir bo‘lim `active` klassiga ega bo‘lsin.
- Salomlashish bo‘limida `input` va `button`, natija uchun `div` yoki `p`.
- Rang bo‘limida rangli kvadrat (`div#box`) va rangni almashtiruvchi `button`.
- Matn bo‘limida paragraf va `button`.

### 2.3. `style.css` — oddiy dizayn
- `.section { display: none; }` va `.section.active { display: block; }`.
- Tugmalar, `#box` va umumiy layout uchun minimal style qo‘shing.

### 2.4. `script.js` — vazifalar
Bajarilishi kerak bo‘lgan funksiyalar:

1. `showSection(id)` — barcha bo‘limlardan `active` klassini olib tashlab, tanlanganiga `active` qo‘shadi. (Xatolikdan himoya: `document.getElementById(id)` null bo‘lsa console warning chiqsin.)

2. `salomlash()` — `input`dagi qiymatni olib, agar bo‘sh bo‘lsa ogohlantirish, aks holda `Salom, [ism]!` chiqaradi.

3. `rangOzgartir()` — `ranglar` massividan navbatdagi rangni oladi, `#box` elementining `style.backgroundColor`ini va `innerText`ini yangilaydi.

4. `matnOzgartir()` — paragraf matnini almashtiradi (toggle qilishi mumkin).

---

## 3. Boshlang‘ich (starter) kod namunasi
Quyidagi qisqa namunaviy kodni boshlang‘ich nuqta sifatida ishlatishingiz mumkin.

**index.html** (faqat strukturani ko‘rsatadi, style va script tashqi fayllarda bo‘lishi mumkin):

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mini Interaktiv Sahifa</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Mini Interaktiv Sahifa</h1>
  <div class="nav">
    <button onclick="showSection('salom')">Salomlashish</button>
    <button onclick="showSection('rang')">Rang</button>
    <button onclick="showSection('matn')">Matn</button>
  </div>

  <section id="salom" class="section active">
    <h2>Salomlashish</h2>
    <input id="ism" placeholder="Ismingizni kiriting">
    <button onclick="salomlash()">Salom aytish</button>
    <p id="natija"></p>
  </section>

  <section id="rang" class="section">
    <h2>Rang</h2>
    <div id="box">Rang</div>
    <button onclick="rangOzgartir()">Almashtirish</button>
  </section>

  <section id="matn" class="section">
    <h2>Matn</h2>
    <p id="paragraf">Bu matn o‘zgartiriladi.</p>
    <button onclick="matnOzgartir()">Matnni o‘zgartir</button>
  </section>

  <script src="script.js"></script>
</body>
</html>
```

**script.js** (asosiy funksiyalar):

```js
function showSection(id) {
  const sections = document.querySelectorAll('.section');
  sections.forEach(sec => sec.classList.remove('active'));
  const target = document.getElementById(id);
  if (target) {
    target.classList.add('active');
  } else {
    console.warn('showSection: id topilmadi ->', id);
  }
}



---

## 4. Tekshiruv — nima ishlashini sinash
- Sahifani oching (`index.html`).
- Tugmalar orqali bo‘limlar orasida almashishni tekshiring.
- Salomlashish bo‘limida ism yozib "Salom aytish" tugmasini bosing.
- Rang bo‘limida "Almashtirish" tugmasini bir nechta marta bosing — ranglar aylanib turishi kerak.
- Matn bo‘limida tugmani bosib matn toggle bo‘lishini tekshiring.

---

## 5. Qo‘shimcha (bonus) vazifalar — o‘zingizga qiyinroq qilib ko‘ring
1. `input type="color"` qo‘shib, foydalanuvchi tanlagan rangni boxga qo‘yish.
2. Bo‘lim o‘zgarganda eski bo‘limni `fade out`, yangi bo‘limni `fade in` animatsiya bilan ko‘rsatish (CSS transition yoki JavaScript yordamida).
3. LocalStorage bilan foydalanuvchi kirgan ismni saqlash va sahifa qayta yuklanganda avtomatik chiqarish.
4. `keydown` hodisasini qo‘shib, chap/o‘ng o‘q tugmalari bilan bo‘limlar orasida almashish.

---


