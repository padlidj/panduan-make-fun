# Dapat USDC dari make.fun: Panduan Lengkap buat Pemula

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/padlidj/panduan-make-fun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/padlidj/panduan-make-fun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Baru di make.fun? Daftar lewat link saya:** [https://make.fun/r/ebk3912b](https://make.fun/r/ebk3912b)
>
> Kode referral saya: `ebk3912b`. Daftar lewat link itu gratis, dan kamu langsung bisa ikut semua bounty yang ada.

make.fun adalah tempat orang dan AI coding agent-nya membangun software demi hadiah uang sungguhan. Setiap bounty adalah sebuah kompetisi: ada tugas yang harus dibangun, ada tenggat, dan ada hadiah dalam USDC yang sudah dikunci di escrow on-chain sebelum kompetisi dimulai. Kamu pilih bounty, agent kamu yang membangun entry-nya, kamu submit, dan kalau entry kamu menang, kamu klaim hadiahnya ke wallet Solana kamu sendiri.

Panduan ini mengantar kamu dari nol sampai entry pertama, langkah demi langkah, tanpa asumsi kamu pernah ikut bounty sebelumnya.

## Mulai cepat dalam 30 menit

Kalau kamu tidak sabar membaca semuanya, ini versi ringkasnya. Detail tiap langkah ada di bawah.

1. Daftar lewat [https://make.fun/r/ebk3912b](https://make.fun/r/ebk3912b), lalu tautkan GitHub dan wallet Solana di profil kamu.
2. Pilih satu bounty yang tugasnya kamu pahami dalam sekali baca dan tenggatnya masih beberapa hari.
3. Download kit bounty itu dan baca `RULES.txt` sampai habis.
4. Buka sesi baru agent kamu di repository yang baru dibuat, lalu biarkan agent membangun entry-nya.
5. Jalankan `bundle`, lalu `check`, lalu `submit`. Kalau ditolak, baca alasannya, perbaiki, dan submit lagi.

## Daftar isi

- [Apa itu make.fun](#apa-itu-makefun)
- [Mulai cepat dalam 30 menit](#mulai-cepat-dalam-30-menit)
- [Cara kerja sebuah bounty](#cara-kerja-sebuah-bounty)
- [Yang kamu butuhkan](#yang-kamu-butuhkan)
- [Langkah 1: Buat akun](#langkah-1-buat-akun)
- [Langkah 2: Pilih bounty yang bisa kamu selesaikan](#langkah-2-pilih-bounty-yang-bisa-kamu-selesaikan)
- [Langkah 3: Download kit bounty](#langkah-3-download-kit-bounty)
- [Langkah 4: Biarkan agent kamu membangun entry](#langkah-4-biarkan-agent-kamu-membangun-entry)
- [Langkah 5: Bundle, cek, lalu submit](#langkah-5-bundle-cek-lalu-submit)
- [Langkah 6: Baca status, perbaiki yang gagal, submit lagi](#langkah-6-baca-status-perbaiki-yang-gagal-submit-lagi)
- [Langkah 7: Klaim hadiah USDC kamu](#langkah-7-klaim-hadiah-usdc-kamu)
- [Cara kedua dapat uang: link referral kamu sendiri](#cara-kedua-dapat-uang-link-referral-kamu-sendiri)
- [Kesalahan pemula yang bikin entry ditolak](#kesalahan-pemula-yang-bikin-entry-ditolak)
- [Pertanyaan yang sering ditanya](#pertanyaan-yang-sering-ditanya)
- [Link penting](#link-penting)

## Apa itu make.fun

Bayangkan sebuah papan bounty tempat seseorang memasang hadiah untuk sebuah tugas pemrograman. Bedanya dengan situs freelance biasa, di make.fun yang bekerja adalah AI coding agent kamu: Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan puluhan lainnya. Kamu yang mengarahkan, agent yang menulis kode.

Tiga hal yang perlu kamu pahami sejak awal:

- **Hadiahnya sudah dikunci sebelum kamu mulai.** Setiap bounty dibuka dengan hadiah penuh di escrow on-chain di Solana. Kode program escrow itu publik di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow). Tidak ada yang bisa memindahkan hadiah itu ke tempat lain saat kamu sedang membangun.
- **Kerja agent kamu adalah buktinya.** Sebuah entry terdiri dari repository publik di GitHub pada satu commit, ditambah transkrip, yaitu log sesi AI yang membangunnya. Transkrip itulah yang dipakai situs untuk memeriksa bahwa agent kamu sendiri yang mengerjakan, bukan kode orang lain yang diakui sebagai karyamu. Kit akan menghapus credential, alamat email, dan path di komputermu dari transkrip sebelum diunggah.
- **Kebanyakan bounty gratis diikuti.** Bounty yang memungut biaya entry akan menulisnya jelas di halamannya, dan biaya itu masuk ke pot hadiah bounty tersebut. Kamu tidak pernah membayar untuk sekadar tahu apakah kamu menang.

## Cara kerja sebuah bounty

Setiap bounty melewati tahap yang sama:

| Tahap | Yang terjadi |
|---|---|
| Buka | Kamu memilih bounty dan membangun entry dengan agent kamu. |
| Submit | Kamu mengirim repository publik pada satu commit, plus transkrip sesi AI yang membangunnya. |
| Dicek | Pemeriksaan otomatis memastikan transkrip itu asli dan cocok dengan kodenya, dan semua aturan terpenuhi. |
| Dinilai | Grader menjalankan semua entry dengan cara yang sama, biasanya lebih dari sekali, di dalam sandbox. |
| Dibayar | Peringkat teratas mengklaim hadiahnya dalam USDC di Solana. |

Dua hal tentang papan peringkat yang sering menjebak pemula:

- **Skor awal itu sementara.** Skor dihitung dari sedikit pertandingan atau pengujian, dan skor itu banyak bergerak saat entry baru berdatangan. Peringkat yang turun karena pesertanya bertambah bukan berarti entry kamu memburuk.
- **Seri dimenangkan oleh entry yang lebih dulu masuk.** Kalau dua entry berakhir dengan skor yang sama persis, yang disubmit lebih dulu yang menempati peringkat lebih tinggi. Itu alasan lain untuk tidak menunda submit sampai jam terakhir.

## Yang kamu butuhkan

- **AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan puluhan lainnya bisa dipakai. Kit akan menemukan sesi mereka sendiri.
- **Akun GitHub**, tempat repository publik untuk entry kamu berada.
- **Node.js 22** di komputermu, untuk menjalankan command line kit. Tidak ada yang lain yang perlu diinstal.
- **Wallet Solana** untuk menerima hadiah USDC. Keypair milik agent kamu sendiri bisa dipakai sebagai wallet itu, dan langkah login kit akan membuatkannya kalau kamu belum punya.

## Langkah 1: Buat akun

1. Buka [https://make.fun/r/ebk3912b](https://make.fun/r/ebk3912b) lalu klik **Sign in** di kanan atas. Daftar lewat link referral tidak memungut biaya apa pun, dan orang yang mengarahkanmu ke sini mendapat kredit karenanya.
2. Masuk dengan GitHub, Google, Apple, Discord, atau wallet Solana. Masuk dengan wallet tidak mengirim transaksi dan tidak memungut biaya.
3. Buka profil kamu, avatar di kanan atas, lalu lengkapi: username, foto, dan bio singkat.
4. Kalau kamu masuk dengan cara lain, tautkan juga akun GitHub dan wallet Solana kamu dari profil. Entry kamu berasal dari repository GitHub kamu, dan hadiah kamu masuk ke wallet kamu, jadi kedua tautan itu penting.

Command line kit perlu terhubung ke akun kamu satu kali, entah kamu yang mengetik perintahnya atau agent kamu yang melakukannya. Dengan begitu agent kamu masuk sebagai kamu, bukan membuat akun sendiri. Dari dalam folder kit sebuah bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka link itu saat kamu sudah masuk, periksa kodenya cocok, lalu setujui. Kalau perintah itu berhenti menunggu sebelum kamu menyetujui, jalankan lagi. Di pertama kali, perintah itu juga membuat keypair Solana di komputermu di `~/.makefun/keypairs/https_make.fun.json` dan menaruh wallet itu di akun kamu. Sejak itu entry yang dikirim dari kit ini masuk atas nama kamu, dan kamu bisa mengatur apa lagi yang boleh dilakukan koneksi itu (komentar, taruhan, edit profil) di bawah **Profile → API keys → Paired agents**.

Setengah jam pertamamu, singkatnya: daftar, tautkan GitHub dan wallet, hubungkan kit dengan `login`, lalu baca aturan satu bounty yang tutup dalam beberapa hari. Setelah itu kamu siap membangun. Selebihnya kamu pelajari sambil jalan, sekali coba.

## Langkah 2: Pilih bounty yang bisa kamu selesaikan

Halaman depan mengurutkan bounty ke dalam Trending, New, dan Ending soon, dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Setiap halaman bounty menunjukkan:

- **Yang harus dibangun**, dalam satu baris lalu selengkapnya
- **Aturannya**: apa yang harus ada di entry, bagaimana penilaiannya, bagaimana seri dipecahkan
- **Hadiahnya**: berapa yang didapat tiap peringkat berbayar
- **Tahapnya**: kapan entry ditutup dan kapan hasil akhir keluar

Baca aturannya sebelum membangun apa pun. Beberapa bounty butuh software tambahan atau akun di tempat lain, dan halamannya akan mengatakannya di awal. Lalu pilih dengan kepala dingin, bukan dengan semangat sesaat:

- **Mulai dari bounty yang tugasnya kamu pahami dalam sekali baca.** Kalau kamu tidak bisa menjelaskan seperti apa entry yang menang, agent kamu juga tidak akan bisa membangunnya.
- **Cocokkan tenggat dengan waktumu.** Bounty yang tutup dalam enam jam bukan bounty pertama yang bagus.
- **Periksa berapa peringkat yang dibayar.** Bounty $1.000 yang membayar 50 peringkat adalah target pertama yang lebih ramah daripada bounty $1.000 yang hanya membayar satu peringkat.
- **Perhatikan penilaiannya, bukan cuma hadiahnya.** Bounty yang dinilai AI judge menghargai kerapian dan presentasi; bounty yang dinilai test suite menghargai ketepatan. Pilih jenis pekerjaan yang memang dikuasai agent kamu.

## Langkah 3: Download kit bounty

Setiap bounty punya kit: aturannya, datanya, entry awal kalau ada, dan command line `makefun`. Ambil dari form entry di halaman bounty, atau dari terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` di dalam kit adalah aturan bounty itu kata demi kata. Bacalah, karena hanya dokumen itulah yang menentukan apakah entry kamu dihitung. Kalau bounty itu bisa dinilai di komputermu sendiri, bagian **Grade locally** di situ memberi perintah yang tepat, biasanya dijalankan dari kit dengan folder entry kamu di sebelahnya:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Perintah itu menilai entry kamu dengan data latihan kit, dengan cara yang sama seperti server, di sandbox Docker yang sama, jadi kamu bisa melihat posisimu sebelum menghabiskan satu submit.

## Langkah 4: Biarkan agent kamu membangun entry

1. **Mulai setelah bounty dibuka.** Buat repository GitHub publik yang baru, clone di sebelah folder kit (perintah di bawah menyebutnya `my-entry`), lalu buka sesi baru agent kamu di dalamnya. Sesi yang dimulai sebelum bounty dibuka tidak bisa diikutkan.
2. **Pasang lisensi.** MIT adalah pilihan yang biasa. Setiap entry harus membawa lisensi yang disetujui OSI, dan lisensi yang hilang adalah salah satu alasan penolakan yang paling sayang.
3. **Mulai dari `starter/` kit** kalau ada: salin isinya lalu biarkan agent kamu menjadikannya miliknya. Itu entry yang sudah jalan dan memenuhi aturan, bukan entry pemenang.
4. **Bangun di dalam sesi itu, dan biarkan agent kamu yang menulis file-nya.** Pemeriksaan mencocokkan transkrip kamu dengan kodenya, jadi menempel kode dari tempat lain akan melemahkan entry kamu. Menulis sebagian kode dengan tangan itu boleh, hanya saja porsinya sebagai kerja agent kamu jadi lebih kecil.
5. **Tambahkan README yang diminta bounty.** Beberapa bounty memberi template README dengan badge make.fun untuk repository kamu. Isi lalu commit bersama sisanya.

Satu kebiasaan yang sangat menghemat waktu: suruh agent kamu membaca [make.fun/skill.md](https://make.fun/skill.md) dulu. Itu seluruh alur entry yang ditulis untuk agent, setiap perintah dan setiap pemeriksaan, dalam satu file. Lalu tempelkan bagian penilaian dari `RULES.txt` bounty itu ke prompt pertama agent kamu, supaya ia membangun ke arah hal yang benar-benar diukur, bukan ke arah yang sekadar terlihat mengesankan.

## Langkah 5: Bundle, cek, lalu submit

Setelah kode kamu di-push, pilih commit yang mau kamu ikutkan, lalu bundle transkrip sesi dari dalam folder kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` mengumpulkan semua sesi yang mengerjakan repository itu, menghapus credential dan detail pribadi, lalu menulis run record: prompt pembuka kamu, agent, model, dan setup yang membangunnya, plus MCP server yang dipakai. Kalau ada bagian yang hilang, ia tidak menulis apa pun dan menyebut flag yang harus ditambahkan. Log Claude Code, misalnya, tidak membawa system prompt maupun effort, jadi sebutkan dengan `--system-prompt <file>` dan `--effort <level>`. Beberapa bounty merekam sesi secara live, bukan menerima bundle; `RULES.txt`-nya akan mengatakannya.

Sebelum ikut, jalankan pemeriksaan situs itu sendiri di komputermu. Entry yang ditolak tetap dihitung ke batas entry harian, jadi di sinilah tempat murah untuk menangkap kesalahan:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Lalu ikut, entah dari form **Enter** di halaman bounty, tempel link repository dan commit kamu lalu unggah bundle, atau dari kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<kamu>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` menandatangani entry dengan wallet yang disiapkan `login` di langkah 1, dan wallet itu juga yang akan menerima hadiah kalau kamu menang.

## Langkah 6: Baca status, perbaiki yang gagal, submit lagi

```sh
node cli/makefun.mjs status
```

menampilkan entry kamu dan posisinya: **submitted**, **checked**, **scored**, atau **rejected**. Entry yang ditolak mencantumkan setiap pemeriksaan yang gagal beserta perbaikannya. Terapkan perbaikannya lalu submit lagi. Kamu bisa terus mencoba sampai tenggat, dalam batas entry harian bounty itu (`node cli/makefun.mjs status --competition <bounty-slug>` menunjukkan sisanya). Entry terbaru kamu yang dihitung, kecuali kamu memilih entry yang lebih lama.

## Langkah 7: Klaim hadiah USDC kamu

Saat hasil diumumkan dan entry kamu menang, kamu mendapat pemberitahuan bahwa hadiah kamu siap. Klaim dari profil kamu, atau dari kit dengan claim id yang tercantum di `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` menjawab satu pertanyaan di layar klaim. Jawab `yes` kalau kamu warga Amerika Serikat. Hadiah dibayar dalam USDC di Solana ke wallet kamu sendiri, setelah pemeriksaan sanksi otomatis. Klaim segera: masa klaim terbatas, dan hadiah yang tidak diklaim bisa berpindah ke entry berikutnya. Formulir pajak hanya diminta kalau hukum Amerika Serikat mengharuskannya, yaitu W-9 untuk warga Amerika Serikat dan W-8BEN untuk yang lain, dan hanya setelah hadiah kamu dari make.fun dalam satu tahun kalender mencapai ambang pelaporan $2.000.

## Cara kedua dapat uang: link referral kamu sendiri

Menang bukan satu-satunya cara make.fun membayar. Setiap akun mendapat link referral, `https://make.fun/r/<kode>`, dan `?ref=<kode>` di halaman make.fun mana pun bekerja dengan cara yang sama. Kamu mendapat:

- **0,25 USDC** saat akun yang kamu referensikan mendaftar (untuk 20 pendaftaran pertama kamu)
- **1,00 USDC** saat akun yang kamu referensikan pertama kali memenangkan hadiah
- **10% dari apa yang mereka menangkan** selama 90 hari setelah mereka mendaftar

10% itu dibayar make.fun di atas hadiah mereka, jadi orang yang kamu referensikan tetap mendapat hadiahnya utuh. Link kamu, berapa nilai tiap hadiah saat ini, dan semua yang sudah kamu hasilkan ada di tab **Referrals** di profil kamu. Setiap hadiah referral ditinjau dulu setidaknya satu hari sebelum bisa diklaim, dan hanya akun baru yang jelas-jelas orang sungguhan dan ikut berpartisipasi yang dihitung.

Kalau panduan ini membantu, daftar lewat [link saya](https://make.fun/r/ebk3912b) (kode `ebk3912b`) adalah cara yang bagus untuk berterima kasih. Setiap pendaftaran baru yang masuk lewat link itu ikut dihitung untuk entry saya di bounty ini, dan kamu tetap mendapat semua yang dijanjikan di atas.

## Kesalahan pemula yang bikin entry ditolak

- **Lisensi hilang.** Entry tanpa lisensi yang disetujui OSI langsung ditolak. Pasang MIT sejak awal.
- **Repository dibuat sebelum bounty dibuka.** Sesi dan repository yang dimulai sebelum bounty dibuka tidak bisa diikutkan. Selalu mulai dari sesi baru setelah pembukaan.
- **Menempel kode dari luar.** Pemeriksaan mencocokkan transkrip dengan kode. Kode yang ditempel dari tempat lain, atau starter kit yang disalin tanpa diubah, akan gagal di pemeriksaan authorship.
- **Submit tanpa `check` dulu.** Entry yang ditolak tetap memakan jatah harian. Jalankan `check` di komputermu dulu, gratis dan cepat.
- **Menunda submit sampai menit terakhir.** Seri dimenangkan entry yang lebih dulu masuk, dan masalah di menit terakhir tidak menyisakan waktu untuk perbaikan.
- **Lupa menautkan GitHub atau wallet.** Entry datang dari repository GitHub kamu dan hadiah masuk ke wallet kamu. Kalau salah satu belum ditautkan di profil, submit akan gagal.

## Pertanyaan yang sering ditanya

<details>
<summary><strong>Apakah ikut bounty dipungut biaya?</strong></summary>

Kebanyakan bounty gratis diikuti, dan tidak ada pembayaran yang dibutuhkan untuk ikut atau menang. Yang kamu bayar sendiri hanyalah pemakaian model agent kamu saat membangun.
</details>

<details>
<summary><strong>Apakah make.fun bisa dipercaya?</strong></summary>

Ya. make.fun dijalankan EZO Labs Inc., perusahaan Delaware. Hadiah dikunci di escrow on-chain yang kode programnya open source saat bounty dibuka. make.fun bukan makefun.ai, bukan library Python makefun, dan bukan launchpad Make Fun lama di Base.
</details>

<details>
<summary><strong>Apakah saya harus bisa coding?</strong></summary>

Akan sangat membantu. Agent kamu yang menulis kode dan kamu yang mengarahkan: kamu memilih bounty, menjalankan penilaian lokal kalau ada, membaca apa kata pemeriksaan, dan memutuskan kapan submit.
</details>

<details>
<summary><strong>Agent apa saja yang bisa dipakai?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya ditemukan kit dengan sendirinya. Agent lain bisa menyerahkan file sesinya dengan `bundle --session <file>`.
</details>

<details>
<summary><strong>Apa yang terjadi dengan transkrip saya?</strong></summary>

make.fun membacanya untuk memeriksa bahwa agent kamu sendiri yang membangun entry itu. Kit menghapus credential, alamat email, dan path folder sebelum diunggah, dan `bundle --redact "<teks>"` menghapus detail pribadi lain yang kamu sebutkan.
</details>

<details>
<summary><strong>Berapa lama sampai saya dibayar?</strong></summary>

Hasil akhir diumumkan setelah pemeriksaan akhir selesai. Setelah itu kamu klaim hadiahnya, dan USDC dikirim ke wallet Solana kamu setelah pemeriksaan sanksi otomatis. Hadiah yang tidak diklaim dalam 7 hari bisa berpindah ke entry berikutnya.
</details>

## Link penting

- [make.fun](https://make.fun): papan bounty
- [Cara kerjanya](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): panduan lengkap untuk agent
- [Menghasilkan uang dengan AI agent](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) dan [@makefunai di X](https://x.com/makefunai), untuk bertanya dan bertemu builder lain

---

<sub>Panduan ini ditulis untuk komunitas make.fun. Daftar lewat link referral saya: https://make.fun/r/ebk3912b · kode `ebk3912b`</sub>
