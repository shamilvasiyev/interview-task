### JS Yekun (Hissə 2)

| Tapşırıq                                 | Fokus                      | Çətinlik   | Təxmini Vaxt |
| ---------------------------------------- | -------------------------- | ---------- | ------------ |
| **1. İstifadəçi Siyahısı İdarəedilməsi** | Massiv CRUD (Əlavə et/Sil) | Asan-Orta  | 20 dəq       |
| **2. Canlı Axtarış Filtri**              | `filter()` və Real-vaxt UI | Orta       | 25 dəq       |
| **3. Filtrli Todo Sistemi**              | State əsaslı UI            | Orta-Çətin | 25 dəq       |

---

### 1. İstifadəçi Siyahısı İdarəedilməsi (User List Manager)

**Məqsəd:** İstifadəçilərin ad əlavə edib silə biləcəyi dinamik bir siyahı hazırlayın.

- **Tələblər:** - Adın daxil edilməsi üçün bir giriş sahəsi (input) və massivə ad əlavə edən "Əlavə et" düyməsi.
- Siyahıdakı hər bir elementin yanında həmin elementi silən "Sil" (Delete) düyməsi olmalıdır.
- Boş mətnlərin siyahıya əlavə edilməsinin qarşısını alın.

- **Nə üçün?** "Event Delegation" və massivlər üzərində təməl əməliyyatları öyrədir.

### 2. Canlı Axtarış Filtri (Live Search Filter)

**Məqsəd:** İstifadəçi yazı yazdıqca real vaxtda yenilənən kurs axtarış sistemi yaradın.

- **Tələblər:** - Massivdə olan kursların siyahısını ekranda göstərin.
- Axtarış sahəsində yazı yazıldıqda, `.filter()` metodundan istifadə edərək yalnız uyğun gələn kursları göstərin (böyük/kiçik hərf həssaslığı olmasın).
- Heç bir nəticə tapılmadıqda "Kurs tapılmadı" mesajını göstərin.

- **Nə üçün?** `input` hadisələri ilə massiv filtrləmə məntiqi arasındakı əlaqəni mənimsədir.

---

### 3. Status Filtrli Todo Siyahısı

**Məqsəd:** UI-ın "Filtr" parametrinə görə dəyişdiyi, state yönümlü Todo tətbiqi hazırlayın.

- **Tələblər:** - İstifadəçilər tapşırıq əlavə edə və onları "Tamamlanmış" (class-ı dəyişərək) kimi qeyd edə bilsinlər.
- Üç düymə təmin edin: **Hamısı**, **Tamamlanmışlar** və **Aktivlər**.
- Seçilmiş filtrə əsasən siyahı avtomatik olaraq yenidən render edilməli və yalnız uyğun tapşırıqları göstərməlidir.

- **Nə üçün?** - Ekranda gördüyümüz hər şey birbaşa JavaScript-dəki məlumatlardan (massivdən) asılı olmalıdır. Yəni, kodda məlumat dəyişirsə, səhifə də ona uyğun avtomatik yenilənməlidir.
