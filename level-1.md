# Level 1

Link YouTube: https://youtu.be/3ClY98oVbQI

Disclaimer: vidio di youtube sudah dibuat sesingkat mungkin jadi bisa saja ada perbedaan command, tetapi tujuannya tetap satu yaitu menyelesaikan level ini

Berikut ini dokumentasi pengerjaan level 1:

## Daftar Isi atau Pertanyaan

-   [1. Apa yang harus dikerjakan?](#1-apa-yang-harus-dikerjakan)
-   [2. Implementasikan penggunaan branching yang terdiri dari master, development, featureA, dan featureB. Codebase dibebaskan.](#2-implementasikan-penggunaan-branching)
-   [3. Implementasikan intruksi git untuk push, pull, stash, reset, diff, dan merge. Adanya tambahan intruksi git selain yang disebutkan akan lebih baik.](#3-implementasikan-intruksi-git)
-   [4. Implementasikan sebuah penanganan conflict di branch development ketika setelah merge dari branch featureA lalu merge dari branch featureB. Catatan: conflict bisa terjadi jika kedua branch mengerjakan di file dan line code yang sama. Buatlah skenario sendiri.](#4-implementasikan-sebuah-penanganan-conflict-di-branch-development-ketika-setelah-merge-dari-branch-featureA-lalu-merge-dari-branch-featureB)
-   [5. Gunakan merge no fast forward.](#5-gunakan-merge-no-fast-forward)
-   [6. Kendala atau kesulitan](#kendala-atau-kesulitan)

<br>

### 1. Apa yang harus dikerjakan?

Buat sebuah repository di GitHub. Nama repository dalam format ajk-[nama panggilan]-penugasan1. Repository ini juga sebagai tempat menaruh laporan pengerjaan untuk level selanjutnya.

Contoh: ajk-nur-penugasan1

Struktur:

/src (Berisi kode pengerjaan level 1 kalian)

README.md (Readme utama)

level-1.md (Laporan level 1)

level-2.md (Laporan level 2)

level-3.md (Laporan level 3)

level-4.md (Laporan level 4)

<br>

#### Langkah-langkah di github

Kunjungi github.com

Klik 'New'

![New Button](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/new.png)

Repository name diisi sesuai format seperti ajk-riyan-penugasan1

![Repo Name](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/repo-name.png)

Atur ke private, setelah itu klik 'Create repository'

![Create Repo](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/create-repo.png)

<br>

#### Langkah-langkah di file explorer

Buat folder di 'working directory'/local folder dan rename sesuai format seperti ajk-riyan-penugasan1

![Working Directory](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/working-dir.png)

Setelah itu buat file dan folder seperti struktur di bawah ini

![Folder Structure](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/folder-structure.png)

Setelah itu buka vs code di directory tersebut

<br>

### 2. Implementasikan penggunaan branching

<br>

#### Langkah-langkah di vscode:

Buka terminal vscode (lihat menu 'Terminal' dan pilih 'New Terminal') atau melalui shortcut Ctrl+Shift+~

Ketik 'git init'

![Git Init](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-init.png)

Copy remote yang ada di github dan paste ke terminal vscode

![Git Remote](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-remote-terminal.png)

<br>

#### Implementasi ke branch development:

Buat branch development terlebih dahulu dengan cara ketik 'git branch -M development'

![Git Branch Development](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-branch-development.png)

Tambahkan semua file bertipe MD dengan cara ketik 'git add \*.md'

![Git Add All MD Type](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-all-md-ext.png)

Commit file yang sudah diadd ke dalam staging area dengan cara ketik 'git commit -m "initial commit"'

![Git Commit Initial Commit](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-commit-inital-commit.png)

![Git Graph After Initial Commit](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-graph-after-initial-commit.png)

Setelah itu dipush dengan cara ketik 'git push --set-upstream origin development'

![Git Push SetUpstream Origin Development](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-push--set-upstream-origin-development.png)

Setelah itu, tambahkan file app.css ke dalam staging area dengan cara ketik 'git add .\src\css\app.css'

Dan commit dengan cara ketik 'git commit -m "Add file app"'

![Git Add and Commit App](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-and-commit-app-css.png)

Jika ingin mengubah commit terakhir, ketik 'git commit --amend -m "Add file app.css"'

![Git Commit Amend App Css](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-and-commit-app-css.png)

Jika ingin membatalkan commit dan menyimpan perubahan dalam working directory, ketik 'git reset --soft HEAD^'

![Git Reset Soft HEAD](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-reset-commit-app-css.png)

Pesan yang dicommit akan hilang

Add kembali file app.css seperti sebelumnya

Lalu jika ingin melihat status (apa yang kurang dan apa yang sudah dilakukan), ketik git status

![Git status](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-status-app-js.png)

Hanya sebagai ilustrasi saja

Setelah itu commit ulang dengan commit message yang sama dan push

![Commit and Push App JS](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-commit-push-add-file-app-js.png)

Hanya ilustrasi saja walaupun filenya berbeda

<br>

#### Implementasi ke branch feature/login:

Ketik 'git checkout --orphan feature/login' untuk membuat branch baru tanpa membawa commit history dari branch manapun

![Git Checkout FeatLogin](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-checkout--orphan-feature-login.png)

Ketik 'git reset --hard' untuk menghapus file-file yang ada di dalam staging area, untuk menghapus file yang berada di working directory tinggal dihapus manual, lalu add filenya juga secara manual

![Git Reset Hard At FeatLogin](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-reset--hard.png)

Setelah itu tambahkan file index.html ke dalam staging area lalu commit dengan cara ketik 'git add .\src\index.html' dan 'git commit -m "Add file index.html"'

![Git Add Index At FeatLogin](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-add-index-html.png)

![Git Push Index At FeatLogin](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-push-index-html.png)

Lalu dipush

![Git Push SetUps At FeatLogin](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-push-set-ups-featLogin.png)

![git graph after push index](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-graph-after-push-index.png)

Lalu tambahkan file login.html ke dalam staging area dan commit menggunakan conventional commit message

![git-add-login-html](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-add-login-html.png)

![git-commit-feat-login](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-commit-feat-login.png)

Setelah itu push dengan cara ketik 'git push'

Setelah itu perhatikan apakah ada folder/file lain selain index.html dan login.html, jika ada hapus saja karena jika tidak dihapus maka akan ada semacam peringatan untuk menghapus(file/folder tersebut) sebelum switch branch

<br>

#### Implementasi ke branch feature/register:

Ketik 'git checkout --orphan feature/register' untuk membuat branch baru tanpa membawa commit history dari branch manapun

![git-checkout-feature-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-checkout-feature-register.png)

Ketik 'git reset --hard' untuk menghapus file-file yang ada di dalam staging area, untuk menghapus file yang berada di working directory tinggal dihapus manual, lalu add filenya juga secara manual

![git-reset-hard](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-reset-hard.png)

Setelah itu tambahkan file index.html ke dalam staging area lalu commit dengan cara ketik 'git add .\src\index.html' dan 'git commit -m "Add file index.html"'

Lalu dipush, dengan cara ketik 'git push --set-upstream origin feature/register'

![git-add-commit-push-file-index-html.png](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-add-commit-push-file-index-html.png)

Lalu tambahkan file register.html ke dalam staging area dan commit menggunakan conventional commit message

![git-add-commit-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-add-commit-register.png)

Setelah itu push dengan cara ketik 'git push'

![git-push](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-push.png)

Setelah itu perhatikan apakah ada folder/file lain selain index.html dan login.html, jika ada hapus saja karena jika tidak dihapus maka akan ada semacam peringatan untuk menghapus(file/folder tersebut) sebelum switch branch

<br>

#### Implementasi ke branch master:

git checkout --orphan master

![git-checkout--orphan-master](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/master/git-checkout--orphan-master.png)

git merge development

![git-merge-dev](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/master/git-merge-dev.png)

setelah itu lakukan sedikit perubahan di file README

![edit-readme](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/master/edit-readme.png)

tambahkan ke staging area, commit, dan push

![git-add](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/master/git-add.png)

![git-commit-push](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/master/git-commit-push.png)

<br>

### 3. Implementasikan intruksi git

<br>

-   git stash

    git stash memiliki banyak manfaat seperti menyimpan perubahan tanpa membuat commit, beralih branch tanpa komit, mengatasi konflik saat pull, dan pembersihan working directory

    contoh penggunaan git stash

    sebelum ketik git stash saya delete suatu script (lebih jelasnya bisa dilihat di gambar)

    ![before use stash](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/before-git-stash.png)

    setelah ketik git stash, apa yang saya delete akan kembali

    ![after use stash](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/after-git-stash.png)

    jadi siapapun dapat berpindah branch untuk melakukan commit atau yang lainnya

    jika ingin kembali, tinggal ketik git stash pop

    ![stash pop](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-stash-pop.png)

-   git push --force-with-lease

    perintah yang digunakan untuk memaksa push ke remote repository tanpa menghancurkan perubahan yang telah dilakukan oleh kontributor lain. Perintah ini aman digunakan ketika Anda ingin memperbarui remote repository dengan perubahan lokal Anda, tetapi Anda ingin memastikan bahwa Anda tidak menimpa perubahan yang telah ada di remote repository oleh kontributor lain.

    bisa lihat gambar di bawah ini, di sebelah kanan merupakan akun saya yang lain (bukan RYCS123) dan di sebelah kiri merupakan history commit yang terjadi di branch development

    ![before-git-push-force](<https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-push-force(1).png>>)

    Bisa dilihat saat saya ketik git commit --amend, melakukan sedikit perubahan, dan menyimpannya

    Lalu saya coba ketik git log untuk melihat commit history yang terjadi

    Setelah itu coba fokus pada commit hash keduanya maka yang di sebelah kanan akan berubah

    Lalu coba ketik git push seharusnya akan terjadi error

    Jadi gimana cara untuk menangani error tersebut? Ketik git push --force-with-lease

    ![git-push-force-apply](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-push-force-apply.png)

    Setelah itu refresh webnya dan liat commit hashnya bakalan berubah dan sama

    ![git-push-force-refresh](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-push-force-refresh.png)

-   git pull

    jika bekerja dalam tim atau yang berkontribusi lebih dari satu orang di sebuah repo, maka perintah ini sangat berguna untuk menarik perubahan-perubahan yang sudah dilakukan oleh kontributor lain

    misal contributor lain sudah ngepush suatu perubahan ke branch development

    lalu saya ingin mendapatkan perubahan (push) dari contributor lain, ketik git pull

    ![git-pull](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-pull.png)

-   git diff

    digunakan untuk melihat perbedaan antara dua keadaan dalam repositori Git. Ini dapat digunakan untuk melihat perubahan yang belum di-commit (perubahan yang belum di-staging) atau perubahan antara dua commit tertentu.

    misal saya mempunyai source code seperti di bawah ini

    ![git-diff-before-change-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-diff-before-change-register.png)

    lalu saya menambahkan huruf random dan ingin melihat perbedaannya, ketik git diff

    ![git-diff-usage-before-and-after-change](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-diff-usage-before-and-after-change.png)

-   git reflog

    ![git-reflog](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-reflog.png)

-   git log

    ![git-log](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-log.png)

-   git log --oneline

    ![git-log--oneline](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-log--oneline.png)

-   git checkout <branch_name>

    perintah di atas dapat membuat kita berpindah pindah cabang, tapi ada juga kegunaan lainnya

    ![git-checkout-development](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-checkout-development.png)

    ![git-checkout-feature-login](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-checkout-feature-login.png)

    ![git-checkout-feature-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-checkout-feature-register.png)

-   git checkout <commit_hash>

    jika kita ingin mengambil code yang sudah dicommit sebelumnya (di masa lalu), ketik perintah di atas

    ![git checkout with commit-hash](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/git-checkout-commit-hash-past.png)

    jika ingin kembali ke commit terbaru caranya juga sama tinggal ganti commit hashnya dengan yang baru

-   git reset

    jika ingin membatalkan apa yang ditambakan ke staging area, ketik git reset

    digunakan untuk mengubah history commit, oleh karena itu, perlu digunakan dengan hati-hati.

    ![git-add](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add.png)

    ![git-reset](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-reset.png)

-   git reset --soft

    jika ingin membatalkan commit terakhir, tetapi masih tetap ingin mempertahankan file yang ada di working directory

    ![git-reset-commit-app-css](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-reset-commit-app-css.png)

-   git reset --hard

    jika ingin membatalkan commit terakhir dan ingin membuang file yang ada di working directory

    ![git-reset-hard](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-reset-hard.png)

-   git branch

    perintah di atas dapat menampilkan branch apa saja yang ada dan posisi saya ada di branch mana

    ![git-brancht](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-branch.png)

-   git restore --staged <file>

    digunakan untuk mengembalikan perubahan dari staging area ke direktori kerja.

    tidak mengubah history commit dan hanya mempengaruhi keadaan staging area dan direktori kerja.

    ![git-restore-staged](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-restore-staged.png)

### 4.Implementasikan sebuah penanganan conflict di branch development ketika setelah merge dari branch featureA lalu merge dari branch featureB

<br>

git merge --no-ff <branch_name>

git merge --no-ff <branch_name> -m "commit message"

Setelah saya mencoba perintah di atas dengan branch feature/login, saya menemukan error

![git-merge-no-ff-feat-login-m](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-merge-no-ff-feat-login-m.png)

Solusinya tambahin --allowed-unrelated-histories

![git-merge-no-ff-feat-login-allow-unrelated-histories](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-merge-no-ff-feat-login-allow-unrelated-histories.png)

setelah itu add ulang dan commit

![git-add-commit-merge-feat-login-into-development](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-commit-merge-feat-login-into-development.png)

lalu merge feature/register ke (branch) development dan akan muncul conflict

![git-merge-no-ff-feat-regist-allow-unrelated-histories-into-dev](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-merge-no-ff-feat-regist-allow-unrelated-histories-into-dev.png)

solusinya bisa accept current change, accept incoming change, accept both changes, atau mau dicompare (compare changes)

lalu add, commit, dan push

![git-add-commit-push-merge-index](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-commit-push-merge-index.png)

jangan lupa file register.html diadd, dicommit, dan dipush

![git-add-commit-push-merge-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-add-commit-push-merge-register.png)

### 5. Gunakan merge no fast forward

git merge --no-ff <branch_name>

git merge --no-ff <branch_name> -m "commit message"

Setelah saya mencoba perintah di atas, saya menemukan error

![git-merge-no-ff-feat-login-m](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-merge-no-ff-feat-login-m.png)

Solusinya tambahin --allowed-unrelated-histories

![git-merge-no-ff-feat-login-allow-unrelated-histories](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureLogin/git-merge-no-ff-feat-login-allow-unrelated-histories.png)

setelah itu add ulang, commit, dan push jika ingin ditambahkan ke dalam commit history

<br>

## Kendala atau kesulitan

sebenarnya saya sudah melakukan uji coba terlebih dahulu sebelum membuat vidio sekitar 10x record

saat uji coba, saya mencoba git checkout --orphan <branch_naame> dan sedikit bingung kenapa malah semuanya (file dan folder) logonya kembali jadi "U" atau working directory

kemudian saya mencoba memahami maksud perintah itu lalu saya pun mengerti ternyata file-filenya harus dihapus jika tidak ingin ada file tersebut di branch

lalu saya berpikir ingin pindah branch dalam kondisi ada file yang sudah dicommit dan masih ada yang di working directory, saya akhirnya mendapat semacam pemberitahuan bahwa file tersebut harus diremove atau dihapus

Sekian dari saya terima kasih
