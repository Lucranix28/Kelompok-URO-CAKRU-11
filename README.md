# Kelompok-URO-CAKRU-11
Tugas Programming day 3 URO
#https://www.codingame.com/ide/puzzle/platinum-rift-episode-2

- Made Yogga Anggara Pangestu 16918038 

- Muhammad Ikhsan Kusrachmansyah 16518395

- David Fauzi 16518323

- Rosyid Ridho 16418279

#PENJELASAN GAME
Game ini adalah suatu jenis game bergenre dominasi , dimana map dari game ini terdiri dari tile-tile yang berbentuk hexagonal 
, tiap sisi hexagonal dapat terhubung dengan tile-tile hexagonal lainnya . Kita bermain sebagai pengendali pesawat \ POD yang 
memiliki markas dan mampu menggerakan 1 / lebih POD dari 1 tile ke tile lainnya . Ketika POD bergerak ke tile yang kosong ,
maka tile tersebut akan menjadi tile milik kita, dan jika POD kita bertabrakan dengan POD musuh , maka akan terjadi clash/bertempur. 
Jika POD bergerak ke tile yang telah dimiliki musuh Kita melawan pesawat" musuh dan kondisi menang adalah ketika kita berhasil menguasai 
HQ/ markas musuh atau setelah 250 turn , kita memiliki dominasi tile yang lebih banyak daripada musuh kita . Setiap Tile memiliki platinum
yang ber-range 0-6 , platinum adalah currency dari game ini , ketika platinum telah mencapai 20 platinum , akan terbeli 1 POD secara
otomatis .
# KONDISI MENANG
MENANG : Jika POD kita dapat mencapai base / HQ dan tidak ada lagi POD musuh tersisa di HQ untuk men-defend atau setelah 250 turns , POd kita menguasai lebih banyak tiles

# Strategi :
- POD akan bergerak dengan memprioritaskan zona yang dapat memberikan platinum terbesar

# Pembuka / Initialisasi
 Apabila POD tidak melihat musuh , maka strategi yang diterapkan adalah menyebar. Strateginya adalah 8 POD masing-masing      menguasai zona berbeda secara menyebar , selainkan 2 pod lain akan bergerak mengikuti satu sama lain untuk menguasai daerah yang berada dekat dengan musuh sambil menyerang musuh secara bersama-sama apabila POD mendeteksi musuh yang datang .
 
 Apabila POD melihat musuh , maka strategi berubah menjadi menyerang . 6 pod menyerang musuh dan disaat bersamaan 4 pod lain tetap berfokus untuk menguasai zona yang jauh dari musuh . 6 POD yang menyerang musuh akan mengincar POD lawan yang posisinya paling dekat dengan zona 

 
 MIDDLE GAME 

  Apabila zona sendiri sudah banyak yang dikuasai lawan maka semua POD akan berfokus untuk terlebih dahulu menyerang musuh secara bersama -sama agar daerah yang telah dikuasai tidak jatuh ke tangan musuh 
  
  :Apabila musuh telah terdesak maka POD yang sedang bertahan difokuskan secara menyeluruh untuk menyerang musuh agar musuh lebih cepat kehilangan zona mereka 
  
 Apabila terdapat musuh yang mengikuti arah gerak POD kepunyaan sendiri yang sedang menguasai zona lain maka POD kita akan fokus untuk menyerang POD tersebut terlebih dahulu agar gerakan POD tidak terasa sia-sia
  
   Apabila zona milik sendiri diserang oleh musuh secara bersamaan dan kemungkinan menguasai kembali zona tersebut adalah kecil, maka 8 POD akan fokus untuk menguasai area lain serta area lawan agar tidak menyia-nyiakan POD yang ada dan 2 lainnya akan menjaga base 


# Disclaimer ( Algoritma Program yang dibuat )
Kami telah menyusun strategi yang menurut kami adalah strategi terbaik untuk dapat memenangkan game secara konsisten , tapi pada kenyataannya karena keterbatasan waktu dan pengetahuan , kami hanya dapat membuat program dengan kemampuan algoritma sebagai berikut :
- POD mampu membaca tiles POD tersebut dalam bentuk array dengan index-1 sebagai posisi tiap tilesnya dan juga tiles-tiles apa sajakah yang adjacent atau menempel pada hexagon tiles POD tersebut yang disimpan dalam array didalam array .
- dari beberapa tiles adjacent ,POD mampu memprioritaskan kemana POD akan bergerak dengan kriteria : Apakah daerah yang dituju sudah pernah dikunjungi ? dan Apakah tiles tersebut merupakan tiles milik kita,lawan , atau netral . 
-POD memiliki kemampuan untuk men-split jumlah plot agar tiles lebih cepat terisi dengan beberapa pertimbangan


