# Tugas 2

**1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).**

Pertama-tama saya membuat repositori github baru dengan nama in-stock. kemudian, saya membuat folder in_stock dan menginisiasinya sebagai repositori git dengan perintah 

`git init`

`git config user.name "adindanurdzykra"`

`git config user.email "adinda.nurdzykra@gmail.com"`

`git config --global user.name "adindanurdzykra"`

`git config --global user.email "adinda.nurdzykra@gmail.com"`

kemudian, saya membuat file README.md lalu melakukan `add`, `commit`, dan `push`

setelah itu, saya membuat virtual environment dengan perintah `python3 -m venv env` dan mengaktifkannya dengan `source env/bin/activate`. Untuk memulai membuat projek baru Django, saya membuat file requirements.txt kemudian menjalankan `pip3 install -r requirements.txt`, barulah perintah membuat projek Django `django-admin startproject in_stock .`

Setelah itu, saya akan membuat aplikasi dengan nama main dengan menjalankan perintah `python3 manage.py startapp main` dan menambahkan 'main' pada INSTALLED_APPS di file settings.py. setelah itu, saya membuat folder baru di dalam directory main dengan nama 'templates' dan mengisi folder tersebut dengan file 'main.html' 

Dalam berkas models.py di folder main, saya membuat class Item yang berisi atribut name, amount, dan description.

Kemudian, saya membuka file views.py di folder main dan menambahkan kode yang ada di tutorial dengan mengubah nama dan kelas. 

Untuk melakukan routing, saya membuat file urls.py di dalam folder main dan mengisi nya dengan kode yang ada di tutorial. lalu saya membuka file urls.py dalam directory proyek in_stock dan menambahkan kodenya sesuai dengan tutorial. 

sebelum men-deploy aplikasi, saya melakukan `add`, `commit`, dan `push` ke repositori in-stock. barulah saya membuka adaptable.io dan men-deploy aplikasi menggunakan repositori in-stock

**2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.**

Link gambar: https://drive.google.com/file/d/1ytPj0tPjOwapb92SLn3D9WKD6qXFbyCl/view?usp=drive_link

Setelah request datang, urls.py berperan sebagai router yang akan mencocokan url sesuai request untuk memutuskan view yang harus dipanggil. View dapat melibatkan Model apabila request berkaitan dengan akses atau manipulasi data dalam models.py. Kemudian berkas HTML mangatur template tampilan yang akan dilihat user. Sehingga view dapat menampilkan data dari models.py sesuai dengan template dari berkas HTML dan menampilkannya sebagai response.

**3. Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?**

virtual environment berperan penting dalam pembuatan aplikasi web dalam fungsi isolasi package untuk setiap proyek yang dibuat agar tidak bertabrakan dan menghindari konflik dependencies.
Namun pembuatan web berbasis Django masih dapat dilakukan tanpa menggunakan virtual environment. Namun akan lebih baik kita menggunakan virtual environment untuk menghindari potensi konflik dependencies yang dapat terjadi.

**4. Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.**

- MVC atau Model-View-Controller adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk menampilkan user interface, dan Controller sebagai perantara antar keduanya dengan menerima input, memprosesnya, dan melakukan perubahan pada View

Konsep MVC lebih umum digunakan pada saat membuat aplikasi web dengan framework Ruby on Rails

- MVT atau Model-View-Template adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk mengatur apa yang akan ditampilkan, dan Template untuk mengatur tampilan akhir user interface.

Konsep MVT lebih umum digunakan pada saat membuat aplikasi web dengan framework Python Django

- MVVM atau Model-View-ViewModel adalah konsep arsitektur dengan Model yang mewakili pengolahan data dan logika aplikasi, View yang berperan untuk mengatur tampilan user interface, dan ViewModel yang mengkonversi data dari Model menjadi format yang sesuai dengan View. Selain itu VM menangani interaksi user untuk diteruskan kepada Model.

Konsep MVVM lebih banyak digunakan pada pengembangan aplikasi dekstop dan mobile karena ViewModel yang berperan penting untuk mengelola tampilan dan interaksi user

