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

===============================================================

-- OBJECT--  [LIHAT Folder belajar / (14)]

>> cara penulisan 

const person = {
  firstName: "Lentera",
  lastName: "Cahaya",
  age: 50,
  eyeColor: "blue"
};

>> cara menampilkan nya 
cara 1 :
  objectName.propertyName

cara 2 : 
  objectName["propertyName"]
----------

>> tentang this keyword
  -> this merujuk pada objek saat ini yang sedang di eksekusi 

>> -- OBJEK METHODE --
    diakses dengan cara :
      objectName.methodName()

===============================================================

---- Javascript Event --- [LIHAT Folder belajar / (15)]
  -> tindakan atau kejadian yang terjadi di dalam aplikasi web, seperti klik mouse, penekanan tombol keyboard, perubahan nilai dalam elemen HTML, atau proses pemuatan halaman. 

  terdiri atas :
    1. onchange
    2. onclick
    3. onmouseover
    4. onmouseout
    5. onkeydown
    6. onload

===============================================================
-- JS STRING --[LIHAT Folder belajar / (16)]

> lenght  -> menghitung jumlah elemen dalam sebuah array atau panjang dari sebuah string
  text.lenght; 


> string bisa mendefenisikan sebuah objek
  let y = new String("Joni");

> Cukup gunakan at()  untuk mengakses 2 karakter terakhir dari sebuah kata, sebelumnya memang bisa pakai myString.at(-2) ,atau sharAt(myString.lenght-2)

  let str = "Roger";
    console.log(str.at(-2));    //output : "e"


---  JS STRING METHOD --- [LIHAT Folder belajar / (17)]

  1. slice(start, end) -> Mengembalikan bagian dari string mulai dari start hingga akhir (end tidak termasuk). Jika start nya negatif atau kosong maka diambil karakter akhir string
  2. substring(start, end) -> mirip dengan slice(), tetapi tidak mendukung indeks negatif.
  3. substr(start, length) -> Mulai dari indeks start, ambil sejumlah karakter sebanyak length dari string. 
  4. toLowerCase() : konversi ke huruf kecil
  5. toUpperCase() : konversi ke huruf besar
  6. concat() : Untuk menggabungkan dua atau lebih string
  7. trim() : menghapus spasi kosong diawal dan akhir sebuah string
  8. trimStart() : mengapus spasi hanya yang di depan
  9. trimEnd() : mengapus spasi hanya yang di belakang
  10. padStart() :mengisi string dengan karakter tertentu hingga mencapai panjang yang ditentukan di depan
  11. padEnd() :mengisi string dengan karakter tertentu hingga mencapai panjang yang ditentukan di belakang
  12. repeat() : membuat atau mengembalikan string baru yang berisi pengulangan string asli sebanyak yang ditentukan 
  13. replace() : digunakan untuk mengganti kecocokan pertama dari sebuah pola dengan string pengganti tertentu. Namun, untuk mengganti semua kecocokan dalam string, Anda perlu menggunakan ekspresi reguler dengan flag /g (pencocokan global)
  14. /g : Ini akan menyebabkan pencarian semua kecocokan dalam string, bukan hanya kecocokan pertama.
  15. replaceAll() : memungkinkan penggantian semua kecocokan dari sebuah pola dalam sebuah string. tanpa harus menggunakan flag '/g', TAPI ini hanya tersedia mulai dariECMAScript 2021 (ES12) dan seterusnya
        pola : string.replaceAll(pola, pengganti)

<!-- convert string ke Array -->
  16. split() : membagi string menjadi Array , berguna ketika memisahkan string berdasarkan spasi,koma
    > text.split(" , ")
    > text.split(" ")
    > text.split("|")

-----------------------------------------------------
>> STRING SEARCH METHODS

 1. indexOf()  -> mencari indeks dari awal string dari suatu substring yang diberikan, jika substring tidak ditemukan metode ini mengembalikan -1.
 2. lastIndexOf()  -> mencari substring dari akhir string ke awal
 3. search() -> mencari teks yang coock dengan ekspresi regular dalam string , jika tidak ditemukan mengembalikan nilai -1
 4. match() -> mencocokan string dengan ekspresi regular tertentu, mengembalikan array dari semua hasil pencocokan atau null jika tidak ada pencocokan 
 5. matchAll() -> mengembalikan iterator dari semua hasil pencocokan dalam string termasuk informasi tambahan 
 6. includes()  -> untuk mengeck apakah string mengandung substring tertentu , mengembalikan nilai boolean
 7. startWith()  -> memeriksa apakah string dimulai dengan substtrinmg tertentu, mengembalikan nilai boolean
 8. endsWith() -> memeriksa apakah string diakhiri dengan substring tertentu , mengembalikan nilai boolean


--------------------------------------------------------
>> JS Template String
 1. back-tics syntax  (``) : di keyboard kiri atas dibawah esc
    ->> Aman digunakan walaupun ada petik 2 ("") atau petik 1 ( '') didalamnya
 2. interpolation  : 
      ${...}

----------------------------------------------------------
>> JS Number
  1. Number.isInteger()  : memeriksa apakah suatu bilangan bulat atau bukan , mengembalikan nilai true atau false
  2. Number.isSafeInteger() : memeriksa apakah bilangan bulat yang aman atau tidak
  3. Number.parseFloat() : mengkonversi sebuah string menjadi float atau desimal
4. Number.parseInt()  : mengonversi sebuah string menjadi tipe data integer (bilangan bulat).
  --------------

  mehod number 
  ----------- 
  1. toString() -> mengonversi sebuah angka menjadi string.
  2. toEksponential()  -> mengonversi angka menjadi notasi eksponensial.
  3. toFixed()  -> mengonversi angka menjadi string dengan jumlah digit desimal tertentu.
  4. toPrecision()  -> mengonversi angka menjadi string dengan panjang tertentu, termasuk digit sebelum dan sesudah titik desimal.
  5. valueOf()  -> mengembalikan nilai dasar dari objek Number, yaitu angka itu sendiri.

    > convert variabel ke number
    1. Number()  -> mengubah variabel atau argumenya ke number
    2. parseFloat()  -> mengkonversi argumen menjadi float / decimal
    3. parseInt()  -> konversi argumen menjadi tipe data integer atau bilangan bulat

--------------------------------------------------------------


