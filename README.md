# unish-core



<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UniShell | إطلاق النواة الهجينة</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @keyframes pulse-glow { 0% { box-shadow: 0 0 5px #3b82f6; } 50% { box-shadow: 0 0 20px #3b82f6; } 100% { box-shadow: 0 0 5px #3b82f6; } }
        .glow { animation: pulse-glow 2s infinite; }
    </style>
</head>
<body class="bg-slate-900 text-white font-sans">
    <div class="min-h-screen flex flex-col items-center justify-center p-6 text-center">
        <div class="mb-8">
            <h1 class="text-6xl font-extrabold tracking-tighter text-blue-500 mb-2">Uni<span class="text-white">Shell</span></h1>
            <p class="text-slate-400 text-xl font-light">لغة البرمجة الهجينة العابرة للمنصات</p>
        </div>

        <div class="bg-slate-800 p-8 rounded-3xl border border-slate-700 glow mb-12">
            <h2 class="text-sm uppercase tracking-widest text-blue-400 mb-4 font-bold">المقاعد المجانية المتبقية</h2>
            <div id="counter" class="text-7xl font-mono font-black text-white">10000</div>
            <p class="mt-4 text-slate-500 text-sm">من أصل 10,000 مقعد للمؤسسين الأوائل</p>
        </div>

        <div class="flex flex-col gap-4">
            <button onclick="downloadStarted()" id="downloadBtn" class="bg-blue-600 hover:bg-blue-700 text-white px-12 py-5 rounded-full text-2xl font-bold transition-all transform hover:scale-105">
                تحميل الحزمة لنظام <span id="osName">جهازك</span>
            </button>
            <p class="text-slate-500 text-xs italic">يتضمن: النواة الهجينة، مستشعر PSS، والشهادة الرقمية</p>
        </div>
    </div>

    <script>
        // الكشف عن نظام التشغيل
        const os = navigator.platform.toLowerCase();
        const osSpan = document.getElementById('osName');
        if (os.includes('win')) osSpan.innerText = 'Windows';
        else if (os.includes('mac')) osSpan.innerText = 'macOS';
        else osSpan.innerText = 'Linux';

        // محاكاة العداد (للعرض فقط الآن)
        let count = 10000;
        const counterEl = document.getElementById('counter');
        const interval = setInterval(() => {
            if (count > 9842) {
                count -= Math.floor(Math.random() * 3);
                counterEl.innerText = count.toLocaleString();
            } else { clearInterval(interval); }
        }, 3000);

        function downloadStarted() {
            alert("بدأ تحميل نواة UniShell... أهلاً بك في المستقبل!");
        }
    </script>
</body>
</html>
