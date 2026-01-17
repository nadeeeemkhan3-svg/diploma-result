
<html lang="en">
<head>
<meta charset="UTF-8">
<title>RGPV Diploma Result </title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{
    margin:0;
    font-family: Arial, sans-serif;
    background:#f2f4f8;
}

/* HEADER */
.header{
    background:#FF0000;
    padding:10px;
    display:flex;
    align-items:center;
}
.logo{
    width:45px;
    height:45px;
    background:#ddd;
    border-radius:50%;
    text-align:center;
    line-height:45px;
    font-weight:bold;
    margin-right:10px;
}
.title{
    font-size:14px;
    font-weight:bold;
}
.login-btns{
    margin-left:auto;
}
.login-btns button{
    background:#f5b335;
    border:1px solid #c98b1e;
    color:#7a1b;
    padding:5px 8px;
    font-size:12px;
    border-radius:4px;
}

/* NAV */
.nav{
    background:#1f3c88;
    color:#fff;
    padding:10px;
    font-size:14px;
}

/* BOX */
.box{
    background:#fff;
    margin:10px;
    padding:15px;
    border-radius:6px;
}

/* INPUT */
input,select,button{
    width:100%;
    padding:10px;
    margin-top:8px;
    font-size:14px;
}
button{
    background:#1f3c88;
    color:#FF0000;
    border:none;
    border-radius:4px;
}

/* RESULT HEADER */
.result-head{
    background:#1f3c88;
    color:#FF0000;
    padding:10px;
    text-align:center;
    margin-top:10px;
    font-size:13px;
}

/* TABLE */
table{
    width:100%;
    border-collapse:collapse;
    margin-top:10px;
}
th,td{
    border:1px solid #ccc;
    padding:6px;
    font-size:12px;
    text-align:center;
}
th{
    background:#f2f2f2;
}

.footer{
    background:#1f3c88;
    color:#fff;
    padding:10px;
    font-size:12px;
    text-align:center;
    margin-top:20px;
}

.hidden{display:none;}
</style>
</head>

<body>

<!-- HEADER -->
<div class="header">
    <div class="logo">RGPV</div>
    <div class="title">
        DIPLOMA WING<br>
        Rajiv Gandhi Proudyogiki Vishwavidyalaya
    </div>
</div>

<div class="nav">☰ Home</div>

<!-- LOGIN PAGE -->
<div class="box" id="loginPage">
    <h3>Student Login</h3>
    <input type="text" id="username" placeholder="Username">
    <input type="password" id="password" placeholder="Password">
    <button onclick="login()">Login</button>
</div>

<!-- DASHBOARD -->
<div class="box hidden" id="dashboard">
    <h3>Student Dashboard</h3>
    <button onclick="openResult()">View Result</button>
    <button onclick="logout()">Logout</button>
</div>

<!-- RESULT PAGE -->
<div class="box hidden" id="resultPage">
    <h3>Result : Diploma Pharmacy</h3>
    <input type="text" id="rollno" placeholder="Enter Roll No">
    <select>
        <option>Semester 2</option>
    </select>
    <button onclick="getResult()">Get Result</button>

    <div id="resultData" class="hidden">
        <div class="result-head">
            RAJIV GANDHI PROUDYOGIKI VISHWAVIDYALAYA<br>
            POLYTECHNIC WING, BHOPAL
        </div>

        <p><strong>Name:</strong> NADEEM KHAN GOURI</p>
        <p><strong>Roll No:</strong> <span id="rno"></span></p>
        <p><strong>Course:</strong> DIPLOMA PHARMACY (2 YEAR)</p>
        <p><strong>Status:</strong> Regular</p>

        <table>
            <tr>
                <th>201</th><th>202</th><th>203</th><th>204</th><th>205</th><th>206</th>
            </tr>
            <tr>
                <td>32+19</td><td>40+19</td><td>32+19</td>
                <td>28+19</td><td>27+19</td><td>24+19</td>
            </tr>
        </table>

        <table>
            <tr>
                <th>Grand Total</th>
                <th>Result</th>
            </tr>
            <tr>
                <td>739</td>
                <td>PASS</td>
            </tr>
        </table>
    </div>
</div>

<div class="footer">
    RGPV Diploma Result Website<br>
    For learning & testing only
</div>

<script>
function login(){
    document.getElementById("loginPage").classList.add("hidden");
    document.getElementById("dashboard").classList.remove("hidden");
}
function logout(){
    location.reload();
}
function openResult(){
    document.getElementById("dashboard").classList.add("hidden");
    document.getElementById("resultPage").classList.remove("hidden");
}
function getResult(){
    let roll = document.getElementById("rollno").value;
    if(roll==="23223P02012"){
        document.getElementById("rno").innerText = roll;
        document.getElementById("resultData").classList.remove("hidden");
    }else{
        alert("Result not found (Demo)");
    }
}
</script>

</body>
</html>
