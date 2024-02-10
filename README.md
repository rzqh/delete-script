# delete-script-ssh

## Cara Penggunaan

Clone repository delete-script-ssh
```bash
  git clone https://github.com/rzqh/delete-script-ssh.git
```

Pindah direktori ke direktori "delete-script-ssh"
```bash
  cd delete-script-ssh
```

Berikan hak akses execute pada file delete_files.sh dan eksekusi
```bash
  chmod +x delete_files.sh
  ./delete_files.sh
```

## Mekanisme script

- Memeriksa apakah semua file tersebut ada atau tidak menggunakan perulangan
- Jika file ada, hapus file tersebut dan tampilkan pesan berhasil dihapus
- Jika file tidak ada, tampilkan pesan error


## Tips
- Anda dapat menambahkan opsi -i ke perintah rm untuk mendapatkan konfirmasi sebelum menghapus file

## Peringatan
- Script tersebut menghapus secara permanen. Pastikan Anda tidak menghapus file yang krusial
- Jika Anda tidak yakin tentang file tersebut, Anda dapat meminta bantuan dengan bertanya ke komunitas atau membaca wiki dari OS yang digunakan

## Catatan
Script bash ini hanya menghapus file yang ada di direktori ```/usr/share/help```. Jika Anda ingin menghapus file yang ada di subdirektori, Anda perlu menggunakan opsi -r dengan perintah find.
Berikut contohnya:
```bash
    find /usr/share/help -name "*.docbook" -type f -exec rm -f {} \;
```
Perintah tersebut akan mencari semua file dengan ekstensi .docbook di direktori /usr/share/help dan subdirektorinya, kemduian akan terhapus semua file dengan ekstensi .docbook
