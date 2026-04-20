<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lumina Fashion | Senior Dev Edition</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: { primary: '#3b82f6' }
                }
            }
        }
    </script>
    <style>
        .page { display: none; }
        .page.active { display: block; }
        /* Custom scrollbar untuk estetika */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #888; border-radius: 10px; }
        .dark ::-webkit-scrollbar-track { background: #1f2937; }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-900 dark:text-white transition-colors duration-300 min-h-screen flex flex-col">

    <nav class="fixed w-full z-50 bg-white/90 dark:bg-gray-800/90 backdrop-blur-md shadow-sm border-b dark:border-gray-700">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-black tracking-tighter cursor-pointer" onclick="showPage('home')">LUMINA.</h1>
            
            <div class="hidden md:flex space-x-8 font-medium">
                <button onclick="showPage('home')" class="hover:text-primary transition">Home</button>
                <button onclick="showPage('produk')" class="hover:text-primary transition">Produk</button>
                <button onclick="showPage('about')" class="hover:text-primary transition">Tentang Kami</button>
                <button onclick="showPage('kontak')" class="hover:text-primary transition">Kontak</button>
            </div>

            <div class="flex items-center space-x-5">
                <button onclick="toggleDarkMode()" class="text-xl p-2 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-full transition">🌓</button>
                <button onclick="showPage('cart')" class="relative p-2 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-full transition">
                    🛒 <span id="cart-count" class="absolute top-0 right-0 bg-red-500 text-white text-[10px] font-bold rounded-full h-5 w-5 flex items-center justify-center">0</span>
                </button>
                <button onclick="toggleLogin()" id="login-btn" class="bg-black dark:bg-white dark:text-black text-white px-5 py-2 rounded-full text-sm font-bold hover:opacity-80 transition">Login</button>
            </div>
        </div>
    </nav>

    <main class="flex-grow pt-20">

        <section id="home" class="page active animate__animated animate__fadeIn">
            <div class="relative h-[80vh] flex items-center justify-center bg-gray-900 overflow-hidden">
                <img src="https://images.pexels.com/photos/3965548/pexels-photo-3965548.jpeg?auto=compress&cs=tinysrgb&w=1260" class="absolute inset-0 w-full h-full object-cover opacity-60">
                <div class="relative text-center text-white px-4">
                    <h2 class="text-6xl md:text-8xl font-black mb-4 animate__animated animate__fadeInUp">ELEVATE STYLE</h2>
                    <p class="text-xl md:text-2xl mb-8 opacity-90 font-light">Koleksi eksklusif untuk tampilan elegan setiap hari.</p>
                    <button onclick="showPage('produk')" class="bg-white text-black px-12 py-4 rounded-full font-bold hover:scale-105 transition shadow-2xl">Belanja Sekarang</button>
                </div>
            </div>
            
            <div class="py-24 container mx-auto px-6 text-center">
                <h3 class="text-4xl font-bold mb-16 italic tracking-tight text-primary">Produk Unggulan</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                    <div class="group relative overflow-hidden rounded-3xl aspect-[4/5] shadow-xl">
                        <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?w=600" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent flex flex-col justify-end p-8 text-left">
                            <h4 class="text-white text-2xl font-bold">Premium Outer</h4>
                            <p class="text-white/80">Koleksi musim dingin terbaru.</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-3xl aspect-[4/5] shadow-xl">
                        <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?w=600" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent flex flex-col justify-end p-8 text-left">
                            <h4 class="text-white text-2xl font-bold">Summer Chic</h4>
                            <p class="text-white/80">Ringan, nyaman, dan berwarna.</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-3xl aspect-[4/5] shadow-xl">
                        <img src="https://images.unsplash.com/photo-1490481651871-ab68de25d43d?w=600" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent flex flex-col justify-end p-8 text-left">
                            <h4 class="text-white text-2xl font-bold">Formal Luxe</h4>
                            <p class="text-white/80">Definisi elegan sesungguhnya.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="produk" class="page animate__animated animate__fadeIn py-12 container mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-center mb-12 gap-6">
                <div>
                    <h2 class="text-4xl font-black mb-2">Semua Produk</h2>
                    <p class="opacity-60">Menampilkan koleksi terbaik kami (Minimal 6 Produk)</p>
                </div>
                <div class="relative w-full md:w-96">
                    <input type="text" onkeyup="searchProduct(this.value)" placeholder="Cari nama produk..." class="w-full pl-12 pr-5 py-4 rounded-2xl border dark:border-gray-700 dark:bg-gray-800 focus:ring-2 focus:ring-primary outline-none transition">
                    <span class="absolute left-4 top-4 opacity-40">🔍</span>
                </div>
            </div>
            <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
                </div>
        </section>

        <section id="detail" class="page animate__animated animate__fadeIn py-12 container mx-auto px-6">
            <button onclick="showPage('produk')" class="mb-8 flex items-center gap-2 font-bold hover:text-primary transition">← Kembali Belanja</button>
            <div id="detail-content" class="grid md:grid-cols-2 gap-16 items-start"></div>
        </section>

        <section id="cart" class="page animate__animated animate__fadeIn py-12 container mx-auto px-6 max-w-5xl">
            <h2 class="text-4xl font-black mb-10">Keranjang Belanja</h2>
            <div class="grid lg:grid-cols-3 gap-12">
                <div id="cart-list" class="lg:col-span-2 space-y-6">
                    </div>
                <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-3xl h-fit shadow-inner">
                    <h3 class="text-2xl font-bold mb-6">Ringkasan Pesanan</h3>
                    <div class="space-y-4 mb-8">
                        <div class="flex justify-between"><span>Subtotal</span><span id="subtotal">Rp 0</span></div>
                        <div class="flex justify-between"><span>Pajak (10%)</span><span id="tax">Rp 0</span></div>
                        <hr class="dark:border-gray-700">
                        <div class="flex justify-between font-bold text-xl"><span>Total</span><span id="cart-total" class="text-primary">Rp 0</span></div>
                    </div>
                    <button onclick="showPage('checkout')" class="w-full bg-primary text-white py-4 rounded-2xl font-bold hover:opacity-90 transition">Lanjut ke Checkout</button>
                </div>
            </div>
        </section>

        <section id="checkout" class="page animate__animated animate__fadeIn py-12 container mx-auto px-6 max-w-3xl">
            <div class="bg-white dark:bg-gray-800 p-10 rounded-[2.5rem] shadow-2xl border dark:border-gray-700">
                <h2 class="text-3xl font-black mb-8">Informasi Checkout</h2>
                <form onsubmit="finishOrder(event)" class="space-y-6 text-black">
                    <div class="grid md:grid-cols-2 gap-6">
                        <input type="text" placeholder="Nama Depan" required class="w-full p-4 rounded-xl border-none bg-gray-100 focus:ring-2 focus:ring-primary">
                        <input type="text" placeholder="Nama Belakang" required class="w-full p-4 rounded-xl border-none bg-gray-100 focus:ring-2 focus:ring-primary">
                    </div>
                    <input type="email" placeholder="Alamat Email" required class="w-full p-4 rounded-xl border-none bg-gray-100 focus:ring-2 focus:ring-primary">
                    <textarea placeholder="Alamat Lengkap Pengiriman" required class="w-full p-4 rounded-xl border-none bg-gray-100 focus:ring-2 focus:ring-primary h-32"></textarea>
                    
                    <div>
                        <label class="block mb-2 font-bold dark:text-white">Metode Pembayaran</label>
                        <select class="w-full p-4 rounded-xl border-none bg-gray-100 focus:ring-2 focus:ring-primary">
                            <option>Transfer Bank BCA (Simulasi)</option>
                            <option>E-Wallet (Gopay/OVO)</option>
                            <option>Virtual Account</option>
                        </select>
                    </div>

                    <div class="p-6 bg-primary/5 rounded-2xl dark:text-white border border-primary/20">
                        <p class="text-sm opacity-60 mb-1">Total yang harus dibayar:</p>
                        <p class="text-3xl font-black text-primary" id="checkout-total">Rp 0</p>
                    </div>

                    <button type="submit" class="w-full bg-primary text-white py-5 rounded-2xl font-black text-xl hover:scale-[1.02] transition shadow-lg">BAYAR SEKARANG</button>
                </form>
            </div>
        </section>

        <section id="about" class="page animate__animated animate__fadeIn py-20 container mx-auto px-6 text-center">
            <h2 class="text-5xl font-black mb-8 tracking-tight">Kisah Lumina.</h2>
            <p class="max-w-3xl mx-auto text-xl opacity-70 leading-relaxed mb-20">Didirikan oleh 5 visioner, Lumina bukan sekadar toko baju. Kami adalah gerakan untuk menghadirkan fashion premium yang tetap memperhatikan nilai-nilai lokal dan keberlanjutan.</p>
            
            <div class="grid md:grid-cols-2 gap-10 mb-24 text-left">
                <div class="p-12 bg-gray-50 dark:bg-gray-800 rounded-[3rem]">
                    <h4 class="text-2xl font-bold mb-4 text-primary underline decoration-4">Visi Kami</h4>
                    <p class="text-lg">Menjadi pusat fashion digital paling terpercaya di Asia dengan mengedepankan kualitas tanpa kompromi.</p>
                </div>
                <div class="p-12 bg-gray-50 dark:bg-gray-800 rounded-[3rem]">
                    <h4 class="text-2xl font-bold mb-4 text-primary underline decoration-4">Misi Kami</h4>
                    <p class="text-lg">Menghubungkan desainer berbakat dengan pasar yang lebih luas melalui teknologi belanja yang intuitif.</p>
                </div>
            </div>

            <h3 class="text-3xl font-bold mb-12">The Development Team</h3>
            <div class="flex flex-wrap justify-center gap-8">
                <div class="group">
                    <div class="w-32 h-32 bg-primary/20 rounded-full flex items-center justify-center text-xl font-bold mb-4 group-hover:bg-primary group-hover:text-white transition-all duration-300">AL</div>
                    <p class="font-bold">Aluna</p>
                </div>
                <div class="group">
                    <div class="w-32 h-32 bg-primary/20 rounded-full flex items-center justify-center text-xl font-bold mb-4 group-hover:bg-primary group-hover:text-white transition-all duration-300">CA</div>
                    <p class="font-bold">Candra</p>
                </div>
                <div class="group">
                    <div class="w-32 h-32 bg-primary/20 rounded-full flex items-center justify-center text-xl font-bold mb-4 group-hover:bg-primary group-hover:text-white transition-all duration-300">JU</div>
                    <p class="font-bold">Juvita</p>
                </div>
                <div class="group">
                    <div class="w-32 h-32 bg-primary/20 rounded-full flex items-center justify-center text-xl font-bold mb-4 group-hover:bg-primary group-hover:text-white transition-all duration-300">AN</div>
                    <p class="font-bold">Anisa</p>
                </div>
                <div class="group">
                    <div class="w-32 h-32 bg-primary/20 rounded-full flex items-center justify-center text-xl font-bold mb-4 group-hover:bg-primary group-hover:text-white transition-all duration-300">GH</div>
                    <p class="font-bold">Ghandis</p>
                </div>
            </div>
        </section>

        <section id="kontak" class="page animate__animated animate__fadeIn py-20 container mx-auto px-6">
            <div class="max-w-5xl mx-auto grid md:grid-cols-2 bg-gray-900 rounded-[3rem] overflow-hidden shadow-2xl">
                <div class="p-16 text-white flex flex-col justify-center">
                    <h2 class="text-5xl font-black mb-8">Hubungi Kami</h2>
                    <p class="opacity-60 mb-10 text-lg">Ada pertanyaan? Tim CS kami siap melayani Anda 24/7.</p>
                    <div class="space-y-6 text-xl">
                        <div class="flex items-center gap-4"><span>📍</span> Jakarta, Indonesia</div>
                        <div class="flex items-center gap-4"><span>📧</span> cs@luminafashion.com</div>
                        <div class="flex items-center gap-4"><span>💬</span> +62 888 7777 666</div>
                    </div>
                </div>
                <div class="bg-white p-16 text-black">
                    <form onsubmit="alert('Pesan Anda telah terkirim!'); return false" class="space-y-6">
                        <input type="text" placeholder="Nama Lengkap" class="w-full p-5 bg-gray-100 rounded-2xl border-none outline-none focus:ring-2 focus:ring-primary">
                        <input type="email" placeholder="Alamat Email" class="w-full p-5 bg-gray-100 rounded-2xl border-none outline-none focus:ring-2 focus:ring-primary">
                        <textarea placeholder="Bagaimana kami bisa membantu?" class="w-full p-5 bg-gray-100 rounded-2xl border-none outline-none h-40 focus:ring-2 focus:ring-primary"></textarea>
                        <button class="w-full bg-black text-white py-5 rounded-2xl font-black text-lg hover:bg-primary transition-all duration-300">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-gray-50 dark:bg-gray-800 py-12 border-t dark:border-gray-700 mt-20">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-2xl font-black mb-4">LUMINA.</h2>
            <p class="opacity-50 text-sm mb-6 max-w-md mx-auto">Platform fashion terbaik untuk Anda yang menghargai kualitas dan kemudahan berbelanja online.</p>
            <div class="flex justify-center gap-6 mb-8">
                <span class="cursor-pointer hover:text-primary transition">Instagram</span>
                <span class="cursor-pointer hover:text-primary transition">Tiktok</span>
                <span class="cursor-pointer hover:text-primary transition">Facebook</span>
            </div>
            <p class="text-xs opacity-40">&copy; 2024 Kelompok Lumina Developer Team. All rights reserved.</p>
        </div>
    </footer>

    <script>
        const products = [
            { id: 1, name: "Urban Overcoat", price: 850000, img: "https://images.unsplash.com/photo-1539109136881-3be0616acf4b?w=500", stock: 12, desc: "Jaket overcoat premium dengan bahan wol Italia." },
            { id: 2, name: "Minimalist Hoodie", price: 420000, img: "https://images.unsplash.com/photo-1556821840-3a63f95609a7?w=500", stock: 25, desc: "Hoodie katun murni untuk kenyamanan aktivitas sehari-hari." },
            { id: 3, name: "Luxury Silk Dress", price: 1250000, img: "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?w=500", stock: 8, desc: "Gaun sutra elegan dengan potongan modern untuk acara formal." },
            { id: 4, name: "Classic Blue Jeans", price: 590000, img: "https://images.unsplash.com/photo-1542272604-787c3835535d?w=500", stock: 30, desc: "Celana jeans potongan lurus dengan denim berkualitas tinggi." },
            { id: 5, name: "Oxford White Shirt", price: 350000, img: "https://images.pexels.com/photos/297933/pexels-photo-297933.jpeg?auto=compress&cs=tinysrgb&w=600", stock: 20, desc: "Kemeja putih basic yang wajib dimiliki setiap pria/wanita." },
            { id: 6, name: "Canvas Totebag", price: 120000, img: "https://images.pexels.com/photos/3731256/pexels-photo-3731256.jpeg?auto=compress&cs=tinysrgb&w=600", stock: 50, desc: "Tas tote kanvas serbaguna dengan kapasitas besar." }
        ];

        let cart = [];

        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            window.scrollTo(0, 0);
            if(pageId === 'produk') renderProducts(products);
            if(pageId === 'cart') renderCart();
        }

        function renderProducts(data) {
            const grid = document.getElementById('product-grid');
            grid.innerHTML = data.map(p => `
                <div class="bg-white dark:bg-gray-800 rounded-3xl overflow-hidden shadow-lg hover:shadow-2xl transition-all duration-500 group border dark:border-gray-700">
                    <div class="h-80 overflow-hidden relative">
                        <img src="${p.img}" class="w-full h-full object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute top-4 right-4 bg-white/90 dark:bg-black/90 px-3 py-1 rounded-full text-xs font-bold shadow-md">Stok: ${p.stock}</div>
                    </div>
                    <div class="p-8">
                        <h4 class="text-xl font-bold mb-2">${p.name}</h4>
                        <p class="text-primary text-2xl font-black mb-6">Rp ${p.price.toLocaleString()}</p>
                        <div class="flex gap-3">
                            <button onclick="showDetail(${p.id})" class="flex-1 border-2 border-black dark:border-white py-3 rounded-2xl text-sm font-bold hover:bg-black hover:text-white dark:hover:bg-white dark:hover:text-black transition">Detail</button>
                            <button onclick="addToCart(${p.id})" class="flex-1 bg-black text-white dark:bg-white dark:text-black py-3 rounded-2xl text-sm font-bold hover:scale-105 transition shadow-lg">Beli</button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        function searchProduct(query) {
            const filtered = products.filter(p => p.name.toLowerCase().includes(query.toLowerCase()));
            renderProducts(filtered);
        }

        function showDetail(id) {
            const p = products.find(x => x.id === id);
            const content = document.getElementById('detail-content');
            content.innerHTML = `
                <div class="relative group">
                    <img src="${p.img}" class="rounded-[3rem] shadow-2xl w-full">
                    <div class="absolute -bottom-6 -right-6 bg-primary text-white p-10 rounded-full font-black text-2xl shadow-2xl animate-bounce">TOP!</div>
                </div>
                <div>
                    <h1 class="text-6xl font-black mb-6 leading-tight">${p.name}</h1>
                    <p class="text-4xl text-primary font-bold mb-8 italic underline">Rp ${p.price.toLocaleString()}</p>
                    <p class="text-xl opacity-70 mb-10 leading-relaxed border-l-4 border-primary pl-6">${p.desc}</p>
                    <div class="flex items-center gap-6 mb-10">
                        <span class="bg-gray-100 dark:bg-gray-700 px-6 py-3 rounded-2xl font-bold">Stok Tersedia: ${p.stock}</span>
                    </div>
                    <button onclick="addToCart(${p.id})" class="w-full bg-black dark:bg-white dark:text-black text-white py-6 rounded-3xl font-black text-2xl hover:scale-[1.03] transition shadow-2xl">TAMBAH KE KERANJANG</button>
                </div>
            `;
            showPage('detail');
        }

        function addToCart(id) {
            const existingItem = cart.find(item => item.id === id);
            if (existingItem) {
                existingItem.qty += 1;
            } else {
                const p = products.find(x => x.id === id);
                cart.push({ ...p, qty: 1 });
            }
            updateCartUI();
            alert("Barang berhasil ditambahkan ke keranjang!");
        }

        function changeQty(index, delta) {
            if (cart[index].qty + delta > 0) {
                cart[index].qty += delta;
            } else {
                cart.splice(index, 1);
            }
            updateCartUI();
            renderCart();
        }

        function updateCartUI() {
            const count = cart.reduce((sum, item) => sum + item.qty, 0);
            document.getElementById('cart-count').innerText = count;
            
            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
            const tax = subtotal * 0.1;
            const total = subtotal + tax;
            
            const format = (num) => `Rp ${num.toLocaleString()}`;
            
            if(document.getElementById('subtotal')) {
                document.getElementById('subtotal').innerText = format(subtotal);
                document.getElementById('tax').innerText = format(tax);
                document.getElementById('cart-total').innerText = format(total);
                document.getElementById('checkout-total').innerText = format(total);
            }
        }

        function renderCart() {
            const list = document.getElementById('cart-list');
            if(cart.length === 0) {
                list.innerHTML = `
                    <div class="text-center py-20 bg-gray-50 dark:bg-gray-800 rounded-3xl">
                        <p class="text-6xl mb-4">🛒</p>
                        <p class="text-xl opacity-50">Keranjang Anda masih kosong.</p>
                        <button onclick="showPage('produk')" class="mt-6 text-primary font-bold underline">Mulai Belanja</button>
                    </div>
                `;
                return;
            }
            list.innerHTML = cart.map((item, index) => `
                <div class="flex flex-wrap items-center justify-between bg-white dark:bg-gray-800 p-8 rounded-3xl shadow-sm border dark:border-gray-700 gap-6">
                    <div class="flex items-center gap-8">
                        <img src="${item.img}" class="w-24 h-24 object-cover rounded-2xl shadow-md">
                        <div>
                            <h4 class="text-xl font-bold">${item.name}</h4>
                            <p class="opacity-60">Rp ${item.price.toLocaleString()}</p>
                        </div>
                    </div>
                    
                    <div class="flex items-center gap-6 bg-gray-100 dark:bg-gray-700 px-6 py-3 rounded-2xl">
                        <button onclick="changeQty(${index}, -1)" class="text-2xl font-black hover:text-primary transition">-</button>
                        <span class="text-xl font-black w-8 text-center">${item.qty}</span>
                        <button onclick="changeQty(${index}, 1)" class="text-2xl font-black hover:text-primary transition">+</button>
                    </div>

                    <div class="text-right min-w-[150px]">
                        <p class="text-2xl font-black text-primary">Rp ${(item.price * item.qty).toLocaleString()}</p>
                    </div>
                </div>
            `).join('');
        }

        function toggleDarkMode() {
            document.documentElement.classList.toggle('dark');
        }

        function toggleLogin() {
            const btn = document.getElementById('login-btn');
            if(btn.innerText === "Login") {
                const name = prompt("Selamat datang di Lumina! Masukkan nama Anda:");
                if(name) {
                    btn.innerText = "Hi, " + name;
                    btn.classList.add("bg-primary");
                }
            } else {
                if(confirm("Apakah Anda ingin logout?")) {
                    btn.innerText = "Login";
                    btn.classList.remove("bg-primary");
                }
            }
        }

        function finishOrder(e) {
            e.preventDefault();
            alert("Terima kasih! Pesanan Anda telah diterima. Kami akan segera menghubungi Anda.");
            cart = [];
            updateCartUI();
            showPage('home');
        }
    </script>
</body>
</html>
