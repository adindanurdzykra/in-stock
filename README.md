Link Adaptable: https://in-stock.adaptable.app


1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).

Pertama-tama saya membuat repositori github baru dengan nama in-stock. kemudian, saya membuat folder in_stock dan menginisiasinya sebagai repositori git dengan perintah 
[git init
git config user.name "adindanurdzykra"
git config user.email "adinda.nurdzykra@gmail.com"
git config --global user.name "adindanurdzykra"
git config --global user.email "adinda.nurdzykra@gmail.com"]
kemudian, saya membuat file README.md lalu melakukan add, commit, dan push

setelah itu, saya membuat virtual environment dengan perintah [python3 -m venv env] dan mengaktifkannya dengan [source env/bin/activate]. Untuk memulai membuat projek baru Django, saya membuat file requirements.txt kemudian menjalankan [pip3 install -r requirements.txt], barulah perintah membuat projek Django [django-admin startproject in_stock .]

Setelah itu, saya akan membuat aplikasi dengan nama main dengan menjalankan perintah [python3 manage.py startapp main] dan menambahkan 'main' pada INSTALLED_APPS di file settings.py. setelah itu, saya membuat folder baru di dalam directory main dengan nama 'templates' dan mengisi folder tersebut dengan file 'main.html' 

Dalam berkas models.py di folder main, saya membuat class Item yang berisi atribut name, amount, dan description.

Kemudian, saya membuka file views.py di folder main dan menambahkan kode yang ada di tutorial dengan mengubah nama dan kelas. 

Untuk melakukan routing, saya membuat file urls.py di dalam folder main dan mengisi nya dengan kode yang ada di tutorial. lalu saya membuka file urls.py dalam directory proyek in_stock dan menambahkan kodenya sesuai dengan tutorial. 

sebelum men-deploy aplikasi, saya melakukan add, commit, dan push  ke repositori in-stock. barulah saya membuka adaptable.io dan men-deploy aplikasi menggunakan repositori in-stock

2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.

Link gambar: https://drive.google.com/file/d/1ytPj0tPjOwapb92SLn3D9WKD6qXFbyCl/view?usp=drive_link

Setelah request datang, urls.py berperan sebagai router yang akan mencocokan url sesuai request untuk memutuskan view yang harus dipanggil. View dapat melibatkan Model apabila request berkaitan dengan akses atau manipulasi data dalam models.py. Kemudian berkas HTML mangatur template tampilan yang akan dilihat user. Sehingga view dapat menampilkan data dari models.py sesuai dengan template dari berkas HTML dan menampilkannya sebagai response.

3. Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?

virtual environment berperan penting dalam pembuatan aplikasi web dalam fungsi isolasi package untuk setiap proyek yang dibuat agar tidak bertabrakan dan menghindari konflik dependencies.
Namun pembuatan web berbasis Django masih dapat dilakukan tanpa menggunakan virtual environment. Namun akan lebih baik kita menggunakan virtual environment untuk menghindari potensi konflik dependencies yang dapat terjadi.

4. Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.

- MVC atau Model-View-Controller adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk menampilkan user interface, dan Controller sebagai perantara antar keduanya dengan menerima input, memprosesnya, dan melakukan perubahan pada View

Konsep MVC lebih umum digunakan pada saat membuat aplikasi web dengan framework Ruby on Rails

- MVT atau Model-View-Template adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk mengatur apa yang akan ditampilkan, dan Template untuk mengatur tampilan akhir user interface.

Konsep MVT lebih umum digunakan pada saat membuat aplikasi web dengan framework Python Django

- MVVM atau Model-View-ViewModel adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk mengatur tampilan user interface, dan ViewModel yang mengkonversi data dari Model menjadi format yang sesuai dengan View. Selain itu VM menangani interaksi user untuk diteruskan kepada Model.

Konsep MVVM lebih banyak digunakan pada pengembangan aplikasi dekstop dan mobile karena ViewModel yang berperan penting untuk mengelola tampilan dan interaksi user