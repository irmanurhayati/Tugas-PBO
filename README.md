# Tugas-PBO
// Kelas utama bernama Mobil
public class Mobil {

    // === Atribut (variabel dalam class) ===
    String merk;
    String warna;
    int tahun;

    // === No-argument constructor ===
    // Constructor ini dipanggil jika objek dibuat tanpa memberikan nilai awal
    public Mobil() {
        merk = "Belum diketahui";
        warna = "Belum diketahui";
        tahun = 0;
    }

    // === Parameterized constructor ===
    // Constructor ini digunakan untuk mengisi atribut mobil secara langsung saat objek dibuat
    public Mobil(String merk, String warna, int tahun) {
        this.merk = merk;   // 'this' menunjukkan variabel dalam class
        this.warna = warna;
        this.tahun = tahun;
    }

    // === Method untuk menampilkan data mobil ===
    public void tampilkanInfo() {
        System.out.println("Merk Mobil  : " + merk);
        System.out.println("Warna Mobil : " + warna);
        System.out.println("Tahun Mobil : " + tahun);
    }

    // === Method overloading 1 ===
    // Method untuk mengubah warna mobil
    public void ubahData(String warnaBaru) {
        this.warna = warnaBaru;
        System.out.println("Warna mobil telah diubah menjadi: " + warna);
    }

    // === Method overloading 2 ===
    // Method dengan nama sama tapi parameter berbeda (ubah warna dan tahun sekaligus)
    public void ubahData(String warnaBaru, int tahunBaru) {
        this.warna = warnaBaru;
        this.tahun = tahunBaru;
        System.out.println("Warna dan tahun mobil telah diperbarui menjadi: " + warna + ", " + tahun);
    }

    // === Method utama (main) untuk menjalankan program ===
    public static void main(String[] args) {

        // Membuat objek menggunakan no-argument constructor
        Mobil mobil1 = new Mobil();
        System.out.println("=== Data Mobil 1 ===");
        mobil1.tampilkanInfo();

        // Membuat objek menggunakan parameterized constructor
        Mobil mobil2 = new Mobil("Toyota", "Hitam", 2022);
        System.out.println("\n=== Data Mobil 2 ===");
        mobil2.tampilkanInfo();

        // Memanggil method overloading
        System.out.println("\n=== Update Data Mobil 2 ===");
        mobil2.ubahData("Merah"); // Memanggil method pertama (ubah warna)
        mobil2.ubahData("Biru", 2024); // Memanggil method kedua (ubah warna dan tahun)
    }
}