# Tugas 3
**1. Apa perbedaan antara form POST dan form GET dalam Django?**
Form POST biasanya digunakan saat data yang dimasukkan akan memengaruhi database, seperti penambahan, penyuntingan, atau penghapusan data. Selain itu, metode POST menggunakan request HTTP untuk mengirimkan data sehingga lebih aman.

Form GET digunakan untuk mengirimkan data yang tidak memengaruhi database, biasanya data yang dikirimkan berupa pencarian data. Berbeda dengan POST yang menggunakan request HTML untuk mengirimkan data, GET mengirimkan data melalui bagian dari URL sehingga memiliki tingkat keamanan yang lebih rendah daripada POST.

**2. Apa perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data?**
XML atau Extensible Markup Language adalah bahasa markup untuk mendefinisikan informasi apa yang akan disampaikan dari data yang tertulis. Informasi ditampilkan dalam tag yang besifat case sensitive sehingga programmer perlu menulis program untuk mengirim, menerima, menyimpan, atau menampilkan informasi tersebut. 

JSON atau JavaScript Object Notation adalah bahasa markup yang dibuat dengan struktur "key": "value". Karena formatnya yang menyerupai bahasa JavaScript, program berbahasa JavaScript dapat dengan mudah diconvert JSON menjadi JavaScript objects. 

HTML atau HyperText Markup Language adalah bahasa markup yang digunakan untuk membuat web yang dapat diakses oleh pengguna sehingga berfokuskan pada tampilan dan interaksi dengan pengguna. Metode pengiriman data dapat dilakukan dengan POST atau GET. Elemen HTML terdiri dari tag untuk memulai, elemen konten, dan tag untuk mengakhiri. 

Biasanya pengiriman data berbasis HTML digunakan dalam konteks form yang dibuka melalui peramban web, sedangkan untuk pengiriman data antar aplikasi dapat menggunakan JSON atau XML

**3. Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?**
- Proses pertukaran data lebih efisien karena JSON merangkumnya dengan lebih terstruktur dan sederhana sehingga server dapat langsung menampilkan data tersebut
- Menyederhanakan proses penerjemahan data agar mudah dipahami oleh manusia
- JSON didukung oleh hampir seluruh peramban web dan platform yang ada
  
source: https://midtrans.com/id/blog/json-format

**4. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).**
-> Membuat input form untuk menambahkan objek model pada app sebelumnya.
Pertama-tama, saya membuat kerangka views dengan membuat folder templates pada direktori utama in_stock yang kemudian diisi dengan berkas `base.html`. Isi berkas tersebut dibuat sama dengan yang tertulis di tutorial. Kemudian menambahkan kode `'DIRS': [BASE_DIR / 'templates'],` pada berkas settings.py di direktori proyek in_stock. Kemudian, saya menambahkan kode dibawah ini pada file main.html yang terdapat di main/templates.
```html
{% extends 'base.html' %}

{% block content %}
    <h1>In Stock Page</h1>

    <h5>Name:</h5>
    <p>{{name}}</p>

    <h5>Class:</h5>
    <p>{{class}}</p>
{% endblock content %}
```
Setelah itu, saya membuat berkas baru bernama forms.py pada direktori main dan menambahkan kode ini
```python
from django.forms import ModelForm
from main.models import Item

class ProductForm(ModelForm):
    class Meta:
        model = Item
        fields = ["name", "amount", "description"]
```
Lalu, pada berkas views.py ada direktori main saya menambahkan import reverse dan ProductForm. Selain itu saya membuat fungsi bernama create_product yang berisi kode ini
```python
def create_product(request):
    form = ProductForm(request.POST or None)

    if form.is_valid() and request.method == "POST":
        form.save()
        return HttpResponseRedirect(reverse('main:show_main'))

    context = {'form': form}
    return render(request, "create_product.html", context)
```
Kemudian, pada berkas urls.py di direktori main tambahkan import fungsi show_main dan tambahkan path `path('create-product', create_product, name='create_product'),`
Lalu, buat berkas create_product.html pada direktori main/templates yang berisi
```html
{% extends 'base.html' %} 

{% block content %}
<h1>Add New Product</h1>

<form method="POST">
    {% csrf_token %}
    <table>
        {{ form.as_table }}
        <tr>
            <td></td>
            <td>
                <input type="submit" value="Add Product"/>
            </td>
        </tr>
    </table>
</form>

{% endblock %}
```
Lalu pada main.html, saya tambahkan kode dibawah
```html
...
<table>
    <tr>
        <th>Name</th>
        <th>Amount</th>
        <th>Description</th>
    </tr>

    {% comment %} Berikut cara memperlihatkan data produk di bawah baris ini {% endcomment %}

    {% for product in products %}
        <tr>
            <td>{{product.name}}</td>
            <td>{{product.amount}}</td>
            <td>{{product.description}}</td>
        </tr>
    {% endfor %}
</table>

<br />

<a href="{% url 'main:create_product' %}">
    <button>
        Add New Product
    </button>
</a>

{% endblock content %}
```
Kemudian saya melakukan migrasi model terlebih dahulu agar perubahan yang saya buat terlacak dengan menjalankan perintah `python3 manage.py makemigrations` dan `python3 manage.py migrate`

