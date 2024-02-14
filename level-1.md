# Level 1

<h6>Link YouTube: https://youtu.be/3ClY98oVbQI</h6>
<p>Disclaimer: vidio di youtube sudah dibuat sesingkat mungkin jadi bisa saja ada perbedaan command, tetapi tujuannya tetap satu yaitu menyelesaikan level ini</p>
<br>

Berikut ini dokumentasi pengerjaan level 1:

1.  Apa yang harus dikerjakan?
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
    <br>
        <b>Langkah-langkah di github</b>

        Kunjungi <a href='github.com'>Github.com<a/>

        Klik 'New'

    ![New Button](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/new.png)

        Repository name diisi sesuai format seperti ajk-riyan-penugasan1

    ![Repo Name](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/repo-name.png)

        Atur ke private, setelah itu klik 'Create repository'

    ![Create Repo](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/create-repo.png)

    <br>
    <br>
        <b>Langkah-langkah di file explorer</b>

        Buat folder di 'working directory'/local folder dan rename sesuai format seperti ajk-riyan-penugasan1

    ![Working Directory](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/working-dir.png)

        Setelah itu buat file dan folder seperti struktur di bawah ini

    ![Folder Structure](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/general/folder-structure.png)

        Setelah itu buka vs code di directory tersebut

2.  Implementasikan penggunaan branching yang terdiri dari master, development, featureA, dan featureB. Codebase dibebaskan.
    <br>
    <br>
    <b>Langkah-langkah di vscode:</b>

        Buka terminal vscode (lihat menu 'Terminal' dan pilih 'New Terminal') atau melalui shortcut Ctrl+Shift+~

        Ketik 'git init'

    ![Git Init](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-init.png)

        Copy remote yang ada di github dan paste ke terminal vscode

    ![Git Remote](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/development/git-remote-terminal.png)

    <br>
    <br>
        <b>Implementasi ke branch development:<b>

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
    <br>
        <b>Implementasi ke branch feature/login:</b>

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
    <br>
        <b>Implementasi ke branch feature/register:</b>

        Ketik 'git checkout --orphan feature/register' untuk membuat branch baru tanpa membawa commit history dari branch manapun

    ![git-checkout-feature-register](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-checkout-feature-register.png)

        Ketik 'git reset --hard' untuk menghapus file-file yang ada di dalam staging area, untuk menghapus file yang berada di working directory tinggal dihapus manual, lalu add filenya juga secara manual

    ![git-reset-hard](https://github.com/Rycs123/ajk-riyan-penugasan1/blob/development/src/img/featureRegister/git-reset-hard.png)

        Setelah itu tambahkan file index.html ke dalam staging area lalu commit dengan cara ketik 'git add .\src\index.html' dan 'git commit -m "Add file index.html"'

        Lalu dipush, dengan cara ketik 'git push --set-upstream origin feature/register'

    ![git-add-commit-push-file-index-html.png](src/img/featureRegister/git-add-commit-push-file-index-html.png)

        Lalu tambahkan file register.html ke dalam staging area dan commit menggunakan conventional commit message

    ![git-add-commit-register](src/img/featureRegister/git-add-commit-register.png)

        Setelah itu push dengan cara ketik 'git push'

    ![git-push](src/img/featureRegister/git-push.png)

        Setelah itu perhatikan apakah ada folder/file lain selain index.html dan login.html, jika ada hapus saja karena jika tidak dihapus maka akan ada semacam peringatan untuk menghapus(file/folder tersebut) sebelum switch branch
