Rerieve Data Geospatial

Melakukan select dan view

Data record dari file dbf dan geometri dari file shp

Tool : lib pyshp

Cara Retrieve data

1.  Buka file terlebih dahulu

    -import shapefile

    -sf = shapefile.Reader(“nama.shp”)

2.  Hitung berapa jumlah Record

    Membuka dbf ;

    -sf.records()

    -sf.record(n)

    -sf.fields = melihat daftar nama field

    Membuka shp :

    -sf.shapes()

    -sf.shape(n)

    -dir(shapes)

Contoh 1 (hitung record)

a = sf.shapes() -&gt; retrieve all data geometri

Len(a) = digunakan untuk menghitung jumlah record di variable a dimana len() itu fungsi menghitung jumlah arrow/dict dalam variable

Contoh 2 (melihat nama fields)

Nama.file = sf.fields

Print nama.fields

File SHP berisi :

-   Bbox :

    Boundary box dapat berupa koordinat dan titik, artinya data view melihat peta

-   Parts :

    Dibagi lebih dari 2 record artinya data keseluruhan

-   Points :

    Koordinat

-   Shapetype :

    Standar nomor

Geom Menurut data geometri oleh ESRI :

| Value | Shape Type | Fields                                                |
|-------|------------|-------------------------------------------------------|
| 1     | Point      | X, Y                                                  |
| 3     | Polyline   | MBR, Number of parts, Number of points, Parts, Points |
| 5     | Polygon    | MBR, Number of parts, Number of points, Parts, Points |

Membuat class di python

-vi gede.py

Import shapefile

Class gede(object) :

Defhitungbaris(self.namafile)

Sf = shapefile.Reader(namafile)

Record = sf.shapes()

Return len(rec)

-Import gede

-inst = gede.Gede()

-inst.hitungbaris(“shp/bts\_negara.shp”)

Constract

Import shapefile

Class gede(object) :

Def\_init\_(shelf,namafile):

Self.sf = shapefile.Reader(namafile)

Def hitungbaris (self)

Rec = self.sf.shapes()

Return len(rec)
