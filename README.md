# Tugas 9 MySQL

#### 1. Buat database niomic kemudian buat tabel mahasiswa_niomic dengan data sebagai berikut:
**(Note: Silahkan teman-teman berkreasi untuk tipe data.)**

![Tugas 9](https://github.com/troy213/tugas_9_mysql/blob/main/Tugas%209.png)
```
CREATE DATABASE niomic;

CREATE TABLE mahasiswa_niomic (
    nim INT UNSIGNED NOT NULL PRIMARY KEY, 
    nama VARCHAR(50), 
    asal VARCHAR(50), 
    jurusan VARCHAR(50), 
    nilai_uan DECIMAL(6,2)
);

INSERT INTO mahasiswa_niomic VALUES 
    (17020217, "James Situmorang", "Medan", "Kedokteran Gigi", 341.10),
    (17080225, "Husli Khairan", "Jakarta", "Akuntansi", 288.55),
    (17080305, "Rina Kumala Sari", "Jakarta", "Akuntansi", 337.99),
    (17090113, "Riana Putria", "Padang", "Kimia", 339.20),
    (17090222, "Sari Citra Lestari", "Jakarta", "Manajemen", 310.60),
    (17090308, "Christine Wijaya", "Medan", "Manajemen", 321.74),
    (17140119, "Sandri Fatmala", "Bandung", "Ilmu Komputer", 322.91),
    (17140120, "Bobby Permana", "Medan", "Ilmu Komputer", 280.82),
    (17140133, "Ikhsan Prayoga", "Jakarta", "Ilmu Komputer", 300.16),
    (17140143, "Rudi Permana", "Bandung", "Ilmu Komputer", 290.44);
```

#### 2. Ubah kolom mahasiswa_baru dengan nama = Irfan Arifin, asal =  Lampung dengan kondisi nim = '17020217'
```
UPDATE mahasiswa_niomic SET nama = "Irfan Arifin", asal = "Lampung" WHERE nim = 17020217;
```

#### 3. Ubah kolom nilai_uan = 5000 atas nama Husli Khairan. (Note: Gunakan perintah update ignore)
```
UPDATE IGNORE mahasiswa_niomic SET nilai_uan = 5000 WHERE nama = "Husli Khairan";
```

#### 4. Gunakan query replace untuk nilai nim = '17090141', nama =  'Lidya Fitriana', asal =  'Surabaya',  jurusan = 'Kimia' dan nilai_uan =  290.54;
```
REPLACE INTO mahasiswa VALUES (17090141, "Lidya Fitriana", "Surabaya", "Kimia", 290.54);
```
