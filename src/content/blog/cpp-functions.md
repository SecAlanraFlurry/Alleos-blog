---
title: 'Fungsi di C++'
description: 'Pelajari tentang deklarasi fungsi, definisi, parameter, tipe pengembalian, dan praktik terbaik di C++'
pubDate: 'Dec 08 2024'
heroImage: 'https://cdn.dribbble.com/userupload/17928988/file/original-7a7bf1d035ae372c12c03b2115a19649.png?resize=752x&vertical=center'
---

Fungsi adalah blok kode yang dapat digunakan kembali untuk melakukan tugas tertentu. Fungsi membantu mengorganisir kode, meningkatkan penggunaan ulang, dan membuat program lebih mudah dikelola.

## Deklarasi dan Definisi Fungsi

Fungsi memiliki dua bagian: deklarasi (prototipe) dan definisi:

```cpp
// Deklarasi fungsi
int hitungJumlah(int a, int b);

// Definisi fungsi
int hitungJumlah(int a, int b) {
    return a + b;
}
```

## Parameter Fungsi

Fungsi dapat menerima berbagai jenis parameter:

### 1. Pass by Value
```cpp
void tambahAngka(int x) {
    x++;  // Nilai asli tidak berubah
}
```

### 2. Pass by Reference
```cpp
void tambahAngka(int& x) {
    x++;  // Nilai asli dimodifikasi
}
```

### 3. Pass by Pointer
```cpp
void tambahAngka(int* x) {
    (*x)++;  // Nilai asli dimodifikasi
}
```

## Tipe Pengembalian

Fungsi dapat mengembalikan berbagai jenis nilai:

```cpp
// Mengembalikan void (tidak ada nilai)
void cetakPesan() {
    cout << "Halo, Dunia!" << endl;
}

// Mengembalikan nilai tunggal
int hitungKuadrat(int x) {
    return x * x;
}

// Mengembalikan beberapa nilai menggunakan struktur
struct Hasil {
    int jumlah;
    int produk;
};

Hasil hitung(int a, int b) {
    Hasil hasil;
    hasil.jumlah = a + b;
    hasil.produk = a * b;
    return hasil;
}
```

## Parameter Default

Fungsi dapat memiliki nilai parameter default:

```cpp
void cetakPesan(string pesan = "Halo") {
    cout << pesan << endl;
}

// Dapat dipanggil sebagai:
cetakPesan();          // Mencetak "Halo"
cetakPesan("Hi");      // Mencetak "Hi"
```

## Function Overloading

C++ memungkinkan beberapa fungsi dengan nama yang sama tetapi parameter berbeda:

```cpp
int tambah(int a, int b) {
    return a + b;
}

double tambah(double a, double b) {
    return a + b;
}

string tambah(string a, string b) {
    return a + b;
}
```

## Fungsi Inline

Fungsi kecil dapat dibuat inline untuk performa yang lebih baik:

```cpp
inline int dapatkanMaksimum(int a, int b) {
    return (a > b) ? a : b;
}
```

## Praktik Terbaik

1. Gunakan nama fungsi yang bermakna yang menggambarkan tujuannya
2. Buat fungsi kecil dan fokus pada satu tugas
3. Dokumentasikan parameter fungsi dan nilai pengembalian
4. Gunakan parameter const ketika nilai tidak boleh dimodifikasi
5. Pertimbangkan menggunakan parameter referensi untuk objek besar
6. Selalu deklarasikan prototipe fungsi di file header
7. Implementasikan penanganan kesalahan untuk fungsi yang kuat

Ingat bahwa fungsi yang dirancang dengan baik membuat kode kamu lebih mudah dibaca, dikelola, dan digunakan kembali.