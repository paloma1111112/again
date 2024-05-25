<html>
<meta charset='UTF-8'/>
<meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5' name='viewport'/>
<meta content='IE=edge' http-equiv='X-UA-Compatible'/>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">

<script src="https://cdn.jsdelivr.net/npm/sweetalert2@11.0.19/dist/sweetalert2.all.min.js"></script>
<script src="https://kit.fontawesome.com/4f3ce16e3e.js" crossorigin="anonymous"></script>
<link href="https://feeldreams.github.io/night/style.css" rel="stylesheet" type="text/css" />
<link rel="stylesheet" href="Sticker.css">
<head>
<title>Script HTML Night</title>
</head>
<style>
  body {
    margin: 0;
    padding: 0;
    font-family: 'Work Sans', sans-serif;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #2c3e50;
    color: white;
    animation: fadeIn 2s ease-in-out;
}

@keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
}

#bodyblur {
    position: fixed;
    width: 100%;
    height: 100%;
    overflow: hidden;
}

#wallpaper {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    z-index: -2;
    animation: zoomIn 30s infinite;
}

@keyframes zoomIn {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

#beneranblur {
    background-color: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -1;
}

#Content {
    text-align: center;
    z-index: 1;
    opacity: 0;
    transition: opacity 1s;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

#suratin {
    margin-bottom: 20px;
}

#suratin img {
    width: 150px;
    cursor: pointer;
    transition: transform 0.3s ease-in-out;
}

#suratin img:hover {
    transform: scale(1.1);
}

#ket {
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 20px;
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

#halo {
    font-family: 'Dancing Script', cursive;
    font-size: 3em;
    margin-top: 0;
    animation: slideIn 3s ease-out;
}

@keyframes slideIn {
    0% { transform: translateY(-100%); }
    100% { transform: translateY(0); }
}

.kumpulanstiker {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 20px;
}

.kumpulanstiker img {
    width: 60px;
    margin: 10px;
    transition: transform 0.3s ease-in-out;
}

.kumpulanstiker img:hover {
    transform: scale(1.2);
}

#bq {
  width: 80%;
  max-width: 600px;
  margin: 20px auto;
  padding: 10px;
  border-left: 5px solid #e74c3c;
  background: rgba(0, 0, 0, 0.5);
  border-radius: 5px;
}


#kalimat, #kalimat2, #kalimatbawah, #kalimatbwh, #kalimatbawah2, #kalimatbawah3 {
    margin: 10px 0;
    padding: 0;
    font-family: 'Ubuntu', sans-serif;
    font-size: 1.2em;
}

.fas.fa-heart {
    position: absolute;
    font-size: 20px;
    color: #e74c3c;
    animation: heart 5s linear infinite;
    opacity: 0.7;
}

@keyframes heart {
    0% {
        transform: scale(0.5) translateY(0);
        opacity: 0;
    }
    50% {
        opacity: 1;
    }
    100% {
        transform: scale(1.2) translateY(-100vh);
        opacity: 0;
    }
}

.sembunyi {
    display: none;
}
</style>
<body>
  <audio src="https://feeldreams.github.io/fullsenyum.mp3" id="linkmp3" class="sembunyi"></audio>
  
  <div id="bodyblur">
    <img src="https://feeldreams.github.io/nightin.jpeg" id="wallpaper"/>
    <div id="beneranblur"></div>
  </div>
  
  <div id='Content'>
    <div id="suratin" onClick="memulai();">
      <img src="https://feeldreams.github.io/kadoin.png"/>
    </div>
    <p id="ket">คลิกที่ของขวัญ</p>
    
    <div class="kumpulanstiker">
      <img src="https://feeldreams.github.io/pusn.gif" id="stiker1"/>
      <img src="https://feeldreams.github.io/bunga.gif" id="stiker2"/>
      <img src="https://feeldreams.github.io/mndkat.gif" id="stiker3"/>
      <img src="https://feeldreams.github.io/smprt.gif" id="stiker4"/>
      <img src="https://feeldreams.github.io/ngumpet.gif" id="stiker5"/>
      <img src="https://feeldreams.github.io/bunga.gif" id="stiker"/>
    </div>
    <p id="halo">Good Night!</p>
    
    <script class="sembunyi">
      async function pesanAwal() {
        suratin.style="display:none";ket.style="display:none";
        await swalst.fire({
          title: 'เฮ้ คิระ! ❤️',
          imageUrl: '' + stiker1.src,
        });   	
        await swalst.fire({
          title: 'ฉันแค่อยากจะพูด',
          imageUrl: '' + stiker2.src,
        });
        await swalst.fire({
          title: 'ราตรีสวัสดิ์ใช่! 🤭❤️',
          imageUrl: '' + stiker3.src,
        });
        await swalst.fire({
          title: 'อย่านอนดึกนะ โอเคไหม ',
          imageUrl: '' + stiker4.src,
        });
        await swalst.fire({
          title: 'คุณจะป่วยในภายหลัง❤️  &#x1F60A; ',
          imageUrl: '' + stiker5.src,
        });
        mulaikonten();
      }
    </script>
    <div>
      <blockquote id='bq'>
        <span>
          <p id="kalimat2">พักผ่อนเยอะๆ อย่าลืมอ่านบทสวดมนต์ก่อนเข้านอนนะคะ 😍</p> 
          <p id="kalimatbwh">...พรุ่งนี้ขอให้มีกำลังใจกับวันดีๆ นะคะ...</p>
        </span>
        <p id="kalimat">นั่นคือทั้งหมดที่</p>
        <p id="kalimatbawah">I Miss You 🫰</p> 
        <p id="kalimatbawah2" class="sembunyi">Good Night ❤️</p> 
        <p id="kalimatbawah3" class="sembunyi">ฝันดีนะ โอเค ❤️</p> 
      </blockquote>
    </div>
    
    <span id="pesanWA" class="sembunyi">Awww Good Night too ❤️❤️❤️</span>
  </div>

<!-- Jangan Edit Bagian Ini --><script>
  ftom=0;aksift=0;ftganti=0;flag=1;flagg=1;fungsi=0;fungsiAwal=0;fungsitimer=0;vketikhalo=halo.innerHTML;
  halo.innerHTML = "";var ahalo=0,vketikhalo;pesanwhatsapp = pesanWA.innerHTML;
  Content.style = "opacity:1;margin-top:16vh;";
  
  

  const body = document.querySelector("body");const swalst = Swal.mixin({timer: 2300, allowOutsideClick: false, showConfirmButton: false, timerProgressBar: true, imageHeight: 90,}); const swals = Swal.mixin({allowOutsideClick: false, cancelButtonColor: '#FF0040', imageWidth: 100, imageHeight: 100,});
  audio = new Audio('' + linkmp3.src);
  
  function createHeart() {const heart = document.createElement("div"); heart.className = "fas fa-heart"; heart.style.left = (Math.random() * 90)+"vw"; heart.style.animationDuration = (Math.random()*3)+2+"s"; body.appendChild(heart);} setInterval(function name(params) {var heartArr = document.querySelectorAll(".fa-heart"); if (heartArr.length > 100) {heartArr[0].remove()}},100);
</script>
<script src="https://feeldreams.github.io/night/script.js"></script>
<!-- Sampai Sini -->
</body>
</html>