-> Tambahkan 5 fungsi views untuk melihat objek yang sudah ditambahkan dalam format HTML, XML, JSON, XML by ID, dan JSON by ID.
Pada berkas views.py di direktori main, tambahkan import HttpResponse dan Serializer. Lalu saya buat 4 fungsi baru dibawah dan show_main untuk html nya
```python
def show_main(request):
    products = Item.objects.all()

    context = {
        'name': 'Adinda Nurdzykra', # Nama kamu
        'class': 'PBP E', # Kelas PBP kamu
        'products': products
    }

    return render(request, "main.html", context)

def show_xml(request):
    data = Item.objects.all()
    return HttpResponse(serializers.serialize("xml", data), content_type="application/xml")

def show_json(request):
    data = Item.objects.all()
    return HttpResponse(serializers.serialize("json", data), content_type="application/json")

def show_xml_by_id(request, id):
    data = Item.objects.filter(pk=id)
    return HttpResponse(serializers.serialize("xml", data), content_type="application/xml")

def show_json_by_id(request, id):
    data = Item.objects.filter(pk=id)
    return HttpResponse(serializers.serialize("json", data), content_type="application/json")
```

-> Membuat routing URL untuk masing-masing views yang telah ditambahkan pada poin 2.
Pada berkas urls.py di direktori main, tambahkan import `from main.views import show_main, create_product, show_xml, show_json, show_xml_by_id, show_json_by_id `
dan tambahkan path url agar dapat diakses
```python
urlpatterns = [
    path('', show_main, name='show_main'),
    path('create-product', create_product, name='create_product'),
    path('xml/', show_xml, name='show_xml'),
    path('json/', show_json, name='show_json'),
    path('xml/<int:id>/', show_xml_by_id, name='show_xml_by_id'),
    path('json/<int:id>/', show_json_by_id, name='show_json_by_id'), 
]
```
HTML

<img width="718" alt="HTML" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/239aef04-b811-41d8-90f9-41580551f224">


XML

<img width="706" alt="XML" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/4568913d-5029-4f2b-a71f-9b127696eb28">


XML by id

<img width="714" alt="XML_by_id" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/78cf7023-630e-4b8b-953d-8f11cc674e77">


JSON

<img width="715" alt="JSON" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/4bf06de9-36ca-4eea-a28d-f22eaf708ef6">


JSON by id

<img width="714" alt="JSON_by_id" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/196bac97-40ad-4013-8ec4-d7aa1849f6ac">


# Tugas 4
**1. Apa itu Django UserCreationForm, dan jelaskan apa kelebihan dan kekurangannya?**
Djago UserCreationForm merupakan modul yang dapat digunakan untuk membuat pengguna yang bisa mengakses sebuah aplikasi web. Django UserCreationForm memiliki tiga field, yakni: username, password1, dan password2. Dua field password dibutuhkan untuk mengonfirmasi isi password. 

kelebihan:
+ penggunaan Django UserCreationForm memberikan programmer kemudahan serta menghemat waktu karena Django UserCreationForm telah memiliki sistem validasi bawaan.

