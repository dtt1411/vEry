<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>dear eiu❤️</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f1f1f1;
            text-align: center;
            padding: 0;
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* Phần nội dung */
        .content {
            background-color: #fff;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            text-align: center;
            position: relative;
        }

        /* Câu tỏ tình */
        h1 {
            font-size: 2.5em;
            color: #e91e63;
            margin: 20px 0;
            animation: fadeIn 3s ease-out;
        }

        /* Trái tim động */
        .heart {
            font-size: 4em;
            color: red;
            animation: heartbeat 1.5s ease-in-out infinite;
            margin: 20px 0;
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(-50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        /* Các nút */
        .button {
            padding: 15px 30px;
            font-size: 1.2em;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s;
            display: inline-block;
        }

        .button-yes {
            background-color: #e91e63;
            color: white;
        }

        .button-yes:hover {
            background-color: #d81b60;
        }

        .button-no {
            background-color: #ccc;
            color: #666;
        }

        .button-no:hover {
            background-color: #bbb;
        }

        /* Hiệu ứng ẩn biến mất */
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <div class="content">
        <h1 id="question">Anh nhớ em rất nhiều! Em có nhớ anh không?</h1>
        <div class="heart">❤️</div>

        <button class="button button-yes" id="yesBtn" onclick="handleResponse('yes')">có em cũng nhớ anh</button>
        <button class="button button-no" id="noBtn" onclick="handleResponse('no')">Không nhớ tẹo nào</button>
    </div>

    <script>
        // Hàm xử lý câu trả lời
        function handleResponse(response) {
            const yesBtn = document.getElementById("yesBtn");
            const noBtn = document.getElementById("noBtn");
            const question = document.getElementById("question");
            const heart = document.querySelector(".heart");

            if (response === 'yes') {
                question.innerHTML = " Anh yêu em rất nhiều ❤️";
                heart.innerHTML = "💖";
                heart.style.animation = "none";  // Dừng hiệu ứng động khi đồng ý
                yesBtn.classList.add("hidden");
                noBtn.classList.add("hidden");
            } else if (response === 'no') {
                question.innerHTML = "em không nhớ anh thât ư  💔";
                heart.style.color = "#aaa";
                heart.innerHTML = "💔";
                noBtn.classList.add("hidden");
                setTimeout(() => {
                    location.reload();  // Reload lại trang sau 3 giây
                }, 3000);
            }
        }
    </script>

</body>
</html>

