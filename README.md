# Pre-Test Bootcamp DevOps

## knowledge base

1. Apa yang anda ketahui tentang DevOps?
2. Apa yang anda ketahui tentang Infrastructure?
3. Apa yang anda ketahui tentang server, sebutkan implementasi berserta contohnya?
4. Mengapa server dibutuhkan dalam pengembangan/development suatu software?
5. Apa yang anda ketahui mengenai Virtualisasi dan Container?
6. Mengapa teknology container saat ini sangat populer?
7. Apa yang anda ketahui tentang Orchestration Container System?

Cara pengerjaan, silahkan update file ini tulis jawabanya di bawah ini

Jawaban
1. DevOps merupakan peran yang berhubungan dengan developer dan operations yang dimana devops ini memiliki
  tugas bagaimana caranya aplikasi yang sudah dibuat oleh tim developer untuk bisa berjalan diserver yang dimainteain oleh tim Operation
  
2. Infrastructur merupakan rangkaian dari keseluruhan layanan yang memiliki elemen didalamnya dan nantinya akan bertemu dengan beberapa      aspek seperti People,Server,dan Jaringan

3.server yaitu platform layanan untuk menyimpan dan menampung data atau sumber daya yang dibutuhkan yang dimana layanan server ini bisa     berupa hardware maupun software
  Contohnya : Web server jenis sever yang miliki fungsi khusus untuk melayani request protokol HTTP dan HTTPS ,web server ini melayani      client untuk meminta akses dari web browser yang berupa dokumen web seperti : htlm,css,javascript yang kemudian menampilkan informasi     yang dibutuhkan (teks,gambar,audio,maupun video).

4. server sangat dibutuhkan untuk pengembangan software karena server sangat          membantu untuk proses pengembangan software untuk      sebagai wadah atau penyimpanan dari data atau sumber daya sebuah perangkat lunak

5.- Virtualisasi sebuah teknologi yang dapat merubah suatu material yang yang          sebelumnya bersifat fisik menjadi sebuah virtual       yang dapat memberikan efisiensi   dalam mengerjakan suatu pekerjaan

  - Container berfungsi mempackage aplikasi yang sudah dibuat secara bersamaan         dengan despendensi
  
6. selain karena Container yang membantu para developer ,container juga lebih user friendly dibandingkan teknologi lainya karena memiliki   size yang lebih kecil dibandungkan VM

7. Sebuah Tools untuk melayani host dalam sebuah grup dan membentuk sebuah cluster serta membantu untuk memenuhi layanan
   
## Task 1 (Virtualization)

- Buatlah sebuah VM dengan kententuan
  - username: `<github_user>` contoh `dimasm93`
  - hostname: `<email_without_at>` contoh `dimas.tabeldata.com`
  - OS: `ubuntu-20.04` atau `centos-7`
- Install webserver `nginx`
- Buatlah web profile temen-temen kemudian deploy ke webserver nginx tersebut yang telah di deploy
  
(kirimkan hasil screenshotnya simpan dalam folder `screenshot` dengan nama `task1.png`)

## Task 2 (Container)

Jika saya memiliki architecture seperti berikut:

![container-apps](docs/images/01-container.png)

Dimana berikut adalah configurasi docker image:

1. Backend container
  - image: `dimmaryanto93/udemy-springboot-app:latest`
  - port: `8080`
  - env: 
    - `DATABASE_HOST`: `<ip-domain-db>`
    - `DATABASE_PORT`: `5432` 
    - `DATABASE_NAME`: `<db-name>`
    - `DATABASE_PASSWORD`: `<db-password>`
    - `APPLICATION_PORT`: `8080`
  need:
    - Database PostgreSQL v14.2
2. Frontend container
  - image: `dimmaryanto93/udemy-angular-app:latest`
  - port: `80`
  - env:
    - `APPLICATION_PORT`: `80`
    - `NGINX_ROOT_DOCUMENT`: `/var/www/html`
    - `BACKEND_HOST`: `<ip-backend-apps>`
    - `BACKEND_PORT`: `<port-backend-apps>`
    - `BACKEND_CONTEXT_PATH`: `/`
  - need:
    - Backend container

Silahkan buat docker-compose filenya, kemudian simpan dalam folder `tasks` dengan nama `docker-compose.yaml`

