|   RONY ELTOM ATIBAMAN     |      Sistem Basis data     |
|---------------------------|----------------------------|
|       312010003           |         TI.20.D.1          |

# Tugas_7_SBD
## file pasien 
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
            body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
    <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>Id Pasien</td>
                <td>Nama Pasien</td>
                <td>Jenis Kelamin</td>
                <td>Umur</td>                
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM pasien');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr>
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id_pasien'] ?></td>
                <td><?php echo $data['nama_pasien'] ?></td>
                <td><?php echo $data['jenis_kelamin'] ?></td>
                <td><?php echo $data['umur'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
<style css>
{
        margin: 0;
        padding: 0;
    }
    body {
        line-height:1;
        font-size:100%;
        font-family:'Open Sans', sans-serif;
        color:#5a5a5a;
    }
    #container {
        width: 980px;
        margin: 0 auto;
        box-shadow: 0 0 1em #cccccc;
    }
    /* header */
    header {
        padding: 20px;
    }
    header h1 {
        margin: 20px 10px;
        color: #b5b5b5;
    }
    </style>
```
> hasil browser
![1](https://user-images.githubusercontent.com/101711060/175797822-2f96ec7b-3c3a-4089-ab40-65df1e4beb94.png)




## file obat
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
             body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
        <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>Id obat</td>
                <td>Nama obat</td>              
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM obat');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr>
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id_obat'] ?></td>
                <td><?php echo $data['nama_obat'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
```
> hasil Browser
![2](https://user-images.githubusercontent.com/101711060/175797823-8ca37c38-1fbe-425b-9117-68a109b05850.png)


## file dokter
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
        body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
        <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>Id dokter</td>
                <td>Nama dokter</td>                
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM dokter');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr>
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id_dokter'] ?></td>
                <td><?php echo $data['nama_dokter'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
```
> Hasil Browser
![3](https://user-images.githubusercontent.com/101711060/175797825-45582118-e4a7-4973-b5d8-e6bdd0d20db5.png)



## file berobat
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
         body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
    <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>Id berobat</td>
                <td>id pasien</td>
                <td>id dokter</td>
                <td>tgl berobat</td>
                <td>keluhan pasien</td>
                <td>hasil diagnosa</td>             
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM berobat');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr>
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id_berobat'] ?></td>
                <td><?php echo $data['id_pasien'] ?></td>
                <td><?php echo $data['id_dokter'] ?></td>
                <td><?php echo $data['tgl_berobat'] ?></td>
                <td><?php echo $data['keluhan_pasien'] ?></td>
                <td><?php echo $data['hasil_diagnosa'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
```
> hasil Browser
![4](https://user-images.githubusercontent.com/101711060/175797827-8ae6b2e0-80ca-47b8-8f83-112a9d082b4d.png)


## file Resep_obat
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
       body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
    <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>id_resep</td>
                <td>id_berobat</td>  
                <td>id_obat</td>                      
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM resep_obat');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr style="background-color: aliceblue;">
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id_resep'] ?></td>
                <td><?php echo $data['id_berobat'] ?></td>
                <td><?php echo $data['id_obat'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
```
> Hasil Browser
![5](https://user-images.githubusercontent.com/101711060/175797828-eb7ff1ed-f704-45e6-a363-9748e3a85729.png)


## file user
```
<!DOCTYPE html>
<html>
<head>
    <title>Menampilkan Data Dari Database PHP </title>
    <style>
          body {
        win-height: 95vh;
        background-image: uber-gradient(-20deg,#142846 85, 6944 1085); 
        background: url(klinik.jpg)no-repeat; 
        background-size: cover;
        font-family: quicsand;
       }
       table {
        text-align: center;
       }
       h1{
        color:red; text-align: center;font-size:40px;font-style:bold;font-family:times;
       }

        table, tr,td {
            border: solid in lightsteelblue;
            border-collapse: collapse;
            padding: 10px 35px; 
            font-family: times="bold"; 
            font-size: 20px
        }
        thead {
            background-color: #ccdfcc;
        }
    </style>
</head>
<body>
        <h1 align="center">Welcome Rony Hospital</h1>
    <table>
        <thead>
            <tr>
                <td>No</td>
				<td>Id</td>
                <td>username</td>  
                <td>password</td>
                <td>nama lengkap</td>                      
            </tr>
        </thead>
        <?php
        include "koneksi.php";
        $no = 1;
        $query = mysqli_query($conn, 'SELECT * FROM user');
        while ($data = mysqli_fetch_array($query)) {
        ?>
            <tr>
                <td><?php echo $no++ ?></td>
				<td><?php echo $data['id'] ?></td>
                <td><?php echo $data['username'] ?></td>
                <td><?php echo $data['password'] ?></td>
                <td><?php echo $data['nama_lengkap'] ?></td>
            </tr>
        <?php } ?>
    </table>
</body>
```
> Hasil Browser
![6](https://user-images.githubusercontent.com/101711060/175797831-f37309b0-edc6-4ac5-94db-923d8775f036.png)

## File Home
```
<?php
	require "koneksi.php";
	
	$querypasien = mysqli_query($conn, "SELECT * FROM pasien");
	$jumlahpasien = mysqli_num_rows($querypasien);
	
	$queryobat = mysqli_query($conn, "SELECT * FROM obat");
	$jumlahobat = mysqli_num_rows($queryobat);
	
	$querydokter = mysqli_query($conn, "SELECT * FROM dokter");
	$jumlahdokter = mysqli_num_rows($querydokter);
	
	$queryberobat = mysqli_query($conn, "SELECT * FROM berobat");
	$jumlahberobat = mysqli_num_rows($queryberobat);
	
	$queryresep = mysqli_query($conn, "SELECT * FROM resep_obat");
	$jumlahresep = mysqli_num_rows($queryresep);
	
	$queryuser = mysqli_query($conn, "SELECT * FROM user");
	$jumlahuser = mysqli_num_rows($queryuser);
?>
<!DOCTYPE html>
<html lang="en">
<head>
	
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="css/bootstrap.min.css" />
    <script src="js/bootstrap.min.js"></script>
	<link rel="stylesheet" href="fontawesome/fontawesome/css/all.css" />
    <title>Home</title>
	<link rel="stylesheet" href="style.css">

 <div id="container">

 </div>
</body>
</html>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

<nav>
 <a href="" class="active">Home</a>
 <a href="">Artikel</a>
 <a href="">About</a>
 <a href="">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
 <section id="main"></section>
 <aside id="sidebar"></aside>
</section>

<style css >
/* navigasi */
body {
    min-height: 95vh;
    background-image: linear-gradient(-20deg,#FF7F50 0%, #FF7F50 100%);
    background: url(klinik.jpg)no-repeat;
    position: fixed;
    width: 100%;
    height: 100%;
    background-size: cover;
    font-family: 'Quicksand',sans-serif;

}
table {
    border-collapse: collapse
    color: #FFFFF0;
}
nav {
 display: block;
 background-color: #A52A2A;
}
nav a {
 padding: 15px 30px;
 display: inline-block;
 color: #ffffff;
 font-size: 14px;
 text-decoration: none;
 font-weight: bold;
}
nav a.active,
nav a:hover {
 background-color: #A52A2A;
}
</style>
	
	<style>
		.kotak {
			border: solid;
		}
		.summary-pasien{
			background-color: #FF8C00;
			border-radius: 15px;
		}
		.summary-obat{
			background-color: #0a516b;
			border-radius: 15px;
		}
		.summary-dokter{
			background-color: #008B8B;
			border-radius: 15px;
		}
		.summary-berobat{
			background-color: #8FBC8F;
			border-radius: 15px;
		}
		.summary-resep{
			background-color: #0000FF;
			border-radius: 15px;
		}
		.summary-user{
			background-color: #5F9EA0;
			border-radius: 15px;
		}
		
		.no-decoration{
			text-decoration: none;
		}
		
	</style>

<div class=”row g-0″></div>
<div class="container shadow">
<div style=”margin:21px;”></div>
<div class=”col-sm-11 mx-auto”>
<div class=”card”>
<div class=”card-body”>
<p>
<form method=”POST”>
<table style=”width:50%;padding:15px;”>
</div>
</div>
</div>
</div>
</div>
</div>
<tr>
<td>Id</td>
<td>:</td>
<td><textarea name=”id_pasien” class=”inputanallborder” style=”width:70%”></textarea></td>
</tr>
<tr>
<td>Nama</td>
<td>:</td>
<td><input type=”text” name=”nama” class=”inputan”></td>
</tr>
<tr>
<td>option</td>
<td>:</td>
<td><select name=”option” class=”inputan”>
<option>Pasien</option>
<option>Obat</option>
<option>Resep obat</option>
<option>Dokter</option>
<option>User</option>
<option>Resep_obat</option>
</select></td>
</tr>
</table>


<form  action="index.php" method="get">
<input type="submit" value="Cari">
</form>
<?php 
    if(isset($_GET['cari'])){
        $cari = $_GET['cari'];
        echo "<b>Hasil pencarian : ".$cari."</b>";
    }
?>

	<div class="container mt-4">
		<nav aria-label="breadcrumb">
		  <ol class="breadcrumb">
			<li class="text-black-item active" aria-current="page">
				<i class="fa-solid fa-file-medical fa-2x"></i>
				<h2 align="center" > Data Hospital Rony Eltom</h2>
			</li>
		  </ol>
		</nav>
		
		<div class="container mt-4">
			<div class="row">
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-pasien p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-bed-pulse fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">Pasien</h3>
								<p class="fs-4"><?php echo $jumlahpasien; ?> Pasien</p>
								<p> <a href="pasien.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
				
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-obat p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-capsules fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">Obat</h3>
								<p class="fs-4"><?php echo $jumlahobat; ?> Obat</p>
								<p> <a href="obat.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
				
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-dokter p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-user-doctor fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">Dokter</h3>
								<p class="fs-4"><?php echo $jumlahdokter; ?> Dokter</p>
								<p> <a href="dokter.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
				
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-berobat p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-syringe fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">Berobat</h3>
								<p class="fs-4"><?php echo $jumlahberobat; ?> Berobat</p>
								<p> <a href="berobat.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
				
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-resep p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-receipt fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">Resep_Obat</h3>
								<p class="fs-4"><?php echo $jumlahresep; ?> Resep_obat</p>
								<p> <a href="resep_obat.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
				
				<div class="col-lg-4 col-md-6 col-12 mb-3">
					<div class="summary-user p-3">
						<div class="row">
							<div class="col-6">
								<i class="fa-solid fa-hospital-user fa-7x text-black-50"></i>
							</div>
							<div class="col-6 text-black">
								<h3 class="fs-2">User</h3>
								<p class="fs-4"><?php echo $jumlahuser; ?> User</p>
								<p> <a href="user.php" class="text-black no-decoration">Lihat Detail</a></p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
</body>
</html>
```
> Hasil Browser
![7](https://user-images.githubusercontent.com/101711060/175797953-e495938b-a24b-416b-95af-ceb28f68bfee.png)


## SEKIAN DAN TERIMA KASIH
