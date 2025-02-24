# Digital Clock

This is a simple digital clock that displays the current time using HTML, CSS, and JavaScript. The clock updates every second and features animated circular indicators for hours, minutes, and seconds.

## Features
- Displays time in 12-hour format with AM/PM indicator
- Animated circular indicators for hours, minutes, and seconds
- Responsive design with a dark theme

## Technologies Used
- HTML
- CSS
- JavaScript

## Preview
![Digital Clock Preview](preview.png) *(Replace with an actual screenshot of your project)*

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/Chaitanya14112/digital-clock.git
   ```
2. Navigate to the project folder:
   ```sh
   cd digital-clock
   ```
3. Open `index.html` in your browser.

## Code
### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div id="time">
            <div class="circle" style="--color: #ff2972">
                <div id="hours">00</div>
            </div>
            <div class="circle" style="--color: #fee800">
                <div id="minutes">00</div>
            </div>
            <div class="circle" style="--color: #04fc43">
                <div id="seconds">00</div>
            </div>
            <div class="ap">
                <div id="ampm">AM</div>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;400;500;600;700;800;900&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

.container {
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #2f363e;
}

#time {
  display: flex;
  gap: 40px;
  color: #fff;
}
```

### JavaScript
```js
setInterval(() => {
  let hours = document.getElementById('hours');
  let minutes = document.getElementById('minutes');
  let seconds = document.getElementById('seconds');
  let ampm = document.getElementById('ampm');
  
  let h = new Date().getHours();
  let m = new Date().getMinutes();
  let s = new Date().getSeconds();
  let ap = h >= 12 ? 'PM' : 'AM';
  
  if (h > 12) h -= 12;
  h = h < 10 ? '0' + h : h;
  m = m < 10 ? '0' + m : m;
  s = s < 10 ? '0' + s : s;
  
  hours.innerText = h;
  minutes.innerText = m;
  seconds.innerText = s;
  ampm.innerText = ap;
}, 1000);
```

## Contributing
Feel free to submit a pull request if you'd like to improve this project.

## License
This project is open-source and available under the [MIT License](LICENSE).


