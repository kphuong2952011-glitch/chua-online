
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>An Tâm Tích Đức 🪷</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background: #f7f3e8;
    color: #344d3c;
}

header {
    background: #355b46;
    color: white;
    padding: 22px 15px;
    text-align: center;
}

header h1 {
    font-size: 25px;
}

header p {
    margin-top: 8px;
    font-size: 12px;
    color: #e5dfc7;
}

nav {
    background: #e9e2cf;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 8px;
    padding: 12px;
}

nav a {
    text-decoration: none;
    color: #405b47;
    font-size: 12px;
    padding: 8px 12px;
    border-radius: 20px;
}

nav a:hover {
    background: #d5ddca;
}

.hero {
    text-align: center;
    padding: 35px 15px;
    background: linear-gradient(#edf0e3, #f7f3e8);
}

.hero h2 {
    font-size: 25px;
    margin-bottom: 12px;
}

.hero p {
    font-size: 13px;
    line-height: 1.8;
    color: #718071;
}

.lotus {
    font-size: 65px;
    margin: 20px;
}

.container {
    max-width: 900px;
    margin: auto;
    padding: 15px;
}

.card {
    background: #fffdf7;
    padding: 23px;
    border-radius: 18px;
    margin-bottom: 18px;
    box-shadow: 0 4px 15px #344d3c10;
    border: 1px solid #e9e2d2;
}

.card h2 {
    font-size: 19px;
    margin-bottom: 15px;
}

.stats {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
}

.stat {
    background: #edf0e5;
    padding: 17px;
    border-radius: 13px;
    text-align: center;
}

.stat p {
    font-size: 12px;
    color: #748071;
}

.stat h3 {
    font-size: 24px;
    margin-top: 8px;
    color: #42694d;
}

.mallet-area {
    text-align: center;
    padding: 20px 0;
}

.mallet {
    width: 155px;
    height: 155px;
    border-radius: 50%;
    background: linear-gradient(145deg, #b88755, #79502f);
    border: 8px solid #e1d1ae;
    color: white;
    font-size: 65px;
    cursor: pointer;
    box-shadow: 0 8px 20px #60452c40;
    transition: 0.15s;
}

.mallet:active {
    transform: scale(.9);
}

.mallet-area p {
    margin-top: 14px;
    font-size: 12px;
    color: #778273;
}

button {
    font-family: inherit;
}

.btn {
    padding: 11px 18px;
    border: none;
    background: #466b50;
    color: white;
    border-radius: 10px;
    cursor: pointer;
    margin-top: 12px;
}

.task {
    background: #f0f2e9;
    padding: 13px;
    margin: 9px 0;
    border-radius: 10px;
    font-size: 13px;
}

.task input {
    margin-right: 9px;
    accent-color: #466b50;
}

.task.done {
    opacity: .6;
}

.activity {
    padding: 12px 0;
    border-bottom: 1px solid #eee9dd;
    font-size: 12px;
}

footer {
    text-align: center;
    padding: 25px;
    background: #355b46;
    color: #eee8d6;
    font-size: 12px;
    line-height: 2;
}

#authArea input {
    width: 100%;
    padding: 12px;
    margin: 7px 0;
    border: 1px solid #ddd8c9;
    border-radius: 9px;
}

.hidden {
    display: none;
}

</style>
</head>

<body>

<header>
    <h1>🪷 AN TÂM TÍCH ĐỨC</h1>
    <p>Một chút tĩnh tâm – Một chút yêu thương</p>
</header>

<nav>
    <a href="#home">Trang chủ</a>
    <a href="#mallet">Gõ mõ</a>
    <a href="#tasks">Việc thiện</a>
    <a href="#history">Nhật ký</a>
    <a href="#account">Tài khoản</a>
</nav>

<section class="hero" id="home">
    <div class="lotus">🪷</div>
    <h2>Gieo một niệm lành</h2>
    <p>
        Chào mừng em đến với An Tâm Tích Đức.<br>
        Hãy dành một chút thời gian để tâm mình được bình yên.
    </p>
</section>

<div class="container">

    <section class="card">
        <h2>🌿 Hành trình của em</h2>

        <div class="stats">
            <div class="stat">
                <p>Tổng lượt gõ mõ</p>
                <h3 id="taps">0</h3>
            </div>

            <div class="stat">
                <p>Điểm an lành</p>
                <h3 id="points">0</h3>
            </div>

            <div class="stat">
                <p>Ngày ghé thăm</p>
                <h3 id="days">1</h3>
            </div>

            <div class="stat">
                <p>Cấp độ</p>
                <h3 id="level">Mầm thiện</h3>
            </div>
        </div>
    </section>

    <section class="card" id="mallet">
        <h2>🥁 Gõ mõ an yên</h2>
        <p>Hãy chạm vào chiếc mõ để bắt đầu.</p>

        <div class="mallet-area">
            <button class="mallet" onclick="hitMallet()">🥁</button>
            <p>CHẠM ĐỂ GÕ MÕ</p>
            <h3 id="today">Hôm nay: 0 lượt</h3>
        </div>

        <button class="btn" onclick="toggleSound()">
            🔔 Bật / Tắt âm thanh
        </button>
    </section>

    <section class="card" id="tasks">
        <h2>🌱 Việc thiện mỗi ngày</h2>
        <p>Đánh dấu khi em đã thực hiện những việc tốt.</p>

        <div id="taskList"></div>
    </section>

    <section class="card" id="history">
        <h2>📖 Nhật ký hoạt động</h2>
        <div id="historyList">
            <p>Chưa có hoạt động nào.</p>
        </div>
    </section>

    <section class="card" id="account">
        <h2>👤 Tài khoản</h2>

        <div id="guestArea">
            <p>Em đang sử dụng chế độ khách.</p>
            <p>Dữ liệu được lưu trên trình duyệt của thiết bị.</p>
            <button class="btn" onclick="showLogin()">
                Đăng nhập / Đăng ký
            </button>
        </div>

        <div id="authArea" class="hidden">
            <input id="username" placeholder="Tên tài khoản">
            <input id="password" type="password" placeholder="Mật khẩu">
            <button class="btn" onclick="registerUser()">Đăng ký</button>
            <button class="btn" onclick="loginUser()">Đăng nhập</button>
            <button class="btn" onclick="hideLogin()">Quay lại</button>
            <p id="authMessage"></p>
        </div>
    </section>

    <p style="text-align:center;font-size:11px;color:#829080;margin:15px">
        Điểm an lành là điểm trò chơi, không phải thước đo công đức thật.
    </p>

</div>

<footer>
    🪷 AN TÂM TÍCH ĐỨC 🪷
    <br>
    Sống thiện lành – Giữ tâm an – Lan tỏa yêu thương
</footer>

<script>
let data = JSON.parse(localStorage.getItem("anTamData")) || {
    taps: 0,
    points: 0,
    today: 0,
    days: 1,
    date: new Date().toDateString(),
    done: [],
    history: []
};

let sound = false;

const tasks = [
    ["kind","Nói một lời tử tế",5],
    ["help","Giúp đỡ người thân",10],
    ["thanks","Biết ơn và cảm ơn",5],
    ["green","Bảo vệ môi trường",10],
    ["study","Học tập chăm chỉ",5]
];

function save() {
    localStorage.setItem("anTamData",JSON.stringify(data));
}

function updateLevel() {
    let p = data.points;
    if(p >= 10000) return "Người gieo thiện";
    if(p >= 5000) return "Tâm từ bi";
    if(p >= 1000) return "Tâm sáng";
    if(p >= 500) return "Tâm an";
    if(p >= 100) return "Tâm sen";
    return "Mầm thiện";
}

function render() {
    document.getElementById("taps").innerText = data.taps;
    document.getElementById("points").innerText = data.points;
    document.getElementById("today").innerText =
        "Hôm nay: " + data.today + " lượt";
    document.getElementById("days").innerText = data.days;
    document.getElementById("level").innerText = updateLevel();

    let list = document.getElementById("taskList");
    list.innerHTML = "";

    tasks.forEach(t => {
        let checked = data.done.includes(t[0]);

        let div = document.createElement("div");
        div.className = "task" + (checked ? " done" : "");

        div.innerHTML = `
            <label>
                <input type="checkbox"
                ${checked ? "checked disabled" : ""}
                onchange="completeTask('${t[0]}',${t[2]})">
                ${t[1]}
                (+${t[2]} điểm)
            </label>
        `;

        list.appendChild(div);
    });

    let history = document.getElementById("historyList");

    if(data.history.length === 0) {
        history.innerHTML = "<p>Chưa có hoạt động nào.</p>";
    } else {
        history.innerHTML = data.history.map(x =>
            `<div class="activity">${x}</div>`
        ).join("");
    }
}

function record(message) {
    data.history.unshift(message);
    data.history = data.history.slice(0,15);
}

function hitMallet() {
    data.taps++;
    data.today++;
    data.points++;

    record("🥁 Em vừa gõ một nhịp mõ.");

    if(sound) playSound();

    save();
    render();
}

function completeTask(id,points) {
    if(data.done.includes(id)) return;

    data.done.push(id);
    data.points += points;

    let task = tasks.find(t => t[0] === id);

    record("🌱 Hoàn thành: " + task[1]);

    save();
    render();
}

let audio;

function playSound() {
    try {
        audio = audio || new AudioContext();

        let oscillator = audio.createOscillator();
        let gain = audio.createGain();

        oscillator.frequency.value = 150;
        gain.gain.value = 0.15;

        oscillator.connect(gain);
        gain.connect(audio.destination);

        oscillator.start();
        oscillator.stop(audio.currentTime + 0.15);
    } catch(e) {}
}

function toggleSound() {
    sound = !sound;
    alert(sound ? "Đã bật âm thanh 🔔" : "Đã tắt âm thanh");
}

function showLogin() {
    document.getElementById("authArea").classList.remove("hidden");
}

function hideLogin() {
    document.getElementById("authArea").classList.add("hidden");
}

function registerUser() {
    let name = document.getElementById("username").value;
    let pass = document.getElementById("password").value;

    if(name.length < 3 || pass.length < 6) {
        alert("Tên cần ít nhất 3 ký tự và mật khẩu ít nhất 6 ký tự.");
        return;
    }

    let users = JSON.parse(localStorage.getItem("atdUsers") || "{}");

    if(users[name]) {
        alert("Tên tài khoản đã tồn tại.");
        return;
    }

    users[name] = pass;
    localStorage.setItem("atdUsers",JSON.stringify(users));

    alert("Tạo tài khoản thành công!");
}

function loginUser() {
    let name = document.getElementById("username").value;
    let pass = document.getElementById("password").value;

    let users = JSON.parse(localStorage.getItem("atdUsers") || "{}");

    if(users[name] === pass) {
        alert("Đăng nhập thành công!");
        document.getElementById("guestArea").innerHTML =
            "Xin chào, " + name + " 🪷";
        hideLogin();
    } else {
        alert("Tên tài khoản hoặc mật khẩu không chính xác.");
    }
}

// Tự động chuyển sang ngày mới
if(data.date !== new Date().toDateString()) {
    data.today = 0;
    data.done = [];
    data.days++;
    data.date = new Date().toDateString();
    save();
}

render();
</script>

</body>
</html>
