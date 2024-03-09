package pemlan.case2a;

import java.util.ArrayList;
import java.util.Scanner;

class Mahasiswa {
    private String nim;
    private String nama;
    private String alamat;

    public Mahasiswa(String nim, String nama, String alamat) {
        this.nim = nim;
        this.nama = nama;
        this.alamat = alamat;
    }

    public String getNim() {
        return nim;
    }

    public String getNama() {
        return nama;
    }

    public String getAlamat() {
        return alamat;
    }
}

public class MainClass {

    public static void main(String[] a) {
        ArrayList<Mahasiswa> mahasiswas = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        boolean next = true;
        while (next) {
            System.out.print("Masukkan nim : ");
            String nim = scanner.nextLine();

            System.out.print("Masukkan nama : ");
            String nama = scanner.nextLine();

            System.out.print("Masukkan alamat: ");
            String alamat = scanner.nextLine();

            Mahasiswa mahasiswa = new Mahasiswa(nim, nama, alamat);
            mahasiswas.add(mahasiswa);

            System.out.print("Tambah lagi? ");
            String tambah = scanner.nextLine();

            if (!tambah.equalsIgnoreCase("y")) {
                next = false;
            }
        }
        System.out.println("==================================");
        for (Mahasiswa mahasiswa : mahasiswas) {
            System.out.println(mahasiswa.getNim() + " | " + mahasiswa.getNama() + " | " + mahasiswa.getAlamat());
        }
    }
}
