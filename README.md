
<html lang="en">
<head>
<meta charset="UTF-8">
<title>RGPV Diploma Result</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{margin:0;font-family:Arial,sans-serif;background:#f2f4f8}
.header{background:#0b3c7a;color:#fff;text-align:center;padding:10px}
.container{margin:10px;background:#fff;border-radius:6px;overflow:hidden}
.title{padding:12px;font-size:18px;border-bottom:1px solid #ddd}
.form{padding:15px}
.form input,.form select,.form button{width:100%;padding:10px;margin-top:10px;font-size:16px}
button{background:#000;color:#fff;border:none;border-radius:4px}
.university{background:#0b3c7a;color:#fff;padding:12px;text-align:center}
.details{padding:15px;font-size:14px}
.details p{margin:6px 0}
table{width:100%;border-collapse:collapse;font-size:14px}
th,td{border:1px solid #ddd;padding:6px;text-align:center}
th{background:#f5f5f5}
.summary{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;padding:15px;font-weight:bold;text-align:center}
.result{text-align:center;padding:15px;font-size:18px}
.pass{color:green}
.fail{color:red}
.actions{display:flex;gap:10px;padding:0 15px 15px}
.actions button{flex:1}
.demo{text-align:center;color:red;font-weight:bold;padding:10px}
.footer{background:#0b3c7a;color:#fff;text-align:center;padding:15px;font-size:14px}
.hidden{display:none}

@media print{
.form,.actions,.footer{display:none}
.container{margin:0;border-radius:0}
}
</style>
</head>

<body>

<div class="header">DIPLOMA WING</div>

<div class="container">
<div class="title">Result : Diploma Pharmacy</div>

<div class="form">
<input type="text" id="roll" placeholder="Enter Roll Number">
<select id="sem">
<option value="2">Semester / Year 2</option>
<option value="1">Semester / Year 1</option>
</select>
<button onclick="showResult()">View Result</button>
</div>

<div id="resultBox" class="hidden">

<div class="university">
<b>RAJIV GANDHI PROUDYOGIKI VISHWAVIDYALAYA</b><br>
Polytechnic Wing (DEMO)
</div>

<div class="details">
<p><b>Name:</b> <span id="name"></span></p>
<p><b>Roll No:</b> <span id="rno"></span></p>
<p><b>Semester:</b> <span id="smt"></span></p>
<p><b>Course:</b> DIPLOMA PHARMACY (2 YEAR)</p>
<p><b>Status:</b> Regular</p>
</div>

<table>
<tr>
<th>SUB</th><th>201</th><th>202</th><th>203</th><th>204</th><th>205</th><th>206</th>
</tr>
<tr>
<th>Marks</th>
<td id="m1"></td><td id="m2"></td><td id="m3"></td>
<td id="m4"></td><td id="m5"></td><td id="m6"></td>
</tr>
</table>

<div class="summary">
<div>Total<br><span id="total"></span></div>
<div>Practical<br><span id="pr"></span></div>
<div>Grand<br><span id="grand"></span></div>
</div>

<div class="result">
Result: <span id="res"></span>
</div>

<div class="actions">
<button onclick="window.print()">Print Marksheet</button>
<button onclick="resetPage()">Reset</button>
</div>

<div class="demo">
*** DEMO RESULT – FOR PRACTICE / TEST ONLY ***
</div>

</div>
</div>

<div class="footer">About Us | Vision | Campus Information</div>

<script>
const results={
"2":{
"23223P02009":{name:"ROHIT YADAV",marks:["17+12","18+11","16+10","15+9","14+8","13+7"],total:93,pr:220,grand:406,status:"FAIL"},
"23223P02010":{name:"SAHIL MALIK",marks:["34+20","36+19","35+18","33+17","32+16","31+15"],total:201,pr:370,grand:820,status:"PASS"},
"23223P02011":{name:"AMIT VERMA",marks:["20+14","21+13","22+12","19+11","18+10","17+9"],total:117,pr:260,grand:495,status:"FAIL"},
"23223P02012":{name:"NADEEM KHAN GOURI",marks:["32+19","40+19","32+19","28+19","27+19","24+19"],total:183,pr:349,grand:739,status:"PASS"},
"23223P02013":{name:"RAHUL SHARMA",marks:["35+20","38+19","36+18","34+19","33+18","32+17"],total:208,pr:365,grand:820,status:"PASS"},
"23223P02014":{name:"MOHIT PATEL",marks:["30+18","31+17","29+16","28+15","27+14","26+13"],total:171,pr:330,grand:701,status:"PASS"},
"23223P02015":{name:"ARJUN SINGH",marks:["15+12","16+10","14+11","13+9","12+8","11+7"],total:81,pr:210,grand:381,status:"FAIL"},
"23223P02016":{name:"SAMEER KHAN",marks:["33+18","34+17","35+16","32+15","31+14","30+13"],total:195,pr:340,grand:760,status:"PASS"},
"23223P02017":{name:"VIKAS JAIN",marks:["20+14","21+13","22+12","19+11","18+10","17+9"],total:117,pr:260,grand:495,status:"FAIL"},
"23223P02018":{name:"ANUJ TIWARI",marks:["31+19","32+18","33+17","30+16","29+15","28+14"],total:183,pr:350,grand:750,status:"PASS"}
},
"1":{
"23223P02009":{name:"ROHIT YADAV",marks:["22+15","21+14","20+13","19+12","18+11","17+10"],total:117,pr:250,grand:520,status:"PASS"},
"23223P02010":{name:"SAHIL MALIK",marks:["18+12","17+11","16+10","15+9","14+8","13+7"],total:93,pr:220,grand:406,status:"FAIL"},
"23223P02011":{name:"AMIT VERMA",marks:["24+16","25+15","26+14","23+13","22+12","21+11"],total:141,pr:290,grand:631,status:"PASS"},
"23223P02012":{name:"NADEEM KHAN GOURI",marks:["28+18","29+17","30+16","27+15","26+14","25+13"],total:165,pr:310,grand:695,status:"PASS"},
"23223P02013":{name:"RAHUL SHARMA",marks:["19+13","18+12","17+11","16+10","15+9","14+8"],total:99,pr:230,grand:429,status:"FAIL"},
"23223P02014":{name:"MOHIT PATEL",marks:["26+17","27+16","28+15","25+14","24+13","23+12"],total:153,pr:300,grand:653,status:"PASS"},
"23223P02015":{name:"ARJUN SINGH",marks:["15+10","14+9","13+8","12+7","11+6","10+5"],total:75,pr:200,grand:350,status:"FAIL"},
"23223P02016":{name:"SAMEER KHAN",marks:["29+18","30+17","31+16","28+15","27+14","26+13"],total:171,pr:330,grand:701,status:"PASS"},
"23223P02017":{name:"VIKAS JAIN",marks:["18+12","17+11","16+10","15+9","14+8","13+7"],total:93,pr:220,grand:406,status:"FAIL"},
"23223P02018":{name:"ANUJ TIWARI",marks:["27+19","28+18","29+17","26+16","25+15","24+14"],total:159,pr:340,grand:699,status:"PASS"}
}
};

function showResult(){
const roll=document.getElementById("roll").value.trim();
const sem=document.getElementById("sem").value;
if(!results[sem][roll]){
alert("Result not found for selected semester (DEMO)");
return;
}
const r=results[sem][roll];
document.getElementById("resultBox").classList.remove("hidden");
document.getElementById("name").innerText=r.name;
document.getElementById("rno").innerText=roll;
document.getElementById("smt").innerText="Semester "+sem;
["m1","m2","m3","m4","m5","m6"].forEach((id,i)=>document.getElementById(id).innerText=r.marks[i]);
document.getElementById("total").innerText=r.total;
document.getElementById("pr").innerText=r.pr;
document.getElementById("grand").innerText=r.grand;
const res=document.getElementById("res");
res.innerText=r.status;
res.className=r.status==="PASS"?"pass":"fail";
}

function resetPage(){
document.getElementById("resultBox").classList.add("hidden");
document.getElementById("roll").value="";
}
</script>

</body>
</html>
