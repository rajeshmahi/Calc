# Ex.08 Design of a Standard Calculator
## Date:

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
<html lang="en">

<head>
    <title>CALCULATOR</title>
    <script>
        function fn(e) {
            if (e.innerHTML == '=') {
                output.value = eval(output.value);
            }
            else if (e.id == 'back') {
                v = output.value;
                output.value = v.substring(0, v.length - 1);
            }
            else if (e.innerHTML == 'C') {
                output.value = '';
            }
            else if (e.innerHTML == '√') {
                output.value += 'Math.sqrt(';
            }
            else if (e.innerHTML == '^') {
                output.value += '**';
            }
            else if (e.innerHTML == 'sin') {
                output.value += 'Math.sin(';
            }
            else if (e.innerHTML == 'cos') {
                output.value += 'Math.cos(';
            }
            else if (e.innerHTML == 'tan') {
                output.value += 'Math.tan(';
            }
            else if (e.innerHTML == 'M+') {
                memory += parseFloat(output.value);
                output.value = '';
            }
            else if (e.innerHTML == 'M-') {
                memory -= parseFloat(output.value);
                output.value = '';
            }
            else if (e.innerHTML == 'MR') {
                output.value = memory;
            }
            else if (e.innerHTML == 'MC') {
                memory = 0;
            }
            else if (e.innerHTML == 'Sci') {
                output.value = parseFloat(output.value).toExponential();
            }
            else if (e.innerHTML == 'Dec/Frac') {
                // Implement decimal/fraction conversion logic
                // This feature requires additional JavaScript code
            }
            else {
                output.value += e.innerHTML;
            }
        }
    </script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
</head>
<body>
    <div class=" bg-dark mx-auto m-1 text-center text-white" style="width: 24rem;">RAJESH K (212221220041)</div>
    <div class="bg-dark row mx-auto text-center" style="width: 24rem;">
        <div class="col-12 my-4">
            <input type="text" name="" id="output" style="width: 100%;height: 50px;border-radius: 25px;"></div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">(</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">)</div>
        <div class="m-3 col-2 btn btn-danger rounded-4" onclick="fn(this)">C</div>
        <div class="m-3 col-2 btn btn-danger rounded-4" onclick="fn(this)" id="back"><i class="bi bi-backspace"></i>
        </div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">7</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">8</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">9</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">*</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">4</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">5</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">6</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">-</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">1</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">2</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">3</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">+</div>
        <div class="m-3 col-2 btn btn-success rounded-4" onclick="fn(this)">0</div>
        <div class="m-3 col-2 btn btn-success rounded-4" btn-success onclick="fn(this)">.</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">%</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">/</div>
        <div class="m-3 col-2 btn btn-warning rounded-4" onclick="fn(this)">=</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">√</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">^</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">sin</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">cos</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">tan</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">M+</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">M-</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">MR</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">MC</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">Sci</div>
        <div class="m-3 col-2 btn btn-primary rounded-4" onclick="fn(this)">Dec</div>
    </div>
</body>

</html>
```

## OUTPUT:
![Screenshot 2024-04-17 141527](https://github.com/selvasachein/Calc/assets/117527801/2c99ce45-7713-4de0-ac1d-69da799fc896)


## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
