# program-sederhana-untuk-mengelola-data-mahasiswa-di-sebuah-universitas.
# kelas Manusia 
class Mahasiswa:

    # inisialisasi atribut Nama, NIM, dan Jurusan
    def __init__(self, nama, nim, jurusan):
        self.nama = nama
        self.nim = nim
        self.jurusan = jurusan

    # menampilkan informasi Nama, NIM, dan nama Jurusan mahasiswa
    def tampilkan_info(self):
        print("→ Nama: ", self.nama)
        print("  NIM: ", self.nim)
        print("  Jurusan: ", self.jurusan.NamaJurusan)
        print("")


# Kelas Jurusan:
class Jurusan:

    # inisialisasi atribut NamaJurusan dan DaftarMahasiswa
    def __init__(self, nama_jurusan):
        self.NamaJurusan = nama_jurusan
        self.DaftarMahasiswa = []

    # inisialisasi atribut NamaJurusan dan DaftarMahasiswa
    def tambah_mahasiswa(self, mahasiswa):
        self.DaftarMahasiswa.append(mahasiswa)

    # menampilkan daftar mahasiswa yang terdaftar dalam Jurusan 
    def tampilkan_daftar_mahasiswa(self):
        print("")
        print("Berikut ini Daftar Mahasiswa di Jurusan", self.NamaJurusan)
        for mahasiswa in self.DaftarMahasiswa:
            mahasiswa.tampilkan_info()

# Kelas Universitas:
class Universitas:

    #  inisialisasi atribut NamaUniversitas dan DaftarJurusan
    def __init__(self, nama_universitas):
        self.NamaUniversitas = nama_universitas
        self.DaftarJurusan = []

    # menambahkan objek Jurusan ke dalam DaftarJurusan
    def tambah_jurusan(self, jurusan):
        self.DaftarJurusan.append(jurusan)

    # menampilkan daftar jurusan yang ada di Universitas
    def tampilkan_daftar_jurusan(self):
        print(" ~~~~~ Daftar Jurusan di Universitas", self.NamaUniversitas,"~~~~~")
        for jurusan in self.DaftarJurusan:
            print(">",jurusan.NamaJurusan)


# Objek Universitas
universitas_xyz = Universitas("XYZ")

# Objek Jurusan
teknik_informatika = Jurusan("Teknik Informatika")
teknik_sipil = Jurusan("Teknik Sipil")
teknik_mesin = Jurusan("Teknik Mesin")
teknik_elektro = Jurusan("Teknik Elektro")
arsitektur = Jurusan("Arsitektur")
sistem_informasi = Jurusan("Sistem Informasi")


# Objek Jurusan ke dalam Universitas XYZ
universitas_xyz.tambah_jurusan(teknik_informatika)
universitas_xyz.tambah_jurusan(teknik_sipil)
universitas_xyz.tambah_jurusan(teknik_mesin)
universitas_xyz.tambah_jurusan(teknik_elektro)
universitas_xyz.tambah_jurusan(sistem_informasi)
universitas_xyz.tambah_jurusan(arsitektur)

# Objek Mahasiswa
mahasiswa1A = Mahasiswa("Ulfa Stevi Juliana", "G1A022042", teknik_informatika)
mahasiswa2A = Mahasiswa("Muhammad Hisbulah Endima Tandjung", "G1A022034", teknik_informatika)
mahasiswa3A = Mahasiswa("Akbar Agpranata", "G1A022062", teknik_informatika)
mahasiswa4A = Mahasiswa("MERLY YUNI PURNAMA", "G1A022006", teknik_informatika)
mahasiswa5A = Mahasiswa("TIESYA ANDRIANI RAMADHANTI", "G1A022014", teknik_informatika)

mahasiswa1B = Mahasiswa("Jelitha Adlin", "G1B022096", teknik_sipil)
mahasiswa2B = Mahasiswa("Emirza hafiz hidayatullah", "G1B022004", teknik_sipil)
mahasiswa3B = Mahasiswa("Fadhilah ayu utami ", "G1B022001", teknik_sipil)
mahasiswa4B = Mahasiswa("Meilinda ayu veronika", "G1B022003", teknik_sipil)
mahasiswa5B = Mahasiswa("Dianti puspa sari ", "G1B022095", teknik_sipil)

mahasiswa1C = Mahasiswa("Bayu wirya Sanjaya ", "G1C022001", teknik_mesin)
mahasiswa2C = Mahasiswa("Riski Hotman Misael", "G1C022003", teknik_mesin)
mahasiswa3C = Mahasiswa("Musdalifah Hasibuan", "G1C022005", teknik_mesin)
mahasiswa4C = Mahasiswa("Syaugi Fathi walizah", "G1C022009", teknik_mesin)
mahasiswa5C = Mahasiswa("Antoni muslik", "G1C022011", teknik_mesin)

