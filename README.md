# 🏺 Halli-Santhe Digital

**Hyper-Local Marketplace for Rural Artisans**

A Kotlin Android application connecting artisans with urban buyers, digitizing the traditional weekly market (santhe).

---

## 📱 Features

### Buyer Module
- Browse products in a 2-column grid (RecyclerView + GridLayoutManager)
- Live search by product name or category
- Detailed product view with artisan info and location
- Mock inquiry/messaging system

### Artisan Module
- Upload product with name, price, category, description, location
- Pick product image from gallery
- View and manage all listings
- Delete listings with confirmation

---

## 🏗 Architecture

```
MVVM
├── Model       → Room DB (Product, Inquiry entities)
├── ViewModel   → ProductViewModel (LiveData, coroutines)
└── View        → Activities + RecyclerView adapters
```

## 🎨 UI Theme

- **Primary**: Forest green `#2E7D32`
- **Dark green**: `#1B5E20`
- **Brown (earthy)**: `#5D4037` / `#3E2723`
- **Accent**: Amber `#FF8F00`

---

## 🚀 Setup Instructions

### Prerequisites
- Android Studio Hedgehog or newer
- JDK 17
- Android SDK 34

### Steps

1. **Open in Android Studio**
   ```
   File → Open → Select the HalliSanthe folder
   ```

2. **Sync Gradle**
   Android Studio will prompt you — click **Sync Now**

3. **Run on Device / Emulator**
   - Min SDK: API 21 (Android 5.0)
   - Click the ▶ Run button

> ⚠️ No Firebase/API keys needed — the app uses local Room database only.

---

## 📂 Project Structure

```
app/src/main/
├── java/com/halliSanthe/app/
│   ├── data/
│   │   ├── model/         Product.kt, Inquiry.kt
│   │   └── repository/    AppDatabase.kt, DAOs, Repository
│   ├── viewmodel/         ProductViewModel.kt
│   └── ui/
│       ├── SplashActivity.kt   (Role selection)
│       ├── buyer/              MainActivity + ProductAdapter
│       ├── artisan/            Dashboard + AddProduct + Adapter
│       └── detail/             ProductDetailActivity
└── res/
    ├── layout/            All XML layouts
    ├── values/            Colors, strings, themes, dimens
    └── drawable/          Badges, placeholders, icons
```

---

## ✅ PRD Objectives Achieved

| Requirement | Status |
|---|---|
| Artisan upload products | ✅ |
| Buyer browse grid layout | ✅ |
| Search by name/category | ✅ |
| Product detail view | ✅ |
| Mock inquiry/messaging | ✅ |
| Empty state handling | ✅ |
| MVVM architecture | ✅ |
| Room local database | ✅ |
| Image upload & preview | ✅ |
| Cultural green-brown UI | ✅ |
