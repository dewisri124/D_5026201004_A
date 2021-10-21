# D_5026201004_A
ETS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <title>Form Pendaftaran Kuota Internet</title>

    <script>
        function validation(){
            var hasil = true
            if($("#Nama").val().length>1){
                $("#namaerror").text("nama harus lebih dari 1 kata")
                $("#namaerror").focus
                hasil = false
            }
            else{
                $("#namaerror").text("")
            }

            var n = $("#nrp").val()
            if(isNaN(n) || n.length !=10){
                $("#nrperror").text("nrp harus angka dan berjumlah 10 digit")
                $("nrperror").focus
                hasil = false
            }
            else{
                $("#nrperror").text("")
            }

            if($("#jurusan").val() == 0){
                $("#jurusanerror").text("jurusan harus diisi")
                $("#jurusanerror").focus
                hasil = false
            }
            else{
                $("#jurusanerror").text("")
            }
            return hasil
        }
    </script>
    <style>
        body{
            background-image: url("https://backgroundcheckall.com/wp-content/uploads/2017/12/background-teknologi-informasi.jpg");
            background-repeat: no-repeat;
            background-size: cover;
        }

        form{
            background-color: white;
        }
       #title{
           text-align: center;
       } 
       label{
           font-size: large;
           font-weight: 500;
       }
       .error{
           color: rgb(46, 243, 79);
       }
    </style>
</head>
<body>
    <div class="container">
        <form class="form border border-2 border-dark rounded px-5 py-3 my-5" onsubmit="return validation() " action="https://www.youtube.com/" >
            <p>Dewi Sri Wahyuni</p>
            <p>Dewi Sri</p>
            <p>5026201004</p>

            <h2 id="title">Form Pendaftaran Kuota Internet</h2>
            <br>
            <div class="form-group">
                <div class="row">
                    <div class="col-5">
                        <label for="judul">Nama Mahasiswa</label>
                    </div>
                    <div class="col-1">
                        <p>:</p>
                    </div>
                    <div class="col-6">
                        <input type="text" name="Nama" id="Nama" class="form-control" placeholder="Masukkan Nama lengkap" required>
                    </div>
                </div>
            </div>
            <p id="Nama error" class="error"></p>
            <div class="form-group">
                <div class="row">
                    <div class="col-5">
                        <label for="nobuku">NRP Mahasiswa</label>
                    </div>
                    <div class="col-1">
                        <p>:</p>
                    </div>
                    <div class="col-6">
                        <input type="text" name="nrp" id="nrp" class="form-control" placeholder="Masukkan NRP" required>
                    </div>
                </div>
            </div>
            <p id="nobukuerror" class="error"></p>
            <div class="form-group">
                <div class="row">
                    <div class="col-5">
                        <label for="jenis">Jurusan</label>
                    </div>
                    <div class="col-1">
                        <p>:</p>
                    </div>
                    <div class="col-6">
                            <select class="form-control" id="jenis" name="jenis" required>
                                <option value="0"></option>
                              <option value="biasa">Sistem Informasi</option>
                              <option value="kilat">Elektro</option>
                              <option value="lama">Informatika</option>
                            </select>
                    </div>
                </div>
            </div>
            <p id="jurusanerror" class="error"></p>
            <div class="form-group">
                <div class="row">
                    <div class="col-5">
                        <label for="Nomor Telephone">Nomor Telephone</label>
                    </div>
                    <div class="col-1">
                        <p>:</p>
                    </div>
                    <div class="col-6">
                        <input type="number" name="telephone" id="telephone" class="form-control" minlength="10" maxlength="12" required>
                    </div>
                </div>
            </div>
            <br>
                <div class="row">
                    <div class="col-6 text-center">
                        <button type="submit" class="btn btn-primary btn-lg mx-3">Kirim</button>
                    </div>
                    <div class="col-6 text-center">
                        <button type="reset" class="btn btn-success btn-lg mx-3">Reset</button>
                    </div>
                </div>
        </form>
        
    </div>
    
</body>
</html>
