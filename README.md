<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>मेरी दुकान</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .product-card {
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <!-- Header Section -->
    <header class="bg-white shadow-sm py-4">
        <div class="container mx-auto px-4 flex justify-between items-center">
            <h1 class="text-3xl font-bold text-indigo-600">मेरी दुकान</h1>
            <a href="#contact" class="bg-indigo-600 text-white font-medium py-2 px-6 rounded-full hover:bg-indigo-700 transition-colors">हमसे संपर्क करें</a>
        </div>
    </header>

    <!-- Products Section -->
    <main class="container mx-auto p-8">
        <h2 class="text-4xl font-extrabold text-center text-gray-900 mb-12">हमारे प्रोडक्ट्स</h2>
        <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
            <!-- Product cards will be inserted here by JavaScript -->
        </div>
    </main>

    <!-- Contact Section -->
    <section id="contact" class="bg-white py-16 mt-12 shadow-inner">
        <div class="container mx-auto px-8 text-center">
            <h2 class="text-4xl font-extrabold text-gray-900 mb-4">हमसे संपर्क करें</h2>
            <p class="text-gray-600 mb-8 max-w-2xl mx-auto">अगर आप किसी भी प्रोडक्ट के बारे में जानना चाहते हैं या ऑर्डर देना चाहते हैं, तो नीचे दिए गए बटन पर क्लिक करें।</p>
            <div class="flex flex-col sm:flex-row justify-center gap-4">
                <!-- WhatsApp Button -->
                <a id="whatsapp-link" href="#" target="_blank" class="bg-green-500 text-white font-bold py-3 px-8 rounded-full shadow-lg hover:bg-green-600 transition-colors flex items-center justify-center">
                    <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12.04 2C6.54 2 2 6.54 2 12.04c0 1.67.48 3.3.43 3.32-.47 1.83-1.63 3.42-3.1 4.54l-1.63 4.5 4.67-1.57c1.39.77 2.82 1.15 4.29 1.15 5.5 0 10-4.54 10-10.04S17.54 2 12.04 2zM12 21.6c-1.3 0-2.6-.4-3.7-1.2l-3.3.9 1.1-3.3c-1.1-1.3-1.7-2.9-1.7-4.6 0-4.9 4-8.9 8.9-8.9s8.9 4 8.9 8.9-4 8.9-8.9 8.9zM16.9 14.8c-.3-.2-.9-.5-1-.5-.2 0-.4 0-.6.2s-.5.5-.6.6-.2.4 0 .6c.2.2.3.4.5.6.2.2.4.2.6.2.2 0 .9-.4 1.1-.9.2-.5.2-.9.2-1.1s-.1-.5-.2-.7zM12 7.5c-2.7 0-4.9 2.2-4.9 4.9s2.2 4.9 4.9 4.9 4.9-2.2 4.9-4.9S14.7 7.5 12 7.5zm.9 8.4c-1.5 0-2.8-1.2-2.8-2.8s1.2-2.8 2.8-2.8 2.8 1.2 2.8 2.8-1.3 2.8-2.8 2.8z"/>
                    </svg>
                    WhatsApp पर संपर्क करें
                </a>
                <!-- Phone Call Button -->
                <a id="phone-link" href="#" class="bg-gray-800 text-white font-bold py-3 px-8 rounded-full shadow-lg hover:bg-gray-900 transition-colors flex items-center justify-center">
                    <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M6.62 10.79a15.09 15.09 0 006.59 6.59l2.21-2.21a.997.997 0 011.08-.26c1.12.3 2.3.46 3.48.46a1 1 0 011 1v3.42a1 1 0 01-1 1c-6.62 0-12-5.38-12-12a1 1 0 011-1h3.42a1 1 0 011 1c0 1.18.16 2.36.46 3.48a.997.997 0 01-.26 1.08l-2.21 2.21z"/>
                    </svg>
                    कॉल करें
                </a>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-gray-800 text-white text-center py-4 mt-12">
        <p>&copy; 2024 मेरी दुकान। सर्वाधिकार सुरक्षित।</p>
    </footer>

    <script>
        // अपनी दुकान और प्रोडक्ट्स की जानकारी यहाँ डालें
        const shopInfo = {
            shopName: "मेरी दुकान",
            contactNumber: "9876543210", // अपना फ़ोन नंबर यहाँ डालें
            whatsappMessage: "नमस्ते, मैंने आपकी वेबसाइट देखी और मैं आपके प्रोडक्ट्स के बारे में जानना चाहता हूँ।" // WhatsApp पर भेजा जाने वाला मैसेज
        };

        const products = [
            {
                name: "सुंदर लाल टॉप",
                description: "यह टॉप बहुत ही आरामदायक और स्टाइलिश है। इसे पहनकर आप बहुत ही आकर्षक दिखेंगी।",
                image: "https://placehold.co/400x400/FF5733/FFFFFF?text=Product+1",
                price: "₹750"
            },
            {
                name: "नीली जींस",
                description: "उच्च गुणवत्ता वाली डेनिम से बनी, जो पहनने में आरामदायक और टिकाऊ है।",
                image: "https://placehold.co/400x400/3385FF/FFFFFF?text=Product+2",
                price: "₹1,200"
            },
            {
                name: "चमड़े का हैंडबैग",
                description: "यह स्टाइलिश और मजबूत हैंडबैग आपकी सभी ज़रूरी चीज़ों के लिए एकदम सही है।",
                image: "https://placehold.co/400x400/8A2BE2/FFFFFF?text=Product+3",
                price: "₹1,500"
            },
            {
                name: "ब्लैक स्पोर्ट्स शूज़",
                description: "यह शूज़ आपकी दैनिक कसरत और दौड़ के लिए एकदम सही हैं।",
                image: "https://placehold.co/400x400/000000/FFFFFF?text=Product+4",
                price: "₹2,500"
            },
            {
                name: "सिल्क साड़ी",
                description: "सिल्क साड़ी जो किसी भी खास मौके पर आपको बेहतरीन लुक देगी।",
                image: "https://placehold.co/400x400/FFC0CB/000000?text=Product+5",
                price: "₹4,000"
            },
            {
                name: "पुरुषों की जैकेट",
                description: "मौसम के लिए आरामदायक और स्टाइलिश जैकेट।",
                image: "https://placehold.co/400x400/A9A9A9/000000?text=Product+6",
                price: "₹1,800"
            }
        ];

        // प्रोडक्ट्स को डायनामिक रूप से पेज पर जोड़ें
        function renderProducts() {
            const productGrid = document.getElementById('product-grid');
            productGrid.innerHTML = products.map(product => `
                <div class="product-card bg-white rounded-lg shadow-md overflow-hidden p-4 flex flex-col items-center text-center">
                    <img src="${product.image}" alt="${product.name}" class="w-full h-48 object-cover rounded-md mb-4">
                    <h3 class="text-xl font-semibold mb-2">${product.name}</h3>
                    <p class="text-sm text-gray-500 mb-4">${product.description}</p>
                    <span class="text-2xl font-bold text-indigo-600">${product.price}</span>
                </div>
            `).join('');
        }

        // WhatsApp और फ़ोन लिंक सेट करें
        function setContactLinks() {
            const whatsappLink = document.getElementById('whatsapp-link');
            const phoneLink = document.getElementById('phone-link');

            const wa_number = shopInfo.contactNumber.replace(/\D/g, '');
            const wa_message = encodeURIComponent(shopInfo.whatsappMessage);

            whatsappLink.href = `https://wa.me/${wa_number}?text=${wa_message}`;
            phoneLink.href = `tel:${shopInfo.contactNumber}`;
        }

        // पेज लोड होने पर फंक्शन चलाएं
        window.onload = function() {
            renderProducts();
            setContactLinks();
        };
    </script>
</body>
</html>
