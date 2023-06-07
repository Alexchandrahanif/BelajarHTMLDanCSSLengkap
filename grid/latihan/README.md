## Belajar Grid System

#### Latihan 1 =>

#### Latihan 2 =>

#### Latihan 3 =>

#### Latihan 4 =>

   <!--
        CSS Grid Terminology
        1. Grid Container
            => Pembungkus Element grid (display : grid)

        2. Grid Item
            => Element yang ada didalam pembungkus

        3. Grid Line
            => Garis horizontal/vertikal yang memisahkan grid
            menjadi beberapa bagian

        4. Grid Cell
            => Perpotongan antara baris dan koolon dalam grid

        5. Grid Area
            => Kumpulan lebih dari satu grid cell yang membentuk kotak

        6. Grid Track
            =>  Jarak antar 2 grid line
        
        7. Grid Gap
            => Jarak antara grid track atau grid cell
    
        CSS Grid Properties
        Pada Container(pembungkus) :

        1. grid-template-columns & grid-template-rows
            => untuk mendefenisikan column dan baris, nilai yang
            kira kasih mempresentasikan grid track dan grid line

        2. grid-auto-columns & grid-auto-rows
            => untuk mengatur column atau baris yang impicit,
            atau baris yang tidak terdefenisikan di template

        3. grid-auto-flow
            => mengatur penempatan item/cell pada grid track (implicit)
            pada grid auto flow ini default nya adalah row, makanya ketika
            template column nya kita atur 2, maka yg ke 3 turun
            namun ketika kita atur menjadi column, maka dia akan membentuk 1 baris saja

            ketika kita atur menjadi column, maka yg seharusnya
            1 2 3
            3 4 6 => default => row

            menjadi
            1 3 5
            2 4 6 => column

        4. grid Values
            Membuat pakai nama, dan fr (fraction)
            contoh ; {
                grid-template-columns : 1fr 3fr 1fr (dari kiri ke kanan => baris)
                grid-template-rows : 1fr 5fr 1fr (dari atas ke bawah => column)
            }

        Explicit => Menjelaskan dengan jelas ukuran column dan barisnya
        Implicit => Otomatis ditentukan oleh grid
    
        Special Keyword
        1. repeat()
            => untuk menentukan ukutan grid tracl secara berulang
            {
                display : grid,
                grid-template-columns : repeat(5, 1fr) => (1fr 1fr 1fr 1fr 1fr)
            }
            kalau mau dibuat 2x atau berbeda maka :
            {
                display : grid,
                grid-template-columns : repeat(2, 1fr) repeat(3, 1fr) => (2fr 2fr 1fr 1fr 1fr)
            }
        2. min-content & max-content
            => disini untuk mengatur dari lebar dari content
            contoh : {
                grid-template-columns : 1fr min-content 1fr
            }
            maka pada column ke 2, lebar nya menyesuaikan minimal content
            perbedaan max dan min content, ketika min content, maka ketika ada 2 kata
            maka akan dipisah dan menjadi 2 baris, dan ketika max maka dia ambil semuanya misal :

            (alex chandra) => max
            jadi :
            (alex
            chandra) => min

        3. minmax()
            => menentukan ukuran minimal dan maksimal dari semuah grid track
            contoh : {
                display : grid
                grid-template-columns : minmax (200px, 300px) => artinya minimal 200px, dan maksimal nya 300px
            }

        4. auto-fill & auto-fit
            =>  untuk menentukan jumlah item, biasanya digunakan dalam fungsi repeat
            contoh : {
                width : 60%,
                grid-template-columns : repeat(auto-fill, 100px)
            }
            => artinya setiap item lebarnya 100px
            ketika lebar container : 550px maka
            [ [][][][] ]
            [ [][][][] ]
            namun ketika 700, maka dia akan mengisi menjadi 7, dan dibaris ke 2 nya 1
            karena container muat 700
            [ [][][][][][][] ]
            [ [] ]

            beda dari auto fill dan auto fit adalah :
            - auto-fit => ketika dia ada 3 item, dan container masih muat untuk 4 item
            maka untuk gridnya cuma sampai ke item ke 3, namun :
            - auto-fill => tetap akan memetakan berapa item yang muat didalam container

            dan ini cocok untuk repsonsive
    -->
