<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S.L.E.E.K</title>
  <!-- Change 7: Added meta description for SEO -->
  <meta name="description" content="Shop fashion and accessories at S.L.E.E.K. Discover clothes, bags, and jewelry for all styles with fast WhatsApp delivery.">
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">
  <style>
    html {
      scroll-behavior: smooth;
    }
    .sticky-nav {
      position: sticky;
      top: 0;
      z-index: 50;
      background: white;
    }
    /* Change 6: Styling tweaks for product cards and pagination */
    .product-card:hover img {
      transform: scale(1.05);
      transition: transform 0.3s ease;
    }
    .pagination-btn:hover {
      background-color: #e5e7eb;
      transition: background-color 0.3s ease;
    }
  </style>
</head>
<body class="bg-white text-gray-800">

  <!-- Sticky Navbar -->
  <nav class="sticky-nav shadow-md py-4 px-6 flex justify-between items-center">
    <img src="sleek-logo.png" alt="SLEEK Logo" class="h-10">
    <div class="space-x-4 text-sm">
      <a href="#home" class="text-green-600">Home</a>
      <a href="#about" class="text-green-600">About</a>
      <a href="#services" class="text-green-600">Services</a>
      <a href="#shop" class="text-green-600">Shop</a>
      <a href="#upload" class="text-green-600">Upload</a>
      <a href="#contact" class="text-green-600">Contact</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <!-- Change 1: Updated tagline -->
  <section id="home" class="h-screen flex items-center justify-center bg-green-100" data-aos="fade-up">
    <div class="text-center px-4">
      <h2 class="text-4xl font-bold mb-4 text-green-700">Welcome to S.L.E.E.K</h2>
      <p class="text-lg mb-6">Style for Every Story: From Luxury to Everyday</p>
      <a href="#shop" class="bg-green-600 text-white px-6 py-3 rounded-full">Shop Now</a>
    </div>
  </section>

  <!-- About Section -->
  <!-- Change 1: Updated description -->
  <section id="about" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-4">About Us</h3>
    <p>S.L.E.E.K offers stylish fashion and accessories for everyone, from luxury collections to everyday essentials. Shop trendy clothes, bags, jewelry, and more with seamless WhatsApp ordering.</p>
  </section>

  <!-- Services Section -->
  <!-- Change 1: Updated services -->
  <section id="services" class="py-16 px-6 bg-green-50" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Our Services</h3>
    <ul class="list-disc list-inside space-y-2">
      <li>Personalized styling advice</li>
      <li>Wide range of sizes and styles</li>
      <li>Fast delivery via WhatsApp</li>
    </ul>
  </section>

  <!-- Shop Section -->
  <!-- Change 3: Added category filter; Change 6: Updated grid styling -->
  <section id="shop" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Shop Fashion</h3>
    <div class="mb-4">
      <select id="category-filter" class="p-2 border rounded">
        <option value="all">All Categories</option>
        <option value="Men’s">Men’s</option>
        <option value="Women’s">Women’s</option>
        <option value="Luxury">Luxury</option>
        <option value="Casual">Casual</option>
      </select>
    </div>
    <div id="product-grid" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4"></div>
    <div id="pagination" class="mt-6 text-center"></div>
  </section>

  <!-- Upload Section -->
  <!-- Change 4: Enhanced upload form -->
  <section id="upload" class="py-16 px-6 bg-green-50" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Add Your Product</h3>
    <form id="product-form" class="space-y-4">
      <input type="text" id="product-name" placeholder="Product Name" class="w-full p-2 border rounded" required>
      <input type="file" id="product-image" accept="image/*" class="w-full p-2 border rounded" required>
      <input type="text" id="product-price" placeholder="Price (e.g., $99.99)" class="w-full p-2 border rounded" required>
      <select id="product-category" class="w-full p-2 border rounded" required>
        <option value="" disabled selected>Select Category</option>
        <option value="Men’s">Men’s</option>
        <option value="Women’s">Women’s</option>
        <option value="Luxury">Luxury</option>
        <option value="Casual">Casual</option>
      </select>
      <input type="text" id="product-description" placeholder="Product Description" class="w-full p-2 border rounded" required>
      <input type="text" id="product-whatsapp" placeholder="WhatsApp Order Text" class="w-full p-2 border rounded">
      <button type="submit" class="bg-green-600 text-white px-4 py-2 rounded">Upload Product</button>
    </form>
    <div class="mt-8">
      <h4 class="text-xl font-semibold mb-4">Your Uploaded Products</h4>
      <div id="custom-products" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4"></div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Contact Us</h3>
    <form action="https://formspree.io/f/xayraoqz" method="POST" class="space-y-4">
      <input type="text" name="name" placeholder="Your Name" class="w-full p-2 border rounded" required>
      <input type="email" name="email" placeholder="Your Email" class="w-full p-2 border rounded" required>
      <textarea name="message" placeholder="Your Message" class="w-full p-2 border rounded" required></textarea>
      <button type="submit" class="bg-green-600 text-white px-4 py-2 rounded">Send Message</button>
    </form>
    <div class="mt-4">
      <a href="https://wa.me/2348100123242" class="text-green-600 underline">Order via WhatsApp</a>
    </div>
  </section>

  <!-- Footer -->
  <footer id="footer" class="py-6 text-center bg-green-100">
    <p>© 2025 S.L.E.E.K. All rights reserved.</p>
  </footer>

  <!-- WhatsApp Floating Button -->
  <a href="https://wa.me/2348100123242" class="fixed bottom-4 right-4 bg-green-500 text-white p-3 rounded-full shadow-lg hover:bg-green-600 transition">
    💬
  </a>

  <!-- Search Bar -->
  <div class="fixed bottom-4 left-4 bg-white border rounded-full shadow-md flex items-center px-3 py-1 w-60">
    <input type="text" id="search-input" placeholder="Search products..." class="outline-none flex-1 p-1 text-sm">
  </div>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init();

    // Change 2: Enhanced product structure with sample fashion products
    const products = [
      { name: "Elegant Dress", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Elegant%20Dress", img: "https://via.placeholder.com/150", price: "$99.99", category: "Women’s Luxury", description: "A stunning evening dress in soft silk." },
      { name: "Casual Sneakers", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Casual%20Sneakers", img: "https://via.placeholder.com/150", price: "$49.99", category: "Casual", description: "Comfortable sneakers for daily wear." },
      { name: "Leather Jacket", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Leather%20Jacket", img: "https://via.placeholder.com/150", price: "$129.99", category: "Men’s", description: "Classic black leather jacket." },
      { name: "Gold Necklace", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Gold%20Necklace", img: "https://via.placeholder.com/150", price: "$199.99", category: "Luxury", description: "Elegant 18k gold necklace." },
      { name: "Summer Skirt", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Summer%20Skirt", img: "https://via.placeholder.com/150", price: "$39.99", category: "Women’s", description: "Light and breezy floral skirt." },
      { name: "Denim Jeans", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Denim%20Jeans", img: "https://via.placeholder.com/150", price: "$59.99", category: "Casual", description: "Slim-fit blue denim jeans." },
      { name: "Designer Sunglasses", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Designer%20Sunglasses", img: "https://via.placeholder.com/150", price: "$149.99", category: "Luxury", description: "Trendy polarized sunglasses." },
      { name: "Formal Shirt", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Formal%20Shirt", img: "https://via.placeholder.com/150", price: "$69.99", category: "Men’s", description: "Crisp white dress shirt." },
      { name: "Tote Bag", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Tote%20Bag", img: "https://via.placeholder.com/150", price: "$79.99", category: "Women’s", description: "Spacious leather tote bag." },
      { name: "Sports Cap", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Sports%20Cap", img: "https://via.placeholder.com/150", price: "$29.99", category: "Casual", description: "Breathable cotton sports cap." }
    ];

    const productsPerPage = 8;
    let currentPage = 1;

    // Change 5: Extended search to include custom products
    document.getElementById('search-input').addEventListener('input', function(e) {
      const searchValue = e.target.value.toLowerCase();
      const grids = ['product-grid', 'custom-products'];
      grids.forEach(gridId => {
        const items = document.querySelectorAll(`#${gridId} > div`);
        items.forEach(item => {
          const text = item.textContent.toLowerCase();
          item.style.display = text.includes(searchValue) ? 'block' : 'none';
        });
      });
    });

    // Change 2 & 3: Display products with enhanced structure and category filtering
    function displayProducts(page, category = 'all') {
      const grid = document.getElementById('product-grid');
      grid.innerHTML = "";
      const filteredProducts = category === 'all' ? products : products.filter(p => p.category === category);
      const start = (page - 1) * productsPerPage;
      const end = start + productsPerPage;
      const paginatedItems = filteredProducts.slice(start, end);

      paginatedItems.forEach(p => {
        const div = document.createElement('div');
        // Change 6: Added hover effects; Change 7: Added alt attribute
        div.className = 'p-4 border rounded shadow hover:shadow-lg product-card';
        div.innerHTML = `<img src="${p.img}" alt="${p.name}" class="h-48 w-full object-cover mb-2 rounded">
                         <h4 class="font-semibold mb-1 text-center">${p.name}</h4>
                         <p class="text-sm text-gray-600 text-center">${p.price}</p>
                         <p class="text-xs text-gray-500 text-center">${p.description}</p>
                         <a href="${p.link}" target="_blank" class="text-green-600 underline block text-center mt-2">Order via WhatsApp</a>`;
        grid.appendChild(div);
      });

      renderPagination(filteredProducts.length);
    }

    // Change 6: Styled pagination buttons
    function renderPagination(totalItems) {
      const pagination = document.getElementById('pagination');
      pagination.innerHTML = "";
      const pageCount = Math.ceil(totalItems / productsPerPage);
      for (let i = 1; i <= pageCount; i++) {
        const btn = document.createElement('button');
        btn.textContent = i;
        btn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn ' + (i === currentPage ? 'bg-green-600 text-white' : 'bg-white');
        btn.setAttribute('aria-label', `Go to page ${i}`);
        btn.onclick = () => {
          currentPage = i;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        };
        pagination.appendChild(btn);
      }
    }

    // Change 3: Category filter event listener
    document.getElementById('category-filter').addEventListener('change', function() {
      currentPage = 1;
      displayProducts(currentPage, this.value);
    });

    // Change 4: Updated custom products to include new fields
    function loadCustomProducts() {
      const container = document.getElementById('custom-products');
      container.innerHTML = "";
      const items = JSON.parse(localStorage.getItem('custom-products') || '[]');
      items.forEach(p => {
        const div = document.createElement('div');
        div.className = 'p-4 border rounded shadow hover:shadow-lg product-card';
        div.innerHTML = `<img src="${p.img}" alt="${p.name}" class="h-48 w-full object-cover mb-2 rounded">
                         <h4 class="font-semibold mb-1 text-center">${p.name}</h4>
                         <p class="text-sm text-gray-600 text-center">${p.price}</p>
                         <p class="text-xs text-gray-500 text-center">${p.description}</p>
                         <a href="https://wa.me/2348100123242?text=${encodeURIComponent(p.whatsapp)}" target="_blank" class="text-green-600 underline block text-center mt-2">Order</a>`;
        container.appendChild(div);
      });
    }

    // Change 4: Handle enhanced product form submission
    document.getElementById('product-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('product-name').value;
      const price = document.getElementById('product-price').value;
      const category = document.getElementById('product-category').value;
      const description = document.getElementById('product-description').value;
      const whatsapp = document.getElementById('product-whatsapp').value || name;
      const imgFile = document.getElementById('product-image').files[0];

      const reader = new FileReader();
      reader.onload = function() {
        const imgData = reader.result;
        const products = JSON.parse(localStorage.getItem('custom-products') || '[]');
        products.push({ name, price, category, description, whatsapp, img: imgData });
        localStorage.setItem('custom-products', JSON.stringify(products));
        loadCustomProducts();
        document.getElementById('product-form').reset();
      };
      if (imgFile) {
        reader.readAsDataURL(imgFile);
      }
    });

    // Combined window.onload
    window.addEventListener('load', function() {
      displayProducts(currentPage);
      loadCustomProducts();
    });
  </script>
</body>
</html>
