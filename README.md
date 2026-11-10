<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Fitness</title>
    <!-- استيراد خطوط وتصميم عصري -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #0f172a;
            color: #ffffff;
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in-out forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between overflow-x-hidden">

    <!-- القسم الأول: الصفحة الرئيسية -->
    <section id="home-section" class="flex-grow flex flex-col items-center justify-center px-4 py-12 text-center transition-all duration-500">
        <div class="max-w-md w-full bg-slate-800/60 backdrop-blur-md p-8 rounded-3xl border border-slate-700 shadow-2xl">
            
            <!-- الشعار في المنتصف -->
            <div class="mb-8 flex justify-center">
                <div class="w-32 h-32 bg-white rounded-2xl p-3 shadow-inner flex items-center justify-center">
                    <!-- استبدل الرابط أدناه برابط شعارك بصيغة PNG بعد رفعه -->
                    <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?q=80&w=300&auto=format&fit=crop" alt="A Fitness Logo" class="max-h-full max-w-full object-contain filter drop-shadow">
                </div>
            </div>

            <h1 class="text-3xl font-black mb-3 text-red-500 tracking-wider">A FITNESS</h1>
            <p class="text-slate-300 text-sm mb-8 leading-relaxed">
                ابدأ رحلتك الرياضية الآن نحو جسد أقوى وصحة أفضل. خطوتك الأولى تبدأ من هنا.
            </p>

            <!-- زر "ابدأ الان" -->
            <button onclick="goToNextStep()" class="w-full bg-red-600 hover:bg-red-700 text-white font-bold py-4 rounded-xl shadow-lg transition duration-300 transform hover:scale-[1.02] text-lg">
                ابدأ الآن
            </button>
        </div>
    </section>

    <!-- القسم الثاني: الخانة التالية (تظهر عند الضغط وتختفي الأولى) -->
    <section id="next-section" class="hidden flex-grow flex flex-col items-center justify-center px-4 py-12 text-center fade-in">
        <div class="max-w-md w-full bg-slate-800/60 backdrop-blur-md p-8 rounded-3xl border border-slate-700 shadow-2xl">
            <h2 class="text-2xl font-bold mb-4 text-white">أهلاً بك في الخطوة الثانية!</h2>
            <p class="text-slate-300 text-sm mb-6">
                لقد دخلت بنجاح إلى القسم الثاني دون مغادرة الصفحة. أخبرني بالخطوة التالية أو المحتوى الذي ترغب بإضافته هنا (مثل: إدخال الوزن والطول، أو اختيار البرنامج التدريبي).
            </p>
            <button onclick="goBack()" class="bg-slate-700 hover:bg-slate-600 text-white text-sm font-semibold py-2 px-6 rounded-lg transition">
                العودة للخلف
            </button>
        </div>
    </section>

    <!-- تذييل بسيط -->
    <footer class="py-6 text-center text-xs text-slate-500">
        جميع الحقوق محفوظة &copy; 2026 A Fitness
    </footer>

    <!-- سكربت التنقل السلس بين الأقسام دون إعادة تحميل -->
    <script>
        function goToNextStep() {
            const home = document.getElementById('home-section');
            const next = document.getElementById('next-section');

            home.classList.add('hidden');
            next.classList.remove('hidden');
        }

        function goBack() {
            const home = document.getElementById('home-section');
            const next = document.getElementById('next-section');

            next.classList.add('hidden');
            home.classList.remove('hidden');
        }
    </script>
</body>
</html>
