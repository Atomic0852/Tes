# Website dengan Database dan Server

Website lengkap dengan backend Express.js, database SQLite, dan frontend modern yang responsive.

## Fitur

- ✅ **Backend Server**: Express.js dengan REST API
- ✅ **Database**: SQLite dengan tabel Users dan Posts
- ✅ **Frontend**: HTML/CSS/JavaScript modern dan responsive
- ✅ **CRUD Operations**: Create, Read, Update, Delete untuk Users dan Posts
- ✅ **UI/UX**: Design modern dengan gradient, animations, dan responsive layout
- ✅ **Search**: Fitur pencarian untuk Users dan Posts
- ✅ **Modals**: Form popup untuk menambah/edit data
- ✅ **Notifications**: Toast notifications untuk feedback

## Prerequisites

Pastikan kamu sudah install:
1. **Node.js** (versi 14 atau lebih baru)
   - Download dari: https://nodejs.org/
   - Atau install via package manager

2. **npm** (biasanya sudah include dengan Node.js)

## Cara Menjalankan

### 1. Install Dependencies
```bash
npm install
```

### 2. Jalankan Server
```bash
npm start
```

Atau untuk development mode (auto-restart):
```bash
npm run dev
```

### 3. Buka Website
Buka browser dan akses: `http://localhost:3000`

## Struktur Project

```
├── package.json          # Dependencies dan scripts
├── server.js             # Backend server (Express.js)
├── database.sqlite       # Database SQLite (auto-generated)
└── public/               # Frontend files
    ├── index.html        # Main HTML file
    ├── style.css         # CSS styling
    └── script.js         # JavaScript functionality
```

## API Endpoints

### Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `POST /api/users` - Create new user
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

### Posts
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post

## Database Schema

### Users Table
- `id` (INTEGER PRIMARY KEY)
- `name` (TEXT NOT NULL)
- `email` (TEXT UNIQUE NOT NULL)
- `phone` (TEXT)
- `created_at` (DATETIME)

### Posts Table
- `id` (INTEGER PRIMARY KEY)
- `title` (TEXT NOT NULL)
- `content` (TEXT NOT NULL)
- `author_id` (INTEGER FOREIGN KEY)
- `created_at` (DATETIME)

## Fitur Website

### 1. Manajemen Users
- Tampilkan daftar users dalam tabel
- Tambah user baru dengan form modal
- Edit user yang sudah ada
- Hapus user dengan konfirmasi
- Pencarian users berdasarkan nama, email, atau phone

### 2. Manajemen Posts
- Tampilkan posts dalam grid layout
- Tambah post baru dengan form modal
- Hapus post dengan konfirmasi
- Pencarian posts berdasarkan judul, konten, atau author

### 3. UI/UX Features
- Design modern dengan gradient background
- Responsive layout untuk mobile dan desktop
- Smooth animations dan transitions
- Loading spinner saat proses data
- Toast notifications untuk feedback
- Modal forms untuk input data
- Search functionality dengan real-time filtering

## Customization

### Mengubah Port
Edit file `server.js` dan ubah:
```javascript
const PORT = process.env.PORT || 3000; // Ubah 3000 ke port yang diinginkan
```

### Mengubah Database
Untuk menggunakan database lain (MySQL, PostgreSQL), install driver yang sesuai dan update konfigurasi di `server.js`.

### Mengubah Styling
Edit file `public/style.css` untuk mengubah tampilan website.

## Troubleshooting

### Error "npm not found"
- Pastikan Node.js sudah terinstall
- Restart terminal/command prompt
- Cek PATH environment variable

### Port sudah digunakan
- Ubah port di `server.js`
- Atau kill process yang menggunakan port tersebut

### Database error
- Pastikan folder project bisa diakses untuk write
- Database akan dibuat otomatis saat pertama kali menjalankan server

## Development

Untuk development, gunakan:
```bash
npm run dev
```

Ini akan menjalankan server dengan nodemon yang auto-restart saat ada perubahan file.

## Production

Untuk production:
```bash
npm start
```

Pastikan untuk:
- Set environment variables yang diperlukan
- Gunakan database production (bukan SQLite)
- Setup reverse proxy (nginx/apache)
- Enable HTTPS
- Setup monitoring dan logging