kekurangan:
- Namun, field yang dapat digunakan terbatas (hanya 3) sehingga programmer harus bisa membuat/mengubah kode untuk dapat menambahkan field baru

**2. Apa perbedaan antara autentikasi dan otorisasi dalam konteks Django, dan mengapa keduanya penting?**
- authentication adalah sistem yang mem-verivikasi pengguna yang masuk merupakan pengguna itu sendiri. 
- authorization adalah sistem yang menentukan apa saja yang dapat dilakukan oleh pengguna di dalam aplikasi web.
Kedua hal ini sangat penting untuk menjaga keamanan aplikasi web dan memberikan kontrol pada aktivitas pengguna. Hal ini akan sangat penting bagi aplikasi web yang menyimpan data user yang banyak. Selain itu, kita juga dapat memberikan dan menyesuaikan laman web dengan personalisasi tiap pengguna. 

**3. Apa itu cookies dalam konteks aplikasi web, dan bagaimana Django menggunakan cookies untuk mengelola data sesi pengguna?**
Cookies merupakan jejak yang ditinggalkan saat suatu pengguna mengunjungi sebuah aplikasi web. Hal ini digunakan agar aplikasi web tersebut dapat mengingat kunjungan serta apa aja yang user lakukan pada aplikasi web tersebut sehingga memudahkan user saat ingin melakukan login kembali. Django memiliki "session framework" yang dapat membantu untuk mengelola data sesi pengguna di server. Histori data sesi pengguna digunakan untuk mengidentifikasi sesi pengguna saat melakukan suatu hal pada aplikasi web kita sehingga kita dapat membuat personalisasi yang berbeda untuk tiap pengguna

**4. Apakah penggunaan cookies aman secara default dalam pengembangan web, atau apakah ada risiko potensial yang harus diwaspadai?**
Pada umumnya, aktivitas yang disimpan cookies tidak berbahaya karena hanya berwujud suatu data kecil. Namun, tidak menutup kemungkinan adanya risiko potensial yang dapat terjadi. Cookies memiliki beberapa jenis, salah satunya adalah persistent cookies. Persistent cookies adalah tipe cookies yang jangka panjang. Persistent cookies menyimpan data dari aktivitas penggunanya tidak hanya pada web yang mengeluarkan cookies, tetapi juga pada web-web lain. 

**5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).**
-> Mengimplementasikan fungsi registrasi, login, dan logout untuk memungkinkan pengguna untuk mengakses aplikasi sebelumnya dengan lancar
Pertama-tama, kita harus membuat laman untuk regiter. Jadi, saya menjalankan virtual environment terlebih dahulu. pada views.py di direktori main, tambahkan import ini di paling atas
```python
from django.shortcuts import redirect
from django.contrib.auth.forms import UserCreationForm
from django.contrib import messages  
```
lalu dibagian bawa, ditambahkan fungsi register ini
```python
def register(request):
    form = UserCreationForm()

    if request.method == "POST":
        form = UserCreationForm(request.POST)
        if form.is_valid():
            form.save()
            messages.success(request, 'Your account has been successfully created!')
            return redirect('main:login')
    context = {'form':form}
    return render(request, 'register.html', context)
```
lalu saya membuat file baru di main/templates, bernama register.html yang berisi
```html
{% extends 'base.html' %}

{% block meta %}
    <title>Register</title>
{% endblock meta %}

{% block content %}  

<div class = "login">
    
    <h1>Register</h1>  

        <form method="POST" >  
            {% csrf_token %}  
            <table>  
                {{ form.as_table }}  
                <tr>  
                    <td></td>
                    <td><input type="submit" name="submit" value="Daftar"/></td>  
                </tr>  
            </table>  
        </form>

    {% if messages %}  
        <ul>   
            {% for message in messages %}  
                <li>{{ message }}</li>  
                {% endfor %}  
        </ul>   
    {% endif %}

</div>  

{% endblock content %}
```
pada urls.py yang ada di direktori main, tambahkan import register dan juga tambahkanpath register pada urlpatterns

