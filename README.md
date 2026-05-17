# 📍 MyLocationTracker

<p align="center">
  <strong>Aplikasi Android berbasis Google Maps untuk melacak posisi pengguna dan menggambar rute perjalanan secara real-time.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin&logoColor=white" alt="Kotlin"/>
  <img src="https://img.shields.io/badge/Maps-Google%20Maps-4285F4?logo=googlemaps&logoColor=white" alt="Google Maps"/>
  <img src="https://img.shields.io/badge/Location-Fused%20Location-green" alt="Fused Location"/>
  <img src="https://img.shields.io/badge/UI-ViewBinding-orange" alt="ViewBinding"/>
</p>

---

## 📖 Tentang Project

**MyLocationTracker** adalah aplikasi Android yang menampilkan posisi pengguna di Google Maps dan merekam pergerakan lokasi sebagai lintasan. Aplikasi menggunakan **Fused Location Provider** untuk mengambil lokasi secara periodik, lalu menggambar polyline pada map.

## ✨ Fitur

| Fitur | Deskripsi |
|-------|-----------|
| 🗺️ **Google Maps View** | Menampilkan peta sebagai layar utama aplikasi |
| 📌 **Start Marker** | Menandai lokasi awal pengguna |
| ▶️ **Start / Stop Tracking** | Mengaktifkan atau menghentikan pelacakan lokasi |
| 🧵 **Polyline Route** | Menggambar lintasan perjalanan di atas peta |
| 🔐 **Runtime Permission** | Meminta permission lokasi fine dan coarse |
| 🛰️ **GPS Settings Check** | Mengecek dan meminta aktivasi GPS jika diperlukan |

## 🛠️ Tech Stack

| Layer | Teknologi |
|-------|-----------|
| Language | Kotlin |
| Map | Google Maps SDK |
| Location | Google Play Services Location |
| UI | XML Layout, ViewBinding |
| Android | AppCompat |

## 📂 Struktur Project

```text
MyLocationTracker/
├── app/src/main/java/com/dicoding/mylocationtracker/
│   └── MapsActivity.kt        # Logic map, permission, location update, polyline
├── app/src/main/res/layout/
│   └── activity_maps.xml      # Layout map dan tombol tracking
├── app/src/main/res/values/
│   └── strings.xml            # Label aplikasi dan tombol
└── app/src/main/AndroidManifest.xml
```

## 🚀 Cara Menjalankan

1. Buka project di **Android Studio**.
2. Pastikan Google Maps API key aktif dan valid.
3. Jalankan **Gradle Sync**.
4. Run aplikasi pada emulator atau device dengan Google Play Services.
5. Berikan permission lokasi saat aplikasi meminta akses.

## 🔄 Alur Tracking

```text
Cek permission lokasi
        ↓
Ambil lokasi terakhir
        ↓
Tampilkan start marker
        ↓
Start location updates
        ↓
Tambah titik LatLng ke list
        ↓
Gambar polyline di Google Maps
```

## 🔐 Catatan API Key

Untuk production, API key Google Maps sebaiknya tidak ditulis langsung di `AndroidManifest.xml`. Batasi API key melalui Google Cloud Console dan gunakan konfigurasi yang lebih aman.