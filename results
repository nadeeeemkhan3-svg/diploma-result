<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>RGPV Diploma Result</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body {
    font-family: Arial, sans-serif;
    background:#f2f4f8;
    margin:0;
}
.header {
    background:#0b3c91;
    color:#fff;
    padding:15px;
    text-align:center;
}
.container {
    max-width:800px;
    margin:20px auto;
    background:#fff;
    padding:20px;
    box-shadow:0 0 10px rgba(0,0,0,0.15);
}
.login-box {
    text-align:center;
}
input, select {
    width:260px;
    padding:10px;
    margin:8px;
}
button {
    padding:10px 25px;
    background:#0b3c91;
    color:#fff;
    border:none;
    cursor:pointer;
}
table {
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}
table, th, td {
    border:1px solid #000;
}
th, td {
    padding:8px;
    text-align:center;
}
.result-box {
    display:none;
}
.pass {
    color:green;
    font-weight:bold;
}
.fail {
    color:red;
    font-weight:bold;
}
.footer {
    background:#0b3c91;
    color:#fff;
    text-align:center;
    padding:10px;
    margin-top:20px;
}
@media print {
    button { display:none; }
}
</style>
</head>

<body>

<div class="header">
    <h2>RAJIV GANDHI PROUDYOGIKI VISHWAVIDYALAYA</h2>
    <p>Diploma Wing – Madhya Pradesh</p>
</div>

<div class="container">

<div class="login-box">
    <h3>Result : Diploma Pharmacy</h3>
    <input type="text" id="roll" placeholder="Enter Enrollment Number"><br>
    <select id="sem">
        <option value="2">Semester / Year 2</option>
    </select><br>
    <button onclick="showResult()">View Result</button>
    <p id="error" style="color:red;"></p>
</div>

<div class="result-box" id="result">

<hr>

<p><b>Name:</b> NADEEM KHAN GOURI</p>
<p><b>Roll No:</b> 23223P02012</p>
<p><b>Branch:</b> Diploma Pharmacy (2 Year)</p>
<p><b>Status:</b> Regular</p>

<table>
<tr>
    <th>Subject</th>
    <th>Marks</th>
</tr>
<tr><td>201</td><td>32 + 19</td></tr>
<tr><td>202</td><td>40 + 19</td></tr>
<tr><td>203</td><td>32 + 19</td></tr>
<tr><td>204</td><td>28 + 19</td></tr>
<tr><td>205</td><td>27 + 19</td></tr>
<tr><td>206</td><td>24 + 19</td></tr>
</table>

<p><b>Grand Total:</b> 739</p>
<p class="pass">Result: PASS</p>

<button onclick="window.print()">Print / Save PDF</button>

</div>

</div>

<div class="footer">
    © RGPV Diploma Wing (Demo Result Page)
</div>

<script>
function showResult() {
    let roll = document.getElementById("roll").value;
    if (roll === "23223P02012") {
        document.getElementById("result").style.display = "block";
        document.getElementById("error").innerHTML = "";
    } else {
        document.getElementById("result").style.display = "none";
        document.getElementById("error").innerHTML = "Invalid Enrollment Number";
    }
}
</script>

</body>
</html>