Selanjutnya saya membuat fungsi login dan logout. Buka views.py di direktori main dan tambahkan import di bagian paling atas
```python
from django.contrib.auth import authenticate, login, logout
```
kemudian ubah fungsi login_user dan tambahkan fungsi logout_user menjadi
```python
def login_user(request):
    if request.method == 'POST':
        username = request.POST.get('username')
        password = request.POST.get('password')
        user = authenticate(request, username=username, password=password)
        if user is not None:
            login(request, user)
            return redirect('main:show_main')
        else:
            messages.info(request, 'Sorry, incorrect username or password. Please try again.')
    context = {}
    return render(request, 'login.html', context)

def logout_user(request):
    logout(request)
    return redirect('main:login')
```
kemudian buat file html di dalam main/templates bernama login.html yang berisi
```html
{% extends 'base.html' %}

{% block meta %}
    <title>Login</title>
{% endblock meta %}

{% block content %}

<div class = "login">

    <h1>Login</h1>

    <form method="POST" action="">
        {% csrf_token %}
        <table>
            <tr>
                <td>Username: </td>
                <td><input type="text" name="username" placeholder="Username" class="form-control"></td>
            </tr>
                    
            <tr>
                <td>Password: </td>
                <td><input type="password" name="password" placeholder="Password" class="form-control"></td>
            </tr>

            <tr>
                <td></td>
                <td><input class="btn login_btn" type="submit" value="Login"></td>
            </tr>
        </table>
    </form>

    {% if messages %}
        <ul>
            {% for message in messages %}
                <li>{{ message }}</li>
            {% endfor %}
        </ul>
    {% endif %}     
        
    Don't have an account yet? <a href="{% url 'main:register' %}">Register Now</a>

</div>

{% endblock content %}
```
dan kemudian tambahkan button logout pada file main.html di direktori yang sama
```html
...
<a href="{% url 'main:logout' %}">
    <button>
        Logout
    </button>
</a>
...
```
Kembali ke file urls.py di direktori main dan tambahkan import
```python
from main.views import login_user, logout_user
```
dan tambahkan path url di dalam urlspatterns
```python
...
path('login/', login_user, name='login'),
path('logout/', logout_user, name='logout'),
...
```
Kemudian agar akses halaman main hanya untuk user yang telah ter-autentikasi, saya buat restriksi akses. Buka views.py di direktori main dan tambahkan import `from django.contrib.auth.decorators import login_required` dan tambahkan kode `@login_required(login_url='/login')` sebelum fungsi show_main

-> Membuat dua akun pengguna dengan masing-masing tiga dummy data menggunakan model yang telah dibuat pada aplikasi sebelumnya untuk setiap akun di lokal.

<img width="1378" alt="Screenshot 2023-09-27 at 08 04 42" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/b06a1c05-1d3f-4047-9907-fac0692e3529">

<img width="1367" alt="Screenshot 2023-09-27 at 07 59 39" src="https://github.com/adindanurdzykra/in-stock/assets/121367510/2e1cd889-f494-4ed4-af1b-5622299bbc5c">



-> Menghubungkan model Item dengan User
Pertama, buka file models.py yang ada di direktori main dan tambahkan import `from django.contrib.auth.models import User`. Selanjutnya tambahkan `user = models.ForeignKey(User, on_delete=models.CASCADE)` di dalam fungsi Item untuk menghubungan item pada satu user. Lalu, buka file views.py pada direktori yang sama dan ubah kode menjadi
```python
 if form.is_valid() and request.method == "POST":
     product = form.save(commit=False)
     product.user = request.user
     product.save()
     return HttpResponseRedirect(reverse('main:show_main'))
```

-> Menampilkan detail informasi pengguna yang sedang logged in seperti username dan menerapkan cookies seperti last login pada halaman utama aplikasi.

agar pada field nama ditampilkan username user yang sedang masuk, ubah kode `'name': request.user.username,` pada fungsi show_main. Lalu migrasikan model.

