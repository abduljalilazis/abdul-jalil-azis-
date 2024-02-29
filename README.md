<?php
session_start();
?>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="gege.css">
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css">
</head>

<body>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container">
            <a class="navbar-brand" href="#">Cafe Ceria</a>
            <a class="navbar-toggler" type="a" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="home.php">Home</a>
                    </li>
                    <li class="nav-item dropdown dropdown-menu-end">
                        <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                            Pesanan
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="pesanan.php?jenis=wash iron">Kopi Hitam</a></li>
                            <li><a class="dropdown-item" href="pesanan.php?jenis=only iron">Kopi Sachet</a></li>
                            <li><a class="dropdown-item" href="pesanan.php?jenis=dry cleaning">Jus Buah</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="bg-info" style="min-height: 100vh;">

        <div class="container pt-5">
            <div class="card">
                <div class="card-body">
                    <div class="mb-3">
                        <label for="exampleInputtext1" class="form-label">NAMA</label>
                        <input type="text" class="form-control" id="exampleInputtext1" value="<?= $_SESSION['nama'] ?>">
                    </div>
                    <div class="mb-3">
                        <label for="exampleInputtext1" class="form-label">EMAIL</label>
                        <input type="text" class="form-control" id="exampleInputtext1" value="<?= $_SESSION['email'] ?>">
                    </div>
                    <div class="mb-3">
                        <label for="exampleInputtext1" class="form-label">NOMOR TELPON</label>
                        <input type="text" class="form-control" id="exampleInputtext1" value="<?= $_SESSION['no_hp'] ?>">
                    </div>

                    <button class="btn btn-danger" onclick="document.location.href = 'logout.php'">Logout</button>
                </div>
            </div>
        </div>
    </div>

    <script src="js/bootstrap.bundle.min.js"></script>

</body>

</html>
