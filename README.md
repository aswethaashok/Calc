# Ex.08 Design of a Standard Calculator
## Date:22-04-24

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
calc.html

<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title> Calculator </title>
    <style type="text/css">
        .container {
    text-align: center;
    margin-top:23px
}

table {
    margin: auto;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(123, 119, 227);
    padding: 20px;
    background: rgb(255, 255, 255);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

button {
    border-radius: 20px;
    border: 0;
    outline: 0;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: transparent;
    color: rgb(107, 219, 237);
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.calculator { 
    border: none;
    background-color: #0b3538;
    padding: 30px;
    border-radius: 30px;
    display: inline-block;
    
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

.color {
    color: rgb(28, 214, 77);
}
.text{
    font-weight: bold;
    color: black;
    text-align: center;
        margin: auto;
        margin-top: 40px;
        margin-left: 30px;
        
}

    </style>
</head>
<body>
    
    </div>
    <div class="container">
        <h1>Calculator
            <br>
           <h3> SWETHA A (212223220114) </h3>
        </h1>
        

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color"> C </button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button> 7 </button></td>
                    <td><button> 8 </button></td>
                    <td><button> 9 </button></td>
                    <td><button class="color"> * </button></td>
                </tr>
                <tr>
                    <td><button> 4 </button></td>
                    <td><button> 5 </button></td>
                    <td><button> 6 </button></td>
                    <td><button class="color"> - </button></td>
                </tr>
                <tr>
                    <td><button> 1 </button></td>
                    <td><button> 2 </button></td>
                    <td><button> 3 </button></td>
                    <td><button class="color"> + </button></td>
                </tr>
                <tr>
                    <td><button> 0 </button></td>
                    <td><button class="color"> . </button></td>
                    <td><button class="color"> / </button></td>
                    <td><button class="color"> = </button></td>
                </tr>
            </table>
        </div>
    </div>
</body>
<script src="index.js"></script>
</html>

#style.css

/* Import Google font - Poppins */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
body {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: whitesmoke;
}

.container {
  position: relative;
  max-width: 500px;
  width: 100%;
  border-radius: 12px;
  padding: 10px 20px 20px;
  background: #fff;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.05);
}
.display {
  height: 80px;
  width: 100%;
  outline: none;
  border: none;
  text-align: right;
  margin-bottom: 10px;
  font-size: 25px;
  color: #000e1a;
  pointer-events: none;
}
.buttons {
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(4, 1fr);
}
.buttons button {
  padding: 10px;
  border-radius: 6px;
  border: none;
  font-size: 20px;
  cursor: pointer;
  background-color: #eee;
}
.buttons button:active {
  transform: scale(0.99);
}
.operator {
  color: #2f9fff;
}

index.js

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```

## OUTPUT:

![Screenshot 2024-04-24 213220](https://github.com/aswethaashok/Calc/assets/149987410/9bc47ca2-033d-4b0a-ace1-5c7169668638)

![Screenshot 2024-04-24 213229](https://github.com/aswethaashok/Calc/assets/149987410/5f69e329-27ce-4910-88bd-f7eca62d8823)


## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
