> Pelajari dengan menggunakan berbagai bahasa & lokasi [#23](https://github.com/anmol098/waka-readme-stats/issues/23)

# Metricas de Desenvolvimento no Readme com feature flags adicionáveis ​​🎌

![Pratinjau Proyek](https://user-images.githubusercontent.com/25841814/79395484-5081ae80-7fac-11ea-9e27-ac91472e31dd.png)

<p align="pusat">
  
  ![Pratinjau Proyek](https://user-images.githubusercontent.com/15426564/88030180-8e1c4780-cb58-11ea-8a8b-b3576dd73652.png)
  
  <h3 align="center">📌✨Incríveis Estatísticas no Readme</h3>
</p>

----

<p align="pusat">
   <img src="https://img.shields.io/badge/language-python-blue?style"/>
   <img src="https://img.shields.io/github/license/anmol098/waka-readme-stats"/>
   <img src="https://img.shields.io/github/stars/anmol098/waka-readme-stats"/>
   <img src="https://img.shields.io/github/forks/anmol098/waka-readme-stats"/>
   <img src="https://img.shields.io/static/v1?label=%F0%9F%8C%9F&message=If%20Useful&style=style=flat&color=BC4E99" alt="Lencana Bintang"/>
</p>
<p align="pusat">
   Você é diurno 🐤 ou noturno 🦉?
   <br/>
   Apakah Anda lebih produktif selama dia?
   <br/>
   Apakah Anda ingin menggunakan bahasa sebagai program Anda?
   <br/>
   Vamos ver isso em seu perfil!
</p>

<p align="pusat">
    <a href="https://github.com/anmol098/waka-readme-stats/issues">Laporkan Bug</a>
    ·
    <a href="https://github.com/anmol098/waka-readme-stats/issues">Permintaan Fungsi</a>
  </p>

## Configuração Previa

1. Anda benar-benar memperbarui arquivo markdown(.md) dengan 2 komentar. Verifique [aqui](#atualize-seu-readme) como fazer isso.
2. Anda perlu mengetahui Kunci API Anda untuk WakaTime. Anda dapat mencoba melakukan konfigurasi pada konten Wakatime
    - Você pode verificar [aqui](#novo-no-wakatime), caso seja novo no WakaTime
3. Anda perlu mengetahui Token API di GitHub dengan escopo de `repo` dan `user` yang dapat Anda temukan [aqui](https://github.com/settings/tokens) jika Anda menggunakan Tindakan untuk mengurangi sebagai metrik de berkomitmen
   > habilitar o escopo de `repo` parece **PERIGOSO**<br/>
   > Tindakan GitHub ini hanya akan mengakses data dan melakukan apa yang Anda lakukan dan saat kode ditambahkan atau dihapus dari repositori yang Anda kontribusikan.
   - Anda dapat menggunakan [esse](#perfil-do-repositório) contoh sebagai model
4. Anda hanya perlu menyimpan Kunci API dari Wakatime eo Token API dari GitHub tanpa menyimpan rahasia. Anda dapat menemukan konfigurasi dari repositori Anda. Sertifikat-se de salva-los sebagai kebanyakan tidak ada contoh abaixo.
    - Kunci API untuk WakaTime como `WAKATIME_API_KEY=<kunci API wakatime Anda>`
    - Token de Accesso Pessoal dari GitHub sebagai `GH_TOKEN=<token akses github Anda>`
5. Anda dapat mengaktifkan dan menonaktifkan sebagai bendera fitur berdasarkan kebutuhan Anda.


Essa Ação dijalankan setiap hari pada pukul 00.00 IST

## Atualisasikan Readme Anda

Tambahkan komentar igual ini ke `README.md`:

``` md
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->
```

Lini ini sering kali menjadi titik masuk untuk sebagai metrik pengembangan.

## Novo no WakaTime

WakaTime adalah ide tentang tempo yang benar-benar Anda butuhkan untuk program Anda. Anda harus memutuskan untuk meningkatkan produk Anda sendiri dan bukan pesaing Anda.

- Vá para <https://wakatime.com> dan menulis konten.
- Gunakan Kunci API untuk WakaTime di [Pengaturan Akun di WakaTime](https://wakatime.com/settings/account).
- Instal [plugin WakaTime](https://wakatime.com/plugins) bukan editor favorit / IDE Anda.
- Cole sua API key untuk memulai suas alálises.

### File Repositori

Anda akan diminta untuk [Token Akses GitHub](https://docs.github.com/en/actions/configuring-and-managing-workflows/authenticating-with-the-github_token) dengan cakupan `repo` dan `pengguna ` dan menyelamatkan tanpa Rahasia melakukan penyimpanan `GH_TOKEN = <Token Akses GitHub Anda>`

Ini adalah contoh dari arquivo dengan Workflow para executa-lo:

``` yml
nama: Waka Readme

pada:
  jadwal:
    # Berjalan pada jam 12 pagi IST
    - cron: '30 18 * * *'

pekerjaan:
  perbarui-baca:
    nama: Perbarui Readme dengan Metrik
    berjalan: ubuntu-terbaru
    Langkah:
      - kegunaan: anmol098/waka-readme-stats@master
        dengan:
          WAKATIME_API_KEY: ${{ rahasia.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ rahasia.GH_TOKEN }}
```
## Ekstra

1. Jika Anda ingin menambahkan informasi lain dari properti Anda, Anda dapat menambahkan beberapa `FLAGS` pada arsip alur kerja. Oleh padrão, todas as flags estão habilitadas
>Exceto a flag de linhas de códigos devido ao peso de your processamento

``` yml
- kegunaan: anmol098/waka-readme-stats@master
        dengan:
          WAKATIME_API_KEY: ${{ rahasia.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ rahasia.GH_TOKEN }}
          SHOW_OS: "Salah"
          SHOW_PROJECTS: "Salah"
```

### Bendera Disponíveis

---

`LOCALE` Bendera Essa dapat digunakan untuk sebagian besar sebagai aset di bahasa Anda sendiri, atau padrão é Inglês, gunakan Lokal [Forma Abreviada](https://saimana.com/list-of-country-locale-code/) untuk mengatribusikan ke variavel na flag. Sebagai contoh, hasil akhir dapat Anda lihat dengan mudah [aqui](https://github.com/anmol098/anmol098/blob/master/Readme-fr.md)


`SHOW_LINES_OF_CODE` flag ini dapat dikonfigurasi untuk `True` untuk menampilkan sebagian besar baris kode eskrip pada data aktual

![Linhas de Códigos](https://img.shields.io/badge/Desde%20o%20Hello%20World%20Eu%20Escrevi-1.3%20milhões%20de%20Linhas%20de%20Código-blue)

Bendera `SHOW_PROFILE_VIEWS` dapat dikonfigurasi untuk `False` untuk okultisme sebagai Vizualizações do File

![Vizualizações do Perfil](http://img.shields.io/badge/Vizualizações%20do%20Perfil-2189-blue)


Bendera `SHOW_COMMIT` dapat dikonfigurasikan untuk `False` untuk okultisme sebagai aset yang dilakukan

**Eu sou Diurno 🐤**
``` teks
🌞 Manhã 95 melakukan ███████░░░░░░░░░░░░░░░░░░ 30,55%
🌆 Tarde 78 melakukan ██████░░░░░░░░░░░░░░░░░░░ 25,08%
🌃 Noite 112 melakukan █████████░░░░░░░░░░░░░░░░ 36,01%
🌙 Madrugada 26 melakukan ██░░░░░░░░░░░░░░░░░░░░░░░ 8,36%

```

Bendera essa `SHOW_DAYS_OF_WEEK` dapat dikonfigurasikan untuk `False` untuk os okular melakukan feitos em berbeda dias da semana

📅 **Eu Sou Mais Produtivo aos Domingos**

``` teks
Segunda-Feira 50 melakukan ███░░░░░░░░░░░░░░░░░░░░░░ 13,19%
Terça-Feira 85 melakukan █████░░░░░░░░░░░░░░░░░░░░ 22,43%
Quarta-Feira 56 melakukan ███░░░░░░░░░░░░░░░░░░░░░░ 14,78%
Quinta-Feira 44 melakukan ███░░░░░░░░░░░░░░░░░░░░░░ 11,61%
Sexta-Feira 28 melakukan █░░░░░░░░░░░░░░░░░░░░░░░░ 7,39%
Sábado 30 melakukan ██░░░░░░░░░░░░░░░░░░░░░░░ 7,92%
Domingo 86 melakukan █████░░░░░░░░░░░░░░░░░░░░ 22,69%

```

Bendera `SHOW_LANGUAGE` dapat dikonfigurasikan untuk `False` untuk bahasa pemrograman yang Anda gunakan

``` teks
💬 Bahasa Programação:
JavaScript 5 jam 26 menit ███████████████░░░░░░░░░░ 61,97%
PHP 1 jam 35 menit ████░░░░░░░░░░░░░░░░░░░░░ 18,07%
Penurunan harga 1 jam 9 menit ███░░░░░░░░░░░░░░░░░░░░░░ 13,3%
Python 22 menit █░░░░░░░░░░░░░░░░░░░░░░░░ 4,32%
XML 8 menit ░░░░░░░░░░░░░░░░░░░░░░░░░ 1,62%
```


Bendera `SHOW_OS` dapat dikonfigurasi untuk `False` untuk detail sistem operasi

``` teks
💻 Sistem Operasi:
Windows 8 jam 46 menit █████████████████████████ 100,0%
```

Bendera `SHOW_PROJECTS` dapat dikonfigurasi untuk `False` untuk Proyek okultisme yang akan Anda kerjakan

``` teks
🐱‍💻 Proyek:
ctx_connector 4 jam 3 menit ███████████░░░░░░░░░░░░░░ 46,33%
NetSuite-Connector 1 jam 31 menit ████░░░░░░░░░░░░░░░░░░░░░ 17,29%
manga-web-master 1 jam 12 menit ███░░░░░░░░░░░░░░░░░░░░░░ 13,77%
kabel 54 menit ██░░░░░░░░░░░░░░░░░░░░░░░ 10,41%
denAPI 40 menit ██░░░░░░░░░░░░░░░░░░░░░░░ 7,66%
```

`SHOW_TIMEZONE` bendera ini dapat dikonfigurasikan untuk `False` untuk menyembunyikan atau menampilkan horor yang Anda inginkan

``` teks
⌚︎ Fuso horário: America/Sao_Paulo
```

Bendera essa `SHOW_EDITORS` dapat dikonfigurasi untuk `False` untuk editor kode yang digunakan

``` teks
🔥 Editor:
WebStorm 6 jam 47 menit ███████████████████░░░░░░ 77,43%
PhpStorm 1 jam 35 menit ████░░░░░░░░░░░░░░░░░░░░░ 18,07%
PyCharm 23 menit █░░░░░░░░░░░░░░░░░░░░░░░░ 4,49%
```

Bendera `SHOW_LANGUAGE_PER_REPO` dapat dikonfigurasi untuk `False` untuk okultisme atau nomor repositori dengan bahasa dan kerangka kerja yang berbeda

**Eu geralmente programo em Vue**

``` teks
Vue 8 repo ██████░░░░░░░░░░░░░░░░░░░ 25,0%
Java 6 repo ████░░░░░░░░░░░░░░░░░░░░░ 18,75%
JavaScript 6 repo ████░░░░░░░░░░░░░░░░░░░░░ 18,75%
PHP 3 repo ██░░░░░░░░░░░░░░░░░░░░░░░ 9,38%
Python 2 repo █░░░░░░░░░░░░░░░░░░░░░░░░ 6,25%
Dart 2 repo █░░░░░░░░░░░░░░░░░░░░░░░░ 6,25%
Repo CSS 2 █░░░░░░░░░░░░░░░░░░░░░░░░ 6,25%

```

`SHOW_SHORT_INFO` bendera ini dapat dikonfigurasi untuk `False` untuk informasi kecil tentang pengguna
>Essa seção requer um token pessoal de accesso com permissão de usuário, caso contrário, os dados mostrados aqui estarão incorretos

**🐱 Meus Dados no GitHub**

> 🏆 433 Kontribusi no ano de 2020
 >
> 📦 Gunakan 292,3 kB di GitHub
 >
> 💼 Aberto para contratação
 >
> 📜 25 Repositórios Públicos
 >
> 🔑 15 Repositori Pribadi

Bendera `SHOW_LOC_CHART` dapat dikonfigurasikan untuk `False` untuk mata karena baris kode ditulis pada trimestres yang berbeda dari yang lain

**Linha do Tempo**

![Gráfico não Encontrado](https://raw.githubusercontent.com/anmol098/anmol098/master/charts/bar_graph.png)

## :sparkling_heart: Apoie o Projeto

Saya menggunakan kode ini untuk menjadi apa pun yang saya miliki, dan saya cenderung menjawab semua yang saya anggap tepat untuk menggunakan proyek ini. Tentu saja ini membutuhkan tempo. Anda dapat menggunakan layanan ini secara gratis.

Entretanto, jika Anda menggunakan proyek ini dan menikmatinya dengan senang hati atau apa yang membuat saya memberi insentif untuk solusi berkelanjutan, dengan beberapa cara yang dapat Anda lakukan:-

- Dando credits a mim whendo usar essa ação no seu readme, and linkando-o de volta to esse repositório :D
- Dando uma star e compartilhando o projeto :roket:
- [![paypal.me/aapreneur](https://ionicabizau.github.io/badges/paypal.svg)](https://www.paypal.me/aapreneur) - Anda dapat melakukan banyak hal melalui PayPal. Eu provávelmente irei comprar ~~cerveja~~ vinho 🍷

Wajib! :jantung:

---

# Kontribusi

Contributed são bem vidas! ♥! Silakan bagikan fungsi apa pun dan tambahkan perangkat testis! Gunakan sistem permintaan tarik dan terbitkan untuk berkontribusi.

# Kontributor Selecionados

1. [Anmol Pratap Singh](https://github.com/anmol098): Mantenedor
2. [Prabhat Singh](https://github.com/prabhatdev): Pelo gráfico de linha do tempo de código [#18](https://github.com/anmol098/waka-readme-stats/pull/18 )
3. [Hedy Li](https://github.com/hedythedev): Pelo Pull Request [#34](https://github.com/anmol098/waka-readme-stats/pull/34) e [#23 ](https://github.com/anmol098/waka-readme-stats/pull/23)
4. [Pedro Torres](https://github.com/Corfucinas): Permintaan Tarik Pelo [#29](https://github.com/anmol098/waka-readme-stats/pull/29)
5. [Aaron Meese](https://github.com/ajmeese7): Pelo Pull Request [#45](https://github.com/anmol098/waka-readme-stats/pull/45)
6. [Arnav Jindal](https://github.com/Daggy1234): Pelo Pull Request [#48](https://github.com/anmol098/waka-readme-stats/pull/48)
7. [Daniel Rowe](https://github.com/DanRowe): Pelo Pull Request [#57](https://github.com/anmol098/waka-readme-stats/pull/57)
8. [Ss5h](https://github.com/tlatkdgus1): Untuk tambahan dukungan eskrita de frase alami untuk tradução [#136](https://github.com/anmol098/waka-readme-stats/pull/ 136)

<detail>
<summary>Menção especial for aqueles que estão deixando seus readmes more incríveis :smile: :tada:</summary>

  - [Stanislas](https://github.com/angristan)
  
  - [Pratik Kumar](https://github.com/pr2tik1)
  
  - [Vladimir](https://github.com/sergeev-vn)

  - [Pedro Torres](https://github.com/Corfucinas)
  
  - [leverglowh](https://github.com/leverglowh)
  
  - [patdc](https://github.com/patdc)
  
  - [极客挖掘机](https://github.com/meteor1993)
  
  - [Fan()](https://github.com/Fanduzi)
  
  - [Miller Camilo Vega](https://github.com/minoveaz)
  
  - [XLor](https://github.com/yjl9903)
  
  - [Jesse Okeya](https://github.com/jesseokeya)
  
  - [aniel](https://github.com/anaiel)
  
  - [Dipto Mondal](https://github.com/diptomondal007)
  
  - [Jerry F. Zhang](https://github.com/JerryFZhang)
  
  - [Karan Singh](https://github.com/karan06126)
  
  - [Erwin Lejeune](https://github.com/guilyx)
  
  - [Manuel Cepeda](https://github.com/mecm1993)
  
  - [Jonathan S](https://github.com/TGTGamer)
  
  - [Tsotne Gvadzabia](https://github.com/RockiRider)
  
  - [Miray](https://github.com/MirayXS)
  
  - [Varad Patil](https://github.com/varadp2000)
  
  - [Prabhat Singh](https://github.com/prabhatdev)
  
  - [Nikhil](https://github.com/nikhilgorantla)
  
  - [大白](https://github.com/2720851545)
  
  - [Du Yizhuo](https://github.com/dyzdyz010)
  
  - [Manas Talukdar](https://github.com/manastalukdar)
  
  - [Simranjeet Singh](https://github.com/smrnjeet222)
  
  - [Aaron Meese](https://github.com/ajmeese7)
  
  - [Prasad Narkhede](https://github.com/p014ri5)
  
  - [Manish Kushwaha](https://github.com/tzmanish)
  
  - [Hedy Li](https://github.com/hedythedev)
  
  - [SHIMIZU Taku](https://github.com/takuan-osho)
  
  - [Jude Wilson](https://github.com/mr-winson)
  
  - [Daniel Rowe](https://github.com/DanRowe)
  
  - [Muhammad Hassan Ahmed](https://github.com/hassan11196)
  
  - [Alessandro Maggio](https://github.com/Tkd-Alex)
  
  - [Siddharth Gupta](https://github.com/siddg97)
  
  - [Dev-Mehta](https://github.com/Dev-Mehta/)
  
  - [> EdgyCoder ✌](https://github.com/edgycoder)
  
  - [> EdgyCoder ✌](https://github.com/edgycoder)
  
  - [Korel Kashri](https://github.com/korelkashri)
  
  - [Gustavo Barbosa](https://github.com/gusbdev)

  - [eagleanurag](https://github.com/eagleanurag)
  
  - [Aravind V. Nair](https://github.com/aravindvnair99)
  
  - [Raman Preet Singh](https://github.com/raman08)
  
  - [Hayat Tamboli](https://github.com/hayat-tamboli)
  
  - [Henry Boisdequin](https://github.com/henryboisdequin)
   
  - [Raman Preet Singh](https://github.com/raman08)

  

</detail>

- Kamu! Caso esteja usando isso agora e seu nome não esteja na lista, por favor contacte-nos envirando um [Menção Especial](https://github.com/anmol098/waka-readme-stats/issues/new/choose) issue :blush : Tidak ada ficaremos gratis untuk menambahkan daftar Anda.


Feito com :heart: e Python 🐍.

#Inspirado por

> [Inti Pinned yang Keren](https://github.com/matchai/awesome-pinned-gists) <br/>
> [athul/waka-readme](https://github.com/athul/waka-readme)

### Esse projeto precisa de uma **star** ⭐ sua ♥.
