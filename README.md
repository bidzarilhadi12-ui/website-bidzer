<!-- ===================== -->
<!-- FILE: index.html -->
<!-- ===================== -->
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Caffe Bidzar</title>


<!-- HUBUNGKAN FILE CSS -->
<link rel="stylesheet" href="style.css">
</head>
<body>


<div class="container">
<h1>Caffe Bidzar</h1>


<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93" class="caffe-img" alt="Caffe">


<label>Nama Pelanggan</label>
<input type="text" id="nama">


<label>Pilih Minuman</label>
<select id="menu">
<option value="">-- Pilih --</option>
<option value="kopi">Kopi</option>
<option value="teh">Teh</option>
</select>


<label>Jumlah</label>
<input type="number" id="jumlah">


<button onclick="hitung()">Pesan</button>


<div class="hasil" id="output">Hasil akan tampil di sini</div>
</div>


<!-- HUBUNGKAN FILE JAVASCRIPT -->
<script src="script.js"></script>
</body>
</html>

body {
background: white;
padding: 20px;
max-width: 400px;
margin: auto;
border-radius: 8px;
box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}


h1 {
text-align: center;
color: #5a3825;
}


label {
display: block;
margin-top: 15px;
}


input, select, button {
width: 100%;
padding: 8px;
margin-top: 5px;
}


button {
background-color: #5a3825;
color: white;
border: none;
margin-top: 20px;
cursor: pointer;
}


.caffe-img {
width: 100%;
border-radius: 6px;
margin: 15px 0;
}


.hasil {
margin-top: 20px;
padding: 10px;
background: #eee;
}

function hitung() {
let nama = document.getElementById("nama").value;
let menu = document.getElementById("menu").value;
let jumlah = document.getElementById("jumlah").value;


let harga = 0;


// LOGIC IF ELSE
if (menu === "kopi") {
harga = 15000;
} else if (menu === "teh") {
harga = 10000;
} else {
document.getElementById("output").innerHTML = "Silakan pilih menu";
return;
}


let total = harga * jumlah;


// OUTPUT
document.getElementById("output").innerHTML =
"Halo " + nama + "<br>Total Bayar: Rp " + total;
}
