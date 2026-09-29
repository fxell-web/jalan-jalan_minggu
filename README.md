<!doctype html>
<html lang="id"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jadwal Jalan-Jalan Bulan Oktober</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f7f3f9;
            color: #4a4a4a;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            background: #ffffff;
            width: 100%;
            max-width: 480px;
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(182, 157, 196, 0.15);
            border: 1px solid #f0e6f5;
        }

        h1 {
            color: #8e6c9a;
            font-size: 22px;
            text-align: center;
            margin-bottom: 8px;
        }

        p.subtitle {
            text-align: center;
            color: #a08da3;
            font-size: 14px;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label.section-title {
            display: block;
            font-weight: 600;
            color: #6d5277;
            margin-bottom: 10px;
            font-size: 15px;
        }

        input[type="text"], select {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e8def0;
            border-radius: 12px;
            font-size: 14px;
            outline: none;
            transition: all 0.3s ease;
            background-color: #faf8fc;
            color: #4a4a4a;
        }

        input[type="text"]:focus, select:focus {
            border-color: #bfa2cf;
            background-color: #ffffff;
        }

        .option-card {
            display: flex;
            align-items: center;
            background-color: #faf8fc;
            border: 2px solid #e8def0;
            padding: 12px 15px;
            border-radius: 12px;
            margin-bottom: 10px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .option-card:hover {
            border-color: #ccaedc;
            background-color: #f5eef9;
        }

        .option-card input[type="radio"],
        .option-card input[type="checkbox"] {
            margin-right: 12px;
            accent-color: #9d75ad;
            width: 18px;
            height: 18px;
        }

        .option-card span {
            font-size: 14px;
            color: #555555;
            line-height: 1.3;
        }

        .btn-send {
            width: 100%;
            background-color: #25d366;
            color: white;
            padding: 14px;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 12px rgba(37, 211, 102, 0.25);
            transition: background-color 0.2s ease, transform 0.1s ease;
            margin-top: 10px;
        }

        .btn-send:hover {
            background-color: #20bd5a;
        }

        .btn-send:active {
            transform: scale(0.98);
        }

        .alert-box {
            display: none;
            background-color: #ffe6e6;
            color: #d9534f;
            padding: 10px;
            border-radius: 8px;
            font-size: 13px;
            margin-bottom: 15px;
            text-align: center;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>✨ Jadwal Jalan-Jalan ✨</h1>
        <p class="subtitle">Pilih jadwal dan destinasi seru untuk bulan Oktober!</p>

        <div id="alertBox" class="alert-box">Harap pilih minggu dan minimal 1 destinasi!</div>

        <!-- Input Nama -->
        <div class="form-group">
            <label class="section-title" for="nama">Nama Kamu:</label>
            <input type="text" id="nama" placeholder="Masukkan nama kamu...">
        </div>

        <!-- Pilihan Minggu/Jadwal -->
        <div class="form-group">
            <label class="section-title">Pilih Minggu (Bulan Oktober):</label>
            <select id="jadwal">
                <option value="">-- Pilih Minggu --</option>
                <option value="Minggu ke-1">Minggu ke-1</option>
                <option value="Minggu ke-2">Minggu ke-2</option>
                <option value="Minggu ke-3">Minggu ke-3</option>
                <option value="Minggu ke-4">Minggu ke-4</option>
            </select>
        </div>

        <!-- Pilihan Destinasi -->
        <div class="form-group">
            <label class="section-title">Ingin jalan-jalan kemana?</label>
            
            <label class="option-card">
                <input type="checkbox" name="destinasi" value="Bon Pisa, Sawojajar Malang">
                <span>Bon Pisa, Sawojajar Malang</span>
            </label>

            <label class="option-card">
                <input type="checkbox" name="destinasi" value="Bakso Gacoan, Jl. Letjend S. Parman, Purwantoro">
                <span>Bakso Gacoan, Jl. Letjend S. Parman, Purwantoro</span>
            </label>

            <label class="option-card">
                <input type="checkbox" name="destinasi" value="UB Tabebuya, Dieng">
                <span>UB Tabebuya, Dieng</span>
            </label>

            <label class="option-card">
                <input type="checkbox" name="destinasi" value="Tempat Makan, Tumpang">
                <span>Tempat Makan, Tumpang</span>
            </label>

            <label class="option-card">
                <input type="checkbox" name="destinasi" value="Jalan-jalan Dieng - Batu">
                <span>Jalan-jalan Dieng - Batu</span>
            </label>
        </div>

        <button class="btn-send" onclick="kirimWhatsApp()">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="white">
                <path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"></path>
            </svg>
            Kirim via WhatsApp
        </button>
    </div>

    <script>
        function kirimWhatsApp() {
            const nama = document.getElementById('nama').value.trim();
            const jadwal = document.getElementById('jadwal').value;
            const alertBox = document.getElementById('alertBox');
            
            // Ambil semua checkbox destinasi yang dicentang
            const checkboxes = document.querySelectorAll('input[name="destinasi"]:checked');
            let destinasiPilihan = [];
            
            checkboxes.forEach((cb) => {
                destinasiPilihan.push(cb.value);
            });

            // Validasi input
            if (!jadwal || destinasiPilihan.length === 0) {
                alertBox.style.display = 'block';
                return;
            } else {
                alertBox.style.display = 'none';
            }

            // Susun teks pesan WhatsApp
            let teksPesan = `Halo, saya ingin konfirmasi agenda jalan-jalan bulan Oktober! 🚀\n\n`;
            if (nama) {
                teksPesan += `👤 *Nama:* ${nama}\n`;
            }
            teksPesan += `📅 *Jadwal:* ${jadwal} Oktober\n`;
            teksPesan += `📍 *Destinasi Pilihan:*\n`;
            
            destinasiPilihan.forEach((item, index) => {
                teksPesan += `${index + 1}. ${item}\n`;
            });

            teksPesan += `\nSampai jumpa! ✨`;

            // Nomor tujuan (+6285198240592)
            const nomorHP = "6285198240592";
            
            // Generate link WhatsApp api
            const urlWA = `https://api.whatsapp.com/send?phone=${nomorHP}&text=${encodeURIComponent(teksPesan)}`;

            // Buka WhatsApp
            window.open(urlWA, '_blank');
        }
    </script>

</body></html>
