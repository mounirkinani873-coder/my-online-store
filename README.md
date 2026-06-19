<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Store Mounir - كراسي الباكيت الفاخرة</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap');
        body { font-family: 'Cairo', sans-serif; }
        .hero-bg { background: linear-gradient(rgba(10, 20, 40, 0.75), rgba(10, 20, 40, 0.75)), url('https://picsum.photos/id/1015/2000/1200') center/cover no-repeat; }
        .product-img { transition: all 0.4s ease; }
        .nav-link { transition: all 0.3s; }
        .nav-link:hover { color: #10b981; transform: translateY(-2px); }
        .swatch { width: 52px; height: 52px; border: 3px solid #fff; box-shadow: 0 0 0 2px #0a1428; cursor: pointer; }
    </style>
</head>
<body class="bg-gray-50 text-gray-900">

<!-- Navbar -->
<nav class="bg-[#0A1428] text-white sticky top-0 z-50 shadow-lg">
    <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
        <div class="flex items-center gap-3">
            <i class="fa-solid fa-chair text-4xl text-emerald-500"></i>
            <div>
                <span class="text-3xl font-bold tracking-tight">Store Mounir</span>
                <p class="text-xs text-emerald-400 -mt-1">كراسي باكيت فاخرة</p>
            </div>
        </div>
        <div class="hidden md:flex items-center gap-8 text-lg">
            <a href="#home" class="nav-link">الرئيسية</a>
            <a href="#product" class="nav-link">المنتج</a>
            <a href="#about" class="nav-link">من نحن</a>
            <a href="#shipping" class="nav-link">الشحن والتوصيل</a>
            <a href="#faq" class="nav-link">أسئلة شائعة</a>
        </div>
        <div class="flex items-center gap-4">
            <button onclick="openCart()" class="relative px-5 py-2.5 bg-white text-[#0A1428] rounded-2xl font-semibold flex items-center gap-2 hover:bg-emerald-100">
                <i class="fa-solid fa-shopping-bag"></i>
                <span id="cart-count" class="absolute -top-1 -right-1 bg-emerald-500 text-white text-xs w-5 h-5 rounded-full flex items-center justify-center">0</span>
            </button>
            <button onclick="toggleMobileMenu()" class="md:hidden text-3xl"><i class="fa-solid fa-bars"></i></button>
        </div>
    </div>
</nav>

<!-- Hero -->
<section id="home" class="hero-bg h-screen flex items-center text-white">
    <div class="max-w-5xl mx-auto px-6 text-center">
        <h1 class="text-5xl md:text-6xl font-bold leading-tight mb-6">
            كراسي الباكيت الفاخرة<br>لبيتك ومشروعك
        </h1>
        <p class="text-2xl md:text-3xl text-emerald-200 mb-10">راحة • أناقة • فخامة • جودة عالمية بأسعار مغربية</p>
        <div class="flex flex-col sm:flex-row gap-5 justify-center">
            <button onclick="openProductModal()" 
                    class="bg-emerald-600 hover:bg-emerald-700 text-white text-2xl font-bold px-12 py-6 rounded-3xl shadow-2xl flex items-center gap-3 mx-auto sm:mx-0">
                <i class="fa-solid fa-bolt"></i>
                اطلب الآن
            </button>
            <button onclick="document.getElementById('wholesale').scrollIntoView({behavior:'smooth'})" 
                    class="border-2 border-white hover:bg-white hover:text-[#0A1428] text-2xl font-bold px-12 py-6 rounded-3xl transition-all">
                طلبات الجملة (مقاهي ومطاعم)
            </button>
        </div>
        <div class="mt-12 flex justify-center gap-8 text-sm">
            <div class="flex items-center gap-2"><i class="fa-solid fa-truck text-emerald-400"></i> <span>توصيل 24-48 ساعة</span></div>
            <div class="flex items-center gap-2"><i class="fa-solid fa-hand-holding-dollar text-emerald-400"></i> <span>الدفع عند الاستلام</span></div>
            <div class="flex items-center gap-2"><i class="fa-solid fa-shield-halved text-emerald-400"></i> <span>ضمان الجودة</span></div>
        </div>
    </div>
</section>

<!-- Trust Bar -->
<div class="bg-white py-4 shadow-sm">
    <div class="max-w-6xl mx-auto px-6 flex flex-wrap justify-center items-center gap-x-10 gap-y-3 text-sm text-gray-600">
        <div class="flex items-center gap-2"><span class="text-emerald-600 font-bold">+٥٢٠</span> زبون راضي في المغرب</div>
        <div>✓ مخزون محدود – العرض مستمر حتى نهاية الشهر</div>
        <div class="text-emerald-600 font-semibold">الدار البيضاء • مراكش • الرباط • طنجة • أكادير • فاس</div>
    </div>
</div>

<!-- Product Section -->
<section id="product" class="max-w-7xl mx-auto px-6 py-20">
    <div class="grid md:grid-cols-2 gap-12 items-center">
        <div>
            <img id="main-product-img" src="https://picsum.photos/id/201/800/800" alt="كرسي باكيت فاخر" 
                 class="product-img w-full rounded-3xl shadow-2xl">
            <div class="flex gap-4 mt-6 justify-center">
                <div onclick="selectColor(0)" class="swatch bg-emerald-600 rounded-2xl"></div>
                <div onclick="selectColor(1)" class="swatch bg-gray-400 rounded-2xl"></div>
                <div onclick="selectColor(2)" class="swatch bg-blue-700 rounded-2xl"></div>
                <div onclick="selectColor(3)" class="swatch bg-black rounded-2xl"></div>
            </div>
        </div>
        
        <div>
            <h2 class="text-4xl font-bold mb-3">كرسي باكيت لوكس (Bucket Chair Luxe)</h2>
            <p class="text-emerald-600 text-xl mb-6">مخمل فاخر • تصميم إيطالي • مريح لساعات طويلة</p>
            
            <div class="bg-gray-100 rounded-2xl p-6 mb-8">
                <table class="w-full text-right">
                    <thead>
                        <tr class="border-b">
                            <th class="pb-3">الكمية</th>
                            <th class="pb-3 text-center">السعر للوحدة</th>
                            <th class="pb-3 text-emerald-600">الإجمالي</th>
                        </tr>
                    </thead>
                    <tbody class="text-lg">
                        <tr class="border-b"><td class="py-4">1-3 كراسي (تقسيط)</td><td class="text-center">٦٩٠ درهم</td><td class="font-bold text-emerald-600">٦٩٠ درهم</td></tr>
                        <tr class="border-b"><td class="py-4">4-9 كراسي</td><td class="text-center">٥٩٠ درهم</td><td class="font-bold text-emerald-600">٢٣٦٠ درهم (لـ4)</td></tr>
                        <tr><td class="py-4">١٠+ (جملة - مشاريع)</td><td class="text-center">٤٩٠ درهم</td><td class="font-bold text-emerald-600">اتصل بنا</td></tr>
                    </tbody>
                </table>
            </div>

            <div class="flex gap-4">
                <button onclick="addToCart()" 
                        class="flex-1 bg-[#0A1428] text-white py-5 rounded-3xl text-xl font-bold hover:bg-emerald-700 transition-all">
                    أضف إلى السلة
                </button>
                <button onclick="openCheckoutModal()" 
                        class="flex-1 bg-emerald-600 text-white py-5 rounded-3xl text-xl font-bold hover:bg-emerald-700 transition-all">
                    اطلب الآن (COD)
                </button>
            </div>
            
            <p class="text-xs text-center mt-6 text-gray-500">✓ التوصيل مجاني فوق ٢٠٠٠ درهم • ✓ معاينة قبل الدفع • ✓ ضمان ١ سنة</p>
        </div>
    </div>
</section>

<!-- Reviews -->
<section class="bg-white py-20">
    <div class="max-w-6xl mx-auto px-6">
        <h2 class="text-4xl font-bold text-center mb-12">آراء زبنائنا المغاربة</h2>
        <div class="grid md:grid-cols-3 gap-8">
            <div class="bg-gray-50 p-8 rounded-3xl">
                <p class="italic mb-6">"الكرسي زوين بزاف ومريح بزاف. استعملتو فالكافي ديالي، الزبائن كيسولو عليه. التوصيل كان فـ٢٤ ساعة فقط."</p>
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 bg-amber-200 rounded-2xl"></div>
                    <div>
                        <div class="font-bold">عبد الرحيم الطاهري</div>
                        <div class="text-sm text-emerald-600">الدار البيضاء - صاحب مقهى</div>
                    </div>
                </div>
            </div>
            <div class="bg-gray-50 p-8 rounded-3xl">
                <p class="italic mb-6">"اشتريت ٤ كراسي للصالون. الجودة فاخرة واللون الأخضر الزمردي تحفة. خدمة احترافية وثمن مناسب."</p>
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 bg-purple-200 rounded-2xl"></div>
                    <div>
                        <div class="font-bold">مريم بنعيسى</div>
                        <div class="text-sm text-emerald-600">مراكش</div>
                    </div>
                </div>
            </div>
            <div class="bg-gray-50 p-8 rounded-3xl">
                <p class="italic mb-6">"كراسي ممتازة للمكتب. الراحة استثنائية والتصميم عصري. نشكر Store Mounir على المهنية."</p>
                <div class="flex items-center gap-3">
                    <div class="w-12 h-12 bg-blue-200 rounded-2xl"></div>
                    <div>
                        <div class="font-bold">يوسف الرحماني</div>
                        <div class="text-sm text-emerald-600">الرباط - مهندس</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- About Us -->
<section id="about" class="max-w-6xl mx-auto px-6 py-20 bg-gray-900 text-white rounded-t-[4rem]">
    <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-4xl font-bold mb-8">من نحن</h2>
        <p class="text-lg leading-relaxed text-gray-300">
            Store Mounir هو متجر متخصص حصرياً في كراسي الباكيت الفاخرة. تأسس على يد مونير، الذي قضى سنوات في استيراد أجود أنواع الأثاث العصري من تركيا وإيطاليا ليقدم للمغاربة راحة وفخامة بأسعار منافسة. 
            سواء كنت تبحث عن ديكور منزلك أو تجهيز مقهى أو مطعم أو مكتب، نحن هنا لنقدم لك الحل الأمثل.
        </p>
        <p class="mt-8 text-emerald-400 font-semibold">الجودة • الراحة • السرعة • الثقة</p>
    </div>
</section>

<!-- Shipping -->
<section id="shipping" class="max-w-6xl mx-auto px-6 py-20">
    <h2 class="text-4xl font-bold text-center mb-12">الشحن والتوصيل</h2>
    <div class="bg-emerald-50 rounded-3xl p-12 max-w-2xl mx-auto text-center">
        <i class="fa-solid fa-truck text-7xl text-emerald-600 mb-6"></i>
        <h3 class="text-3xl font-bold mb-4">توصيل سريع لكافة مدن المغرب</h3>
        <p class="text-2xl mb-8">24 إلى 48 ساعة فقط</p>
        <ul class="space-y-4 text-right max-w-md mx-auto text-lg">
            <li class="flex items-center gap-3"><i class="fa-solid fa-check text-emerald-600"></i> الدفع بعد الاستلام والمعاينة</li>
            <li class="flex items-center gap-3"><i class="fa-solid fa-check text-emerald-600"></i> التوصيل مجاني للطلبات فوق ٢٠٠٠ درهم</li>
            <li class="flex items-center gap-3"><i class="fa-solid fa-check text-emerald-600"></i> تتبع الطلب عبر الهاتف</li>
        </ul>
        <button onclick="openCheckoutModal()" class="mt-10 bg-emerald-600 text-white px-10 py-4 rounded-2xl text-xl font-bold">
            ابدأ طلبك الآن
        </button>
    </div>
</section>

<!-- FAQ -->
<section id="faq" class="bg-gray-100 py-20">
    <div class="max-w-4xl mx-auto px-6">
        <h2 class="text-4xl font-bold text-center mb-12">الأسئلة الشائعة</h2>
        <div class="space-y-4">
            <div class="faq-item bg-white rounded-2xl p-6 cursor-pointer" onclick="toggleFAQ(this)">
                <div class="flex justify-between items-center font-semibold">كم هو سعر الكرسي الواحد؟ <span class="text-2xl">+</span></div>
                <div class="faq-answer hidden mt-4 text-gray-600">٦٩٠ درهم للقطعة الواحدة (تقسيط). أسعار خاصة تبدأ من ٤ كراسي.</div>
            </div>
            <div class="faq-item bg-white rounded-2xl p-6 cursor-pointer" onclick="toggleFAQ(this)">
                <div class="flex justify-between items-center font-semibold">هل تقدمون عروض للمقاهي والمطاعم؟ <span class="text-2xl">+</span></div>
                <div class="faq-answer hidden mt-4 text-gray-600">نعم، أسعار الجملة تبدأ من ٤٩٠ درهم للوحدة عند ١٠ كراسي فما فوق. تواصل معنا عبر الواتساب.</div>
            </div>
            <div class="faq-item bg-white rounded-2xl p-6 cursor-pointer" onclick="toggleFAQ(this)">
                <div class="flex justify-between items-center font-semibold">كم مدة التوصيل؟ <span class="text-2xl">+</span></div>
                <div class="faq-answer hidden mt-4 text-gray-600">من 24 إلى 48 ساعة إلى جميع المدن المغربية.</div>
            </div>
            <div class="faq-item bg-white rounded-2xl p-6 cursor-pointer" onclick="toggleFAQ(this)">
                <div class="flex justify-between items-center font-semibold">هل الكراسي مريحة فعلاً؟ <span class="text-2xl">+</span></div>
                <div class="faq-answer hidden mt-4 text-gray-600">نعم، تصميم ergonomic مع حشوة عالية الكثافة. زبناؤنا يؤكدون الراحة لساعات طويلة.</div>
            </div>
        </div>
    </div>
</section>

<!-- Floating WhatsApp -->
<a href="https://wa.me/212600000000" target="_blank"
   class="fixed bottom-8 left-8 bg-green-500 text-white w-16 h-16 rounded-3xl flex items-center justify-center shadow-2xl text-4xl hover:scale-110 transition-all z-50">
    <i class="fa-brands fa-whatsapp"></i>
</a>

<!-- Product Modal -->
<div id="product-modal" class="hidden fixed inset-0 bg-black/70 z-[100] flex items-center justify-center p-4">
    <div class="bg-white max-w-4xl w-full rounded-3xl max-h-[95vh] overflow-auto">
        <!-- Content populated by JS -->
        <div class="p-8" id="modal-content">
            <!-- JS will fill this -->
        </div>
    </div>
</div>

<!-- Checkout Modal -->
<div id="checkout-modal" class="hidden fixed inset-0 bg-black/70 z-[100] flex items-center justify-center p-4">
    <div class="bg-white rounded-3xl max-w-lg w-full p-8">
        <h3 class="text-3xl font-bold mb-6">إتمام الطلب - الدفع عند الاستلام</h3>
        <form id="checkout-form" onsubmit="submitOrder(event)" class="space-y-6">
            <input type="text" id="name" placeholder="الاسم الكامل" required class="w-full px-6 py-4 border rounded-2xl text-lg">
            <input type="tel" id="phone" placeholder="رقم الهاتف (مع رمز المدينة)" required class="w-full px-6 py-4 border rounded-2xl text-lg">
            <input type="text" id="city" placeholder="المدينة (الدار البيضاء، مراكش...)" required class="w-full px-6 py-4 border rounded-2xl text-lg">
            <textarea id="address" placeholder="العنوان التفصيلي" rows="3" class="w-full px-6 py-4 border rounded-2xl text-lg"></textarea>
            
            <div class="bg-gray-100 p-5 rounded-2xl text-sm">
                <p id="order-summary" class="font-medium"></p>
            </div>
            
            <button type="submit" 
                    class="w-full bg-emerald-600 hover:bg-emerald-700 text-white py-6 rounded-3xl text-2xl font-bold">
                تأكيد الطلب
            </button>
            <p class="text-center text-xs text-gray-500">سنتصل بك فوراً لتأكيد الطلب • الدفع بعد المعاينة</p>
        </form>
        <button onclick="closeCheckoutModal()" class="absolute top-6 right-6 text-3xl text-gray-400 hover:text-gray-600">✕</button>
    </div>
</div>

<footer class="bg-[#0A1428] text-white py-16 text-center">
    <p class="text-2xl font-bold mb-2">Store Mounir © ٢٠٢٦</p>
    <p class="text-emerald-400">أفضل كراسي الباكيت في المغرب</p>
    <p class="mt-8 text-sm text-gray-400">هاتف: ٠٦٠٠-٠٠٠-٠٠٠ | الواتساب: نفس الرقم</p>
</footer>

<script>
    // Tailwind script already loaded
    function initializeTailwind() {
        // Already configured via CDN
    }

    let currentColor = 0;
    const colors = [
        {name: "الأخضر الزمردي", hex: "#059669", img: "https://picsum.photos/id/201/800/800"},
        {name: "الرمادي الفاتح", hex: "#9CA3AF", img: "https://picsum.photos/id/160/800/800"},
        {name: "الأزرق الملكي", hex: "#1E40AF", img: "https://picsum.photos/id/29/800/800"},
        {name: "الأسود", hex: "#111827", img: "https://picsum.photos/id/201/800/800"}
    ];

    let cartCount = 0;

    function selectColor(index) {
        currentColor = index;
        document.getElementById('main-product-img').src = colors[index].img;
    }

    function openProductModal() {
        const modal = document.getElementById('product-modal');
        const content = document.getElementById('modal-content');
        content.innerHTML = `
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-3xl font-bold">كرسي باكيت لوكس</h2>
                <button onclick="closeProductModal()" class="text-4xl text-gray-400">✕</button>
            </div>
            <div class="grid md:grid-cols-2 gap-8">
                <img src="${colors[currentColor].img}" class="rounded-3xl shadow-xl" id="modal-main-img">
                <div>
                    <div class="flex gap-3 mb-8">
                        ${colors.map((c,i) => `<div onclick="changeModalColor(${i});" class="swatch" style="background-color:${c.hex}"></div>`).join('')}
                    </div>
                    <h3 class="font-bold text-xl mb-2">اختر اللون: <span id="selected-color-name" class="text-emerald-600">${colors[currentColor].name}</span></h3>
                    <div class="mb-8">
                        <h4 class="font-semibold mb-3">جدول الأسعار</h4>
                        <table class="w-full text-sm">
                            <tr class="border-b"><td class="py-3">1-3 كراسي</td><td class="text-left">690 درهم / الوحدة</td></tr>
                            <tr class="border-b"><td class="py-3">4-9 كراسي</td><td class="text-left">590 درهم / الوحدة</td></tr>
                            <tr><td class="py-3">10 كراسي فما فوق (جملة)</td><td class="text-left text-emerald-600">490 درهم / الوحدة</td></tr>
                        </table>
                    </div>
                    <button onclick="addToCartFromModal();closeProductModal();" 
                            class="w-full py-6 bg-[#0A1428] text-white rounded-3xl text-xl font-bold mb-4">
                        أضف إلى السلة
                    </button>
                    <button onclick="closeProductModal();openCheckoutModal();" 
                            class="w-full py-6 bg-emerald-600 text-white rounded-3xl text-xl font-bold">
                        اطلب الآن - الدفع عند الاستلام
                    </button>
                </div>
            </div>
        `;
        modal.classList.remove('hidden');
        modal.classList.add('flex');
    }

    function changeModalColor(i) {
        currentColor = i;
        document.getElementById('modal-main-img').src = colors[i].img;
        document.getElementById('selected-color-name').textContent = colors[i].name;
    }

    function closeProductModal() {
        const modal = document.getElementById('product-modal');
        modal.classList.add('hidden');
        modal.classList.remove('flex');
    }

    function openCheckoutModal() {
        closeProductModal();
        const modal = document.getElementById('checkout-modal');
        document.getElementById('order-summary').innerHTML = `
            كرسي باكيت لوكس - ${colors[currentColor].name}<br>
            الكمية: 1<br>
            <span class="text-emerald-600 font-bold">الإجمالي: 690 درهم</span><br>
            <span class="text-xs">(الدفع عند الاستلام والتسليم)</span>
        `;
        modal.classList.remove('hidden');
        modal.classList.add('flex');
    }

    function closeCheckoutModal() {
        const modal = document.getElementById('checkout-modal');
        modal.classList.add('hidden');
        modal.classList.remove('flex');
    }

    function submitOrder(e) {
        e.preventDefault();
        const name = document.getElementById('name').value;
        alert(`شكراً لك ${name}!\nتم استلام طلبك بنجاح.\nسنتصل بك خلال دقائق لتأكيد التفاصيل والتوصيل.`);
        closeCheckoutModal();
        document.getElementById('checkout-form').reset();
        cartCount = 0;
        updateCartCount();
    }

    function addToCart() {
        cartCount++;
        updateCartCount();
        alert('تمت إضافة الكرسي إلى السلة ✓');
    }

    function addToCartFromModal() {
        cartCount++;
        updateCartCount();
    }

    function updateCartCount() {
        document.getElementById('cart-count').textContent = cartCount;
    }

    function openCart() {
        if (cartCount === 0) {
            alert('السلة فارغة. أضف بعض الكراسي أولاً!');
            return;
        }
        alert('السلة:\n1 × كرسي باكيت لوكس (' + colors[currentColor].name + ') = 690 درهم\n\nاضغط "اطلب الآن" لإتمام عملية الشراء.');
    }

    function toggleFAQ(el) {
        const answer = el.querySelector('.faq-answer');
        answer.classList.toggle('hidden');
    }

    function toggleMobileMenu() {
        alert('قائمة الهاتف: (في نسخة حقيقية ستكون sidebar)');
    }

    // Initialize
    window.onload = function() {
        initializeTailwind();
        updateCartCount();
        // Make FAQ items nicer
        console.log('%cStore Mounir جاهز! متجر احترافي عالي التحويل.', 'color:#10b981; font-size:18px; font-weight:bold');
    };
</script>
</body>
</html>
