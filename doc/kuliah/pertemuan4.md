Retrieve Data Geospatial Bagian 2

Retrieve data mengambil data shapefile dari ESRI retrieve data di bagi menjadi 2 yaitu :

1.  Dbf : table atribut data

2.  Shp : data geometri

Geometri standard ESRI

Point : data berupa titik

Polyline : data berupa garis

Poligon : data berupa garis yang dari titik awal bertemu dengan titik akhir

Operasi Pada Python

Library pyshp dipanggil dengan :

**Import shapefile**

instansiasi kelas shapefile kepada sebuah variabel :

sf = shapefile.Reader(‘coastline.shp’)

Maka variable sf adalah instansi dari kelas shapefile kita bias jalankan method 2 variabel instant sf

Method

Dbf : sf.fields

Untuk melihat atribut tabel

Sf.records()

Sf Untuk mengambil semua record

Sf.record(n)

Mengambil baris ke n records

Shp : sf.shapes()

mengambil semua recorde geom

sf.shape(n)

mengambil data ke n baris

BBOX ( Bonding Box)

Titik pinggir view peta

Parts

Record ini bagian dari record lain

Point

Koordinat oembentiuk shapetype

CONTOH MEMBUAT CLASS MEMILIH CLASS

**Import shapefile **

**Class Gede(object):**

**Def\_\_init\_\_(self,namafile):**

**Self.sf = shapefile.reader(namafile)**

**Def itungbaris(self):**

**Rec = self.sf.shapes()**

**Return len(rec)**

**Def selectNegara(self,NEGARA):**

**i = 0**

**for a in self.sf.records():**

**if a\[8\] ==NEGARA:**

**return i**

**i=i+1**
