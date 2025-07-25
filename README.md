# gradient
changes the background
# gradient
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   <link rel="stylesheet" href="C:\Users\Prachi\Documents\GitHub\colorr-theory\stylesheet.css">
</head> 
<style> 
body{
    height: 100 vh;
    background-image:linear-gradient( toright top,#051937,#004d7a,#008793,#00bf72,#a8eb15);
    display:flex;
    justify-content: center;
    align-items: center;
}
#mybtn1{
    color:#a8eb15;
}</style>

<body>
    <div class="main">
        <div class="inner-main">
            <div class="btn-group">
                <button class="btn1">#a1bb45</button>
                <button class="btn2">#bd56b4</button>
            </div>
            <h3 class="heading">Copy your code here</h2>
                <div class="para-group">
                    <p class="para">background-image : linear-gradient(to right,rgb(92,145,229),rgb(152,63,198))</p>
                </div>
        </div>
    </div>
    <script>
        let btn1 = document.querySelector(".btn1")
        let btn2 = document.querySelector(".btn2")
        let copydiv = document.querySelector(".para")
        let rgb1 = "#004773"
        let rgb2 = "#54d542"

        const newhexvalues = () => {
            let myHexValues = "0123456789abcdef";
            let colour = "#";
            for (let i = 0; i < 6; i++) {
                colour = colour + myHexValues[Math.floor(Math.random() * 16)];
            }
            // console.log(colour);
            return colour;

        }

        const handlebtn1 = () => {
            rgb1 = newhexvalues()
            console.log(rgb1);
            btn1.innerText = rgb1
            document.body.style.backgroundImage = `linear-gradient(to right,${rgb1},${rgb2})`;
            copydiv.innerHTML = `linear-gradient(to right,${rgb1},${rgb2})`
        }

        const handlebtn2 = () => {
            rgb2 = newhexvalues()
            console.log(rgb2);
            btn2.innerText = rgb2
            document.body.style.backgroundImage = `linear-gradient(to right,${rgb1},${rgb2})`;
            copydiv.innerHTML = `linear-gradient(to right,${rgb1},${rgb2})`
        }

        //for copy the text
        copydiv.addEventListener("click", () => {
            navigator.clipboard.writeText(copydiv.innerText);
            alert("text is copied to clipboard")
        })


        btn1.addEventListener("click", handlebtn1)
        btn2.addEventListener("click", handlebtn2)


    </script>
</body>

</html>
