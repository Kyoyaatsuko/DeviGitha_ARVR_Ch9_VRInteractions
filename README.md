# VR Interactions Demo — Chapter 9  
**Nama**: Devi Githa  
**NIM**: 21552011322
**Mata Kuliah**: Augmented & Virtual Reality  
**Dosen**: Andri Nugraha R  
**Unity Version**: 2022.3.20f1 (URP)  
**XR Interaction Toolkit**: v2.5.3  

---

## 🎯 Tujuan
Mengimplementasikan 4 jenis interaksi dasar VR menggunakan **XR Interaction Toolkit (XRIT)**:
1. Teleportation (Area & Anchor)  
2. Grab Interactables (Direct, Socket, Distance)  
3. Gaze Interactables (Hover, Combined, Timed)  
4. Poke Interactables (Button with particle, sound, UI update)

---

## 🖼️ Screenshot & Keterangan

### 1. Teleportation System  
![teleport_area_anchor](Screenshots/teleport_area_anchor.png)  
- **Kiri**: Teleportation Area (bidang biru) → bebas teleport di dalam area.  
- **Kanan**: Teleportation Anchor (cakram kuning) → snap ke posisi pasti.  
- Digunakan untuk navigasi antar meja demo.

### 2. Grab Interactables  
![grab_three_types](Screenshots/grab_three_types.png)  
Tiga kubus dengan jenis grab berbeda:  
- **Merah (Direct Grab)**: Velocity Tracked — bisa dilempar.  
- **Hijau (Socket Grab)**: Kinematic — kembali ke socket saat dilepas.  
- **Biru (Distance Grab)**: Instantaneous — tarik dari jarak jauh (ray highlight aktif).

### 3. Gaze Interactables  
![gaze_interactions](Screenshots/gaze_interactions.png)  
- **Hover Gaze**: Objek menyala saat dilihat.  
- **Combined Gaze**: Ray controller otomatis snap ke objek yang dilihat.  
- **Timed Gaze**: Tunggu 2 detik → teks berubah jadi “✔ Selected”.

### 4. Poke Interactables  
![poke_button_demo](Screenshots/poke_button_demo.png)  
Tombol 3D yang bereaksi saat “ditekan” oleh jari virtual:  
- ✅ Particle System menyala  
- ✅ Suara *click* diputar  
- ✅ UI counter bertambah (0 → 1 → 2…)

---

## ⚙️ Setup Teknis
- XR Origin (VR) digunakan sebagai base.  
- XR Device Simulator aktif untuk testing tanpa headset.  
- Input: Mouse + Keyboard (`WASD`, `1/2`, `Left Ctrl`, `Mouse0`).  
- Semua interaksi menggunakan komponen bawaan XRIT (tidak ada custom script selain `PokeButton.cs`).

> 🔗 Source referensi: [XRIT Examples Repo](https://github.com/Unity-Technologies/XR-Interaction-Toolkit-Examples)

---

## 📝 Catatan Tambahan
- Proyek ini dibuat sebagai latihan konsep Chapter 9, bukan untuk deployment komersial.  
- Kendala awal: konfigurasi XR Origin sempat gagal karena pakai `XR Player` lama — sudah diperbaiki dengan pakai `XR Origin (VR)` resmi XRIT.  
- Poke filter tidak diimplementasi karena fokus pada dasar interaksi; bisa dikembangkan di tugas lanjutan.

--- 

> *"The purpose of computing is insight, not numbers."*  
> — Richard Hamming
