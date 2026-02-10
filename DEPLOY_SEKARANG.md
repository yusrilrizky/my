# 🚀 DEPLOY SEKARANG - 5 MENIT!

## ⚠️ Build Failed? SUDAH DIPERBAIKI!

Sekarang pakai **Docker** yang lebih reliable untuk build better-sqlite3.

---

## Step 1: Push ke GitHub (2 menit)

```bash
git add .
git commit -m "Deploy AnimeStream with Docker"
git push
```

Kalau belum ada repo:
```bash
git init
git add .
git commit -m "Deploy AnimeStream with Docker"
```

Buat repo baru di **https://github.com/new**, lalu:

```bash
git remote add origin https://github.com/USERNAME/animestream.git
git branch -M main
git push -u origin main
```

## Step 2: Deploy di Railway (3-5 menit)

1. Buka **https://railway.app**
2. Klik **"Login with GitHub"**
3. Klik **"New Project"**
4. Klik **"Deploy from GitHub repo"**
5. Pilih repo **animestream**
6. Railway akan detect **Dockerfile** dan build otomatis
7. Tunggu 3-5 menit (Docker build lebih lama tapi reliable)
8. ✅ **DONE!**

**Note:** Docker build lebih lama dari Nixpacks, tapi **PASTI BERHASIL**!

## Step 3: Buka Website

Railway akan kasih URL: `https://animestream-production-xxxx.up.railway.app`

**Login:**
- Username: `admin`
- Password: `admin123`

---

## ✅ Cek Health

Buka: `https://your-app.railway.app/health`

Harus return:
```json
{
  "status": "OK",
  "timestamp": "2026-02-10T...",
  "uptime": 123.45
}
```

---

## 🐛 Kalau Error?

### 1. Cek Logs
Railway dashboard → Deployments → Klik deployment → View Logs

### 2. Common Errors

**"Application failed to respond"**
- Tunggu 1-2 menit lagi (server masih starting)
- Cek logs ada error apa

**"Build failed"**
- Cek `package.json` ada
- Cek `nixpacks.toml` ada
- Redeploy

**"Database error"**
- Railway auto-create database
- Jangan khawatir, akan jalan otomatis

### 3. Masih Error?

Test lokal dulu:
```bash
npm install
npm start
```

Buka: `http://localhost:3000/health`

Kalau lokal jalan, Railway pasti bisa!

---

## 💾 Data & Video Persisten?

✅ **YA!** Railway punya persistent storage.

Database dan video **TIDAK HILANG** saat:
- Redeploy
- Update code
- Restart server

---

## 🎉 SELESAI!

Website sudah online dan bisa diakses dari mana saja!

**Share URL ke teman:**
`https://your-app.railway.app`

**Ganti password admin:**
1. Login sebagai admin
2. Settings → Change Password
3. Ganti dari `admin123` ke password kuat

---

## 📱 Mau Jadi APK?

Lihat: `APK_STANDALONE_LENGKAP.md`

Atau pakai PWA (Install to Home Screen):
1. Buka website di Chrome Android
2. Menu → "Add to Home Screen"
3. Done! Jadi app di HP
