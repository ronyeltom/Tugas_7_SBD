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


## SEKIAN DAN TERIMA KASIH
