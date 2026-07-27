<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Imaad AI Classes</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:#050816;
color:white;
}


/* HEADER */

header{

background:#0f172a;
padding:20px 8%;
display:flex;
justify-content:space-between;
align-items:center;

}


.logo{

font-size:30px;
font-weight:bold;
color:#38bdf8;

}


.logo span{

display:block;
font-size:13px;
color:white;
letter-spacing:4px;

}


nav a{

color:white;
text-decoration:none;
margin:15px;

}



/* HERO */

.hero{

padding:100px 8%;
text-align:center;

background:
linear-gradient(
rgba(0,0,0,.6),
rgba(0,0,0,.8)
),
url("https://images.unsplash.com/photo-1677442136019-21780ecad995");

background-size:cover;
background-position:center;

}


.hero h1{

font-size:55px;

}


.hero p{

font-size:20px;
margin:20px;

}



.search{

display:flex;
max-width:600px;
margin:30px auto;

}


.search input{

flex:1;
padding:15px;
border:none;
border-radius:30px 0 0 30px;

}


.search button{

background:#38bdf8;
border:none;
padding:15px 25px;
border-radius:0 30px 30px 0;

}



/* COURSES */


section{

padding:60px 8%;

}


.courses{

display:grid;
grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
gap:20px;

}


.card{

background:#111827;
padding:25px;
border-radius:15px;
transition:.3s;

}


.card:hover{

transform:translateY(-8px);
background:#1e293b;

}


.card h3{

color:#38bdf8;

}



/* CHATBOT */


.chat-button{

position:fixed;
right:25px;
bottom:25px;

background:#38bdf8;

width:60px;
height:60px;

border-radius:50%;

display:flex;
align-items:center;
justify-content:center;

font-size:30px;

cursor:pointer;

}



.chat-box{

display:none;

position:fixed;
right:25px;
bottom:100px;

width:330px;

background:#111827;

border-radius:15px;

overflow:hidden;

}


.chat-header{

background:#38bdf8;
padding:15px;

display:flex;
justify-content:space-between;

}



.chat-body{

height:250px;
padding:15px;
overflow:auto;

}



.chat-input{

display:flex;

}


.chat-input input{

flex:1;
padding:12px;

}


.chat-input button{

background:#38bdf8;

}



/* WHATSAPP */


.whatsapp{

position:fixed;

left:20px;
bottom:25px;

background:#25D366;

padding:15px 20px;

border-radius:30px;

color:white;

text-decoration:none;

font-weight:bold;

}



footer{

background:#020617;

padding:30px;

text-align:center;

}



@media(max-width:700px){

.hero h1{

font-size:35px;

}

header{

flex-direction:column;

}

}


</style>

</head>


<body>


<header>


<div class="logo">

🚀 IMAAD AI

<span>CLASSES</span>

</div>


<nav>

<a href="#">Home</a>
<a href="#">Courses</a>
<a href="#">Contact</a>

</nav>


</header>




<div class="hero">


<h1>

Master Artificial Intelligence

</h1>


<p>

Learn AI skills for the future with Imaad AI Classes

</p>



<div class="search">

<input id="search"
placeholder="Search AI courses...">


<button onclick="searchCourse()">

Search

</button>

</div>


<p id="result"></p>


</div>






<section>


<h2>
20 Professional AI Courses
</h2>

<br>


<div class="courses">


<div class="card"><h3>AI Fundamentals</h3></div>
<div class="card"><h3>ChatGPT Masterclass</h3></div>
<div class="card"><h3>Generative AI</h3></div>
<div class="card"><h3>Python For AI</h3></div>
<div class="card"><h3>Machine Learning</h3></div>
<div class="card"><h3>Deep Learning</h3></div>
<div class="card"><h3>Neural Networks</h3></div>
<div class="card"><h3>AI Automation</h3></div>
<div class="card"><h3>Prompt Engineering</h3></div>
<div class="card"><h3>AI Content Creation</h3></div>
<div class="card"><h3>AI Video Creation</h3></div>
<div class="card"><h3>AI Image Generation</h3></div>
<div class="card"><h3>Robotics AI</h3></div>
<div class="card"><h3>Computer Vision</h3></div>
<div class="card"><h3>NLP</h3></div>
<div class="card"><h3>AI App Development</h3></div>
<div class="card"><h3>AI Website Building</h3></div>
<div class="card"><h3>AI Marketing</h3></div>
<div class="card"><h3>AI Business Tools</h3></div>
<div class="card"><h3>Future AI Technology</h3></div>


</div>


</section>





<section>

<h2>
Why Choose Imaad AI Classes?
</h2>

<br>

<p>

✔ Professional AI Training<br>
✔ Practical Projects<br>
✔ Beginner To Advanced Courses<br>
✔ Future Technology Skills

</p>

</section>






<!-- CHATBOT -->


<div class="chat-button" onclick="openChat()">

🤖

</div>



<div class="chat-box" id="chatBox">


<div class="chat-header">

Imaad AI Tutor

<span onclick="closeChat()">✖</span>

</div>



<div class="chat-body" id="chatBody">

<p>
AI Tutor: Hello! Ask me about AI courses.
</p>

</div>



<div class="chat-input">

<input id="chatInput"
placeholder="Ask something...">

<button onclick="sendChat()">

Send

</button>

</div>


</div>






<a class="whatsapp"
href="https://wa.me/9596191037">

WhatsApp Us

</a>





<footer>

© 2026 Imaad AI Classes

</footer>






<script>


function searchCourse(){

let text=document.getElementById("search").value;

document.getElementById("result").innerHTML=

"Searching: "+text;

}




function openChat(){

document.getElementById("chatBox").style.display="block";

}



function closeChat(){

document.getElementById("chatBox").style.display="none";

}



function sendChat(){


let input=document.getElementById("chatInput");

let msg=input.value;


if(msg=="") return;


let chat=document.getElementById("chatBody");


chat.innerHTML +=

"<p><b>You:</b> "+msg+"</p>";



let reply;


if(msg.toLowerCase().includes("course"))

reply="We have 20 AI courses including ChatGPT, Python AI and Machine Learning.";


else if(msg.toLowerCase().includes("chatgpt"))

reply="ChatGPT course teaches prompting and AI automation.";


else

reply="Imaad AI Tutor helps with AI courses and admissions.";



chat.innerHTML +=

"<p><b>Imaad AI:</b> "+reply+"</p>";



input.value="";

chat.scrollTop=chat.scrollHeight;


}


</script>


</body>
</html>
