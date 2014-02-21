REPO_LOMBA
==========

REPO_LOMBA DIES NATALIS STMIK ADHIGUNA 2013
Mempersiapkan repositori lokal
instal git

[1] Buka terminal emulator favorit Anda (Konsole, {gnome|mate}-terminal, xterm, or whatever) jika windows menyesuaikan.

[2] Clone repositori  ke repositori lokal.

    $ git clone https://github.com/Adhi-Guna-Lomba/REPO_LOMBA.git


[3] Setelah proses cloning selesai, akan muncul direktori baru, yaitu REPO_LOMBA.
[4] Yes! Repositori lokal sudah siap :)

Mengajukan perubahan di repositori online

    Setiap kontributor punya akses ke branch master. Tapi, percayalah, jangan bermain di branch master jika tidak ingin galau di kemudian hari. -Anonim


Jika Anda ingin mengubah, entah itu menambah atau mengurangi isi repositori online, manfaatkanlah fitur cantik bernama Pull Request.

[1] Buka kembali terminal emulator dan pindah ke repositori lokal.

    $ cd REPO_LOMBA


[2] [Penting] Selalu refresh repositori lokal sebelum melakukan langkah selanjutnya (branching).

    $ git pull


[3] Buat branch baru. Nama branch sebaiknya menggambarkan sesuatu yang ingin Anda lakukan/ajukan. Misalnya Anda ingin menambahkan Aplikasi, maka branch baru yang akan Anda buat bisa dinamai dengan Aplikasi anda.

    $ git checkout -b FOLDER_APLIKASI_LOMBA


Sebuah branch baru akan terbentuk dan otomatis Anda langsung siap bekerja di branch tersebut. Untuk memastikannya, cek daftar branch yang ada di repositori.

    $ git branch


Tanda bintang di output menandakan "tempat kerja" Anda.

[4] Lakukan perubahan (mengedit, menambah, menghapus, dsb). Setelah selesai, cek file-file yang diubah dengan perintah "git status".

    $ git status
    # On branch FOLDER_APLIKASI_LOMBA
    # Changes not staged for commit:
    #   (use "git add <file>..." to update what will be committed)
    #   (use "git checkout -- <file>..." to discard changes in working directory)
    #
    #    modified:   main.cpp
    #
    # Untracked files:
    #   (use "git add <file>..." to include in what will be committed)
    #
    #    DOCS.html
    no changes added to commit (use "git add" and/or "git commit -a")
    </file></file></file>


Terlihat bahwa Anda telah memodifikasi  file "Sesuai yang anda modif" contah "main.cpp" dan menambahkan file "DOCS.html".

Catatan: untuk menghapus file/direktori yang sudah ada sebelumnya, jangan gunakan

    $ rm -rf namadirektori/


tapi

    $ git rm -rf namadirektori/


sehingga perubahan tersebut nantinya bisa terekam.

[5] Pindahkan file yang telah Anda ubah ke staging area. Staging area adalah "ruang tunggu" sebelum perubahan-perubahan dimasukkan ke repositori.

    $ git add FOLDER_APLIKASI_LOMBA DOCS.html


Catatan:
* File-file yang dihapus dengan "git rm" otomatis akan masuk staging area.
* Usahakan untuk memasukkan perubahan-perubahan sejenis/dengan topik yang sama. Jika Anda mengubah beberapa file namun dengan topik yang berbeda, lebih baik bergantian (untuk memudahkan proses review dan koreksi)
* [Penting] Usahakan untuk hanya memindahkan perubahan-perubahan yang telah Anda lakukan sendiri. Jadi, jangan lakukan

    $ git add *


untuk menghindari pemindahan perubahan-perubahan yang tidak sengaja Anda lakukan.

[6] Masukkan perubahan-perubahan dari staging area ke repositori menggunakan perintah "git commit" disertai pesan commit yang sesuai.

    $ git commit -m "Nama Aplikasi Anda"


[7] Lakukan perubahan-git add-git commit sesuai keinginan. Jika dirasa cukup, segera unggah branch FOLDER_APLIKASI_LOMBA ke repositori online.

    $ git push origin FOLDER_APLIKASI_LOMBA   <-- Sesuaikan Dengan yang anda buat


[8] Buka repositori LOMBA di browser. Branch yang telah Anda unggah sebelumnya akan muncul dan siap untuk di "Pull Request". Tekan tombol hijau (deket dropdown branch). Untuk base, pilih master, sedangkan untuk compare pilih FOLDER_APLIKASI_LOMBA . Tekan "Turn this comparison into pull request" (or something like that, aku lupa). Masukkan judul dan deskripsi yang sesuai dengan perubahan yang ingin Anda ajukan, kemudian tekan "Send this pull request".

Catatan:
* Kontributor tidak diperkenankan menekan tombol Close atau Merge. Jadi jangan pernah ditekan :p

Tips:
* Perubahan yang sudah diajukan sebagai pull request masih bisa diubah lagi (misalnya ada koreksi atau penambahan). Prosesnya sama, dari nomor [4] s.d. nomor [7].

[9] Jika maintainer sudah menutup pull request (statusnya merged/closed), silakan hapus branch FOLDER_APLIKASI_LOMBA di repositori lokal dengan cara berpindah dahulu ke branch master.

    $ git checkout master
    $ git branch -D FOLDER_APLIKASI_LOMBA


[10] Refresh repositori lokal

    $ git pull


[11] Selesai!
