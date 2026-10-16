# Laporan Tugas Personal Blockchain Level 1–5

- **Nama:** JUMRI RAMADHAN
- **NIM (4 digit terakhir):** 2157
- **Dibuat:** 2026-10-16 15:03  (waktu proses 4.7 detik)
- **Kode verifikasi:** `3C9C4FBC243E`

> Bagian hasil dibuat otomatis. Jangan diubah: dosen menghitung ulang semua angka dari data Anda.
> Isi bagian **Analisis** dengan kata-kata Anda sendiri.

## Level 1 — Hash data pribadi

| Hasil | Nilai |
|---|---|
| SHA-256 nama | `c2ddc3ac51b43909930a72af29ce6e4686fa68ebb15cf8743827727a979323bc` |
| hash_dict profil | `4b6ba23b4dc2e7a06e1afc79b6714f02bd409e7787dc9c481f63931ad4730301` |
| hash_dict profil (urutan key dibalik) | `4b6ba23b4dc2e7a06e1afc79b6714f02bd409e7787dc9c481f63931ad4730301` |
| Bit berubah: tanggal lahir vs tanggal lahir + 1 hari | 45.31% |
| ID mahasiswa (Modifikasi 1) | `ea127fac` |

## Level 2 — Blockchain personal

- Proof genesis: **2157** (dari NIM)
- Proof blok 2, 3, 4: **49896, 828, 17404**
- Pemilik setiap blok: `ea127fac`
- Rantai valid: True

## Level 3 — Pemalsuan data pribadi

- Posisi yang dipalsukan: **2**
- Data asli: `JUMRI RAMADHAN berasal dari JAWA`
- Data palsu: `JUMRI RAMADHAN berasal dari JAWA (DIPALSUKAN)`
- Valid sebelum dipalsukan: True
- Tautan putus di indeks: **3**
- Valid setelah dipalsukan: **False**
- Valid setelah disambung ulang: **True**

## Level 4 — Transaksi dari data pribadi

| Blok | Pengirim | Penerima | Jumlah |
|---|---|---|---|
| 2 | JUMRI RAMADHAN | TEMAN_A | 7 |
| 2 | TEMAN_A | JUMRI RAMADHAN | 11 |
| 3 | JUMRI RAMADHAN | DOSEN | 8 |

- Ringkasan saldo (Modifikasi 4): masuk **11**, keluar **15**, bersih **-4**
- Kirim ke diri sendiri ditolak: True
- Amount 0 ditolak: True

## Level 5 — Proof of Work dengan nonce (deterministik)

| Blok | Nonce | Hash |
|---|---|---|
| 0 | 71250 | `00007c8878d1b7268bec0e95…` |
| 1 | 2826 | `00000f4919abcb567b441d66…` |
| 2 | 53151 | `00006ba8131cc92771eb2394…` |
| 3 | 10351 | `0000ea96f40c1d324c986aff…` |

- Valid: True → setelah blok 1 dipalsukan: **False**
- Percobaan hash untuk menambang ulang blok 1–3: **301.528**
- Valid setelah ditambang ulang: True

## Analisis (isi dengan kata-kata Anda sendiri)

1. **Level 1.** Bandingkan SHA-256 nama Anda dengan milik seorang teman. Apakah ada pola yang mirip? Jelaskan juga mengapa dua hash profil Anda sama, dan mengapa hanya menambah 1 hari pada tanggal lahir mengubah 45.31% bit.

   _Jawaban:_

2. **Level 2.** Kode Anda dan teman sama persis, tetapi proof Anda (49896, 828, 17404) berbeda. Jelaskan penyebabnya.

   _Jawaban:_

3. **Level 3.** Anda memalsukan posisi 2 dan tautan putus terdeteksi di indeks 3, sedangkan valid setelah dipalsukan = False. Jelaskan hasil ini, lalu bandingkan dengan teman yang posisi pemalsuannya berbeda.

   _Jawaban:_

