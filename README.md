# TODO

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="css/bootstrap.min.css">
  <link rel="stylesheet" href="css/test1.css">
  <title>Document</title>
</head>

<style>
   ul li{

    list-style: none;
    
    padding: 10px;
    font-weight:bolder;
    font-kerning: normal;
    font-size: large;

   }
   a{
     float: right;
     text-decoration: none;
     font-weight:bold;
     color:black;
   }

   #error{
    text-size-adjust: 15px;
    color: red;
    font-weight: bold;

   }
</style>
<body>
  
  
  <div class="container m-5 text-center border bg-danger ">
     <h3> MY TODO PROJECT</h3>
    <div class="col-6 mx-auto shadow bg-success">
       <ul>
      <!--- <li> HOME<a style="float:right;" href="javascript:aviod(0)">X</a></li>
       <li> ABOUT <a style="float:right;" href="javascript:aviod(0)">X</a></li>
       <li> MESSAGE<a style="float:right;" href="javascript:aviod(0)">X</a></li>
       </ul>-->
    </div>
  </div>

  <div class="text-center">
    <input type="text" name="" id="input">
    
    <BUtton>Add</BUtton><br>
    <span id="error"></span>
  </div>
<script>

const ab=document.querySelector('ul')
const a=document.querySelector('li')
console.log(ab)
ab.addEventListener('click',(e)=>{
  const ab=document.querySelector('ul')
  console.log(e.target)
  let el=e.target.parentNode;
  ab.removeChild(el)

});

const btn=document.querySelector('button')
btn.addEventListener('click',()=>{
const input=document.querySelector('input').value;
const err=document.querySelector('#error')
if (input==''){
  err.innerText="Pls Enter Valid value"
}else{
  err.innerText=" "
const li=document.createElement('li')
const a=document.createElement('a')
      a.innerText='x'
      a.href="javascript:avoid(0)"
      li.innerText=input
      li.appendChild(a)
      console.log(li,a)
      ab.appendChild(li)
      document.querySelector('input').value=""
    }
})
</script>

</body>
</html>