mahasiswa1D = Mahasiswa("Fadillah mardiansyah putra", "G1D022039", teknik_elektro)
mahasiswa2D = Mahasiswa("Ikram sani pangestu", "G1D022017", teknik_elektro)
mahasiswa3D = Mahasiswa("Febrian valentino", "G1D022071", teknik_elektro)
mahasiswa4D = Mahasiswa("Lorenza valentin", "G1D022073", teknik_elektro)
mahasiswa5D = Mahasiswa("Marco gabriel damanik", "G1D022029", teknik_elektro)

mahasiswa1E = Mahasiswa("M. FADHIL ARIDHA", "G1E022030", arsitektur)
mahasiswa2E = Mahasiswa("David Ainal Yakin", "G1E022001", arsitektur)
mahasiswa3E = Mahasiswa("RISMA SARI HARIYANTI", "G1E022002", arsitektur)
mahasiswa4E = Mahasiswa("AMARA PUTRI", "G1E022003", arsitektur)
mahasiswa5E = Mahasiswa("FERDI JANGJAYA ", "G1A022066", arsitektur)

mahasiswa1F = Mahasiswa("M Hidayat Pahlevi ", "G1F022031", sistem_informasi)
mahasiswa2F = Mahasiswa("Annas zam zam", "G1F022013", sistem_informasi)
mahasiswa3F = Mahasiswa("Dwi saputra", "G1F022069", sistem_informasi)
mahasiswa4F = Mahasiswa("Muhammad atthariq", "G1F022023", sistem_informasi)
mahasiswa5F = Mahasiswa("Faturrahman atalah", "G1F022063", sistem_informasi)



# Menambahkan objek Mahasiswa ke dalam Jurusan Teknik Informatika di Universitas XYZ
teknik_informatika.tambah_mahasiswa(mahasiswa1A)
teknik_informatika.tambah_mahasiswa(mahasiswa2A)
teknik_informatika.tambah_mahasiswa(mahasiswa3A)
teknik_informatika.tambah_mahasiswa(mahasiswa4A)
teknik_informatika.tambah_mahasiswa(mahasiswa5A)

teknik_sipil.tambah_mahasiswa(mahasiswa1B)
teknik_sipil.tambah_mahasiswa(mahasiswa2B)
teknik_sipil.tambah_mahasiswa(mahasiswa3B)
teknik_sipil.tambah_mahasiswa(mahasiswa4B)
teknik_sipil.tambah_mahasiswa(mahasiswa5B)

teknik_mesin.tambah_mahasiswa(mahasiswa1C)
teknik_mesin.tambah_mahasiswa(mahasiswa2C)
teknik_mesin.tambah_mahasiswa(mahasiswa3C)
teknik_mesin.tambah_mahasiswa(mahasiswa4C)
teknik_mesin.tambah_mahasiswa(mahasiswa5C)

teknik_elektro.tambah_mahasiswa(mahasiswa1D)
teknik_elektro.tambah_mahasiswa(mahasiswa2D)
teknik_elektro.tambah_mahasiswa(mahasiswa3D)
teknik_elektro.tambah_mahasiswa(mahasiswa4D)
teknik_elektro.tambah_mahasiswa(mahasiswa5D)

arsitektur.tambah_mahasiswa(mahasiswa1E)
arsitektur.tambah_mahasiswa(mahasiswa2E)
arsitektur.tambah_mahasiswa(mahasiswa3E)
arsitektur.tambah_mahasiswa(mahasiswa4E)
arsitektur.tambah_mahasiswa(mahasiswa5E)

sistem_informasi.tambah_mahasiswa(mahasiswa1F)
sistem_informasi.tambah_mahasiswa(mahasiswa2F)
sistem_informasi.tambah_mahasiswa(mahasiswa3F)
sistem_informasi.tambah_mahasiswa(mahasiswa4F)
sistem_informasi.tambah_mahasiswa(mahasiswa5F)

# Menampilkan daftar jurusan di Universitas XYZ
universitas_xyz.tampilkan_daftar_jurusan()

''' Meminta input dari pengguna untuk memilih jurusan
disini user harus menginput nama jurusan yang ingin dilihat datanya'''

pilihan_jurusan = input("Masukkan pilihan jurusan : ")

# Menentukan objek Jurusan berdasarkan pilihan
if pilihan_jurusan == "Teknik Informatika":
    jurusan = teknik_informatika
elif pilihan_jurusan == "Teknik Sipil":
    jurusan = teknik_sipil
elif pilihan_jurusan == "Teknik Mesin":
    jurusan = teknik_mesin
elif pilihan_jurusan == "Teknik Elektro":
    jurusan = teknik_elektro
elif pilihan_jurusan == "Sistem Informasi":
    jurusan = sistem_informasi
elif pilihan_jurusan == "Arsitektur":
    jurusan = arsitektur       
else: 
    print("Pilihan jurusan tidak valid.")
   

# Menampilkan daftar mahasiswa di Jurusan yang dipilih menggunakan percabangan if
if jurusan:
    jurusan.tampilkan_daftar_mahasiswa()
   
