**Membuat Particles Hujan**

Pertama, saya menambahkan node baru GPUParticles2D pada scene Level1, dan membuat ParticlesMaterial baru pada Process Material pada Inspector tab node tersebut. Selanjutnya saya mengubah Amount menjadi 100, dan Lifetime menjadi 4.
Kemudian pada tab Display/Scale saya ubah Scale max menjadi 10, pada Spawn/Position saya ubah Emision Shape menjadi box, dan saya ubah Emision Box Extents value x menjadi 2000. Saya juga mengubah color pada tab Display/Color Curves menjadi warna biru seperti hujan (#84a6b6).
Lalu pada tab Velocity, saya ubah Spread menjadi 20 agar persebaran particle tidak terlalu jauh, dan pada tab Accelerations/Gravity saya ubah gravity x menjadi -500 dan gravity y menjadi 500 agar particle terpengaruh gravitasi ke arah kiri bawah.
Selanjutnya supaya particle tidak hilang jika kita bergerak, pada tab Drawing sauya ubah Visibilty Rect menjadi width = 2000 dan height = 500. Kemudian supaya particle menjadi ada ekornya, pada tab Trail saya ubah Enabled menjadi true.

**Membuat Particles Jalan**

Untuk membuat particles ini, saya melakukan steps awal yang sama dengan sebelumnya, namun kali ini saya menggunakan texture dari folder assets. Kemudian pada pada tab GPUParticles2D, saya ubah Amount menjadi 4 dan Lifetime menjadi 0.5.
Kemudian agar particle muncul ke segala arah dan terbang ke atas, saya ubah Gravity nilai y menjadi -200, lalu pada tab Spawn/Velocity saya ubah Spread menjadi 180 derajat, dan Initial Velocity menjadi 50. Lalu agar particle tidak hanya muncul dari satu titik, saya ubah Spawn/Position/Emission Shape menjadi box dengan nilai x 30, dan saya pindahkan node GPUParticles2D ke bagian kaki player dengan cara mengubah nilai y menjadi 30 pada tab Transform.
Setelah itu saya tweak script agar particle hanya muncul saat player berjalan di lantai.

**Game Balancing**

Untuk melakukan balancing pada game ini dan memastikan game ini tidak terlalu susah sehingga tidak dapat dimainkan, dan tidak juga terlalu mudah sehingga player bosan, saya ubah spawn rate menjadi 1 detik.
