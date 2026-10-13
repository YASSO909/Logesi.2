<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LOGI_SI - LIVE </title>
<style>
*{box-sizing:border-box} body{margin:0;background:#0a0a0a;color:#fff;font-family:sans-serif}
.card{background:#1a1a1a;border:1px solid #2a2a2a;border-radius:22px;padding:20px;margin-bottom:16px}
input,select,textarea{width:100%;background:#111;border:2px solid #333;color:#fff;border-radius:16px;margin:10px 0}
button{border:none;border-radius:16px;font-weight:bold;cursor:pointer}
.btn-red{background:#ff0000;color:#fff;width:100%}.btn-gray{background:#2a2a2a;color:#fff;width:100%}
.btn-green{background:#22c55e;color:#fff}.btn-gold{background:#f59e0b;color:#000}
.hidden{display:none!important}
.app{min-height:100vh}
.sidebar{background:#111;border-bottom:1px solid #222;padding:12px;display:flex;gap:8px;flex-wrap:wrap;align-items:center;position:sticky;top:0;z-index:10}
.menu-btn{background:#222;color:#aaa;padding:10px 14px;border-radius:12px;border:1px solid #333;font-size:13px}
.menu-btn.active{background:#fff;color:#000}
.menu-btn.logout{background:#1f1212;color:#ff5555;margin-right:auto}
.page{padding:14px;max-width:700px;margin:0 auto}
.admin-box{border:3px dashed #ff0000!important;background:#1f1212!important}
.big-select{padding:22px!important;font-size:22px!important;font-weight:bold;background:#000!important;border-color:#ffaa00!important}
.big-textarea{padding:22px!important;font-size:22px!important;min-height:180px!important;background:#000!important}
.big-btn{padding:24px!important;font-size:22px!important}
.task-big{background:#1c1c1c;border:1px solid #333;padding:18px;border-radius:18px;margin-top:12px;font-size:18px;line-height:1.6;display:flex;justify-content:space-between;gap:10px;white-space:pre-wrap}
.task-big.done{border-color:#22c55e;background:#122012}
.badge{background:#f59e0b;color:#000;padding:5px 12px;border-radius:20px;font-weight:bold;font-size:13px}
.notif-dot{background:#ff0000;color:#fff;padding:2px 8px;border-radius:50%;font-size:12px}
.user-follow{background:#111;border:1px solid #333;border-radius:16px;padding:12px;margin-top:12px}
.points-card{background:linear-gradient(135deg,#1a1a1a,#222);border:1px solid #f59e0b!important;text-align:center}
</style>
<script src="https://cdn.jsdelivr.net/npm/gun/gun.js"></script>
</head>
<body>
<div id="loginPage" style="min-height:100vh;display:flex;align-items:center;justify-content:center;padding:20px">
<div class="card" style="width:100%;max-width:400px">
<h2 style="color:#ff0000;margin:0;font-size:30px">LOGI_SI <span style="font-size:10px;background:#22c55e;padding:3px 8px;border-radius:10px;color:#fff">LIVE AUTO</span></h2>
<input id="userName" placeholder="الاسم" style="padding:18px;font-size:18px">
<input id="userPass" type="password" placeholder="الباسوورد" style="padding:18px;font-size:18px">
<select id="userRole" style="padding:18px;font-size:18px;border-color:#ff0000;background:#111">
  <option value="editor">إديتور (مش أدمن)</option>
  <option value="admin">أدمن</option>
</select>
<button class="btn-red big-btn" onclick="login()" style="margin-top:12px">دخول</button>
<p id="status" style="color:#22c55e;font-size:11px;text-align:center;margin-top:10px">متصل Live ✅</p>
</div>
</div>

<div id="dashboard" class="app hidden">
  <div class="sidebar">
    <b style="color:#ff0000">LOGI_SI</b>
    <button id="btn-view" class="menu-btn active" onclick="switchPage('viewPage')">👁️ مهامي</button>
    <button id="btn-points" class="menu-btn" onclick="switchPage('pointsPage')">⭐ نقاطي <span id="pointsBadge" class="badge">0</span></button>
    <button id="btn-notif" class="menu-btn" onclick="switchPage('notifPage')">🔔 إشعارات <span id="notifDot" class="notif-dot hidden">0</span></button>
    <button id="btn-admin" class="menu-btn" onclick="switchPage('adminPage')">👑 لوحة الأدمن</button>
    <span style="color:#888;font-size:12px"><span id="showName"></span> <span id="showRole" style="background:#333;padding:3px 10px;border-radius:20px"></span></span>
    <button class="menu-btn logout" onclick="logout()">🚪</button>
  </div>
  <div class="main">
    <div id="viewPage" class="page">
      <h2>📋 مهامي</h2><div id="myTasksList"></div>
      <h2 style="margin-top:20px">⏳ اللي المفروض ينزل</h2><div id="upcomingList"></div>
      <h2 style="margin-top:20px">✅ اللي نزل</h2><div id="publishedList"></div>
    </div>
    <div id="pointsPage" class="page hidden">
      <div class="card points-card"><h2>نقاطك</h2><div style="font-size:60px;font-weight:bold;color:#f59e0b" id="myPointsBig">0</div><p style="color:#888">كل مهمة = 5 نقاط</p><button class="btn-gold big-btn" onclick="requestSalary()" id="salaryBtn">حول 10 نقاط لزيادة راتب 💰</button><p id="salaryHint" style="color:#666;font-size:12px;margin-top:10px"></p></div>
      <div class="card"><h3>🏆 قايمة النقاط</h3><div id="leaderboardList"></div></div>
    </div>
    <div id="notifPage" class="page hidden"><h2>🔔 الإشعارات</h2><div id="notifList"></div></div>
    <div id="adminPage" class="page hidden">
      <div class="card admin-box"><h2 style="text-align:center">👑 توزيع المهام LIVE</h2><label style="color:#ff8888;font-weight:bold">اختار الحساب:</label><select id="assignTo" class="big-select"></select><label style="color:#ff8888;font-weight:bold;display:block;margin-top:10px">اكتب المهمة:</label><textarea id="taskInput" class="big-textarea" placeholder="اكتب المهمة..."></textarea><button class="btn-red big-btn" onclick="addTask()">إضافة المهمة 🚀</button></div>
      <div class="card"><h3>كل الحسابات</h3><div id="allAccountsList"></div></div>
      <div class="card" style="border-color:#22c55e"><h3>📊 متابعة كل واحد خلص ايه</h3><div id="adminFollowList"></div></div>
    </div>
  </div>
</div>

<script>
const gun = Gun(['https://gun-manhattan.herokuapp.com/gun', 'https://peer.wall.ng/gun']);
const root = gun.get('logesi_yassin_final_live_v10');
const usersGun = root.get('users');
const tasksGun = root.get('tasks');
const notifsGun = root.get('notifs');

let currentUser = JSON.parse(localStorage.getItem("ogi_user")||"null");
let users={}, tasks={}, notifs={};

function switchPage(id){
  if(id=='adminPage'&&!currentUser?.isAdmin){alert("للأدمن بس");return;}
  document.querySelectorAll('.page').forEach(p=>p.classList.add('hidden'));
  document.getElementById(id).classList.remove('hidden');
  document.querySelectorAll('.menu-btn').forEach(b=>b.classList.remove('active'));
  let btnId = id=='viewPage'?'btn-view':id=='pointsPage'?'btn-points':id=='notifPage'?'btn-notif':'btn-admin';
  document.getElementById(btnId).classList.add('active');
}

function login(){
  let n=document.getElementById("userName").value.trim();
  let p=document.getElementById("userPass").value.trim();
  let r=document.getElementById("userRole").value;
  if(!n||!p){alert("اكتب الاسم والباسوورد");return;}
  let isAdmin = r=='admin';
  let existing = users[n];
  let data = {name:n, pass:p, role:r, isAdmin:isAdmin, points: existing? existing.points||0 : 0, approvedRaises: existing? existing.approvedRaises||0 : 0};
  if(isAdmin) data.points=0;
  usersGun.get(n).put(data);
  currentUser=data;
  localStorage.setItem("ogi_user", JSON.stringify(currentUser));
  showDashboard();
}
function logout(){ localStorage.removeItem("ogi_user"); location.reload(); }

function showDashboard(){
  if(!currentUser) return;
  document.getElementById("loginPage").style.display="none";
  document.getElementById("dashboard").classList.remove("hidden");
  document.getElementById("showName").innerText=currentUser.name;
  document.getElementById("showRole").innerText=currentUser.isAdmin?"أدمن":"إديتور";
  document.getElementById("showRole").style.background=currentUser.isAdmin?"#ff0000":"#333";
  if(!currentUser.isAdmin) document.getElementById("btn-admin").classList.add("hidden");
  listen();
}

function listen(){
  usersGun.map().on((data, key)=>{
    if(!data ||!data.name){ delete users[key]; render(); return; }
    users[key]=data;
    if(currentUser && key==currentUser.name){ currentUser=data; localStorage.setItem("ogi_user", JSON.stringify(currentUser)); }
    render();
  });
  tasksGun.map().on((data, key)=>{
    if(!data ||!data.text){ delete tasks[key]; render(); return; }
    tasks[key]=data;
    render();
  });
  notifsGun.map().on((data, key)=>{
    if(!data ||!data.from){ delete notifs[key]; render(); return; }
    notifs[key]=data;
    render();
  });
}

function addTask(){
  let el=document.getElementById("taskInput"), sel=document.getElementById("assignTo");
  if(!el.value.trim()) return;
  let id = Date.now().toString();
  tasksGun.get(id).put({id:id, text:el.value, assignedTo:sel.value, status:'pending', createdAt:Date.now()});
  el.value="";
}
function completeTask(id){
  let t=tasks[id]; if(!t) return;
  let newStatus = t.status=='pending'?'done':'pending';
  tasksGun.get(id).put({status:newStatus});
  let u = users[t.assignedTo];
  if(u &&!u.isAdmin){
    let pts = u.points||0;
    pts = newStatus=='done'? pts+5 : Math.max(0, pts-5);
    usersGun.get(t.assignedTo).put({points:pts});
  }
}
function deleteTask(id){ tasksGun.get(id).put(null); }
function deleteUser(name){
  if(!confirm("تمسح "+name+" ؟")) return;
  usersGun.get(name).put(null);
  Object.keys(tasks).forEach(k=>{ if(tasks[k].assignedTo==name) tasksGun.get(k).put(null); });
  if(currentUser.name==name){ localStorage.removeItem("ogi_user"); location.reload(); }
}
function requestSalary(){
  if(currentUser.isAdmin) return alert("الأدمن مالهوش نقاط");
  if((currentUser.points||0)<10){alert("محتاج 10 نقاط");return;}
  let id=Date.now().toString();
  notifsGun.get(id).put({id:id, from:currentUser.name, points:10, status:'pending', time:new Date().toLocaleString()});
  alert("تم ارسال طلبك");
}
function approveNotif(id){
  let n=notifs[id]; if(!n) return;
  notifsGun.get(id).put({status:'approved'});
  let u=users[n.from];
  if(u){ usersGun.get(n.from).put({points:Math.max(0,(u.points||0)-10), approvedRaises:(u.approvedRaises||0)+1}); }
}

function render(){
  let sel=document.getElementById("assignTo"); if(!sel) return;
  let opt=""; Object.values(users).forEach(u=>{ if(!u.name) return; opt+='<option value="'+u.name+'">'+u.name+' - '+(u.isAdmin?'أدمن':'إديتور')+' ('+(u.isAdmin?0:(u.points||0))+' pts)</option>'; });
  sel.innerHTML=opt||'<option>مفيش حسابات لسه - اعمل حساب جديد</option>';

  let allTasks = Object.values(tasks).filter(t=>t.text);
  let my = allTasks.filter(t=>currentUser.isAdmin||t.assignedTo==currentUser.name);
  let a=""; my.forEach(t=>{ a+='<div class="task-big '+(t.status=='done'?'done':'')+'"><div><b>👤 '+t.assignedTo+':</b><br>'+t.text+(t.status=='done'?' <br><small style="color:#22c55e">خلصت ✔️</small>':'')+'</div><div style="display:flex;gap:6px"><button onclick="completeTask(\''+t.id+'\')" class="'+(t.status=='done'?'btn-gray':'btn-green')+'" style="padding:10px 16px">'+(t.status=='done'?'تراجع':'Done ✅')+'</button>'+(currentUser.isAdmin?'<button onclick="deleteTask(\''+t.id+'\')" style="background:#222;color:#fff;padding:10px;border-radius:10px">حذف</button>':'')+'</div></div>'; });
  document.getElementById("myTasksList").innerHTML=a||'<p style="color:#555;padding:20px">مفيش مهام</p>';
  document.getElementById("upcomingList").innerHTML='<p style="color:#555;padding:10px">سيبها فاضية زي ما انت عامل</p>';
  document.getElementById("publishedList").innerHTML='<p style="color:#555;padding:10px">سيبها فاضية زي ما انت عامل</p>';

  document.getElementById("myPointsBig").innerText=currentUser.isAdmin?0:(currentUser.points||0);
  document.getElementById("pointsBadge").innerText=currentUser.isAdmin?0:(currentUser.points||0);

  let lb=""; Object.values(users).filter(u=>u.name&&!u.isAdmin).sort((a,b)=>(b.points||0)-(a.points||0)).forEach((u,i)=>{ lb+='<div class="task-big"><span>'+(i==0?'🥇':i==1?'🥈':i==2?'🥉':'#'+(i+1))+' '+u.name+'</span><span class="badge">'+(u.points||0)+' pts</span></div>'; });
  document.getElementById("leaderboardList").innerHTML=lb||'<p style="color:#555">مفيش</p>';

  let btn=document.getElementById("salaryBtn"); if(btn){ btn.disabled=currentUser.isAdmin||(currentUser.points||0)<10; btn.style.opacity=btn.disabled?'0.4':'1'; document.getElementById("salaryHint").innerText=btn.disabled?"محتاج 10 نقاط":""; }

  let allNotifs = Object.values(notifs).filter(n=>n.from);
  let pending=allNotifs.filter(n=>n.status=='pending').length;
  let dot=document.getElementById("notifDot"); if(pending>0){dot.innerText=pending; dot.classList.remove('hidden');}else{dot.classList.add('hidden');}
  let nl=""; let relevant=currentUser.isAdmin?allNotifs:allNotifs.filter(n=>n.from==currentUser.name);
  [...relevant].reverse().forEach(n=>{ nl+='<div class="task-big"><div><b>💰 طلب - '+n.from+'</b><br><small>'+n.time+' - '+(n.status=='pending'?'قيد الانتظار ⏳':'تمت الموافقة ✅')+'</small></div>'+(currentUser.isAdmin&&n.status=='pending'?'<button onclick="approveNotif(\''+n.id+'\')" class="btn-green" style="padding:10px 16px">Approve ✅</button>':'')+'</div>'; });
  document.getElementById("notifList").innerHTML=nl||'<p style="color:#555">مفيش اشعارات</p>';

  let acc=""; Object.values(users).forEach(u=>{ if(!u.name) return; acc+='<div class="task-big" style="padding:12px;font-size:16px"><span>👤 '+u.name+' '+(u.isAdmin?'👑':'🟢')+' - '+(u.isAdmin?0:(u.points||0))+' pts</span><button onclick="deleteUser(\''+u.name+'\')" style="background:#ff0000;color:#fff;padding:6px 12px;border-radius:10px">حذف</button></div>'; });
  document.getElementById("allAccountsList").innerHTML=acc;

  let followHtml=""; Object.values(users).filter(u=>u.name&&!u.isAdmin).forEach(u=>{
    let uTasks = allTasks.filter(t=>t.assignedTo==u.name);
    let done = uTasks.filter(t=>t.status=='done');
    followHtml+=`<div class="user-follow"><div style="display:flex;justify-content:space-between"><b>👤 ${u.name}</b><span class="badge">${u.points||0} pts - ${done.length}/${uTasks.length}</span></div><div style="margin-top:8px;font-size:14px">${done.map(t=>`<div style="color:#22c55e">✅ ${t.text}</div>`).join('')}${uTasks.filter(t=>t.status=='pending').map(t=>`<div style="color:#aaa">⏳ ${t.text}</div>`).join('')}${uTasks.length==0?`<div style="color:#555">مفيش مهام لسه</div>`:""}</div></div>`;
  });
  document.getElementById("adminFollowList").innerHTML=followHtml||'<p style="color:#555">مفيش إديتورز لسه</p>';
}
if(currentUser) showDashboard();
</script>
</body>
</html>
