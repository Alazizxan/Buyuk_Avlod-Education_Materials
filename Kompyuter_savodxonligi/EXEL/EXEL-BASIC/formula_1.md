# Excel Formulalari (Rus Tili) – Mukammal Qo‘llanma

Ushbu faylda Excel dasturidagi rus tilidagi asosiy formulalar va funksiyalar keltirilgan. Har bir formula uchun inglizcha ekvivalenti, tavsif va amaliy misol mavjud.  

---

## 1. Matematik va Statistik formulalar

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| SUM(A1:A10) | СУММ(A1:A10) | Tanlangan diapazonni yig‘adi | =СУММ(A1:A5) → 10 |
| AVERAGE(A1:A10) | СРЗНАЧ(A1:A10) | O‘rtacha qiymat | =СРЗНАЧ(A1:A5) → 2 |
| MAX(A1:A10) | МАКС(A1:A10) | Eng katta qiymat | =МАКС(A1:A5) → 5 |
| MIN(A1:A10) | МИН(A1:A10) | Eng kichik qiymat | =МИН(A1:A5) → 1 |
| COUNT(A1:A10) | СЧЁТ(A1:A10) | Sonlarni sanaydi | =СЧЁТ(A1:A5) → 5 |
| ROUND(A1, 2) | ОКРУГЛ(A1; 2) | Qiymatni yaxlitlaydi | =ОКРУГЛ(3.1415;2) → 3.14 |
| INT(A1) | ЦЕЛОЕ(A1) | Butun qismini chiqaradi | =ЦЕЛОЕ(3.7) → 3 |
| ABS(A1) | МОД(A1) | Modul (musbat qiymat) | =МОД(-5) → 5 |
| POWER(A1,2) | СТЕПЕНЬ(A1;2) | Darajaga ko‘taradi | =СТЕПЕНЬ(3;2) → 9 |
| SQRT(A1) | КОРЕНЬ(A1) | Kvadrat ildiz | =КОРЕНЬ(9) → 3 |

---

## 2. Matn bilan ishlash

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| CONCAT(A1, B1) | СЦЕПИТЬ(A1; B1) | Matnlarni birlashtiradi | =СЦЕПИТЬ("Salom"; " Dunyo") → Salom Dunyo |
| LEFT(A1,5) | ЛЕВСИМВ(A1;5) | Chapdan belgilarni oladi | =ЛЕВСИМВ("Excel";3) → Exc |
| RIGHT(A1,5) | ПРАВСИМВ(A1;5) | O‘ngdan belgilarni oladi | =ПРАВСИМВ("Excel";3) → cel |
| LEN(A1) | ДЛСТР(A1) | Matn uzunligi | =ДЛСТР("Excel") → 5 |
| TRIM(A1) | СЖПРОБЕЛЫ(A1) | Bo‘sh joylarni olib tashlaydi | =СЖПРОБЕЛЫ(" Excel  ") → Excel |
| FIND("x", A1) | НАЙТИ("x";A1) | Belgini matnda qidiradi | =НАЙТИ("c";"Excel") → 4 |
| REPLACE(A1,2,3,"abc") | ЗАМЕНИТЬ(A1;2;3;"abc") | Belgilarni almashtiradi | =ЗАМЕНИТЬ("Excel";2;3;"abc") → Eabcel |

---

## 3. Mantiqiy formulalar

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| IF(A1>10,"Yes","No") | ЕСЛИ(A1>10;"Да";"Нет") | Shartga qarab qiymat | =ЕСЛИ(12>10;"Да";"Нет") → Да |
| AND(A1>5,B1<10) | И(A1>5;B1<10) | Barcha shartlar to‘g‘ri bo‘lsa TRUE | =И(6>5;3<10) → TRUE |
| OR(A1>5,B1<10) | ИЛИ(A1>5;B1<10) | Har qanday shart to‘g‘ri bo‘lsa TRUE | =ИЛИ(4>5;3<10) → TRUE |
| NOT(A1>5) | НЕ(A1>5) | Shartni inkor qiladi | =НЕ(6>5) → FALSE |
| IFERROR(A1/B1,"Error") | ЕСЛИОШИБКА(A1/B1;"Ошибка") | Xatolik bo‘lsa qiymat beradi | =ЕСЛИОШИБКА(5/0;"Ошибка") → Ошибка |

---

## 4. Qidiruv formulalari

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| VLOOKUP(lookup_value, table_array, col_index, FALSE) | ВПР(lookup_value;table_array;col_index;ЛОЖЬ) | Vertikal qidiruv | =ВПР(2;A1:B5;2;ЛОЖЬ) → mos qiymat |
| HLOOKUP(lookup_value, table_array, row_index, FALSE) | ГПР(lookup_value;table_array;row_index;ЛОЖЬ) | Gorizontal qidiruv | =ГПР(2;A1:E2;2;ЛОЖЬ) → mos qiymat |
| MATCH(lookup_value, lookup_array,0) | ПОИСКПОЗ(lookup_value;lookup_array;0) | Qiymatning indeksini qaytaradi | =ПОИСКПОЗ(5;A1:A10;0) → 3 |
| INDEX(array, row, col) | ИНДЕКС(array; row; col) | Tanlangan element | =ИНДЕКС(A1:B5;2;2) → qiymat |

---

## 5. Sana va vaqt

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| TODAY() | СЕГОДНЯ() | Bugungi sana | =СЕГОДНЯ() → 2025-10-13 |
| NOW() | ТДАТАВРЕМЯ() | Hozirgi sana va vaqt | =ТДАТАВРЕМЯ() → 2025-10-13 13:45 |
| YEAR(A1) | ГОД(A1) | Yil | =ГОД("2025-10-13") → 2025 |
| MONTH(A1) | МЕСЯЦ(A1) | Oy | =МЕСЯЦ("2025-10-13") → 10 |
| DAY(A1) | ДЕНЬ(A1) | Kun | =ДЕНЬ("2025-10-13") → 13 |
| HOUR(A1) | ЧАС(A1) | Soat | =ЧАС("13:45") → 13 |
| MINUTE(A1) | МИНУТА(A1) | Daqiqa | =МИНУТА("13:45") → 45 |
| SECOND(A1) | СЕКУНДА(A1) | Soniya | =СЕКУНДА("13:45:30") → 30 |

---

## 6. Pul va moliya

| Inglizcha | Ruscha | Tavsif | Misol |
|------------|--------|--------|-------|
| PMT(rate,nper,pv) | ПЛТ(ставка;срок;сумма) | Har oy to‘lovini hisoblaydi | =ПЛТ(0.05/12;12*5;10000) |
| FV(rate,nper,pmt) | БС(ставка;срок;платеж) | Kelajakdagi qiymat | =БС(0.05/12;12*5;-100) |
| PV(rate,nper,pmt) | НС(ставка;срок;платеж) | Hozirgi qiymat | =НС(0.05/12;12*5;-100) |

---

**Izoh:**  
- Ruscha formulalar sizning Excel interfeysingiz rus tilida bo‘lganda ishlaydi.  
- Inglizcha formulalar global standart, ruscha esa faqat rus interfeysi uchun.  
- Ushbu fayl GitHub README.md sifatida ishlatilishi qulay.  

