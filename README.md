<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>RGPV Diploma Result</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{
    margin:0;
    font-family: Arial, Helvetica, sans-serif;
    background:#e9eef5;
}
.top-bar{
    background:#003366;
    padding:10px;
    color:#fff;
    text-align:center;
    font-weight:bold;
}
.nav{
    background:#0b3c91;
    padding:8px;
    color:white;
    text-align:right;
    font-size:14px;
}
.container{
    max-width:900px;
    margin:20px auto;
    background:#fff;
    padding:20px;
    box-shadow:0 0 8px rgba(0,0,0,0.2);
}
.login-box{
    border:1px solid #ccc;
    padding:15px;
    text-align:center;
}
input, select{
    padding:8px;
    width:250px;
    margin:8px;
}
button{
    padding:8px 20px;
    background:#0b3c91;
    color:#fff;
    border:none;
    cursor:pointer;
}
.result-box{
    display:none;
    margin-top:20px;
}
table{
    width:100%;
    border-collapse:collapse;
    margin-top:10px;
}
th, td{
    border:1px solid #000;
    padding:8px;
    text-align:center;
}
.pass{
    color:green;
    font-weight:bold;
}
.footer{
    background:#003366;
    color:white;
    text-align:center;
    padding:10px;
    margin-top:20px;
}
@media print{
    button{display:none;}
}
</style>
</head>

<body>

<div class="top-bar">
RAJIV GANDHI PROUDYOGIKI VISHWAVIDYALAYA, BHOPAL
</div>

<div class="nav">
Diploma Wing Result Portal
</div>

<div class="container">

<h3>Result : Diploma Pharmacy</h3>

<div class="login-box">
<input type="text" id="roll" placeholder="Enter Enrollment Number"><br>
<select>
<option>Semester / Year 2</option>
</select><br>
<button onclick="checkResult()">View Result</button>
<p id="error" style="color:red;"></p>
</div>

<div class="result-box" id="result">

<p><b>Name:</b> NADEEM KHAN GOURI</p>
<p><b>Roll No:</b> 23223P02012</p>
<p><b>Course:</b> Diploma Pharmacy (2 Year)</p>
<p><b>Status:</b> Regular</p>

<table>
<tr><th>Subject</th><th>Marks</th></tr>
<tr><td>201</td><td>32 + 19</td></tr>
<tr><td>202</td><td>40 + 19</td></tr>
<tr><td>203</td><td>32 + 19</td></tr>
<tr><td>204</td><td>28 + 19</td></tr>
<tr><td>205</td><td>27 + 19</td></tr>
<tr><td>206</td><td>24 + 19</td></tr>
</table>

<p><b>Grand Total:</b> 739</p>
<p class="pass">RESULT : PASS</p>

<button onclick="window.print()">Print / Save PDF</button>

</div>

</div>

<div class="footer">
© RGPV Diploma Wing (Demo Result Page)
</div>

<script>
function checkResult(){
    let roll = document.getElementById("roll").value;
    if(roll === "23223P02012"){
        document.getElementById("result").style.display="block";
        document.getElementById("error").innerHTML="";
    }else{
        document.getElementById("result").style.display="none";
        document.getElementById("error").innerHTML="Invalid Enrollment Number";
    }
}
</script>

</body>
</html>
