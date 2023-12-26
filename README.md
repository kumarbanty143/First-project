<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>

  <style>

    .subscribe{
      border: none;
      background-color: black;
      color: white;
      padding: 10px;
      font-weight: bolder;
      border-radius: 50px;
    }
    .added{
      color: black;
      background-color: aliceblue;
    }

    .input-css{
      font-size: 22px;
      padding:10px ;
      border-radius: 5px;
    }

    .button-css{
      border: none;
      font-size:19px;
      padding: 12px 15px;
      margin-left:7px;
      background-color: green;
      color: white;
    }

  </style>


</head>
<body>
  <h3>
    Youtube Subscribe Button
  </h3>
 <button onclick="
    subscribe();
 "class="sub-but subscribe">Subscribe</button>

<!-- ------------------------------------------- -->

  <h3>Amazon Shipping Calculator</h3>

    <h4>Orders under $40 = +$10</h4>
    <h4>Orders over $40 = FREE shipping</h4>

  <input type="text" class="input input-css" placeholder="Cost of order" onkeydown="keydown(event)"><button 
  class="button-css"
  onclick=" 
  Calculate();
  
  ">Calculate</button>

  <h4 class="show"></h4>

    <h3><a href="r-p-c.html">Click here for rock paper scissor game</a></h3>

    <script>

      function subscribe(){
        const onbutton= document.querySelector('.sub-but');
    
        if(onbutton.innerHTML==='Subscribe'){
          onbutton.innerHTML='Subscribed';
          onbutton.classList.add('added');
        }
        else{
          onbutton.innerHTML='Subscribe';
          onbutton.classList.remove('added');
        }
      }

      function keydown(event){
        if(event.key === 'Enter'){
          Calculate();
        }
      }

      function Calculate(){
        const htmlInput = document.querySelector('.input');
        let store=Number(htmlInput.value);
        console.log(store)

        if(store==0){
          store=0;
        }
        else if(store<40){
          store+=10;
        }
        document.querySelector('.show').innerHTML='$' + store;
      }
    </script>

</body>
</html>
