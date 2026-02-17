# Lapak (Layanan Administrasi Peminjaman Akses Kampus)

## Studi Kasus
Topik: Sistem Peminjaman Ruangan Kampus
  • Bentuk Tugas: Individu
  • Target output:
Aplikasi web yang dikembangkan menggunakan ASP.NET sebagai backend, dengan frontend
diutamakan menggunakan React dengan TypeScript. Apabila belum memungkinkan,
frontend dapat menggunakan teknologi standar berupa HTML, CSS, dan JavaScript.

Fitur Utama yang Diharapkan
1. Pencatatan Peminjaman Ruangan
  Sistem mampu mencatat data peminjaman ruangan yang diajukan oleh pengguna.
  Cakupan umum:
    • Menambah data peminjaman
    • Melihat daftar peminjaman
    • Melihat detail peminjaman
    • Mengubah dan menghapus data peminjaman
2. Pengelolaan Status Peminjaman
  Setiap peminjaman memiliki status yang menunjukkan kondisi terkini, misalnya menunggu persetujuan, disetujui, atau ditolak.
  Cakupan umum:
    • Melihat status peminjaman
    • Mengubah status peminjaman
    • Menyimpan riwayat perubahan status (opsional)
3. Riwayat dan Penelusuran Peminjaman
  Sistem memungkinkan pengelola untuk menelusuri data peminjaman yang telah tersimpan.
  Cakupan umum:
    • Menampilkan riwayat peminjaman
    • Pencarian atau filter data peminjaman
    • Pengurutan data berdasarkan kriteria tertentu (opsional)
    • Kriteria pencarian dan teknik implementasi ditentukan oleh mahasiswa

## Stack
- Frontend = React Typescript
- Styling = Tailwindcss
- Icons = Lucide React
- Backend = Dotnet
- Database = PostgreSQL

##Alur kerja
1. Frontend
   - Request Data: Saat halaman dibuka, React menjalankan useEffect untuk memanggil fungsi fetch (contoh: fetchBookings).
   - State Management: Data dari API disimpan dalam State (Contoh: bookings, rooms, buildings).
   - Rendering: React memapping data ke komponen tabel dan card secara asinkron
2. Backend
   - Endpoint: Backend menyediakan RestfuL API contohnya POST /api/booking
   - Controller dan logic: API menerima JSON, melakukan validasi, dan berkomunikasi dengan database melalui ENtity Framework core
   - Response: Backend mengembalikan kode status HTTP beserta data yang diminta

## Cara menjalankan proyek
1. Clone Repository
2. Setup Backend
    - Namun sebelum itu harus masuk dengan
     jalankan di terminal
    - cd src
    - cd lapak-backend
    - cd lapak-backend
    - Kemudian jalanakna dotnet ef database update
    - dotnet run (untuk menjalankan api)
3. setup frontend
    - Masuk ek folder frontend
    - kemudian masuk ke lapak-frontend 
     jalankan di terminal
    - cd lapak-frontend
    - npm install
    - npm start
  
## API spec
port yang dipakai 5298

1. Booking
   - GET /api/Booking
      untuk dapat semua data peminjam, bisa untuk search dan dapatkan riwayat
   - POST /api/Booking
      untuk buat peminjaman baru, dimana statusnya otomatis pending
   - PUT /api/Booking/{id}
      untuk memperbarui detail data peminjaman 
   - PATCH /api/Booking/{id}/status
      untuk memperbarui status saja
   - DELETE /api/Booking/{id}
      untuk menghapus data peminjaman(hard delete)
     
2. Building
   - GET /api/Building
   - POST /api/Building
   - DELETE /api/Building/{id}
     
3. Room
   - GET /api/Room
   - POST /api/Room
   
