<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SchoolHub | مدرسة الأورمان الإعدادية الثانوية بنات</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root{
    --primary:#6658d9;
    --primary2:#8779ed;
    --pink:#e7a0cf;
    --light:#f6f6fc;
    --white:#fff;
    --text:#252538;
    --muted:#77788c;
    --border:#e8e7f0;
    --green:#55b98a;
    --red:#df6c80;
    --shadow:0 12px 35px rgba(57,48,120,.09);
    --radius:22px;
}

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family:"Cairo",sans-serif;
    background:var(--light);
    color:var(--text);
}

button,input,select{
    font-family:inherit;
}

button{
    cursor:pointer;
}

.hidden{
    display:none!important;
}

/* =========================
   شاشة البداية
========================= */

.setup{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:25px;
    background:
        radial-gradient(circle at 10% 10%,#eadfff 0,transparent 32%),
        radial-gradient(circle at 90% 90%,#ffe0f1 0,transparent 32%),
        #f7f7fc;
}

.setup-card{
    width:100%;
    max-width:650px;
    background:#fff;
    border-radius:32px;
    padding:38px;
    box-shadow:0 25px 80px rgba(55,45,120,.14);
}

.school-mark{
    width:82px;
    height:82px;
    border-radius:25px;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    font-size:35px;
    font-weight:800;
    background:linear-gradient(135deg,var(--primary),var(--pink));
}

.school-title{
    text-align:center;
    font-size:21px;
    font-weight:800;
    margin-top:17px;
}

.platform-title{
    text-align:center;
    font-size:32px;
    font-weight:800;
    color:var(--primary);
}

.platform-subtitle{
    text-align:center;
    color:var(--muted);
    margin:5px 0 28px;
}

.form-group{
    margin-bottom:18px;
}

.form-group label{
    display:block;
    font-size:14px;
    font-weight:700;
    margin-bottom:7px;
}

.form-group input,
.form-group select{
    width:100%;
    padding:14px 15px;
    border:1px solid var(--border);
    border-radius:14px;
    background:#fafaff;
    outline:none;
    font-size:14px;
}

.form-group input:focus,
.form-group select:focus{
    border-color:var(--primary);
    box-shadow:0 0 0 3px rgba(102,88,217,.1);
}

.primary-btn{
    width:100%;
    border:0;
    border-radius:15px;
    padding:14px 18px;
    color:#fff;
    font-size:15px;
    font-weight:800;
    background:linear-gradient(135deg,var(--primary),var(--primary2));
    box-shadow:0 8px 20px rgba(102,88,217,.2);
    transition:.2s;
}

.primary-btn:hover{
    transform:translateY(-2px);
}

.secondary-btn{
    border:1px solid var(--border);
    background:#fff;
    color:var(--primary);
    border-radius:12px;
    padding:10px 15px;
    font-weight:700;
}

/* =========================
   التطبيق
========================= */

.app{
    min-height:100vh;
}

.sidebar{
    position:fixed;
    top:0;
    right:0;
    bottom:0;
    width:275px;
    background:#fff;
    border-left:1px solid var(--border);
    padding:23px 17px;
    z-index:50;
}

.brand{
    display:flex;
    align-items:center;
    gap:11px;
    padding:7px 8px 22px;
    border-bottom:1px solid var(--border);
}

.brand-mark{
    width:48px;
    height:48px;
    border-radius:15px;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,var(--primary),var(--pink));
    color:#fff;
    font-weight:800;
    font-size:21px;
}

.brand strong{
    display:block;
    font-size:15px;
}

.brand small{
    color:var(--muted);
    font-size:10px;
}

.profile-card{
    margin:18px 0;
    padding:14px;
    border-radius:17px;
    background:#f7f6ff;
}

.profile-card strong{
    display:block;
    font-size:14px;
}

.profile-card span{
    color:var(--muted);
    font-size:11px;
}

.nav{
    display:flex;
    flex-direction:column;
    gap:6px;
}

.nav-btn{
    width:100%;
    border:0;
    background:transparent;
    padding:13px 14px;
    border-radius:13px;
    color:#66677b;
    text-align:right;
    font-size:14px;
}

.nav-btn:hover,
.nav-btn.active{
    background:#eeecff;
    color:var(--primary);
    font-weight:800;
}

.sidebar-bottom{
    position:absolute;
    right:17px;
    left:17px;
    bottom:22px;
}

.logout-btn{
    width:100%;
    border:0;
    background:#fff0f3;
    color:#c75f73;
    padding:12px;
    border-radius:13px;
    font-weight:700;
}

.main{
    margin-right:275px;
    padding:22px 32px;
}

.topbar{
    min-height:60px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-bottom:22px;
}

.topbar-right{
    display:flex;
    align-items:center;
    gap:10px;
}

.mobile-menu{
    display:none;
    border:1px solid var(--border);
    background:#fff;
    border-radius:12px;
    padding:9px 12px;
    font-size:18px;
}

.page-title{
    font-size:23px;
}

.top-actions{
    display:flex;
    align-items:center;
    gap:10px;
}

.icon-btn{
    width:43px;
    height:43px;
    border:1px solid var(--border);
    background:#fff;
    border-radius:13px;
    position:relative;
}

.notification-dot{
    position:absolute;
    top:7px;
    right:8px;
    width:8px;
    height:8px;
    background:#e35f78;
    border-radius:50%;
}

.avatar{
    width:43px;
    height:43px;
    border-radius:13px;
    background:linear-gradient(135deg,var(--primary),var(--pink));
    color:#fff;
    display:flex;
    justify-content:center;
    align-items:center;
    font-weight:800;
}

/* الصفحات */

.page{
    display:none;
}

.page.active{
    display:block;
}

/* الرئيسية */

.welcome{
    color:#fff;
    padding:28px;
    border-radius:25px;
    background:linear-gradient(135deg,#6257d3,#9a8dec);
    margin-bottom:20px;
    box-shadow:var(--shadow);
}

.welcome h1{
    font-size:27px;
}

.welcome p{
    margin-top:4px;
    opacity:.9;
}

.stats{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
    margin-bottom:20px;
}

.stat{
    background:#fff;
    padding:20px;
    border-radius:19px;
    box-shadow:var(--shadow);
}

.stat-icon{
    font-size:22px;
}

.stat strong{
    display:block;
    font-size:25px;
    margin-top:5px;
}

.stat span{
    color:var(--muted);
    font-size:12px;
}

.dashboard-grid{
    display:grid;
    grid-template-columns:1.15fr .85fr;
    gap:20px;
}

.card{
    background:#fff;
    border-radius:var(--radius);
    padding:21px;
    box-shadow:var(--shadow);
    margin-bottom:20px;
}

.card-head{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:10px;
    margin-bottom:17px;
}

.card-head h3{
    font-size:17px;
}

.small-btn{
    border:0;
    background:#efedff;
    color:var(--primary);
    border-radius:10px;
    padding:8px 12px;
    font-size:12px;
    font-weight:800;
}

/* المهام */

.task-row{
    display:flex;
    align-items:center;
    gap:10px;
    padding:12px 0;
    border-bottom:1px solid var(--border);
}

.task-row:last-child{
    border-bottom:0;
}

.check{
    flex-shrink:0;
    width:25px;
    height:25px;
    border:2px solid #cfccdf;
    border-radius:8px;
    background:#fff;
    color:#fff;
    display:flex;
    justify-content:center;
    align-items:center;
}

.check.done{
    background:var(--green);
    border-color:var(--green);
}

.task-name{
    flex:1;
    font-size:13px;
}

.task-day{
    color:var(--muted);
    font-size:11px;
}

.empty{
    text-align:center;
    color:var(--muted);
    padding:25px 10px;
    font-size:13px;
}

/* ملخص الجدول */

.week-mini{
    display:grid;
    gap:8px;
}

.week-mini-row{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:10px 12px;
    border-radius:11px;
    background:#f8f7fc;
    font-size:12px;
}

.week-mini-row span{
    color:var(--muted);
}

/* =========================
   الجدول
========================= */

.planner-info{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:15px;
    flex-wrap:wrap;
    margin-bottom:18px;
}

.planner-info p{
    color:var(--muted);
    font-size:13px;
}

.planner-actions{
    display:flex;
    gap:8px;
}

.lock-status{
    display:flex;
    align-items:center;
    gap:7px;
    padding:9px 12px;
    border-radius:11px;
    background:#f5f4ff;
    color:var(--primary);
    font-size:12px;
    font-weight:700;
}

.friday-box{
    background:#fff;
    border-radius:18px;
    padding:15px 18px;
    margin-bottom:18px;
    box-shadow:var(--shadow);
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.friday-box p{
    color:var(--muted);
    font-size:12px;
    margin-top:2px;
}

.toggle{
    display:flex;
    align-items:center;
    gap:8px;
    font-size:13px;
    font-weight:700;
}

.toggle input{
    width:18px;
    height:18px;
    accent-color:var(--primary);
}

.planner-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.day-card{
    background:#fff;
    border-radius:19px;
    padding:16px;
    min-height:190px;
    box-shadow:var(--shadow);
    border:1px solid transparent;
}

.day-card.locked{
    background:#fcfcfe;
}

.day-card.rest{
    background:#f2f2f6;
}

.day-title{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:14px;
}

.day-title strong{
    font-size:15px;
}

.day-title span{
    color:var(--primary);
    background:#efedff;
    border-radius:8px;
    padding:4px 7px;
    font-size:10px;
}

.subject-chip{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:7px;
    background:#f1efff;
    color:#574fb0;
    padding:9px;
    border-radius:10px;
    margin-bottom:8px;
    font-size:12px;
}

.remove-subject{
    border:0;
    background:transparent;
    color:#9e99bd;
    font-size:17px;
}

.add-subject-btn{
    width:100%;
    border:1px dashed #bdb9dc;
    background:#fff;
    color:var(--primary);
    border-radius:10px;
    padding:8px;
    font-size:11px;
    font-weight:800;
}

.locked-note{
    color:var(--muted);
    font-size:11px;
    text-align:center;
    padding:20px 4px;
}

.rest-note{
    text-align:center;
    color:var(--muted);
    padding:30px 0;
    font-size:12px;
}

/* =========================
   المواد
========================= */

.subjects-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.subject-card{
    background:#fff;
    border-radius:20px;
    padding:20px;
    box-shadow:var(--shadow);
}

.subject-icon{
    width:48px;
    height:48px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:14px;
    background:#efedff;
    font-size:22px;
    margin-bottom:13px;
}

.subject-card h3{
    font-size:16px;
}

.subject-card p{
    color:var(--muted);
    font-size:11px;
    margin-top:5px;
}

/* =========================
   التقدم
========================= */

.progress-main{
    background:#fff;
    border-radius:25px;
    padding:32px;
    text-align:center;
    box-shadow:var(--shadow);
}

.progress-circle{
    width:175px;
    height:175px;
    border-radius:50%;
    margin:10px auto 22px;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
    background:conic-gradient(var(--primary) 0deg,#ededf4 0deg);
}

.progress-circle::after{
    content:"";
    position:absolute;
    width:140px;
    height:140px;
    border-radius:50%;
    background:#fff;
}

.progress-circle span{
    position:relative;
    z-index:2;
    font-size:31px;
    font-weight:800;
}

.progress-bar{
    height:11px;
    background:#ededf3;
    border-radius:20px;
    overflow:hidden;
}

.progress-fill{
    height:100%;
    width:0;
    background:linear-gradient(90deg,var(--primary),var(--pink));
    transition:.4s;
}

.achievements{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:13px;
    margin-top:20px;
}

.achievement{
    background:#f7f6fc;
    border-radius:15px;
    padding:17px;
}

.achievement strong{
    display:block;
    color:var(--primary);
    font-size:24px;
}

.achievement span{
    color:var(--muted);
    font-size:11px;
}

/* =========================
   الإشعارات
========================= */

.notice{
    display:flex;
    align-items:flex-start;
    gap:12px;
    padding:15px 0;
    border-bottom:1px solid var(--border);
}

.notice:last-child{
    border-bottom:0;
}

.notice-icon{
    width:44px;
    height:44px;
    flex-shrink:0;
    display:flex;
    justify-content:center;
    align-items:center;
    border-radius:13px;
    background:#efedff;
}

.notice strong{
    font-size:13px;
}

.notice p{
    color:var(--muted);
    font-size:11px;
    margin-top:3px;
}

/* =========================
   Modal
========================= */

.modal{
    position:fixed;
    inset:0;
    z-index:200;
    background:rgba(25,24,42,.5);
    display:flex;
    align-items:center;
    justify-content:center;
    padding:18px;
}

.modal-box{
    width:100%;
    max-width:480px;
    background:#fff;
    border-radius:25px;
    padding:25px;
    box-shadow:0 25px 70px rgba(0,0,0,.2);
}

.modal-head{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:20px;
}

.close-btn{
    width:35px;
    height:35px;
    border:0;
    border-radius:10px;
    background:#f2f2f6;
    font-size:20px;
}

.modal-box select{
    width:100%;
    padding:13px;
    border:1px solid var(--border);
    border-radius:13px;
    margin-bottom:15px;
    background:#fafaff;
}

/* Toast */

.toast{
    position:fixed;
    bottom:25px;
    left:50%;
    transform:translateX(-50%) translateY(20px);
    background:#27263a;
    color:#fff;
    padding:12px 18px;
    border-radius:13px;
    font-size:13px;
    opacity:0;
    pointer-events:none;
    transition:.3s;
    z-index:500;
}

.toast.show{
    opacity:1;
    transform:translateX(-50%) translateY(0);
}

/* =========================
   موبايل
========================= */

@media(max-width:1050px){

    .sidebar{
        transform:translateX(110%);
        transition:.25s;
    }

    .sidebar.open{
        transform:translateX(0);
    }

    .main{
        margin-right:0;
        padding:18px;
    }

    .mobile-menu{
        display:block;
    }

    .stats{
        grid-template-columns:repeat(2,1fr);
    }

    .dashboard-grid{
        grid-template-columns:1fr;
    }

    .planner-grid{
        grid-template-columns:repeat(2,1fr);
    }

    .subjects-grid{
        grid-template-columns:repeat(2,1fr);
    }
}

@media(max-width:600px){

    .setup{
        padding:12px;
    }

    .setup-card{
        padding:25px 18px;
    }

    .school-title{
        font-size:17px;
    }

    .platform-title{
        font-size:27px;
    }

    .welcome{
        padding:22px;
    }

    .welcome h1{
        font-size:22px;
    }

    .stats{
        gap:10px;
    }

    .stat{
        padding:15px;
    }

    .stat strong{
        font-size:20px;
    }

    .planner-grid,
    .subjects-grid{
        grid-template-columns:1fr;
    }

    .achievements{
        grid-template-columns:1fr;
    }

    .planner-info{
        align-items:flex-start;
        flex-direction:column;
    }

    .topbar{
        gap:10px;
    }

    .page-title{
        font-size:18px;
    }
}
</style>
</head>

<body>

<!-- =====================================================
     شاشة إعداد الطالبة
===================================================== -->

<section class="setup" id="setupScreen">

<div class="setup-card">

<div class="school-mark">أ</div>

<div class="school-title">
مدرسة الأورمان الإعدادية الثانوية بنات
</div>

<div class="platform-title">
SchoolHub
</div>

<p class="platform-subtitle">
منصتك الدراسية لتنظيم المذاكرة والمهام والمتابعة
</p>

<div class="form-group">
<label>اسم الطالبة</label>
<input id="studentName" type="text" placeholder="اكتبي اسمك">
</div>

<div class="form-group">
<label>الصف الدراسي</label>

<select id="gradeSelect">
<option value="">اختاري الصف الدراسي</option>

<option value="prep1">الصف الأول الإعدادي</option>
<option value="prep2">الصف الثاني الإعدادي</option>
<option value="prep3">الصف الثالث الإعدادي</option>

<option value="sec1">الصف الأول الثانوي</option>
<option value="sec2">الصف الثاني الثانوي — البكالوريا</option>
<option value="sec3">الصف الثالث الثانوي</option>

</select>
</div>

<div class="form-group hidden" id="pathGroup">

<label>اختاري مسار البكالوريا</label>

<select id="pathSelect">

<option value="">اختاري المسار</option>

<option value="life">
طب وعلوم الحياة
</option>

<option value="engineering">
هندسة وعلوم الحاسب
</option>

<option value="business">
إدارة أعمال
</option>

<option value="arts">
آداب وفنون
</option>

</select>

</div>

<div class="form-group hidden" id="electiveGroup">

<label>اختاري المادة الاختيارية</label>

<select id="electiveSelect">

<option value="">
اختاري المادة الاختيارية
</option>

</select>

</div>

<div class="form-group hidden" id="languageGroup">

<label>اختاري اللغة الثانية</label>

<select id="languageSelect">

<option value="">اختاري اللغة</option>
<option value="فرنساوي">فرنساوي</option>
<option value="ألماني">ألماني</option>
<option value="إيطالي">إيطالي</option>
<option value="إسباني">إسباني</option>

</select>

</div>

<button class="primary-btn" id="startBtn">
دخول إلى منصتي ✨
</button>

</div>
</section>


<!-- =====================================================
     التطبيق
===================================================== -->

<div class="app hidden" id="app">

<aside class="sidebar">

<div class="brand">

<div class="brand-mark">أ</div>

<div>
<strong>SchoolHub</strong>
<small>الأورمان الإعدادية الثانوية بنات</small>
</div>

</div>

<div class="profile-card">

<strong id="sideName">الطالبة</strong>

<span id="sideGrade">الصف الدراسي</span>

</div>

<nav class="nav">

<button class="nav-btn active" data-page="home">
🏠 الرئيسية
</button>

<button class="nav-btn" data-page="planner">
📅 جدول المذاكرة
</button>

<button class="nav-btn" data-page="tasks">
✓ قائمة المهام
</button>

<button class="nav-btn" data-page="subjects">
📚 موادي
</button>

<button class="nav-btn" data-page="progress">
📊 تقدمي
</button>

<button class="nav-btn" data-page="notifications">
🔔 الإشعارات
</button>

</nav>

<div class="sidebar-bottom">

<button class="logout-btn" id="logoutBtn">
إعادة إعداد المنصة
</button>

</div>

</aside>


<main class="main">

<header class="topbar">

<div class="topbar-right">

<button class="mobile-menu" id="mobileMenu">
☰
</button>

<h1 class="page-title" id="pageTitle">
الرئيسية
</h1>

</div>

<div class="top-actions">

<button class="icon-btn" id="notificationBtn">
🔔
<span class="notification-dot" id="notificationDot"></span>
</button>

<div class="avatar" id="topAvatar">
أ
</div>

</div>

</header>


<!-- =====================================================
     الرئيسية
===================================================== -->

<section class="page active" id="page-home">

<div class="welcome">

<h1>
أهلًا يا <span id="welcomeName">طالبة</span> 👋
</h1>

<p id="welcomeMeta">
مدرسة الأورمان الإعدادية الثانوية بنات
</p>

</div>


<div class="stats">

<div class="stat">
<div class="stat-icon">✓</div>
<strong id="statTasks">0%</strong>
<span>إنجاز المهام</span>
</div>

<div class="stat">
<div class="stat-icon">📚</div>
<strong id="statSubjects">0</strong>
<span>المواد الدراسية</span>
</div>

<div class="stat">
<div class="stat-icon">📅</div>
<strong id="statDays">0</strong>
<span>أيام منظمة</span>
</div>

<div class="stat">
<div class="stat-icon">⭐</div>
<strong id="statPoints">0</strong>
<span>النقاط</span>
</div>

</div>


<div class="dashboard-grid">
