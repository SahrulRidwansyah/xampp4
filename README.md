# xampp4
```
Nama  : Sahrul Ridwansyah
Kelas : TI.22.A2
Nim   : 312210063
```
tugas praktikum pegawai

1#
tabel pegawai

pertama tama kita buat dulu tabelnya seperti ini
```
Key column 'id_pegawai' doesn't exist in table
MariaDB [latihan4]> CREATE TABLE pegawaiper (
    ->   id_pegawai int(20) NOT NULL AUTO_INCREMENT,
    ->   nama_depan varchar(25) NOT NULL,
    ->   nama_belakang varchar(25) NOT NULL,
    ->   email varchar(25) NOT NULL,
    ->   telpon int(20) NOT NULL,
    ->   tgl_kontrak int(20) NOT NULL,
    ->   id_job int(20) NOT NULL,
    ->   gaji int(20) NOT NULL,
    ->   tunjangan int(20) NOT NULL,
    ->   PRIMARY KEY (id_pegawai)
    -> );
```
lalu lanjut 'desc pegawaiper;'

![image](https://github.com/sahrul180304/xampp4/assets/115526901/9d9d0759-7dea-4d6f-b2f6-622622722432)



selanjutnya kita ketik
```
INSERT INTO pegawaiper (nama_depan, nama_belakang, email, telpon, tgl_kontrak, id_job, gaji, tunjangan)
    -> VALUES
    ->   ('ferry', 'gustiawan', 'ferry@yahoo.com', 07117059004, '2005-09-01', 'L0001', 2000000, 500000),
    ->   ('aris', 'ganiardi', 'aris@yahoo.com', 081312345678, '2006-09-01', 'L0002', 2000000, 200000),
    ->   ('faiz', 'ahnad', 'faiz@gmail.com', 081367384322, '2006-10-01', 'L0003', 1500000, NULL),
    ->   ('emna', 'bunton', 'enna@gmail.com', 081363484342, '2006-10-01', 'L0004', 1500000, 9),
    ->   ('mike', 'scoff', 'mike@plasa.com', 08163454555, '2007-09-01', 'L0005', 1250000, 9),
    ->   ('licoln', 'burrows', 'linc@yahoo.com', 08527388432, '2008-09-01', 'L0006', 1750000, NULL);
```

lanjut enter dan 'select *from pegawaiper;'

![image](https://github.com/sahrul180304/xampp4/assets/115526901/7c6cbba8-8f7c-4336-9f73-41355a3e2e61)

 lanjut ke tugas pratikum 
 
1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !
```
 'SELECT * FROM pegawaiper WHERE gaji NOT IN (2000000, 1250000);'
```

![image](https://github.com/sahrul180304/xampp4/assets/115526901/0103dcfd-47c0-4a93-b213-5c1f62ddcd0d)


2. Tampilkan pegawai yang tunjangannya NULL!
```
'SELECT * FROM pegawaiper WHERE tunjangan IS NULL;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/a9a5ea02-013c-4731-b718-2f75f29c462e)


3. Tampilkan pegawai yang tunjangannya tidak NULL!
```
'SELECT * FROM pegawaiper WHERE tunjangan IS NOT NULL;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/8d5f416d-3978-4447-9361-d13287f01249)


4. Tampilkan/hitung jumlah baris/record tabel pegawai!
```
'SELECT COUNT(*) FROM pegawaiper;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/c3ce7774-68e6-448d-a50c-f354a3863818)


5. Tampilkan/hitung jumlah total gaji di tabel pegawai!
```
'SELECT SUM(gaji) FROM pegawaiper;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/3e0561a7-1c93-4b9c-8cd2-17932ca3791e)


6. Tampilkan/hitung rata-rata gaji pegawai!
```
'SELECT AVG(gaji) FROM pegawaiper;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/b29eefcf-5184-486e-900e-ad6d01b36049)


7. Tampilkan gaji terkecil!
```
'SELECT MIN(gaji) FROM pegawaiper;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/329b8c4c-573a-4d78-8f03-02086ae0f4b2)


8. Tampilkan gaji terbesar!
```
'SELECT MAX(gaji) FROM pegawaiper;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/49efb1bd-510c-4f48-9e7d-5d20d8b933de)




2#
tabel hewan

pertama kita buat dulu tabelnya dengan cara
```
CREATE TABLE hewan2 (
  id varchar(15) NOT NULL,
  name varchar(15) NOT NULL,
  owner varchar(15) NOT NULL,
  species varchar(15) NOT NULL,
  sex enum('m', 'f', 'NULL') NOT NULL,
  PRIMARY KEY (id)
```
 lalu enter dan ketik 'desc hewan2;'

![image](https://github.com/sahrul180304/xampp4/assets/115526901/4be4c9e8-e6e9-47a5-aac6-81b73a76a08c)


selanjutnya kita ketik
```
 INSERT INTO hewan2 (id, name, owner, species, sex)
    -> values
    -> ('p1', 'Puffball', 'Diane', 'Hamster', 'f'),
    ->   ('p2', 'Claws', 'Gwen', 'Cat', 'm'),
    ->   ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'f'),
    ->   ('p4', 'Buffy', 'Haro 1d', 'Dog', 'f'),
    ->   ('p5', 'Fang', 'Benny', 'Dog', 'm'),
    ->   ('p6', 'Bowser', 'Diane', 'Dog', 'm'),
    ->   ('p7', 'Chirpy', 'Gwen', 'Bird', 'f'),
    ->   ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
    ->   ('p9', 'Slim', 'Benny', 'Snake', 'm');
```
lanjut enter dan 'select *from hewan2;'

![image](https://github.com/sahrul180304/xampp4/assets/115526901/f67174c1-ec4a-4d34-b354-cf7c18acc836)

lanjut ke praktikum

1. Tampilkan jumlah hewan yang dimiliki setiap owner.
```
'SELECT owner, COUNT(*) as jumlah_hewan FROM hewan2 GROUP BY owner;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/6bc71ceb-09b8-445c-9981-fb4b87ac0cbd)


2. Tampilkan jumlah hewan berdasarkan spesies.
```
'SELECT species, COUNT(*) as jumlah_hewan FROM hewan2 GROUP BY species;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/237de259-bf7c-4144-9264-cfa5e0910490)


3. Tampilkan jumlah hewan berdasarkan jenis kelamin.
```
'SELECT sex, COUNT(*) as jumlah_hewan FROM hewan2 GROUP BY sex;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/b1397cec-6a9f-4bdc-8b7c-55fe1249c4d7)


4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin.
```
'SELECT species, sex, COUNT(*) as jumlah_hewan FROM hewan2 GROUP BY species, sex;'
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/701c65ea-51e6-45a8-b559-8b6194ba32b0)


5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja)
dan jenis kelamin.
```
SELECT species, sex, COUNT(*) as jumlah_hewan
    -> FROM hewan2
    -> WHERE species IN ('Cat', 'Dog')
    -> GROUP BY species, sex;
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/3f230e27-c24f-49c4-ab17-4b6e47050b33)


6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui
saja.
```
 SELECT sex, COUNT(*) as jumlah_hewan
    -> FROM hewan2
    -> WHERE sex IS NOT NULL
    -> GROUP BY sex;
```
![image](https://github.com/sahrul180304/xampp4/assets/115526901/a9cc563b-c09b-47b2-ac9d-7e79a4b43726)


#Evaluasi dan Pertanyaan

kesimpulan
```
Dari percobaan SQL yang saya lakukan, dapat disimpulkan yaitu tabel "pegawaiper" telah berhasil dibuat dan diisi dengan data pegawai. quary-quary yang dilakukan berhasil menghasilkan output yang sesuai dengan kondisi yang di tentukan. Data dalam tabel dapat digunakan untuk analisis lebih lanjut seperti menghitung jumlah pegawai, total gaji, rata-rata gaji, gaji terkecil, dan gaji terbesar.
```



