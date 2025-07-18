<script setup lang="ts">
const images = import.meta.glob('./assets/**/*.{png,jpg,jpeg,svg}', { eager: true }) as Record<
  string,
  { default: string }
>

const products = [
  {
    name: 'Keripik Kembang Tahu',
    price: 'Rp12.000',
    image: images['./assets/keripik-kembang-tahu.png'].default,
  },
  {
    name: 'Keripik Kembang Tahu Bumbu Rempah Nusantara',
    price: 'Rp12.000',
    image: images['./assets/keripik-kembang-tahu-bumbu-rempah-nusantara.png'].default,
  },
  {
    name: 'Keripik Opak Kribon',
    price: 'Rp12.000',
    image: images['./assets/keripik-opak-kribon.png'].default,
  },
  {
    name: 'Keripik Kembang Tahu Rasa Daun Kari',
    price: 'Rp12.000',
    image: images['./assets/keripik-kembang-tahu-rasa-daun-kari.png'].default,
  },
  {
    name: 'Keripik Labu',
    price: 'Rp12.000',
    image: images['./assets/keripik-labu.png'].default,
  },
  {
    name: 'Keripik Sayur',
    price: 'Rp12.000',
    image: images['./assets/keripik-sayur.png'].default,
  },
]
</script>

<template>
  <div class="font-sans text-gray-900 bg-white">
    <!-- Header -->
    <header class="flex justify-between items-center px-6 py-4 sticky top-0 bg-white z-50">
      <h1 class="text-2xl font-bold text-orange-600 brand-name">Keripik R & R</h1>
      <nav class="hidden md:flex gap-6 text-sm font-medium">
        <a href="#hero" class="hover:text-orange-600 transition">Beranda</a>
        <a href="#produk" class="hover:text-orange-600 transition">Produk</a>
        <a href="#tentang" class="hover:text-orange-600 transition">Tentang</a>
        <a href="#kontak" class="hover:text-orange-600 transition">Kontak</a>
      </nav>
    </header>

    <main>
      <!-- Hero -->
      <section
        id="hero"
        class="flex flex-col-reverse md:flex-row items-center justify-between gap-10 px-6 md:px-12 py-16 max-w-7xl mx-auto"
      >
        <div class="flex-1 space-y-6">
          <h2 class="text-4xl md:text-5xl font-extrabold leading-tight tracking-tight">
            <span class="text-orange-500">Rasakan Renyahnya</span><br />
            <span class="text-gray-900">Temukan Favoritmu!</span>
          </h2>
          <p class="text-gray-600 text-base md:text-lg max-w-md">
            Keripik lezat dengan berbagai rasa unik, dibuat dari bahan pilihan dan digoreng sempurna
            untuk menemani setiap momen ngemilmu.
          </p>
          <button
            class="bg-orange-500 hover:bg-orange-600 text-white font-semibold px-6 py-3 rounded-full transition"
          >
            Lihat Selengkapnya
          </button>
        </div>
        <div class="flex-1">
          <img
            src="./assets/carousel-1.png"
            alt="Keripik"
            class="w-full max-w-md mx-auto rounded-xl"
          />
        </div>
      </section>

      <!-- Features -->
      <section class="bg-orange-50 py-12 px-6 md:px-12 text-center">
        <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="space-y-2">
            <h3 class="text-lg font-semibold text-orange-600">100% Lokal</h3>
            <p class="text-sm text-gray-700">Bahan baku dari petani lokal berkualitas.</p>
          </div>
          <div class="space-y-2">
            <h3 class="text-lg font-semibold text-orange-600">Rasa Variatif</h3>
            <p class="text-sm text-gray-700">Balado, keju, jagung manis dan lainnya.</p>
          </div>
          <div class="space-y-2">
            <h3 class="text-lg font-semibold text-orange-600">Kemasan Aman</h3>
            <p class="text-sm text-gray-700">Kemasan higienis & ramah lingkungan.</p>
          </div>
        </div>
      </section>

      <!-- Products -->
      <section id="produk" class="px-6 md:px-12 py-16 max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-10">Varian Keripik Kami</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10">
          <div
            v-for="(item, i) in products"
            :key="i"
            class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow hover:shadow-lg transition duration-300"
          >
            <div class="aspect-[4/3] bg-gray-5">
              <img
                :src="item.image"
                :alt="item.name"
                class="w-full h-auto object-cover object-center max-h-85"
              />
            </div>
            <div class="p-4 text-center">
              <h3 class="text-lg font-semibold text-gray-800 mb-2">{{ item.name }}</h3>
              <p class="text-orange-500 font-bold text-base">{{ item.price }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- About Us -->
      <section id="tentang" class="py-16 px-6 md:px-12 bg-gray-100 text-center">
        <div class="max-w-3xl mx-auto space-y-6">
          <h2 class="text-3xl font-bold text-gray-900">Tentang Kami</h2>
          <p class="text-lg text-gray-700">
            Keripik R & R adalah produsen keripik lokal yang berdiri sejak 2020. Kami berkomitmen
            untuk menyajikan camilan berkualitas, aman dikonsumsi, dan menggugah selera.
          </p>
          <p class="text-gray-600">
            Visi kami adalah menjadi brand camilan favorit keluarga Indonesia dengan produk yang
            lezat dan bernilai.
          </p>
        </div>
      </section>

      <!-- CTA -->
      <section class="bg-orange-500 text-white py-16 px-6 md:px-12 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-4">Yuk, Coba Sekarang!</h2>
        <p class="max-w-xl mx-auto text-base md:text-lg mb-6">
          Klik tombol di bawah dan nikmati keripik favoritmu langsung dari rumah.
        </p>
        <button
          class="bg-white text-orange-600 font-semibold px-8 py-3 rounded-full hover:bg-orange-100 transition"
        >
          Pesan Sekarang
        </button>
      </section>

      <!-- Why Us -->
      <section class="py-16 px-6 md:px-12 bg-orange-50">
        <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-12 items-center">
          <div>
            <img
              src="./assets/carousel-1.png"
              alt="Why Us"
              class="rounded-2xl w-full max-w-md mx-auto md:mx-0"
            />
          </div>
          <div class="space-y-6">
            <h2 class="text-3xl font-bold text-gray-900">Kenapa Pilih Kami?</h2>
            <p class="text-gray-700 text-lg">
              Kami menghadirkan keripik pilihan dari bahan lokal terbaik, diproses secara higienis
              dan dikemas modern.
            </p>
            <ul class="space-y-2 text-gray-700 list-disc list-inside">
              <li>100% bahan alami & lokal</li>
              <li>Rasa khas dan beragam</li>
              <li>Sudah dipercaya ribuan pelanggan</li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Testimonials -->
      <section class="bg-white py-16 px-6 md:px-12">
        <div class="max-w-4xl mx-auto text-center space-y-10">
          <h2 class="text-3xl font-bold text-gray-900">Apa Kata Mereka?</h2>
          <div class="grid gap-6 md:grid-cols-2">
            <div class="bg-gray-50 p-6 rounded-xl shadow text-left space-y-4">
              <p class="text-gray-700">
                "Keripiknya enak banget, renyah dan rasa baladonya nampol! Bakal beli lagi."
              </p>
              <div class="flex items-center gap-4">
                <img
                  src="https://i.pravatar.cc/300?img=1"
                  alt="User 1"
                  class="w-10 h-10 rounded-full"
                />
                <div>
                  <p class="font-semibold text-gray-800">Dewi Rahma</p>
                  <p class="text-sm text-gray-500">Pelanggan setia</p>
                </div>
              </div>
            </div>
            <div class="bg-gray-50 p-6 rounded-xl shadow text-left space-y-4">
              <p class="text-gray-700">
                "Saya suka variasi rasanya. Cocok untuk cemilan keluarga di rumah."
              </p>
              <div class="flex items-center gap-4">
                <img
                  src="https://i.pravatar.cc/300?img=2"
                  alt="User 2"
                  class="w-10 h-10 rounded-full"
                />
                <div>
                  <p class="font-semibold text-gray-800">Andi Saputra</p>
                  <p class="text-sm text-gray-500">Customer dari Bandung</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Contact Us -->
      <section id="kontak" class="bg-white py-16 px-6 md:px-12">
        <div class="max-w-3xl mx-auto text-center space-y-6">
          <h2 class="text-3xl font-bold text-gray-900">Hubungi Kami</h2>
          <p class="text-gray-700">
            Jika kamu memiliki pertanyaan, masukan, atau ingin bekerja sama, silakan hubungi kami.
          </p>
          <div class="space-y-2 text-gray-600">
            <p>📞 0821-1234-5678</p>
            <p>📧 cs@keripikrandr.com</p>
            <p>📍 Jl. Cemilan No. 88, Jakarta</p>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-100 text-center py-6 text-sm text-gray-600">
      &copy; {{ new Date().getFullYear() }} Keripik R & R. All rights reserved.
    </footer>
  </div>
</template>
