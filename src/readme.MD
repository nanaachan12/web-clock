Kode ini menggunakan jQuery dan Moment.js untuk menampilkan serta memperbarui waktu dan tanggal secara real-time dalam format lokal Indonesia. Berikut adalah penjelasan bagian per bagiannya:

1️⃣ Import Library
js
Salin
Edit
import $ from 'jquery';
import moment from 'moment';
import $ from 'jquery' → Mengimpor jQuery untuk memudahkan manipulasi DOM.

import moment from 'moment' → Mengimpor Moment.js untuk menangani format waktu dan tanggal.

2️⃣ Fungsi displayTime()
js
Salin
Edit
const displayTime = () => {
  moment.locale('id'); // Mengatur bahasa Indonesia

  $('.time').text(moment().format('LTS')); // Format waktu (Jam:Menit:Detik)
  $('.date').text(moment().format('LL'));  // Format tanggal (Hari, Tanggal Bulan Tahun)
};
✅ Apa yang dilakukan fungsi ini?

Mengatur lokal ke bahasa Indonesia → moment.locale('id').

Menampilkan waktu sekarang dalam format LTS (Long Time String) → "HH:mm:ss".

Menampilkan tanggal sekarang dalam format LL (Long Date) → "D MMMM YYYY".

💡 Contoh hasil tampilan:

html
Salin
Edit
<span class="time">12:34:56</span>  <!-- Format jam -->
<span class="date">24 Maret 2025</span> <!-- Format tanggal -->
3️⃣ Fungsi updateTime()
js
Salin
Edit
const updateTime = () => {
  displayTime(); // Perbarui tampilan waktu
  setTimeout(updateTime, 1000); // Panggil lagi setelah 1 detik
};
✅ Apa yang dilakukan fungsi ini?

Memanggil displayTime() untuk memperbarui waktu saat ini.

Menggunakan setTimeout(updateTime, 1000) agar fungsi ini terus dipanggil setiap 1 detik untuk memperbarui waktu secara real-time.

4️⃣ Menjalankan updateTime()
js
Salin
Edit
updateTime();
Memulai proses pembaruan waktu secara otomatis.

Setiap detik, waktu dan tanggal pada halaman akan diperbarui.

🔹 Kesimpulan
🔥 Kode ini berfungsi untuk menampilkan waktu dan tanggal real-time di halaman web menggunakan jQuery dan Moment.js.
✅ Tampilan waktu diperbarui setiap detik tanpa perlu reload halaman.
✅ Menggunakan bahasa Indonesia untuk format tanggal dan waktu.

🚀 Cocok digunakan untuk jam digital di website!