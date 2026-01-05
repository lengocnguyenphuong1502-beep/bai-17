<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài 17 – Nhóm 4 Lớp 12 Anh</title>

<style>
/* --- GIAO DIỆN CHUNG --- */
body {
    font-family: 'Poppins', sans-serif;
    background: #FFF4B7 url('https://www.transparenttextures.com/patterns/cubes.png');
    margin: 0;
}

header {
    background: linear-gradient(135deg, #000B58, #003161);
    color: white;
    text-align: center;
    padding: 40px 20px;
}

h1 { margin:0; font-size: 36px; }
h2 { color:#000B58; }

section {
    background: white;
    margin: 20px auto;
    width: 90%;
    max-width: 900px;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 6px 15px rgba(0,0,0,0.15);
    transition: .3s;
}
section:hover { transform: translateY(-5px); }

.details { display:none; margin-top: 12px; }

button {
    background: #006A67;
    color:white;
    border:none;
    padding:10px 16px;
    border-radius:8px;
    cursor:pointer;
    font-weight:600;
    transition:.25s;
}
button:hover { transform:scale(1.05); }

nav.topmenu {
    width:100%;
    background:#003161cc;
    backdrop-filter: blur(4px);
    position:fixed;
    top:0;
    left:0;
    padding:12px 25px;
    display:flex;
    align-items:center;
    gap:18px;
    z-index:100;
}
nav.topmenu a {
    color:white;
    text-decoration:none;
    font-weight:600;
    transition:.25s;
}
nav.topmenu a:hover {
    color:#FFD93D;
    transform: translateY(-2px);
}

/* Hình ảnh bo góc */
img.example {
    width:100%;
    border-radius:10px;
    border: 2px solid #003161;
    margin-top:12px;
}
</style>

<script>
function toggle(id){
  var box=document.getElementById(id);
  if(box.style.display==="block"){
     box.style.opacity=0;
     setTimeout(()=>{ box.style.display="none"; },200);
  } else {
     box.style.display="block";
     setTimeout(()=>{ box.style.opacity=1; },10);
  }
}

function bounceScroll(targetID){
    const el = document.getElementById(targetID);
    if (!el) return;
    el.scrollIntoView({ behavior: 'smooth', block:'start' });

    setTimeout(() => {
        el.style.transition = 'transform .45s cubic-bezier(.30,2,.45,1), box-shadow .45s ease';
        el.style.transform = 'scale(1.18)';
        el.style.boxShadow = '0 0 45px #ffe47a, 0 0 75px #FFD93D';

        setTimeout(() => {
            el.style.transform = 'scale(1.06)';
            el.style.boxShadow = '0 0 25px #FFD93D';
            setTimeout(() => {
                el.style.transform = 'scale(1)';
                el.style.boxShadow = 'none';
            }, 220);
        }, 420);
    }, 500);
}
</script>
</head>

<body>

<!-- MENU -->
<nav class="topmenu">
    <a href="https://daisubinta.github.io/Nhom4tin12anh.github.io/">⬅ Quay lại</a>
    <a href="javascript:bounceScroll('lt1')">LT 1</a>
    <a href="javascript:bounceScroll('lt2')">LT 2</a>
    <a href="javascript:bounceScroll('vd1')">Vận dụng 1</a>
    <a href="javascript:bounceScroll('vd2')">Vận dụng 2</a>
</nav>

<br><br><br>

<header>
    <h1>Nhóm 4 – Lớp 12 Anh</h1>
    <h2 style="font-size:52px; font-weight:700; color:#FFD93D;
        text-shadow:0 5px 14px rgba(0,0,0,.55), 0 0 12px #FFD93D;">
        BÀI 17: CÁC MỨC ƯU TIÊN CỦA BỘ CHỌN
    </h2>
</header>

<!-- LT1 -->
<section id="lt1">
<h2>1. Luyện tập 1</h2>
<button onclick="toggle('lt1-content')">Hiện / Ẩn bài làm</button>

<div class="details" id="lt1-content">
    <p><b>Yêu cầu:</b> Giải thích sự khác nhau giữa hai bộ chọn <code>#p123 + p</code> và <code>h2#p123 + p</code>.</p>

    <p><b>• #p123 + p</b>: chọn thẻ p đứng ngay sau phần tử có id="p123".</p>

    <img src="image1.png" class="example">

    <p><b>• h2#p123 + p</b>: chỉ chọn thẻ p đứng sau thẻ h2 có id="p123".</p>

    <img src="image2.png" class="example">
</div>
</section>

<!-- LT2 -->
<section id="lt2">
<h2>2. Luyện tập 2</h2>
<button onclick="toggle('lt2-content')">Hiện / Ẩn bài làm</button>

<div class="details" id="lt2-content">
<pre><code>.name {
  font-style: italic;
  border: 1px solid black;
  padding: 2px;
  display: inline-block;
}
</code></pre>

<p>Dùng class <code>.name</code> để in nghiêng + đóng khung tên riêng.</p>
</div>
</section>

<!-- VẬN DỤNG 1 -->
<section id="vd1">
<h2>3. Vận dụng 1</h2>
<button onclick="toggle('vd1-content')">Hiện / Ẩn bài làm</button>

<div class="details" id="vd1-content">
<p>Các pseudo-class thường gặp:</p>

<ul>
<li><b>:hover</b> – khi rê chuột vào phần tử.</li>
<li><b>:active</b> – khi giữ chuột/nhấn vào phần tử.</li>
<li><b>:focus</b> – khi phần tử được chọn (input được click).</li>
<li><b>:nth-child(n)</b> – chọn phần tử con theo vị trí.</li>
</ul>
</div>
</section>

<!-- VẬN DỤNG 2 -->
<section id="vd2">
<h2>4. Vận dụng 2</h2>
<button onclick="toggle('vd2-content')">Hiện / Ẩn bài làm</button>

<div class="details" id="vd2-content">
<p>Các pseudo-element:</p>

<ul>
<li><b>::before</b> – chèn nội dung trước phần tử.</li>
<li><b>::after</b> – chèn nội dung sau phần tử.</li>
<li><b>::first-line</b> – áp dụng CSS cho dòng đầu tiên.</li>
</ul>
</div>
</section>

</body>
</html>
