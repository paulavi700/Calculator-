# Calculator-
Basic Calculator using HTML,CSS,JAVASCRIPT 

HTML part

<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>Calculator made by Avipriya</title>
  <link href="style.css" rel="stylesheet" type="text/css" />
  <link href="utils.css" rel="stylesheet" type="text/css" />
</head>
<body>
<h1 class="text-center">Calculator using HTML, CSS & JavaScirpt </h1>
  <div class="container flex  flex-col  item-center  mx-auto ">
    <div class="row">
      <input class="input" type="text"/>
    </div>
    <div class="row"> 
      <button class="button">C</button>
      <button class="button">%</button>
      <button class="button">M+</button>
      <button class="button">M-</button>
    </div>
    <div class="row"> 
      <button class="button">7</button>
      <button class="button">8</button>
      <button class="button">9</button>
      <button class="button">*</button>
    </div>
    <div class="row"> 
      <button class="button">4</button>
      <button class="button">5</button>
      <button class="button">6</button>
      <button class="button">/</button>
    </div>
    <div class="row"> 
      <button class="button">1</button>
      <button class="button">2</button>
      <button class="button">3</button>
      <button class="button">+</button>
    </div>
    <div class="row"> 
      <button class="button">0</button>
      <button class="button">.</button>
      <button class="button">=</button>
      <button class="button">-</button>
    </div>
    
  </div>



  
  <script src="script.js"></script>
  <script src="https://replit.com/public/js/replit-badge-v2.js" theme="dark" position="bottom-right"></script>
</body>

</html>


Style.css part

html {
  height: 100%;
  width: 100%;
}
.button{
  width: 66px;
  padding: 20px;
  margin: 0 3px;
  border: 2px sloid black;
  border-radius: 9px;
  cursor: pointer;
}
.row{
  margin: 8px 0;
}
.row input{
  width: 291px;
  font-size: 20px;
  margin: 0;
  padding: 10px 0px;
  border: 2px solid black;
  border-radius: 5px;
}

util.css part

.text-center{
  text-align: center;
}

.mx-auto{
  margin: auto;
}
.flex{
  display: flex;
}
.flex-col{
  flex-direction: column;
}
.item-center{
  align-items: center;
}

Javascript part 

let string = "";
let buttons = document.querySelectorAll('.button');
Array.from(buttons).forEach((button)=>{
  button.addEventListener('click',(e)=>{
    if(e.target.innerHTML == '='){
      string = eval(string);
      document.querySelector('input').value = string;
    }
      else if(e.target.innerHTML == 'C'){
        string = "";
        document.querySelector('input').value = string;
      }
    else{
      console.log(e.target)
      string = string + e.target.innerHTML;
      document.querySelector('input').value = string;
    }
  })
})
