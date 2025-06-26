<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مولد نصوص عربية للتصميم</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
            color: #333;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        textarea {
            width: 100%;
            height: 300px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            margin-bottom: 15px;
        }
        .controls {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }
        button, select, input {
            padding: 8px 15px;
            background: #3498db;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background: #2980b9;
        }
        .copy-btn {
            background: #27ae60;
        }
        .copy-btn:hover {
            background: #219653;
        }
        .footer {
            text-align: center;
            margin-top: 30px;
            color: #7f8c8d;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>مولد نصوص عربية للتصميم</h1>
        
        <div class="controls">
            <select id="paragraphs">
                <option value="1">فقرة واحدة</option>
                <option value="2">فقرتين</option>
                <option value="3" selected>3 فقرات</option>
                <option value="4">4 فقرات</option>
                <option value="5">5 فقرات</option>
            </select>
            
            <select id="length">
                <option value="short">قصير</option>
                <option value="medium" selected>متوسط</option>
                <option value="long">طويل</option>
            </select>
            
            <button id="generate">توليد النص</button>
            <button id="copy" class="copy-btn">نسخ النص</button>
        </div>
        
        <textarea id="output" placeholder="سيظهر النص المولد هنا..."></textarea>
        
        <div class="footer">
            <p>استخدم هذا النص العربي كبديل لـ Lorem Ipsum في تصاميمك ومواقعك</p>
        </div>
    </div>

    <script>
        // نصوص عربية عشوائية يمكنك تعديلها أو إضافة المزيد
        const arabicTexts = [
            "في البداية، كان هناك حاجة ماسة لنصوص تجريبية تعبأ بها المساحات الفارغة في التصاميم، فجاءت فكرة استخدام نصوص لا معنى لها سوى أنها تحاكي النصوص الحقيقية في طريقة توزيع الحروف والكلمات.",
            "مع تطور التصميم الجرافيكي، أصبحت هذه النصوص التجريبية أداة أساسية يستخدمها المصممون لعرض أعمالهم قبل وضع المحتوى النهائي، مما يسمح للعميل بالتركيز على الشكل العام بدلاً من قراءة المحتوى.",
            "تختلف الآراء حول فوائد هذه النصوص، فالبعض يرى أنها ضرورية لعرض التصاميم بشكل واقعي، بينما يعتقد آخرون أنها قد تشتت الانتباه عن العناصر البصرية المهمة في التصميم.",
            "في العصر الرقمي، تطورت أدوات إنشاء النصوص العشوائية لتشمل أنماطاً مختلفة تتراوح بين الكلاسيكية والحديثة، بل وتوجد الآن نصوص عربية متخصصة لهذا الغرض.",
            "لا يجب أن ننسى أن الهدف الأساسي من هذه النصوص هو تمثيل المحتوى الحقيقي في التصاميم، لذلك ينصح بعدم استخدام نصوص طويلة جداً أو قصيرة جداً، بل يجب أن تكون متوازنة.",
            "بعض المصممين يفضلون استخدام محتوى حقيقي حتى في المراحل الأولى من التصميم، بينما يجد آخرون أن النصوص العشوائية توفر عليهم الوقت والجهد في المراحل التمهيدية.",
            "في النهاية، الاختيار بين النصوص العشوائية أو الحقيقية يعتمد على طبيعة المشروع ومرحلة التصميم، وكذلك على تفضيلات المصمم والعميل على حد سواء."
        ];

        const generateBtn = document.getElementById('generate');
        const copyBtn = document.getElementById('copy');
        const output = document.getElementById('output');
        const paragraphsSelect = document.getElementById('paragraphs');
        const lengthSelect = document.getElementById('length');

        generateBtn.addEventListener('click', generateText);
        copyBtn.addEventListener('click', copyText);

        function generateText() {
            const numParagraphs = parseInt(paragraphsSelect.value);
            const length = lengthSelect.value;
            let result = '';

            for (let i = 0; i < numParagraphs; i++) {
                let text = arabicTexts[Math.floor(Math.random() * arabicTexts.length)];
                
                if (length === 'short') {
                    text = text.substring(0, 100) + '...';
                } else if (length === 'long') {
                    text = text + ' ' + arabicTexts[Math.floor(Math.random() * arabicTexts.length)];
                }
                
                result += text + '\n\n';
            }

            output.value = result.trim();
        }

        function copyText() {
            output.select();
            document.execCommand('copy');
            alert('تم نسخ النص إلى الحافظة!');
        }

        // توليد نص عند تحميل الصفحة
        generateText();
    </script>
</body>
</html>
