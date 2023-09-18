NodeJs Code for server Creation using http module:
HTML Code:
align-items: center; height: 100vh; color: white;
text-align: center;}
.container {
padding: 20px; width: 80%;
}
table ,tr{
border-collapse: collapse; border: 2px solid white; color: white;
background-color: rgb(65, 53, 75);
}
.salaryColumn {display: none;} #toggleButton, #totalSalaryButton{
color: white;
}
#toggleButton {
background-color: #e74c3c; border: 2px solid black;
}
#totalSalaryButton {background-color: #27ae60;}
</style>
</head>
<body>
<div class="container">
<h1 style="margin-bottom: 20px;">Employee Salary Details</h1>
<table style="text-align: center;">
<tr>
<th>Serial No</th>
<th>Employee UID</th>
<th>Employee Name</th>
<th>Post</th>
<th class="salaryColumn">Salary</th>
</tr>
<tr>
<td>1</td>
<td>22MCA20112</td>
<td>Shivam Gupta</td>
<td>Software Developer</td>
<td class="salaryColumn">&#8377 50,000</td>
</tr>
<tr>
<td>2</td>
<td>22MCA20091</td>
<td>Alok Kumar</td>
<td>Front End Developer</td>
<td class="salaryColumn">&#8377 40,000</td>
</tr>
<tr>
<td>3</td>
<td>22MCA20107</td>
<td>Tanusree </td>
 
<td>Java Developer</td>
<td class="salaryColumn">&#8377 55,000</td>
</tr>
</table>
<div>
<button id="toggleButton">Show/Hide Salary</button>
<button id="totalSalaryButton">Calculate Total Salary</button>
</div>
<div id="totalSalary" style="display:none; text-align: center; margin-top:20px;">
<strong>Total Salary: </strong><span id="totalSalaryAmount">&#8377</span>
</div>
<script>
const salaryColumns = document.querySelectorAll(".salaryColumn");
const toggleButton = document.getElementById("toggleButton");
const totalSalaryButton = document.getElementById("totalSalaryButton") ;
const totalSalaryDisplay = document.getElementById("totalSalary");
const totalSalaryAmountDisplay = document.getElementById("totalSalaryAmount"); toggleButton.addEventListener("dblclick", () => {
salaryColumns.forEach(column => {
column.style.display = (column.style.display === "none") ? "tablecell" :"none";});
});
 totalSalaryButton.style.display = "none"; totalSalaryDisplay.style.display = "none";
 
toggleButton.addEventListener("click", () => { salaryColumns.forEach(column => {
column.style.display = (column.style.display === "block") ? "tablecell" :"block";});
 });
totalSalaryButton.style.display = "inline-block";""));
totalSalaryButton.addEventListener("click", () => {
let totalSalary = 0; for (let i = 1; i <
salaryColumns.length; i++) {
const column = salaryColumns[i];
if (column.style.display !== "none") {
const salaryValue = parseFloat(column.textContent.replace(/[^0-9.-]+/g,totalSalary += salaryValue;}
});
}totalSalaryAmountDisplay.textContent ="₹ " + totalSalary; totalSalaryDisplay.style.display ="block";
</script>
</body>
</html>
