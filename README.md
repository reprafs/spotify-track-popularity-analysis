# Spotify Track Popularity Analysis

Data cleaning and visualization of Spotify tracks using Python in Google Colab.

## Project Overview

This project explores a Spotify dataset with 8,700+ tracks. Each row has information about the track, the artist, and the album. The goal is to find out what is related to a track's popularity, using simple charts.

## Problem

Why are some songs more popular than others? Is it the artist, the genre, the song length, or something else? This project looks for patterns that can help answer these questions.

## Dataset

- **Source:** https://www.kaggle.com/code/marawanmohsen1/spotify?select=track_data_final.csv
- **Size:** 8,700+ tracks
- **Main columns:** `track_name`, `track_popularity`, `track_duration_ms`, `explicit`, `artist_name`, `artist_popularity`, `artist_followers`, `artist_genres`, `album_release_date`, `album_total_tracks`

> Note: `track_popularity` is a score from 0 to 100 made by Spotify. It is not the exact number of streams.

## Tools

- Python
- Pandas
- Plotly
- Seaborn and Matplotlib
- Google Colab

## Analysis

## 1. Which variables are most related to track popularity, and are they related to each other?

![Correlation Heatmap](images/foto1.png)

Meskipun korelasi  popularitas artis sangat erat kaitannya dengan jumlah *followers*-nya (0.94), popularitas sebuah lagu ternyata sama sekali tidak ditentukan oleh durasi, posisi urutan lagu, maupun ukuran album, di mana nama besar artis (0.46) serta konten eksplisit (0.20) hanya memberikan dorongan moderat tanpa menjamin seluruh karya mereka otomatis menjadi hits.

## 2. How is track popularity spread across the dataset? Are most tracks low, medium, or high?

![Popularity Distribution](images/foto2.png)

Dari grafik kelihatan kalau sebaran popularitas lagunya agak timpang karena numpuk banget di angka 0 (sampai 300 lagu lebih), yang kemungkinan besar itu lagu-lagu baru atau yang emang sepi pendengar. Tapi buat lagu-lagu yang lain, sebarannya lumayan nyebar di kisaran nilai 40 sampai 80. Makanya nilai tengah (median) ada di 56.0, sedikit lebih tinggi dari rata-rata (mean) yang di angka 51.5, karena rata-ratanya ketarik turun sama lagu-lagu ber-skor nol tadi.

## 3. Which genre has the highest average popularity, and is the biggest genre also the most popular?

![Genre Popularity](images/foto3.png)

Dari grafik rata-rata popularitas genre, kelompok genre yang berbau latin (reggaeton, trap latino, urbano latino, latin), k-pop, dan rap menduduki posisi teratas dengan skor popularitas rata-rata paling tinggi. Di sisi lain, meskipun genre pop dan soundtrack punya jumlah lagu yang sangat banyak (terlihat dari warna batang yang paling gelap), rata-rata popularitas mereka justru berada di bawah genre latin atau rap.

## 4. Do popular artists always make popular tracks, and do artists with many followers show a different pattern?

![Artist vs Track Popularity](images/foto4.png)

Dari grafik rata-rata popularitas genre, kelompok genre yang berbau latin (reggaeton, trap latino, urbano latino, latin), k-pop, dan rap menduduki posisi teratas dengan skor popularitas rata-rata paling tinggi. Di sisi lain, meskipun genre pop dan soundtrack punya jumlah lagu yang sangat banyak (terlihat dari warna batang yang paling gelap), rata-rata popularitas mereka justru berada di bawah genre latin atau rap.

## 5. How do the number of releases and average popularity change over the years?

![Popularity Trend](images/foto5.png)

Meskipun jumlah rilis lagu melonjak drastis hingga di atas 300 lagu per tahun dalam satu dekade terakhir, rata-rata popularitas lagu (di kisaran 45–55) dan artis (di kisaran 65–75) justru cenderung stagnan dan tidak ikut naik.

## Conclusion


- *Artist fame helps, but it is not a guarantee.* Artist popularity has a moderate link with track popularity (0.46). Popular artists can still have tracks that few people listen to.
- *Song features matter little.* Duration, track number, and album size have almost no relation to popularity. Explicit songs get only a small boost (0.20).
- *Genre makes a difference.* Latin genres, K-pop, and rap have the highest average popularity. Pop and soundtrack have the most songs, but their average popularity is lower.
- *More songs does not mean more popular.* Releases grew a lot in the last decade, but average popularity stayed flat.