4. **Level 4.** Jelaskan dari mana angka masuk 11, keluar 15, dan bersih -4 berasal. Mengapa transaksi ke diri sendiri perlu ditolak?

   _Jawaban:_

5. **Level 5.** Penyerang butuh 301.528 percobaan hash untuk memalsukan rantai Anda. Mengapa nonce Anda selalu sama setiap kali program dijalankan, padahal di demo Level 5 asli nonce berubah-ubah?

   _Jawaban:_

6. **Etika data.** Anda baru saja menyimpan nama dan tanggal lahir di dalam blockchain. Jika ini blockchain publik, apa risikonya? Kaitkan dengan sifat immutability dan UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi, terutama hak untuk menghapus data.

   _Jawaban:_

---

## Data verifikasi (JANGAN DIUBAH)

<!-- DATA-VERIFIKASI -->
```json
{
  "profil": {
    "nama": "JUMRI RAMADHAN",
    "nim4": "2157",
    "tanggal_lahir": "2003-11-07",
    "kota_asal": "JAWA",
    "hobi": "MEMANCING"
  },
  "level1": {
    "hash_nama": "c2ddc3ac51b43909930a72af29ce6e4686fa68ebb15cf8743827727a979323bc",
    "hash_profil": "4b6ba23b4dc2e7a06e1afc79b6714f02bd409e7787dc9c481f63931ad4730301",
    "hash_profil_urutan_terbalik": "4b6ba23b4dc2e7a06e1afc79b6714f02bd409e7787dc9c481f63931ad4730301",
    "avalanche_tanggal_persen": 45.31,
    "id_mahasiswa": "ea127fac"
  },
  "level2": {
    "proof_genesis": 2157,
    "proof_blok": [
      49896,
      828,
      17404
    ],
    "pemilik_semua_blok": [
      "ea127fac"
    ],
    "valid": true
  },
  "level3": {
    "posisi_dipalsukan": 2,
    "data_asli": "JUMRI RAMADHAN berasal dari JAWA",
    "data_palsu": "JUMRI RAMADHAN berasal dari JAWA (DIPALSUKAN)",
    "valid_asli": true,
    "tautan_putus_di": 3,
    "valid_setelah_dipalsukan": false,
    "valid_setelah_disambung_ulang": true
  },
  "level4": {
    "riwayat": [
      [
        2,
        {
          "sender": "JUMRI RAMADHAN",
          "recipient": "TEMAN_A",
          "amount": 7
        }
      ],
      [
        2,
        {
          "sender": "TEMAN_A",
          "recipient": "JUMRI RAMADHAN",
          "amount": 11
        }
      ],
      [
        3,
        {
          "sender": "JUMRI RAMADHAN",
          "recipient": "DOSEN",
          "amount": 8
        }
      ]
    ],
    "ringkasan_saldo": {
      "masuk": 11,
      "keluar": 15,
      "bersih": -4
    },
    "kirim_ke_diri_sendiri_ditolak": true,
    "amount_nol_ditolak": true,
    "jumlah_blok": 3
  },
  "level5": {
    "nonce": [
      71250,
      2826,
      53151,
      10351
    ],
    "hash": [
      "00007c8878d1b7268bec0e95107336b42e12b908443e2bb8f525b34d0f3930ef",
      "00000f4919abcb567b441d66430348dcb48167296d2ef24bb8ad7a2d13637363",
      "00006ba8131cc92771eb2394026863bc0b0c2c6544718d0cd83e9ea5a6b56274",
      "0000ea96f40c1d324c986aff96ad623532ef43a3311eff1be2d0cb2afe9eeec1"
    ],
    "valid": true,
    "valid_setelah_dipalsukan": false,
    "percobaan_tambang_ulang": 301528,
    "valid_setelah_tambang_ulang": true
  },
  "kode_verifikasi": "3C9C4FBC243E"
}
```
