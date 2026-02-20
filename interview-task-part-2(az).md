### JS Yekun (Hissə 2)

| Tapşırıq                             | Fokus                            | Çətinlik   | Təxmini Vaxt |
| ------------------------------------ | -------------------------------- | ---------- | ------------ |
| **1. Məhsul Kalkulyatoru**           | Checkbox-lar və Riyazi Hesablama | Asan       | 20 dəq       |
| **2. İstifadəçi Siyahısı İdarəçisi** | Massiv CRUD (Əlavə et/Sil)       | Asan-Orta  | 20 dəq       |
| **3. Canlı Axtarış Filtri**          | `filter()` və Real-vaxt UI       | Orta       | 25 dəq       |
| **4. Filtrli Todo Sistemi**          | Vəziyyət (State) əsaslı UI       | Orta-Çətin | 25 dəq       |
| **5. İnteraktiv Quiz Tətbiqi**       | Məntiq Axışı və Bal Hesablama    | Çətin      | 30 dəq       |

---

### 1. Məhsul Qiyməti Kalkulyatoru

**Məqsəd:** Massivdəki məlumatlar əsasında məhsul siyahısı yaradın və istifadəçinin seçiminə görə ümumi məbləği hesablayın.

- **Tələblər:** - Hər bir məhsul üçün ad, qiymət və checkbox olan bir siyahı yaradın.
- "Cəmi Hesabla" düyməsinə kliklədikdə, yalnız seçilmiş (checked) məhsulların qiymətini toplayın və nəticəni səhifədə göstərin.

- **Nə üçün?** Dövr operatorları (loops) və ya `reduce` metodundan istifadə edərək UI elementlərini (checkbox) data xüsusiyyətləri ilə əlaqələndirməyi öyrədir.

### 2. İstifadəçi Siyahısı İdarəçisi (User List Manager)

**Məqsəd:** İstifadəçilərin ad əlavə edib silə biləcəyi dinamik bir siyahı hazırlayın.

- **Tələblər:** - Adın daxil edilməsi üçün bir giriş sahəsi (input) və massivə ad əlavə edən "Əlavə et" düyməsi.
- Siyahıdakı hər bir elementin yanında həmin elementi silən "Sil" (Delete) düyməsi olmalıdır.
- Boş mətnlərin siyahıya əlavə edilməsinin qarşısını alın.

- **Nə üçün?** "Event Delegation" (hadisə nümayəndəliyi) və massivlər üzərində təməl əməliyyatları (`push`, `splice`) öyrədir.

### 3. Canlı Axtarış Filtri (Live Search Filter)

**Məqsəd:** İstifadəçi yazı yazdıqca real vaxtda yenilənən kurs axtarış sistemi yaradın.

- **Tələblər:** - Massivdə olan kursların siyahısını ekranda göstərin.
- Axtarış sahəsində yazı yazıldıqda, `.filter()` metodundan istifadə edərək yalnız uyğun gələn kursları göstərin (böyük/kiçik hərf həssaslığı olmasın).
- Heç bir nəticə tapılmadıqda "Kurs tapılmadı" mesajını göstərin.

- **Nə üçün?** `input` hadisələri ilə massiv filtrləmə məntiqi arasındakı əlaqəni mənimsədir.

---

### 4. Status Filtrli Todo Siyahısı

**Məqsəd:** UI-ın "Filtr" parametrinə görə dəyişdiyi, vəziyyət (state) yönümlü Todo tətbiqi hazırlayın.

- **Tələblər:** - İstifadəçilər tapşırıq əlavə edə və onları "Tamamlanmış" (class-ı dəyişərək) kimi qeyd edə bilsinlər.
- Üç düymə təmin edin: **Hamısı**, **Tamamlanmışlar** və **Aktivlər**.
- Seçilmiş filtrə əsasən siyahı avtomatik olaraq yenidən render edilməli və yalnız uyğun tapşırıqları göstərməlidir.

- **Nə üçün?** Bu məntiqdə böyük bir sıçrayışdır. Tələbələrə öyrədir ki, JS massivi UI üçün "Həqiqət Mənbəyi" (Source of Truth) rolunu oynamalıdır.

### 5. İnteraktiv Quiz Tətbiqi

**Məqsəd:** İrəliləyişi izləyən və yekun balı hesablayan çoxmərhələli proqram hazırlayın.

- **Tələblər:** - Obyektlərdən ibarət massivdən istifadə edərək hər dəfə yalnız bir sual göstərin.
- "Növbəti" (Next) düyməsi yalnız cavab seçildikdə işləməlidir.
- Sual massivi bitdikdə yekun balın göstərildiyi sonuncu ekranı təqdim edin.

- **Nə üçün?** "State Management" (cari indeksin izlənilməsi) və mürəkkəb şərtli məntiqləri (logic flow) yoxlayır.
