console.log("NexaHub Started Successfully");
function calculateAge(){

let dob=document.getElementById("dob").value;

if(dob==""){
document.getElementById("result").innerHTML="Please select your DOB";
return;
}

let birth=new Date(dob);
let today=new Date();

let age=today.getFullYear()-birth.getFullYear();

let month=today.getMonth()-birth.getMonth();

if(month<0 || (month===0 && today.getDate()<birth.getDate())){
age--;
}

document.getElementById("result").innerHTML="Your Age is "+age+" Years";

}
function calculateAge(){

let dob=document.getElementById("dob").value;

if(dob==""){
alert("Select Date of Birth");
return;
}

let birth=new Date(dob);

let today=new Date();

let age=today.getFullYear()-birth.getFullYear();

document.getElementById("result").innerHTML=
"Your Age : "+age+" Years";

}
function createPDF(){

let files=document.getElementById("images").files;

if(files.length==0){
alert("Please select image");
return;
}

document.getElementById("status").innerHTML=
"Images Selected : "+files.length;

}
function mergePDF(){

let files=document.getElementById("pdfFiles").files;

if(files.length<2){
alert("Please select at least 2 PDF files");
return;
}

document.getElementById("mergeStatus").innerHTML=
files.length+" PDF Selected";

}
function resizeImage() {

const file = document.getElementById("imageInput").files[0];

if (!file) {
alert("Please select an image");
return;
}

const width = parseInt(document.getElementById("width").value);
const height = parseInt(document.getElementById("height").value);

const reader = new FileReader();

reader.onload = function(e){

const img = new Image();

img.onload = function(){

const canvas = document.getElementById("canvas");
canvas.width = width;
canvas.height = height;

const ctx = canvas.getContext("2d");

ctx.drawImage(img,0,0,width,height);

const dataURL = canvas.toDataURL("image/jpeg",0.9);

document.getElementById("preview").src = dataURL;

const download = document.getElementById("download");

download.href = dataURL;
download.download = "resized-image.jpg";
download.innerHTML = "⬇ Download Resized Image";
download.style.display = "inline-block";

};

img.src = e.target.result;

};

reader.readAsDataURL(file);

}
const tools = [
  { name: "Age Calculator", page: "age.html" },
  { name: "Image Resize", page: "image-resize.html" },
  { name: "Image to PDF", page: "image-to-pdf.html" },
  { name: "PDF Merge", page: "pdf-merge.html" }
];

function searchTool() {
  const input = document.getElementById("searchBox").value.toLowerCase();
  const result = document.getElementById("searchResults");

  result.innerHTML = "";

  tools.forEach(tool => {
    if (tool.name.toLowerCase().includes(input)) {
      result.innerHTML += `
        <p><a href="${tool.page}">${tool.name}</a></p>
      `;
    }
  });

  if (result.innerHTML === "") {
    result.innerHTML = "<p>No tool found.</p>";
  }
}