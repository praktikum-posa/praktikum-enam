# Pertemuan Enam: Arsip File dan Sistem Kompresi

![Archive and Compress](img/archive.png)

## Outline

- [Teori](##Teori)
- [Praktikum](##Praktikum)
  - [Arsip](####Arsip)
  - [Kompresi](####Kompresi)
  - [Ekstrak](Ekstrak)
- [Challenge](##Challenge)

## Teori

**Arsip**

Arsip adalah proses menggabungkan banyak file ke dalam satu file tunggal.

Perintah arsip di linux menggunakan perintah `tar`.

Opsi arsip:

- c: create (membuat arsip).
- v: verbose (menampilkan proses).
- f: file (nama file).
- t: list (melihat isi file)

**Kompres**

Kompresi adalah proses mengecilkan ukuran file dari ukuran aslinya sehingga menghemat tempat.

**Program Arsip**

Program atau perintah yang digunakan untuk arsip: `tar`

**Program Kompresi**

Program atau perintah yang digunakan untuk kompresi:

- gzip
- bzip2
- zip

## Praktikum

#### Arsip

**1. Membuat file**

Membuat file index.html, style.css:

- Buat file index.html: `yes ini file html | head -n 1000000 > index.html`
- Buat file style.css: `yes ini file css | head -n 1000000 > style.css`
- Buat file script.js: `yes ini file javascript | head -n 1000000 > script.js`

**2. Arsip file**

Arsip semua file (index.html, style.css, script.js) dan beri nama `web.tar`:

- `tar -cvf web.tar index.html style.css`

**3. Melihat isi file arsip**

Melihat isi file arsip `web.tar`:

- `tar -tvf web.tar`

**4. Ekstrak file arsip**

Mengeksrak file arsip `web.tar`.

Hapus file index.html, style.css, script.js terlebih dahulu:

- `rm -rf index.html style.css`.

Ekstrak file arsip web.tar:

- `tar -xvf web.tar`.

#### Kompresi

**1. Arsip dan Kompres File dengan gzip (Terpisah)**

Perhatikan ukuran file `web.tar`.

Mengkompress file web.tar dengan perintah gzip:

- `gzip web.tar`

Perhatikan ukuran file `web.tar.gz`.

Melakukan dekompresi file `web.tar.gz`:

- `gzip -d web.tar.gz`

**2. Arsip dan Kompress File dengan gzip (Bersamaan)**

Melakukan arsip dan kompress dengan tar dan gzip secara bersamaan:

- `tar -czvf web.tar.gz index.html style.css script.js`

**3. Arsip dan Kompress dengan Zip**

Melakukan arsip dan kompress dengan zip:

- `zip web index.html style.css script.js`

Perhatikan hasilnya.

#### Ekstrak

**Ekstrak gzip**

Mengekstrak file `web.tar.gz`.

Hapus file index.html, style.css, script.js terlebih dahulu:

- `rm -rf index.html style.css`

Ekstrak file web.tar.gz:

- `tar -xzvf web.tar.gz`

**Ekstrak zip**

Mengekstrak file `web.zip`.

Hapus file index.html, style.css, script.js terlebih dahulu:

- `rm -rf index.html style.css`

Ekstrak file `web.zip`:

- `unzip web.zip`

Selesai.

## Challenge

**Ketentuan Challenge**:

- Challenge no 1, 3, dan 4 harus menggunakan Screenshot.
- Challenge dikumpulkan di Elen.

**Challenge**:

1. Jalankan perintah di bawah secara bersamaan:
   1. whoami.
   2. hostname.
   3. date.
2. Sebutkan dan jelaskan 3 jenis kompresi file yang ada di linux.
3. Lakukan kompresi dengan 3 jenis tersebut menggunakan terminal:
   1. Tuliskan perintah kompresi jenis 1.
   2. Tuliskan perintah kompresi jenis 2.
   3. Tuliskan perintah kompresi jenis 3.
4. Dari hasil 3 jenis kompresi sebutkan:
   1. Hasil jenis kompresi apa yang paling besar.
   2. Hasil jenis kompresi apa yang paling kecil.
5. Apa evaluasi praktikum keenam? apa masukan dan saran?