lalu untuk menampilkan last login, saya membuka views.py di direktori main dan menambahkan import di bagian atas seperti dibawah ini
```python
import datetime
from django.http import HttpResponseRedirect
from django.urls import reverse
```
di bagian fungsi login_user, saya mengubah kode ini
```python
if user is not None:
    login(request, user)
    response = HttpResponseRedirect(reverse("main:show_main")) 
    response.set_cookie('last_login', str(datetime.datetime.now()))
    return response
```
dan menambahkan `'last_login': request.COOKIES['last_login'],` pada fungsi show_main di dalam variabel context
kemudian, agar last_login dihapus oleh cookies user melakukan logout, pada fungsi logout_user, ubah fungsinya menjadi 
```python
def logout_user(request):
    logout(request)
    response = HttpResponseRedirect(reverse('main:login'))
    response.delete_cookie('last_login')
    return response
```


# Tugas 5
**1. Jelaskan manfaat dari setiap element selector dan kapan waktu yang tepat untuk menggunakannya.**

- Tag Selector adalah cara mengubah properti pada tiap elemen yang menggunakan tag tersebut
```HTML
a {
}
```
- Class Selector adalah pengaturan properti yang dapat digunakan untuk mengelompokan elemen yang memiliki karakteristik sama
```HTML
.class {
}
```
- ID Selector adalah pemanggilan kelas untuk elemen dengan atribut yang unik dalam HTML
```HTML
#id {
}
```
- Universal Selector adalah pengubahan properti yang bersifat global dan berpengaruh pada keseluruhan halaman
```HTML
* {
}
```

**2. Jelaskan HTML5 Tag yang kamu ketahui.**

`<h1></h1>` untuk mendefinisikan header

`<table></table>` untuk mendefinisikan penyusunan table

`<!DOCTYPE>` untuk memberikan spesifikasi tipe dokumen

`<p></p>` untuk mendefinisikan sebuah paragraf

`<img></img>` untuk men-spesifikasikan sebuah gambar

**3. Jelaskan perbedaan antara margin dan padding.**

Margin mengacu pada ruang yang berada di sekitar element. Setiap sisi elemen memiliki margin untuk mengatur sedekat apa suatu elemen dengan elemen lain. 

Sedangkan, padding adalah ruang yang berada di dalam elemen atau ruang antara elemen dengan konten di dalam elemen tersebut. Padding digunakan untuk mengatur seberapa dekat atau jauh suatu konten dengan border dari elemen tempat ia berada. 

**4. Jelaskan perbedaan antara framework CSS Tailwind dan Bootstrap. Kapan sebaiknya kita menggunakan Bootstrap daripada Tailwind, dan sebaliknya?**

Tailwind mengedepankan pendekatan "utility-first" yakni penyusunan tampilan dilakukan dengan menggabungkan class utility yang lebih kecil. Hal ini memungkinkan untuk memberikan fleksilitas yang lebih besar untuk mengatur tampilan sehingga cocok untuk pengembang web yang ingin membuat tampilan web yang unik. Tailwind memiliki ukuran file yang lebih ringan. 

Bootstrap memberikan set class CSS dengan tampilan yang terstruktur melalui kerangka kerjanya sehingga dapat digunakan untuk pengembang web yang mementingkan kestabilan dan kemudahan untuk digunakan namun tetap memiliki fleksibilitas dalam mendesain tampilannya. BootStrap memiliki ukuran file yang lebih besar karena telah menyediakan banyak fitur dan komponen yang dapat langsung digunakan oleh pengembang web.  
**5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).**


-> Kustomisasi halaman login, register, dan tambah inventori semenarik mungkin.

Untuk memberikan desain yang konsisten, saya membuat class dalam tag style yang berisi template desain yang ingin saya gunakan. Seperti yang ada dibawah ini
```HTML
.template {
    background-color: #f3f2dc;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 200px;
    margin-bottom: 200px;
    margin-right: 200px;
    margin-left: 200px;
    font-family: "Times New Roman", sans-serif;
    font-weight: bold;
    border: 1px solid #00000000;
    padding-top: 100px;
    padding-bottom: 100px;
    border-radius: 10px;
    box-sizing: border-box;
    border-style: ridge;
    line-height: 3;
}
```

-> Kustomisasi halaman daftar inventori menjadi lebih berwarna maupun menggunakan apporach lain seperti menggunakan Card.


