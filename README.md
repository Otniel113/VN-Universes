# VN-Universes
Menemukan semua universe pada VN (Visual Novel) dengan menggunakan deteksi komunitas berbasis Modularity pada teori graf berdasarkan data VNDB. Tools yang digunakan adalah Gephi dan Sigma JS.

## Deployment
Untuk melihat langsung dapat ke: https://otniel113.github.io/VN-Universes/

## Tampilan
![image](https://user-images.githubusercontent.com/57952404/203910463-b4e8a19e-5531-41e8-8cd9-ef620fddcc62.png)

## Pendahuluan
Teori deteksi komunitas pada graf digunakan untuk menemukan komunitas pada graf/jaringan VN Relation. Karena kumpulan VN-VN yang ada pada satu komunitas dapat dianggap berada pada satu universe.

## Data
Data didapatkan dengan melakukan query SQL pada [Query VNDB](https://query.vndb.org/)

```sql
SELECT v1.title AS "Source", v2.title AS "Target"
FROM vn_relations vr
JOIN vn v1 ON v1.id = vr.id
JOIN vn v2 ON v2.id = vr.vid
WHERE vr.official = true;
```
Dengan ukuran 17810 x 2

## Spesifikasi Graf

| Parameter | Nilai |
| -- | -- |
| Banyak node | 11503 |
| Banyak edge | 8891 |
| Berarah | Tidak |
| Berbobot | Tidak |
| Multiedge | Tidak |
| Loop | Tidak |
| Jenis graf | Simple graph |

## Komunitas
Banyak komunitas yang terbentuk adalah 3447 dengan memberikan warna pembeda pada top 300 komunitas
