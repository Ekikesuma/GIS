Membuat Data Geospatial

Langkah membuat data/ create data file shp :

-   Import shapefile

-   a = shapefile.Writer(param)

-   a.point(x,y)

-   a.poly(\[x,y\],\[v,w\])

Langkah membuat data/ create data file dbf :

-   import shapefile

-   a = shapefile.Writer(param)

-   a.field(‘namafield’,’C’,’40’)

-   a.record(‘bdg’)

Kemudian disimpan dengan cara :

a.save(‘file.shp’)

Penjelasan Metod Writer :

-   Point(x,y)

    Memasukkan data berbentuk poin ke dalam shp, dan berdasarkan format ESRI : 1

-   Poly(\[a,b\],\[c,d\])

    Memasukkan data geospatial berbentuk poligon(kembal ke titik awal) dan polilyne(tidak kembali ke titik awal)

-   Field(‘Budaya’,’C’,’40’)

    Membuat atribut tabel bernama Budaya dengan tipe data varchar dengan panjang 40 karakter, jika ingin tambah field maka panggil kembali method field

-   Record(‘Bandung’)

    Mengisi tabel yang hanya 1 field dengan value = Bandung, jika ada dua field maka record(‘Bandung’,’kota’)

-   Save(‘namafile.shp’)

    Menyimpan file shapefile di komputer

Parameter pada Writer :

-   Shapefile POLIGON

-   Shapefile POINT

-   Shapefile POLYLINE

Contoh dalam aplikasi

POINT :

Import shapefile

a = shapefile.Writer()

a.point(10,12)

POLYLINE

Import shapefile

a = shapefile.Writer()

a.poly(parts\[{1,5},{5,5},{3,3}\])

shapetype = shapefile.POLYLINE

POLIGON

Import shapefile

a = shapefile.Writer()

a.poly(parts = \[{1,5},{5,5},{3,3}\])