Saya menggunakan class card untuk menyusun dan menampilkan informasi tiap item. Kemudian agar tiap card tidak terlalu berdekatan satu sama lain, saya menyusunnya menggunakan class col-md-4 mb-3 yang akan men-spesifikasi bahwa elemen card akan menggunakan 4 grid colom bootstrap serta memberikan margin bawah untuk menjaga jarak dengan cards dibawahnya.


# Tugas 6

**1. Jelaskan perbedaan antara asynchronous programming dengan synchronous programming.**

Asynchronous Programming adalah sebuah pendekatan dalam pemrogramman yang tidak terikat dengan protokol input dan output sehingga pengeksekusian kode tidak terpaut baris per baris. Kunci utama pada Asynchronous Programming adalah ketidakterikatan satu proses dengan proses lain. Hal ini menyebabkan proses pengeksekusian program dapat berjalan dengan lebih cepat karena tidak perlu menunggu proses dari task lain.

Sebaliknya, Synchronous Programming adalah pendekatan dalam pemrograman yang menggunakan antrean dalam proses eksekusi programnya. Pada Synchronous Programming, waktu eksekusi akan cenderung lebih lama dibandingkan dengan Asynchronous Programming karena program harus menunggu task selesai untuk lanjut ke task selanjutnya. 

**2. Dalam penerapan JavaScript dan AJAX, terdapat penerapan paradigma event-driven programming. Jelaskan maksud dari paradigma tersebut dan sebutkan salah satu contoh penerapannya pada tugas ini.**

Event-driven Programming adalah suatu paradigma programming yang akan menjalankan suatu task berdasarkan event tertentu. Pada Event-driven Programming, program akan melakukan suatu task apabila mendapatkan suatu event tertentu, seperti input, button, dan lain-lain. Oleh karena itu, Event-driven Programming adalah program yang memiliki input, proses, dan output. 

Pada tugas ini, penerapan Event-driven Programming salah satunya ada pada halaman login, setelah kita memasukkan username dan password dan menekan tombol login, program akan membaca username dan password yang kita masukkan dan melakukan autentikasi berdasarkan daftar pengguna yang telah mendaftar. Output yang dihasilkan berupa pengguna masuk atau gagal masuk. 

**3. Jelaskan penerapan asynchronous programming pada AJAX.**

Penerapan Asynchronous Programming pada AJAX digunakan saat terjadi proses masukan lalu akan terjadi proses pertukaran informasi di belakang. Hal ini yang menyebabkan web akan terbarui tanpa harus me-refresh keseluruhan halaman. Berikut merupakan cara kerja AJAX:
- Browser akan memanggil AJAX untuk mengaktifkan HttpRequest dan mengirimkan HTTP request ke server
- kemudian, HttpRequest akan dibuat untuk melakukan pertukaran data di server secara asynchronous
- setelah menerima informasi, server akan memprosesnya lalu mengirimkan kembali hasil proses yang telah dilakukan
- Browser akan menerima dan langsung menampilkannya di laman web

**4. Pada PBP kali ini, penerapan AJAX dilakukan dengan menggunakan Fetch API daripada library jQuery. Bandingkanlah kedua teknologi tersebut dan tuliskan pendapat kamu teknologi manakah yang lebih baik untuk digunakan.**

Fetch API adalah proses request layanan ke endpoint atau letak url yang akan menerima request. Fetch API akan mengambil response yang berupa data berformat json atau teks. Meskipun demikian, Fetch API tidak kompatable dengan beberapa browser yang sudah lama.

Sedangkan, AJAX jQuery adalah library yang menyederhanakan proses request AJAX. Namun, ukuran data jQuery lebih besar daripada Fetch API sehingga akan membutuhkan waktu yang lebih lama untuk memuat laman web

Dalam pemilihan penggunaan kedua teknologi tersebut, kita perlu mempertimbangkan kebutuhan program. Untuk mendapatkan performa web yang lebih cepat, kostumisasi yang lebih beragam, ukuran program yang lebih ringan, maka lebih baik menggunakan Fetch API. Untuk programmer yang ingin menguramakan kemudahan dan kenyamanan, maka lebih baik menggunakan jQuery yang memiliki sintax yang lebih simple. 

**5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).**
