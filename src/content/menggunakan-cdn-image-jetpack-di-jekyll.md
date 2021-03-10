---
author:
- Wildan Fauzy
title: Menggunakan Cdn Image Jetpack di Jekyll
tags:
- jekyll
image: img/20-17-46-jetpack_ryxux4.jpg
date: 2020-11-22T17:00:00Z
draft: false
excerpt: Cukup unik memang cdn gambar dari jetpack

---
Satu hal yang menjadi kendala ketika ngeblog menggunankan ssg jekyll adalah hosting gambar, iya karena jika menyimpan gambar pada repo github dengan pengaturan default maka gambar akan memuat dengan ukuran aslinya.

Hasilnya loading lama gara-gara ngeload gambar yang ukuranya tidak terkompress, memang banyak layanan seperti netlify dengan large medianya, atau cloudfront, gampangnya yang sudah integrasi dengan forestry adalah cloudinary.

Namun cukup mumet kalau harus mengotak-atik beberapa baris kode di tema jekyll, setelah berpikir lumayan singkat, terpikirnya menggunakan layanan cdn gambar dari jetpack yaitu photon.

Cukup unik memang cdn gambar dari jetpack, tanpa menggunakan plugin pun kita bisa mengunakan proxy gambar, hanya memasukan alamat gambar setelah domain [https://i0.wp.com](https://i0.wp.com "https://i0.wp.com") maka gambar langsung ke proxy jetpack.

Pada awalnya manual pada setiap postingan mengganti url dengan url cdn image jetpack, akhirnya tetap harus mengedit beberpa baris kode.

Tambahkan alamat i0.wp.com terus alamat blog tanpa http lalu path gambar di repo github, lalu resize sesuai kebutuhan dengan parameter ?resize=300%2C200&ssl=1 maka berubah seperti magic.