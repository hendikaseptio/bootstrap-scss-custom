# BOOTSTRAP 5.3.X SCSS CUSTOM
Modifikasi semua komponen pada bootstrap 5.3.x dengan custom scss, terdapat hasil tampilan yang bervariasi seperti berikut : 
- Custom **Rounded** dimana ukuran `border-radius` bawaan ditambah sehingga menghasilkan sudut yang lebih melengkung. 
- Custom **Color only** merupakan modifikasi yang hanya menggubah warna dasarnya saja dan tetap mempertahankan style bawaan dari bootstrap. 
- Custom **Flat** merupakan modifikasi yang menghilangkan `border-radius` pada semua pada elemen sehingga berbentuk kotak tanpa ada sudut yang tumpul, dan memodifikasi warna tema secara keseluruhan. 

## Cara instan mendapatkan hasil custom bootstrap
Masukkan perintah berikut pada terminal/console anda :
```bash
git clone https://github.com/hendikaseptio/bootstrap-scss-custom
```
## cara menggunakan 
simpan file bootstrap yang sudah di custom ke folder assets anda dan tambahkan kode berikut pada halman website anda :
- Color Only
    ```html
    <link rel="stylesheet" href="bootstrap-color-only.css">
    ```
- Rounded Version
    ```html
    <link rel="stylesheet" href="bootstrap-rounded.css">
    ```
- Flat Version
    ```html
    <link rel="stylesheet" href="bootstrap-flat.css">
    ```

## Cara mengubah warna tema
buka file `bootstrap-custom.scss` pada folder `sass` dan ubah warna sesuai dengan yang anda inginkan
```scss
@import "mixins/banner";
@include bsBanner("");

// atur warna disini
$primary: #e0a370 !default;
$primary: #e0a370 !default;
$secondary: grey !default;
$success: green !default;
$info: cyan !default;
$warning: yellow !default;
$danger: red !default;
$light: #eee !default;
$dark: #444 !default;
```
jika ada warna yang tidak ingin diubah maka hapus atau berikan komentar pada variabel warna diatas.
setelah proses perubahan sudah selesai, anda harus melakukan build agar perubahan diperbarui masukkan kode berikut
```bash
$ sass scss/bootstrap-custom.scss bootstrap-color-only.css
```
jika ingin mengupdate file css dari semua perubahan pada file scss secara otomatis gunakan perintah berikut 
```bash
$ sass -w scss/bootstrap-custom.scss bootstrap-color-only.css
```

## Demo
[preview hasil custom](https://hendikaseptio.github.io/bootstrap-scss-custom/)