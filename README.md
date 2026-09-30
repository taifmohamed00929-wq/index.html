<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SchoolHub | منصتي الدراسية</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#f7f8fc;
  --card:#ffffff;
  --primary:#6c63d9;
  --primary2:#8179e8;
  --text:#202336;
  --muted:#777b91;
  --border:#e8e9f1;
  --success:#36a269;
  --danger:#e05b68;
  --shadow:0 12px 35px rgba(45,45,80,.08);
  --radius:22px;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  font-family:"Cairo",sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
}

button,input,select{
  font-family:inherit;
}

button{
  cursor:pointer;
  border:0;
}

.hidden{
  display:none!important;
}

/* =========================
   SETUP
========================= */

.setup{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:25px;
  background:
    radial-gradient(circle at 10% 20%,#e8e5ff 0,transparent 30%),
    radial-gradient(circle at 90% 80%,#f4e0ff 0,transparent 30%),
    var(--bg);
}

.setup-box{
  width:100%;
  max-width:720px;
  background:white;
  border:1px solid var(--border);
  border-radius:30px;
  padding:42px;
  box-shadow:var(--shadow);
}

.logo{
  display:flex;
  align-items:center;
  gap:14px;
  margin-bottom:30px;
}

.logo-icon{
  width:58px;
  height:58px;
  border-radius:18px;
  background:linear-gradient(135deg,var(--primary),#a49df7);
  color:white;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:28px;
  font-weight:800;
}

.logo h1{
  font-size:25px;
}

.logo p{
  color:var(--muted);
  font-size:13px;
}

.setup-title{
  font-size:30px;
  margin-bottom:8px;
}

.setup-subtitle{
  color:var(--muted);
  margin-bottom:28px;
}

.field{
  margin-bottom:18px;
}

.field label{
  display:block;
  font-weight:700;
  margin-bottom:8px;
}

.field input,
.field select{
  width:100%;
  padding:14px 16px;
  border:1px solid var(--border);
  border-radius:14px;
  outline:none;
  background:#fbfbfe;
  font-size:15px;
  color:var(--text);
}

.field input:focus,
.field select:focus{
  border-color:var(--primary);
  box-shadow:0 0 0 4px rgba(108,99,217,.1);
}

.start-btn{
  width:100%;
  padding:16px;
  border-radius:15px;
  color:white;
  font-size:16px;
  font-weight:800;
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  margin-top:8px;
  transition:.2s;
}

.start-btn:hover{
  transform:translateY(-2px);
}

/* =========================
   APP
========================= */

.app{
  min-height:100vh;
}

.sidebar{
  position:fixed;
  right:0;
  top:0;
  bottom:0;
  width:260px;
  background:white;
  border-left:1px solid var(--border);
  padding:24px 16px;
  z-index:20;
}

.side-logo{
  display:flex;
  align-items:center;
  gap:10px;
  padding:0 8px 24px;
  border-bottom:1px solid var(--border);
}

.side-logo-icon{
  width:43px;
  height:43px;
  border-radius:13px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:var(--primary);
  color:white;
  font-weight:800;
}

.side-logo strong{
  font-size:17px;
}

.side-logo small{
  display:block;
  color:var(--muted);
  font-size:10px;
}

.profile{
  margin:18px 0;
  padding:14px;
  background:#f7f7fd;
  border-radius:16px;
  display:flex;
  align-items:center;
  gap:11px;
}

.avatar{
  width:43px;
  height:43px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  background:#e8e5ff;
  color:var(--primary);
  font-weight:800;
}

.profile strong{
  font-size:13px;
}

.profile small{
  display:block;
  color:var(--muted);
  font-size:10px;
}

.nav{
  display:flex;
  flex-direction:column;
  gap:5px;
}

.nav button{
  background:transparent;
  text-align:right;
  padding:12px 14px;
  border-radius:13px;
  color:#676b7e;
  font-size:14px;
  transition:.2s;
}

.nav button:hover{
  background:#f5f4fd;
  color:var(--primary);
}

.nav button.active{
  background:#eeeafe;
  color:var(--primary);
  font-weight:800;
}

.side-bottom{
  position:absolute;
  bottom:20px;
  left:16px;
  right:16px;
}

.logout{
  width:100%;
  background:#fff0f1;
  color:var(--danger);
  padding:11px;
  border-radius:12px;
}

/* =========================
   MAIN
========================= */

.main{
  margin-right:260px;
  min-height:100vh;
}

.topbar{
  height:76px;
  background:white;
  border-bottom:1px solid var(--border);
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:0 35px;
  position:sticky;
  top:0;
  z-index:10;
}

.topbar h2{
  font-size:20px;
}

.top-actions{
  display:flex;
  align-items:center;
  gap:12px;
}

.icon-btn{
  width:42px;
  height:42px;
  border-radius:13px;
  background:#f6f6fb;
  color:#55596e;
  font-size:18px;
}

.mobile-menu{
  display:none;
}

.content{
  padding:32px;
  max-width:1400px;
  margin:auto;
}

/* =========================
   PAGE
========================= */

.page{
  display:none;
}

.page.active{
  display:block;
}

/* =========================
   HERO
========================= */

.hero{
  background:linear-gradient(135deg,#6c63d9,#8981ed);
  color:white;
  border-radius:28px;
  padding:32px;
  position:relative;
  overflow:hidden;
  margin-bottom:24px;
}

.hero:after{
  content:"";
  position:absolute;
  width:250px;
  height:250px;
  border-radius:50%;
  background:rgba(255,255,255,.08);
  left:-70px;
  top:-100px;
}

.hero small{
  opacity:.8;
}

.hero h1{
  font-size:29px;
  margin:5px 0;
}

.hero p{
  opacity:.9;
}

/* =========================
   STATS
========================= */

.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
  margin-bottom:25px;
}

.stat{
  background:white;
  border:1px solid var(--border);
  border-radius:20px;
  padding:20px;
  box-shadow:0 5px 20px rgba(30,30,70,.03);
}

.stat-icon{
  font-size:22px;
  margin-bottom:10px;
}

.stat strong{
  display:block;
  font-size:25px;
}

.stat span{
  color:var(--muted);
  font-size:12px;
}

/* =========================
   GRID
========================= */

.two-col{
  display:grid;
  grid-template-columns:1.3fr 1fr;
  gap:20px;
}

.card{
  background:white;
  border:1px solid var(--border);
  border-radius:22px;
  padding:23px;
  margin-bottom:20px;
}

.card-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:18px;
}

.card-head h3{
  font-size:18px;
}

.card-head button{
  background:#eeeafe;
  color:var(--primary);
  padding:8px 12px;
  border-radius:10px;
  font-weight:700;
}

/* =========================
   TASKS
========================= */

.task{
  display:flex;
  align-items:center;
  gap:12px;
  padding:13px 0;
  border-bottom:1px solid #f0f0f5;
}

.task:last-child{
  border-bottom:0;
}

.check{
  width:25px;
  height:25px;
  border:2px solid #d5d6e2;
  border-radius:8px;
  background:white;
  flex-shrink:0;
}

.check.done{
  background:var(--success);
  border-color:var(--success);
  color:white;
}

.task-text{
  flex:1;
}

.task small{
  color:var(--muted);
}

/* =========================
   MINI PLANNER
========================= */

.mini-days{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:8px;
}

.mini-day{
  padding:12px 5px;
  border:1px solid var(--border);
  border-radius:13px;
  text-align:center;
}

.mini-day strong{
  display:block;
  font-size:12px;
}

.mini-day span{
  display:block;
  color:var(--muted);
  font-size:10px;
  margin-top:5px;
}

/* =========================
   PAGES
========================= */

.page-title{
  margin-bottom:6px;
  font-size:28px;
}

.page-desc{
  color:var(--muted);
  margin-bottom:25px;
}

/* =========================
   PLANNER
========================= */

.planner-tools{
  background:white;
  border:1px solid var(--border);
  border-radius:18px;
  padding:15px 18px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:20px;
}

.switch{
  display:flex;
  align-items:center;
  gap:10px;
}

.switch input{
  width:20px;
  height:20px;
  accent-color:var(--primary);
}

.primary-btn{
  background:var(--primary);
  color:white;
  padding:11px 17px;
  border-radius:12px;
  font-weight:700;
}

.planner{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:12px;
}

.day-card{
  background:white;
  border:1px solid var(--border);
  border-radius:19px;
  padding:14px;
  min-height:220px;
}

.day-card.rest{
  background:#f8f7ff;
}

.day-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding-bottom:12px;
  border-bottom:1px solid var(--border);
  margin-bottom:12px;
}

.day-head strong{
  font-size:14px;
}

.day-head span{
  font-size:10px;
  color:var(--muted);
}

.subject{
  background:#f1efff;
  color:#514ab4;
  border-radius:10px;
  padding:9px;
  margin-bottom:8px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  font-size:12px;
}

.subject button{
  background:transparent;
  color:#a19dc6;
  font-size:16px;
}

.add-subject{
  width:100%;
  padding:10px;
  border:1px dashed #c9c6e8;
  background:transparent;
  color:var(--primary);
  border-radius:10px;
  margin-top:3px;
}

.rest-box{
  text-align:center;
  color:var(--muted);
  padding-top:50px;
}

.rest-box div{
  font-size:32px;
  margin-bottom:8px;
}

/* =========================
   SUBJECTS
========================= */

.subjects{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
}

.subject-card{
  background:white;
  border:1px solid var(--border);
  border-radius:20px;
  padding:22px;
  transition:.2s;
}

.subject-card:hover{
  transform:translateY(-3px);
  box-shadow:var(--shadow);
}

.subject-icon{
  width:48px;
  height:48px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:#f0efff;
  border-radius:15px;
  font-size:22px;
  margin-bottom:15px;
}

.subject-card h3{
  font-size:16px;
  margin-bottom:5px;
}

.subject-card p{
  color:var(--muted);
  font-size:11px;
}

/* =========================
   PROGRESS
========================= */

.progress-card{
  display:grid;
  grid-template-columns:240px 1fr;
  gap:35px;
  align-items:center;
}

.circle{
  width:190px;
  height:190px;
  border-radius:50%;
  background:conic-gradient(var(--primary) 0deg,#eeeeF5 0deg);
  display:flex;
  align-items:center;
  justify-content:center;
  margin:auto;
}

.circle-inner{
  width:145px;
  height:145px;
  border-radius:50%;
  background:white;
  display:flex;
  align-items:center;
  justify-content:center;
  flex-direction:column;
}

.circle-inner strong{
  font-size:32px;
}

.circle-inner span{
  color:var(--muted);
  font-size:11px;
}

.progress-line{
  height:12px;
  background:#eeeef5;
  border-radius:20px;
  overflow:hidden;
}

.progress-fill{
  height:100%;
  width:0;
  background:linear-gradient(90deg,var(--primary),#a39df3);
  border-radius:20px;
  transition:.4s;
}

.achievement{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
  margin-top:20px;
}

.achievement div{
  background:#f8f8fc;
  border-radius:16px;
  padding:18px;
  text-align:center;
}

.achievement strong{
  display:block;
  font-size:25px;
  color:var(--primary);
}

.achievement span{
  color:var(--muted);
  font-size:11px;
}

/* =========================
   MODAL
========================= */

.modal{
  position:fixed;
  inset:0;
  background:rgba(25,25,45,.5);
  display:flex;
  align-items:center;
  justify-content:center;
  padding:20px;
  z-index:100;
}

.modal-box{
  width:100%;
  max-width:480px;
  background:white;
  border-radius:25px;
  padding:25px;
}

.modal-head{
  display:flex;
  justify-content:space-between;
  margin-bottom:20px;
}

.close{
  background:#f1f1f6;
  width:35px;
  height:35px;
  border-radius:10px;
}

/* =========================
   EMPTY
========================= */

.empty{
  text-align:center;
  padding:30px 10px;
  color:var(--muted);
}

/* =========================
   TOAST
========================= */

.toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translate(-50%,30px);
  background:#202336;
  color:white;
  padding:13px 20px;
  border-radius:13px;
  opacity:0;
  pointer-events:none;
  transition:.25s;
  z-index:200;
  font-size:13px;
}

.toast.show{
  opacity:1;
  transform:translate(-50%,0);
}

/* =========================
   MOBILE
========================= */

@media(max-width:1050px){
  .planner{
    grid-template-columns:repeat(4,1fr);
  }

  .subjects{
    grid-template-columns:repeat(3,1fr);
  }

  .two-col{
    grid-template-columns:1fr;
  }
}

@media(max-width:800px){
  .sidebar{
    transform:translateX(100%);
    transition:.25s;
  }

  .sidebar.open{
    transform:translateX(0);
  }

  .main{
    margin-right:0;
  }

  .mobile-menu{
    display:block;
  }

  .topbar{
    padding:0 18px;
  }

  .content{
    padding:20px 15px;
  }

  .stats{
    grid-template-columns:repeat(2,1fr);
  }

  .planner{
    grid-template-columns:repeat(2,1fr);
  }

  .subjects{
    grid-template-columns:repeat(2,1fr);
  }

  .progress-card{
    grid-template-columns:1fr;
  }

  .setup-box{
    padding:28px 20px;
  }

  .setup-title{
    font-size:24px;
  }
}

@media(max-width:500px){
  .hero{
    padding:24px 20px;
  }

  .hero h1{
    font-size:23px;
  }

  .mini-days{
    grid-template-columns:repeat(4,1fr);
  }

  .planner{
    grid-template-columns:1fr;
  }

  .subjects{
    grid-template-columns:1fr;
  }

  .achievement{
    grid-template-columns:1fr;
  }
}
</style>
</head>

<body>

<!-- =========================
     SETUP
========================= -->

<section class="setup" id="setup">

  <div class="setup-box">

    <div class="logo">
      <div class="logo-icon">S</div>
      <div>
        <h1>SchoolHub</h1>
        <p>منصتك الدراسية الذكية</p>
      </div>
    </div>

    <h2 class="setup-title">ابدئي تنظيم دراستك</h2>

    <p class="setup-subtitle">
      اختاري بياناتك الدراسية علشان نجهز لكِ المنصة المناسبة.
    </p>

    <div class="field">
      <label>اسم الطالبة</label>
      <input id="studentName" type="text" placeholder="اكتبي اسمك">
    </div>

    <div class="field">
      <label>الصف الدراسي</label>

      <select id="grade">
        <option value="">اختاري الصف</option>
        <option value="prep1">الصف الأول الإعدادي</option>
        <option value="prep2">الصف الثاني الإعدادي</option>
        <option value="prep3">الصف الثالث الإعدادي</option>
        <option value="sec1">الصف الأول الثانوي</option>
        <option value="sec2">الصف الثاني الثانوي — البكالوريا</option>
        <option value="sec3">الصف الثالث الثانوي</option>
      </select>
    </div>

    <div class="field hidden" id="pathField">

      <label>المسار</label>

      <select id="path">
        <option value="">اختاري المسار</option>
        <option value="life">طب وعلوم الحياة</option>
        <option value="engineering">هندسة وعلوم الحاسب</option>
        <option value="business">إدارة أعمال</option>
        <option value="arts">آداب وفنون</option>
      </select>

    </div>

    <div class="field hidden" id="electiveField">

      <label>المادة الاختيارية</label>

      <select id="elective">
        <option value="">اختاري المادة</option>
      </select>

    </div>

    <div class="field hidden" id="languageField">

      <label>اللغة الثانية</label>

      <select id="language">
        <option value="">اختاري اللغة</option>
        <option>فرنساوي</option>
        <option>ألماني</option>
        <option>إيطالي</option>
        <option>إسباني</option>
      </select>

    </div>

    <button class="start-btn" id="start">
      دخول إلى SchoolHub
    </button>

  </div>

</section>


<!-- =========================
     APP
========================= -->

<div class="app hidden" id="app">

  <aside class="sidebar" id="sidebar">

    <div class="side-logo">
      <div class="side-logo-icon">S</div>
      <div>
        <strong>SchoolHub</strong>
        <small>منصتك الدراسية</small>
      </div>
    </div>

    <div class="profile">
      <div class="avatar" id="avatar">س</div>
      <div>
        <strong id="sideName">الطالبة</strong>
        <small id="sideGrade">الصف الدراسي</small>
      </div>
    </div>

    <nav class="nav">

      <button class="active" data-page="home">
        🏠 الرئيسية
      </button>

      <button data-page="planner">
        📅 جدول المذاكرة
      </button>

      <button data-page="tasks">
        ✓ قائمة المهام
      </button>

      <button data-page="subjects">
        📚 موادي
      </button>

      <button data-page="progress">
        📈 تقدمي
      </button>

      <button data-page="notifications">
        🔔 الإشعارات
      </button>

    </nav>

    <div class="side-bottom">
      <button class="logout" id="logout">
        تسجيل الخروج
      </button>
    </div>

  </aside>


  <main class="main">

    <header class="topbar">

      <div style="display:flex;align-items:center;gap:12px">

        <button class="icon-btn mobile-menu" id="mobileMenu">
          ☰
        </button>

        <h2 id="pageTitle">الرئيسية</h2>

      </div>

      <div class="top-actions">

        <button class="icon-btn">
          🔔
        </button>

        <div class="avatar" id="topAvatar">س</div>

      </div>

    </header>


    <div class="content">

      <!-- HOME -->

      <section class="page active" id="page-home">

        <div class="hero">

          <small>أهلًا بيكي 👋</small>

          <h1 id="welcome">
            أهلاً بكِ في SchoolHub
          </h1>

          <p id="welcomeMeta">
            منصتك لتنظيم الدراسة والمتابعة.
          </p>

        </div>


        <div class="stats">

          <div class="stat">
            <div class="stat-icon">✓</div>
            <strong id="taskPercent">0%</strong>
            <span>إنجاز المهام</span>
          </div>

          <div class="stat">
            <div class="stat-icon">📚</div>
            <strong id="subjectCount">0</strong>
            <span>المواد</span>
          </div>

          <div class="stat">
            <div class="stat-icon">📅</div>
            <strong id="studyDays">0</strong>
            <span>أيام المذاكرة</span>
          </div>

          <div class="stat">
            <div class="stat-icon">⭐</div>
            <strong id="points">0</strong>
            <span>نقاط الإنجاز</span>
          </div>

        </div>


        <div class="two-col">

          <div class="card">

            <div class="card-head">

              <h3>مهامك الحالية</h3>

              <button data-jump="tasks">
                عرض الكل
              </button>

            </div>

            <div id="homeTasks"></div>

          </div>


          <div class="card">

            <div class="card-head">
              <h3>جدول الأسبوع</h3>

              <button data-jump="planner">
                تعديل
              </button>
            </div>

            <div class="mini-days" id="miniDays"></div>

          </div>

        </div>

      </section>


      <!-- PLANNER -->

      <section class="page" id="page-planner">

        <h1 class="page-title">جدول المذاكرة</h1>

        <p class="page-desc">
          رتبي المواد على أيام الأسبوع بالطريقة اللي تناسبك — من غير مواعيد إجبارية.
        </p>

        <div class="planner-tools">

          <label class="switch">
            <input type="checkbox" id="fridayOff">
            <span>الجمعة يوم راحة</span>
          </label>

          <button class="primary-btn" id="savePlanner">
            حفظ الجدول
          </button>

        </div>

        <div class="planner" id="planner"></div>

      </section>


      <!-- TASKS -->

      <section class="page" id="page-tasks">

        <h1 class="page-title">قائمة المهام</h1>

        <p class="page-desc">
          اكتبي كل اللي محتاجة تخلصيه، وحددي اليوم فقط. الوقت مفتوح ليكي.
        </p>

        <div class="card">

          <div class="card-head">

            <h3>مهامي</h3>

            <button class="primary-btn" id="addTask">
              + مهمة جديدة
            </button>

          </div>

          <div id="tasks"></div>

        </div>

      </section>


      <!-- SUBJECTS -->

      <section class="page" id="page-subjects">

        <h1 class="page-title">موادي</h1>

        <p class="page-desc" id="subjectsDescription">
          المواد الخاصة بصفك الدراسي.
        </p>

        <div class="subjects" id="subjects"></div>

      </section>


      <!-- PROGRESS -->

      <section class="page" id="page-progress">

        <h1 class="page-title">تقدمي</h1>

        <p class="page-desc">
          تابعي انتظامك في تنظيم الدراسة وإنجاز المهام.
        </p>

        <div class="card progress-card">

          <div>

            <div class="circle" id="circle">

              <div class="circle-inner">

                <strong id="progressNumber">0%</strong>

                <span>التقدم</span>

              </div>

            </div>

          </div>

          <div>

            <h3 style="margin-bottom:10px">
              مستوى تنظيمك الدراسي
            </h3>

            <p style="color:var(--muted);font-size:13px;margin-bottom:18px">
              النسبة بتتحسب من إنجاز المهام وتنظيم أيام المذاكرة.
            </p>

            <div class="progress-line">
              <div class="progress-fill" id="progressFill"></div>
            </div>

            <div class="achievement">

              <div>
                <strong id="doneTasks">0</strong>
                <span>مهام مكتملة</span>
              </div>

              <div>
                <strong id="plannedDays">0</strong>
                <span>أيام منظمة</span>
              </div>

              <div>
                <strong id="progressPoints">0</strong>
                <span>نقاط</span>
              </div>

            </div>

          </div>

        </div>

      </section>


      <!-- NOTIFICATIONS -->

      <section class="page" id="page-notifications">

        <h1 class="page-title">الإشعارات</h1>

        <p class="page-desc">
          آخر التنبيهات والملاحظات الخاصة بالمنصة.
        </p>

        <div id="notifications"></div>

      </section>

    </div>

  </main>

</div>


<!-- TASK MODAL -->

<div class="modal hidden" id="taskModal">

  <div class="modal-box">

    <div class="modal-head">

      <h3>إضافة مهمة جديدة</h3>

      <button class="close" id="closeModal">×</button>

    </div>

    <div class="field">

      <label>اسم المهمة</label>

      <input id="taskText" placeholder="مثال: مراجعة درس الرياضيات">

    </div>

    <div class="field">

      <label>اليوم</label>

      <select id="taskDay">

        <option>السبت</option>
        <option>الأحد</option>
        <option>الاثنين</option>
        <option>الثلاثاء</option>
        <option>الأربعاء</option>
        <option>الخميس</option>
        <option>الجمعة</option>

      </select>

    </div>

    <button class="start-btn" id="confirmTask">
      إضافة المهمة
    </button>

  </div>

</div>


<!-- SUBJECT MODAL -->

<div class="modal hidden" id="subjectModal">

  <div class="modal-box">

    <div class="modal-head">

      <h3>إضافة مادة للجدول</h3>

      <button class="close" id="closeSubjectModal">×</button>

    </div>

    <div class="field">

      <label>اختاري المادة</label>

      <select id="subjectChoice"></select>

    </div>

    <button class="start-btn" id="confirmSubject">
      إضافة للجدول
    </button>

  </div>

</div>


<div class="toast" id="toast"></div>


<script>
/* ==========================================
   DATA
========================================== */

const DAYS=[
  "السبت",
  "الأحد",
  "الاثنين",
  "الثلاثاء",
  "الأربعاء",
  "الخميس",
  "الجمعة"
];

const SUBJECTS={
  prep1:["عربي","English","دراسات","رياضيات","علوم","دين","ICT"],
  prep2:["عربي","English","دراسات","رياضيات","علوم","دين","ICT"],
  prep3:["عربي","English","دراسات","رياضيات","علوم","دين","ICT"],

  sec1:[
    "عربي",
    "تاريخ",
    "English",
    "فلسفة ومنطق",
    "دين",
    "علوم متكاملة",
    "رياضيات",
    "برمجة"
  ],

  sec3:[
    "عربي",
    "English",
    "تاريخ",
    "رياضيات",
    "فيزياء",
    "كيمياء",
    "لغة ثانية"
  ]
};

const PATHS={
  life:"طب وعلوم الحياة",
  engineering:"هندسة وعلوم الحاسب",
  business:"إدارة أعمال",
  arts:"آداب وفنون"
};

const ELECTIVES={
  life:["رياضيات","فيزياء"],
  engineering:["برمجة","كيمياء"],
  business:["محاسبة","إدارة أعمال"],
  arts:["لغة ثانية","علم نفس"]
};

const GRADE_NAMES={
  prep1:"الصف الأول الإعدادي",
  prep2:"الصف الثاني الإعدادي",
  prep3:"الصف الثالث الإعدادي",
  sec1:"الصف الأول الثانوي",
  sec2:"الصف الثاني الثانوي — البكالوريا",
  sec3:"الصف الثالث الثانوي"
};


/* ==========================================
   STATE
========================================== */

let state=
JSON.parse(localStorage.getItem("schoolHub")) || null;

let selectedPlannerDay=null;


/* ==========================================
   HELPERS
========================================== */

const $=id=>document.getElementById(id);

function save(){
  localStorage.setItem(
    "schoolHub",
    JSON.stringify(state)
  );
}

function toast(message){

  const box=$("toast");

  box.textContent=message;

  box.classList.add("show");

  setTimeout(()=>{
    box.classList.remove("show");
  },2200);
}

function escapeHTML(text){

  return String(text)
    .replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");
}


/* ==========================================
   GET SUBJECTS
========================================== */

function getSubjects(){

  if(!state) return [];

  if(state.grade!=="sec2"){
    return SUBJECTS[state.grade] || [];
  }

  let result=[
    "عربي",
    "English",
    "تاريخ"
  ];

  if(state.elective){
    result.push(state.elective);
  }

  if(
    state.path==="arts" &&
    state.elective==="لغة ثانية" &&
    state.language
  ){
    result.push(state.language);
  }

  return [...new Set(result)];
}


/* ==========================================
   SETUP
========================================== */

$("grade").addEventListener("change",function(){

  const grade=this.value;

  $("pathField")
    .classList.toggle(
      "hidden",
      grade!=="sec2"
    );

  $("electiveField")
    .classList.add("hidden");

  $("languageField")
    .classList.add("hidden");

});


$("path").addEventListener("change",function(){

  const path=this.value;

  if(!path){

    $("electiveField")
      .classList.add("hidden");

    return;
  }

  $("electiveField")
    .classList.remove("hidden");

  $("elective").innerHTML=
    `<option value="">اختاري المادة</option>`+
    ELECTIVES[path]
      .map(x=>`<option>${x}</option>`)
      .join("");

});


$("elective").addEventListener("change",function(){

  const arts=
    $("path").value==="arts";

  const second=
    this.value==="لغة ثانية";

  $("languageField")
    .classList.toggle(
      "hidden",
      !(arts && second)
    );

});


$("start").addEventListener("click",function(){

  const name=
    $("studentName").value.trim();

  const grade=
    $("grade").value;

  const path=
    $("path").value;

  const elective=
    $("elective").value;

  const language=
    $("language").value;


  if(!name){
    toast("اكتبي اسمك الأول");
    return;
  }

  if(!grade){
    toast("اختاري الصف الدراسي");
    return;
  }

  if(grade==="sec2" && !path){
    toast("اختاري مسار البكالوريا");
    return;
  }

  if(grade==="sec2" && !elective){
    toast("اختاري المادة الاختيارية");
    return;
  }

  if(
    grade==="sec2" &&
    path==="arts" &&
    elective==="لغة ثانية" &&
    !language
  ){
    toast("اختاري اللغة الثانية");
    return;
  }


  const planner={};

  DAYS.forEach(day=>{
    planner[day]=[];
  });


  state={
    name,
    grade,
    path:grade==="sec2"?path:null,
    elective:grade==="sec2"?elective:null,
    language:
      grade==="sec2" &&
      path==="arts" &&
      elective==="لغة ثانية"
        ?language
        :null,

    planner,
    fridayOff:true,
    tasks:[],
    points:0
  };


  save();

  showApp();

  toast("تم تجهيز منصتك بنجاح ✨");

});


/* ==========================================
   SHOW APP
========================================== */

function showApp(){

  $("setup").classList.add("hidden");

  $("app").classList.remove("hidden");

  render();
}


/* ==========================================
   RENDER ALL
========================================== */

function render(){

  if(!state)return;

  $("sideName").textContent=
    state.name;

  $("sideGrade").textContent=
    GRADE_NAMES[state.grade];

  $("avatar").textContent=
    state.name.charAt(0);

  $("topAvatar").textContent=
    state.name.charAt(0);

  $("welcome").textContent=
    `أهلاً ${state.name} 👋`;

  let meta=
    GRADE_NAMES[state.grade];

  if(state.path){
    meta+=
      " • "+
      PATHS[state.path];
  }

  $("welcomeMeta").textContent=
    meta;

  renderHome();
  renderPlanner();
  renderTasks();
  renderSubjects();
  renderProgress();
  renderNotifications();
}


/* ==========================================
   HOME
========================================== */

function renderHome(){

  const tasks=state.tasks;

  const completed=
    tasks.filter(t=>t.done).length;

  const percentage=
    tasks.length
      ?Math.round(
        completed/tasks.length*100
      )
      :0;


  $("taskPercent").textContent=
    percentage+"%";

  $("subjectCount").textContent=
    getSubjects().length;

  $("studyDays").textContent=
    DAYS.filter(
      day=>state.planner[day].length
    ).length;

  $("points").textContent=
    state.points;


  const active=
    tasks
      .filter(t=>!t.done)
      .slice(0,5);


  $("homeTasks").innerHTML=
    active.length
      ?active.map(taskHTML).join("")
      :`<div class="empty">
          مفيش مهام حالية 🎉
        </div>`;


  $("miniDays").innerHTML=
    DAYS.map(day=>{

      const count=
        state.planner[day].length;

      const rest=
        day==="الجمعة" &&
        state.fridayOff;

      return `
        <div class="mini-day">

          <strong>${day}</strong>

          <span>
            ${
              rest
              ?"راحة 🌿"
              :count+" مواد"
            }
          </span>

        </div>
      `;

    }).join("");

}


/* ==========================================
   TASK HTML
========================================== */

function taskHTML(task){

  return `
    <div class="task">

      <button
        class="check ${task.done?"done":""}"
        onclick="toggleTask('${task.id}')"
      >
        ${task.done?"✓":""}
      </button>

      <span class="task-text">
        ${escapeHTML(task.text)}
      </span>

      <small>
        ${task.day}
      </small>

      <button
        onclick="deleteTask('${task.id}')"
        style="
          background:transparent;
          color:#d35b67;
          font-size:18px;
        "
      >
        ×
      </button>

    </div>
  `;
}


/* ==========================================
   TASKS
========================================== */

function renderTasks(){

  const list=
    state.tasks;

  $("tasks").innerHTML=
    list.length
      ?list.map(taskHTML).join("")
      :`
        <div class="empty">
          لسه مفيش مهام.
          <br>
          أضيفي أول مهمة وابدئي تنظيم يومك ✨
        </div>
      `;
}


function toggleTask(id){

  const task=
    state.tasks.find(t=>t.id===id);

  if(!task)return;

  task.done=!task.done;

  if(task.done){
    state.points+=5;
  }else{
    state.points=
      Math.max(
        0,
        state.points-5
      );
  }

  save();

  render();

  toast(
    task.done
      ?"أحسنتِ! المهمة خلصت ⭐"
      :"رجعت المهمة للقائمة"
  );
}


function deleteTask(id){

  state.tasks=
    state.tasks.filter(
      t=>t.id!==id
    );

  save();

  render();

  toast("تم حذف المهمة");
}


/* ==========================================
   TASK MODAL
========================================== */

$("addTask").addEventListener("click",()=>{

  $("taskModal")
    .classList.remove("hidden");

  $("taskText").focus();

});


$("closeModal").addEventListener("click",()=>{

  $("taskModal")
    .classList.add("hidden");

});


$("confirmTask").addEventListener("click",()=>{

  const text=
    $("taskText").value.trim();

  const day=
    $("taskDay").value;

  if(!text){
    toast("اكتبي اسم المهمة");
    return;
  }


  state.tasks.unshift({

    id:Date.now().toString(),

    text,

    day,

    done:false

  });


  $("taskText").value="";

  $("taskModal")
    .classList.add("hidden");

  save();

  render();

  toast("تمت إضافة المهمة ✓");

});


/* ==========================================
   PLANNER
========================================== */

function renderPlanner(){

  $("fridayOff").checked=
    state.fridayOff;


  $("planner").innerHTML=
    DAYS.map(day=>{

      const rest=
        day==="الجمعة" &&
        state.fridayOff;

      const subjects=
        state.planner[day] || [];


      return `
        <div class="day-card ${rest?"rest":""}">

          <div class="day-head">

            <strong>${day}</strong>

            <span>
              ${rest?"راحة":"مرن"}
            </span>

          </div>

          ${
            rest

            ?`
              <div class="rest-box">

                <div>🌿</div>

                يوم راحة

              </div>
            `

            :

            `
              ${
                subjects.length

                ?subjects.map(
                  (subject,index)=>`

                    <div class="subject">

                      <span>
                        ${escapeHTML(subject)}
                      </span>

                      <button
                        onclick="
                          removeSubject('${day}',${index})
                        "
                      >
                        ×
                      </button>

                    </div>
                  `
                ).join("")

                :

                `<div
                  style="
                    color:#aaa;
                    font-size:11px;
                    margin-bottom:10px;
                  "
                >
                  لم تتم إضافة مواد
                </div>`
              }

              <button
                class="add-subject"
                onclick="openSubjectModal('${day}')"
              >
                + إضافة مادة
              </button>
            `
          }

        </div>
      `;

    }).join("");
}


/* ==========================================
   SUBJECT MODAL
========================================== */

function openSubjectModal(day){

  selectedPlannerDay=day;

  $("subjectChoice").innerHTML=
    `<option value="">اختاري المادة</option>`+
    getSubjects()
      .map(
        subject=>
          `<option>${subject}</option>`
      )
      .join("");

  $("subjectModal")
    .classList.remove("hidden");
}


$("closeSubjectModal")
.addEventListener("click",()=>{

  $("subjectModal")
    .classList.add("hidden");

});


$("confirmSubject")
.addEventListener("click",()=>{

  const subject=
    $("subjectChoice").value;

  if(!subject){
    toast("اختاري المادة");
    return;
  }

  if(
    state.planner[selectedPlannerDay]
      .includes(subject)
  ){

    toast("المادة موجودة بالفعل في اليوم ده");
    return;
  }

  state.planner[selectedPlannerDay]
    .push(subject);

  save();

  $("subjectModal")
    .classList.add("hidden");

  render();

  toast("اتضافت المادة للجدول ✓");

});


function removeSubject(day,index){

  state.planner[day]
    .splice(index,1);

  save();

  render();

}


/* ==========================================
   FRIDAY
========================================== */

$("fridayOff")
.addEventListener("change",function(){

  state.fridayOff=
    this.checked;

  if(this.checked){

    state.planner["الجمعة"]=[];
  }

  save();

  render();

  toast(
    this.checked
      ?"الجمعة بقت يوم راحة 🌿"
      :"الجمعة رجعت متاحة"
  );

});


$("savePlanner")
.addEventListener("click",()=>{

  save();

  toast("تم حفظ جدولك الأسبوعي ✓");

});


/* ==========================================
   SUBJECTS
========================================== */

function renderSubjects(){

  const subjects=
    getSubjects();


  if(state.grade==="sec2"){

    $("subjectsDescription").textContent=
      `المواد الخاصة بمسار ${PATHS[state.path]} حسب اختياراتك.`;

  }else{

    $("subjectsDescription").textContent=
      "المواد الخاصة بصفك الدراسي.";

  }


  const icons=[
    "📚",
    "📖",
    "➗",
    "🧪",
    "💻",
    "🌍",
    "📝",
    "🎨",
    "🔬",
    "🌐"
  ];


  $("subjects").innerHTML=
    subjects.map(
      (subject,index)=>`

        <div class="subject-card">

          <div class="subject-icon">
            ${icons[index%icons.length]}
          </div>

          <h3>
            ${escapeHTML(subject)}
          </h3>

          <p>
            مادة ضمن خطتك الدراسية
          </p>

        </div>
      `
    ).join("");
}


/* ==========================================
   PROGRESS
========================================== */

function calculateProgress(){

  const tasks=
    state.tasks;

  const taskPart=
    tasks.length
      ?tasks.filter(t=>t.done).length/tasks.length
      :0;


  const days=
    DAYS.filter(
      day=>state.planner[day].length>0
    ).length;


  const dayPart=
    Math.min(days/6,1);


  return Math.round(
    (taskPart*.65+
    dayPart*.35)*100
  );
}


function renderProgress(){

  const percent=
    calculateProgress();


  $("progressNumber").textContent=
    percent+"%";


  $("progressFill").style.width=
    percent+"%";


  $("circle").style.background=
    `conic-gradient(
      var(--primary)
      ${percent*3.6}deg,
      #eeeef5
      ${percent*3.6}deg
    )`;


  $("doneTasks").textContent=
    state.tasks.filter(t=>t.done).length;


  $("plannedDays").textContent=
    DAYS.filter(
      day=>state.planner[day].length
    ).length;


  $("progressPoints").textContent=
    state.points;

}


/* ==========================================
   NOTIFICATIONS
========================================== */

function renderNotifications(){

  $("notifications").innerHTML=`

    <div class="card">

      <div class="task">

        <span style="font-size:23px">📢</span>

        <div class="task-text">

          <strong>
            أهلًا بيكي في SchoolHub
          </strong>

          <small style="display:block">
            ابدئي بإضافة موادك إلى جدول الأسبوع.
          </small>

        </div>

      </div>


      <div class="task">

        <span style="font-size:23px">🌿</span>

        <div class="task-text">

          <strong>
            جدولك مرن
          </strong>

          <small style="display:block">
            المنصة لا تفرض عليكِ وقتًا معينًا للمذاكرة.
          </small>

        </div>

      </div>


      <div class="task">

        <span style="font-size:23px">✨</span>

        <div class="task-text">

          <strong>
            حافظي على الاستمرارية
          </strong>

          <small style="display:block">
            أنجزي المهام الصغيرة واحدة واحدة.
          </small>

        </div>

      </div>

    </div>
  `;
}


/* ==========================================
   NAVIGATION
========================================== */

const titles={
  home:"الرئيسية",
  planner:"جدول المذاكرة",
  tasks:"قائمة المهام",
  subjects:"موادي",
  progress:"تقدمي",
  notifications:"الإشعارات"
};


function goPage(page){

  document
    .querySelectorAll(".page")
    .forEach(p=>{
      p.classList.remove("active");
    });


  $("page-"+page)
    .classList.add("active");


  document
    .querySelectorAll(".nav button")
    .forEach(button=>{
      button.classList.toggle(
        "active",
        button.dataset.page===page
      );
    });


  $("pageTitle").textContent=
    titles[page];


  $("sidebar")
    .classList.remove("open");

  window.scrollTo(0,0);

}


document
  .querySelectorAll(".nav button")
  .forEach(button=>{

    button.addEventListener(
      "click",
      ()=>{
        goPage(button.dataset.page);
      }
    );

  });


document
  .querySelectorAll("[data-jump]")
  .forEach(button=>{

    button.addEventListener(
      "click",
      ()=>{
        goPage(button.dataset.jump);
      }
    );

  });


/* ==========================================
   MOBILE
========================================== */

$("mobileMenu")
.addEventListener("click",()=>{

  $("sidebar")
    .classList.toggle("open");

});


/* ==========================================
   LOGOUT
========================================== */

$("logout")
.addEventListener("click",()=>{

  const confirmLogout=
    confirm(
      "هل تريدين تسجيل الخروج؟"
    );

  if(!confirmLogout)return;

  localStorage.removeItem("schoolHub");

  location.reload();

});


/* ==========================================
   START
========================================== */

if(state){

  showApp();

}else{

  $("setup")
    .classList.remove("hidden");

  $("app")
    .classList.add("hidden");

}

</script>

</body>
</html>
