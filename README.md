# project_w3school


- Penulisan Javascript  : [LIHAT folder belajar (6)]
    1. internal Javascript : di head atau di body
    2. eksternal Javascript : file terpisah satu direktori / folder, file di dalam folder berbeda, pakai URL

===============================================================

Javascript Output : [LIHAT folder Belajar (7)]
  - innerHTML -> DOM yang memungkinkan untuk mengambil atau mengubah
             HTML di dalam sebuah elemen
  - document.write()  -> digunakan untuk menulis teks atau HTML langsung ke dokumen saat ini.
  - alert() -> digunakan untuk menampilkan dialog peringatan ke pengguna dengan pesan yang disediakan.
  - console.log() -> digunakan untuk menampilkan output saat mengembangkan dan debugging kode JavaScript. 
  - Prompt() -> digunakan untuk menampilkan dialog yang meminta input dari pengguna.
  - window.print()  -> Untuk mencetak halaman, dengan print.

===============================================================

- Var 
   skop : fungsi global yang jika dideklarasikan di luar fungsi
   Pengubahan Nilai : bisa diubah setelah deklarasi

- let
  skop : hanya diakses di dalam blok dimana ia dideklarasikan , termasuk di dalam struktur if, for, dan while
  Pengubahan Nilai : bisa diubah setelah deklarasi

-Const 
  skop : sama seperti let
  Pengubahan Nilai : tidak dapat diubah nilainya setelah deklarasi, JIKA digunakan dengan objek atau array, properti objek atau elemen array masih bisa diubah.

  akan menghasilkan ReferenceError kalau menggunakan const sebelum di deklarasikan.
    ex :
      alert (carName);
      const carName = "Volvo";
===============================================================

    // How to create variables:
    var x;
    let y;

    // How to use variables:
    x = 5;
    y = 6;
    let z = x + y;

===============================================================
------ LET  vs VAR ------

  {
    let x = 2;
  }

  //x tidak bisa digunakan disini, kalau var bisa

........................................

  let x = "John Doe";
  let x = 0 ;          //Kayak gini ga bisa di let kalau var bisa

........................................

  var x = 2;   //allowed
  let x = 3;   // NOT allowed

  {
    let x = 2;  //allowed
    let x = 3;  //NOT allowed
  }

  {
    let x = 2;   // allowed
    var x = 3;   //NOT allowed
  }
........................................................
........................................................

--------CONST--------
<!-- Correct -->
  const PI = 3.14159265359;   

<!-- incorect -->
  const PI;
  PI = 3.14159265359;

<!-- ===== const bisa diubah di array dan objek ===== -->
>> di array
-----------

  const cars = ["Toyota", "APV", "Ferari"];

  <!-- ubah elemen nya -->
  cars[0] = "Suzuki";

  <!-- Tambah elemen nya -->
  cars.push("Angel");

>> di objek
-----------

  const cars = { type: "Fiat", model:"500", color:"black"};

  cars.color = "white";

  cars.owner = "Johnson";

===============================================================

Javascript Assignment Operators [LIHAT di folder belajar [10]]
 ex :
  let x = 10;
    x += 5;      //otput : 15

===============================================================
Logical Operators [LIHAT Folder belajar / (11)]

&& Logical AND
|| Logical OR
!  Logical NOT

===============================================================
Type Operators
  1. typeof -> Mengecek tipe dasar seperti string, number, boolean, undefined, function, dan object. Mengembalikan nilai dalam bentuk string.  TIDAK BISA membedakan antara array dan objek

  2. instanceof -> Menghasilkan hasil BOOLEAN, Mengecek tipe objek dan hubungan pewarisan di Javascript



Mengambil bagian kata dari kalimat [example]
--------------------------------------------
Use the slice method to return the word "bananas". 

let txt = "I can eat bananas all day";
let x = txt.slice(10, 17);
          --------

===============================================================

Mengganti isi dari arrays :
----------------------------

Change the first item of cars to "Ford".

const cars = ["Volvo", "Jeep", "Mercedes"];
cars[0] = "Ford";
-------

===============================================================

- pop : Menghapus elemen terakhir array
    ex :
      const fruits = ["Banana", "Orange", "Apple"];
      fruits.pop();
            -------

- push : Menambahkan elemen kedalam array
    ex :
      const fruits = ["Banana", "Orange", "Apple"];
      fruits.push("Kiwi");
            --------------

-splice : Memanipulasi Array (Menambah, Menghapus, Mengganti)
    ex :
     >> menghapus ::
        const fruits = ["Banana", "Orange", "Apple", "Kiwi"];
        fruits.splice(1,2);
              -------------

-sort : Mengurutkan elemen - elemen dalam array
  ex :
  >>urutkan secara alfabet
    const fruits = ["banana", "apple", "mango", "orange"];
    fruits.sort();
    console.log(fruits);        // Output: ["apple", "banana", "mango", "orange"]

  >> urutkan angka secara numerik
    const numbers = [40, 1, 5, 200];
    numbers.sort((a, b) => a - b);
    console.log(numbers);         // Output: [1, 5, 40, 200]

  >> urutkan angka secara menurun
    const numbers = [40, 1, 5, 200];
    numbers.sort((a, b) => b - a);
    console.log(numbers);         // Output: [200, 40, 5, 1]















