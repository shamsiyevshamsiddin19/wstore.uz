# 🛒 wstore.uz — Raqamli Mahsulotlar Marketi (Django Platformasi)

**wstore.uz** — dasturchilar, frilanserlar va mualliflar uchun tayyor kod loyihalari, Telegram botlar, veb-saytlar, mobil ilovalar va skriptlarni sotish hamda sotib olish uchun mo'ljallangan raqamli bozor platformasi.

---

## 🚀 Texnologiyalar to'plami

- **Backend:** Python 3.12, Django 5.x
- **Ma'lumotlar bazasi:** PostgreSQL (ishlab chiqarish) / SQLite (lokal test)
- **Frontend & Stil:** HTML5, Modern CSS3 (Dark Theme dizayn), Vanilla JavaScript
- **To'lov integratsiyasi:** Click Merchant API & to'lov ko'prigi
- **Autentifikatsiya:** Google OAuth 2.0 (yagona xavfsiz kirish)
- **Ko'p tillilik (i18n):** O'zbekcha (asosiy), Ruscha, Inglizcha

---

## ✨ Imkoniyatlar va Funksiyalar

1. **Katalog & Qidiruv:**
   - Kategoriya va texnologiyalar (Python, Django, Flutter, PHP, JS va h.k.) bo'yicha saralash
   - Narx oralig'i, reyting va saralash (eng yangi, arzon, qimmat)
   - Jonli qidiruv tizimi

2. **Google OAuth orqali kirish:**
   - Parolsiz, xavfsiz va bir bosqichli Google autentifikatsiyasi
   - Yangi foydalanuvchilar uchun avtomatik profil yaratish

3. **Sotuvchi va Xaridor Paneli:**
   - Yangi mahsulot yuklash (fayllar, skrinshotlar, narx, tavsif)
   - Buyurtmalar tarixi va to'lov holati
   - Sotuvchi balansi va mablag'ni yechib olish so'rovlari

4. **To'lov Tizimi (Click API):**
   - Click tizimi orqali to'lov havolasini generatsiya qilish
   - To'lov tasdiqlangach faylni xavfsiz yuklab olish imkoniyati

5. **Lokalizatsiya (Ko'p tilli):**
   - Sayt interfeysini o'zbek, rus va ingliz tillarida to'liq qo'llab-quvvatlash (`locale/`)

---

## 🛠️ O'rnatish va Ishga Tushirish

### 1. Repozitoriyani klonlash
```bash
git clone https://github.com/shamsiyevshamsiddin19/wstore.uz.git
cd wstore.uz
```

### 2. Virtual muhit yaratish va faollashtirish
```bash
python3 -m venv venv
source venv/bin/activate  # Linux / macOS
# yoki Windows: venv\Scripts\activate
```

### 3. Bog'liqliklarni o'rnatish
```bash
pip install -r requirements.txt
```

### 4. Muhit sozlamalarini sozlash (.env)
```bash
cp .env.example .env
```
`.env` faylida quyidagi sozlamalarni o'zingizga moslang:
- `SECRET_KEY`
- `DEBUG=True` (lokal muhitda)
- `DATABASE_URL` (bo'sh qoldirilsa SQLite ishlatiladi)
- `GOOGLE_OAUTH_CLIENT_ID` va `GOOGLE_OAUTH_CLIENT_SECRET` (Google OAuth uchun)
- `CLICK_SERVICE_ID`, `CLICK_MERCHANT_ID` (to'lovlar uchun)

### 5. Ma'lumotlar bazasi migratsiyalari
```bash
python manage.py migrate
```

### 6. Namunaviy ma'lumotlarni yuklash (ixtiyoriy)
```bash
python manage.py seed_data
```

### 7. Loyihani ishga tushirish
```bash
python manage.py runserver
```
Brauzerda: `http://127.0.0.1:8000` manziliga kiring.

---

## 📂 Loyiha Strukturasi

```
wstore.uz/
├── apps/
│   ├── core/         # Asosiy modellar, Google OAuth, yordamchi filtrlar
│   ├── orders/       # Buyurtmalar, to'lovlar, sotuvchi balansi
│   └── store/        # Mahsulotlar katalogi, sharhlar, wishlist
├── config/           # Django settings, asgi, wsgi, urls
├── locale/           # uz, ru, en tarjima fayllari
├── media/            # Mahsulot skrinshotlari va muqovalari
├── static/           # CSS, JS, rasmlar va logotiplar
├── templates/        # HTML andozalari (base, navbar, footer, catalog)
├── .env.example      # Namunaviy konfiguratsiya
├── manage.py         # Django boshqaruv skripti
└── requirements.txt  # Python paketlari
```

---

## 👨‍💻 Muallif

- **Shamsiddin Shamsiyev** — [GitHub Profili](https://github.com/shamsiyevshamsiddin19)
