# Praktikum4_SQL


## **Query Filtering**

Query filtering mengacu pada proses memfilter atau membatasi data yang diambil dari database berdasarkan kriteria tertentu. Dalam konteks basis data, query filtering melibatkan penggunaan klausa "WHERE" dalam perintah SQL untuk mengatur kondisi atau kriteria yang harus dipenuhi oleh data yang ingin diambil.

Dengan menggunakan query filtering, Anda dapat menentukan kondisi seperti kesamaan, ketidaksamaan, rentang nilai, atau kombinasi kondisi lainnya untuk memilih subset data yang relevan dari tabel. Ini membantu Anda memfokuskan pada data yang spesifik atau memenuhi persyaratan tertentu.

### **Tugas Praktikum**

**TABEL pegawai**   

  ![table_pegawai](image/TABLE%20pegawai.png)
  1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000!
  - Perintah
    ```sql
    SELECT * FROM pegawai WHERE gaji <> 2000000 AND gaji <> 1250000;
    ```
  - Output
    ![img](image/SELECT%20FROM%20pegawai%20WHERE%20gaji%202000000%20AND%20gaji%201250000.png)
  2. Tampilkan pegawai yang tunjangannya NUL!
  - Perintah
    ```sql
    SELECT * FROM pegawai WHERE tunjangan IS NULL;
    ```
  - Output
    ![img](image/SELECT%20FROM%20pegawai%20WHERE%20tunjangan%20IS%20NULL.png)
  3. Tampilkan pegawai yang tunjangannya tidak NULL!
  - Perintah
    ```sql
    SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;
    ```
  - Output
    ![imt](image/SELECT%20FROM%20pegawai%20WHERE%20tunjangan%20IS%20NOT%20NULL.png)
  4. Tampilkan/hitung jumlah baris/record tabel pegawai!
  - Perintah
    ```sql
    SELECT COUNT(*) AS jumlah_baris FROM pegawai;
    ```
  - Output
    ![img](image/SELECT%20COUNT%20AS%20jumlah_baris.png)
  5. Tampilkan/hitung jumlah total gaji di tabel pegawai!
  - Perintah
    ```sql
    SELECT SUM(gaji) AS total_gaji FROM pegawai;
    ```
  - Output
    ![img](image/SELECT%20SUM%20AS%20total_gaji.png)
  6. Tampilkan/hitung jumlah rata-rata gaji pegawai!
  - Perintah
    ```sql
    SELECT AVG(gaji) AS rata_gaji FROM pegawai
    ```
  - Output
    ![img](image/SELECT%20AVG(gaji)%20AS%20rata_gaji.png)
  7. Tampilkan gaji terkecil!
  - Perintah
    ```sql
    SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;
    ```
  - Output
    ![img](image/SELECT%20MIN(gaji)%20AS%20gaji_terkecil.png)
  8. Tampilkan gaji terbesar!
  - Perintah
    ```sql
    SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;
    ```
  - Output
    ![img](image/SELECT%20MAX(gaji)%20AS%20gaji_terbesar.png)

```
```
**TABEL hewan**     

  ![tabel_hewan](image/TABLE%20hewan.png)
  1. Tampilkan jumlah hewan yang dimiliki setiap owner!
  - Perintah
    ```sql
    SELECT owner, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY owner;
    ```
  - Output
    ![img](image/SELECT%20owner%2C%20COUNT%20AS%20jumlah_hewan%20FROM%20hewan%20GROUP%20BY%20owner%3B.png)
  2. Tampilkan jumlah hewan berdasarkan spesies!
  - Perintah
    ```sql
    SELECT species, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species;
    ```
  - Output
    ![img](image/SELECT%20species%2C%20COUNT%20AS%20jumlah_hewan%20GROUP%20BY%20species%3B.png)
  3. Tampilkan jumlah hewan berdasarkan jenis kelamin!
  - Perintah
    ```sql
    SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY sex;
    ```
  - Output
    ![img](image/SELECT%20sex%2C%20COUNT%20AS%20jumlah_hewan%20GROUP%20BY%20sex.png)
  4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin!
  - Perintah
    ```sql
    SELECT species,sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species,sex;
    ```
  - Output
    ![img](image/SELECT%20species%2Csex.png)
  5. Tampilkan jumlah hewan berdasarkan spesies (cat dan dog saja) dan jenis kelamin!
  - Perintah
    ```sql
    SELECT species,sex, COUNT(*) AS jumlah_hewan FROM hewan
    WHERE species IN('Cat','Dog')
    GROUP BY species,sex;
    ```
  - Output
    ![img](image/SELECT%20species%2Csex%20WHERE%20species%20IN('Cat'%2C'Dog').png)
  6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja!
  - Perintah
    ```sql
    SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan
    WHERE sex IN('f','m')
    GROUP BY sex;
    ```
  - Output
    ![img](image/SELECT%20sex%2C%20COUNT%20AS%20jumlah_hewan%20WHERE%20IN.png)

### **Kesimpulan**

Query filtering adalah proses menyaring atau memfilter data dari basis data berdasarkan kriteria tertentu menggunakan perintah query dalam bahasa SQL. Tujuan utama dari query filtering adalah membatasi atau mengambil subset data yang sesuai dengan kondisi yang ditentukan.  
 Dengan menggunakan query filtering, Anda dapat menentukan berbagai jenis kondisi seperti kesamaan (equal), ketidaksamaan (not equal), rentang nilai (range), kondisi logis (AND, OR), atau kombinasi kondisi lainnya. Dengan mengatur kondisi yang sesuai, Anda dapat mengambil hanya data yang relevan atau yang memenuhi persyaratan tertentu.

### **Evaluasi dan Pertanyaan**

- [Tulis semua perintah-perintah SQL percobaan di atas besarta outputnya!](#tugas-praktikum)
- [Beri kesimpulan anda!](#kesimpulan)