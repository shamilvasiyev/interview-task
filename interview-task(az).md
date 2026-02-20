### JS Final

| Tapşırıq                   | Fokus                              | Çətinlik   | Təxmini Vaxt |
| -------------------------- | ---------------------------------- | ---------- | ------------ |
| **1. Fon Rəng**            | DOM Seçimi və Stil                 | Asan       | 15 dəq       |
| **2. Input Validation**    | Hadisələr (Events) və Şərtlər      | Asan-Orta  | 20 dəq       |
| **3. Qiymət Kalkulyatoru** | Massiv İterasiyası və Checkbox-lar | Asan-Orta  | 25 dəq       |
| **4. Taymer**              | Asinxron JS (`setInterval`)        | Orta-Çətin | 30 dəq       |
| **5. Data Fetching**       | Async/Await və API Məntiqi         | Çətin      | 30 dəq       |

---

### 1. Fon Rəngi (The Background Color Flipper)

**Məqsəd:** Düyməyə kliklədikdə `document.body`-nin fon rəngini verilmiş massivdən təsadüfi bir rənglə dəyişən proqram hazırlayın: `['#FF5733', '#33FF57', '#3357FF', '#F333FF']`.

- **Tələb:** Cari rəngin hex kodunu ekrandakı `<span>` daxilində göstərin.
- **Nə üçün?** Elementlərin seçilməsi və CSS xüsusiyyətlərinin JS vasitəsilə manipulyasiyasını yoxlayır.

### 2. Input Validation

**Məqsəd:** Bir `<input>` və sayğac (məsələn, "0/20") yaradın. İstifadəçi yazdıqca rəqəm yenilənməlidir.

- **Tələb:** Əgər simvol sayı 20-ni keçərsə, sayğacın mətni qırmızıya çevrilməli və "Göndər" (Submit) düyməsi bloklanmalıdır (disabled).
- **Nə üçün?** `input` hadisələrini və UI vəziyyətinin (state) sinxronizasiyasını öyrədir.

### 3. Məhsul Qiyməti Kalkulyatoru

**Məqsəd:** İstifadəçilərin məhsulları seçə biləcəyi və ümumi qiyməti hesablaya biləcəyi bir səhifə yaradın.

- **Massiv:**

```js
const products = [
  { id: 1, name: "Keyboard", price: 50 },
  { id: 2, name: "Mouse", price: 30 },
  { id: 3, name: "Monitor", price: 300 },
  { id: 4, name: "Headphones", price: 80 },
];
```

- **Tələb:** 1. Hər bir məhsulun yanında **checkbox** olmaqla siyahını ekranda göstərin (render).

2. İstifadəçi "Cəmi Hesabla" düyməsinə kliklədikdə, yalnız seçilmiş məhsulların qiymətini toplayın və nəticəni ekranda göstərin.

- **Nə üçün?** Tələbələrə DOM elementlərini (checkbox) məlumat mənbəyi (array) ilə əlaqələndirməyi öyrədir.

---

### 4. 60 Saniyəlik Geri Sayım

**Məqsəd:** Ekrandakı 60-dan 0-a qədər geri sayımı başladan "Start" düyməsi yaradın.

- **Tələb:** "Start" düyməsi bir neçə dəfə kliklənsə belə, taymerin sürətlənməsinin qarşısını alın. Sayğac 0-a çatdıqda "Vaxt bitdi!" mesajını (alert) göstərin.
- **Nə üçün?** `setInterval` funksiyasını və yaddaş sızmalarının (memory leaks) qarşısını almaq üçün "interval təmizləmə" məntiqini mənimsədir.

### 5. "Dinamik İstifadəçi" Kartı

**Məqsəd:** "Yeni İstifadəçi" düyməsinə kliklədikdə əvvəlcə 1-dən 10-a qədər təsadüfi bir ID yaradın, sonra həmin ID-yə uyğun istifadəçini `fetch()` vasitəsilə gətirin.

- **Tələb:** 1. Düyməyə klikləndikdə `Math.random()` istifadə edərək 1 və 10 daxil olmaqla təsadüfi tam ədəd yaradın.

2. Həmin rəqəmi sorğu ünvanına əlavə edin (məsələn: `https://jsonplaceholder.typicode.com/users/ID`).
3. Gələn məlumatdan istifadəçinin adını, e-poçtunu və ünvan (address/city) məlumatlarını ekranda göstərin.

- **Nə üçün?** Bu tapşırıq tələbənin həm riyazi metodlarla işləmək, həm də **Template Literals** (şablon sətirlər) vasitəsilə dinamik URL-lər yaratmaq bacarığını yoxlayır.

---

### Tələbələr üçün kiçik ipucu:

Sorğu ünvanını qurarkən statik link deyil, dəyişəndən istifadə etmək daha effektivdir:
`fetch(\`[https://www.google.com/search?q=https://jsonplaceholder.typicode.com/users/$](https://jsonplaceholder.typicode.com/users/$){randomID}`)`
