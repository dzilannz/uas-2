# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama		: Dzilan Nazira Zahratunnisa
<br>NIM		:	1227050040
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Source code kali ini masih menggunakan array dua dimensi, namun tujuannya nanti _output_ yang dihasilkan akan berbentuk deret aretmatika. Dimana deret aritmatika tersebut merupakan bilangan yang tidak habis dibagi oleh bilangan tertentu. Di program ini memakai bilangan 3, 5, dan. Berarti nanti tampilannya akan menampilkan deret aritmatika yang tidak habis dibagi 3, 5, dan 7 dari nilai yang kita masukkan.

<p> Untuk algoritmanya seperti ini :
<br> 1. Pengguna menginput jumlah baris dan kolom yang rangenya 0–20.
<br> 2. Pengguna memasukkan satu per satu nilai pada array dua dimensi yang sudah tadi dimasukkan.
<br> 3. Nilai yang dimaukkan akan tertampil dalam bentuk matriks.
<br> 4. Nilai tersebut akan dicek apakah habis dibagi 3, 5, dan 7 atau tidak.
<br> 5. Bila nilai yang dimasukkan tidak habis dibagi 3, 5, dan 7, maka tampilannya akan keluar dengan bentuk deret aritmatika. Kemudian jika habis dibagi oleh bilangan 3, 5, dan 7, tampilannya akan kosong.

## Source Code
```cpp
#include <iostream>
using namespace std;

int main (){
	int data[20][20];
	int baris, kolom, i, j;

	cout << "Masukkan jumlah baris : ";
	cin >> baris;
	cout << "Masukkan jumlah kolom : ";
	cin >> kolom;
	cout << endl;
	
	for (i=0;i<=baris-1;i++) {
		for(j=0;j<=kolom-1;j++) {
			cout << "Baris " << i+1 << " , Kolom " << j+1<< " = ";
			cin >> data [i][j];
		}
	}
	cout << "Nilai yang diinputkan : \n";
	for(int i = 0; i < baris; i++){
		for(int j = 0; j < kolom; j++){
			cout<< data[i][j]<<"\t";
		}
		cout<<endl;
	}
	int angka[100];
	int index = 0;
	for(i=0;i<baris;i++){
		for(j=0;j<kolom;j++) {
			if (data [i][j]%3 != 0 && data[i][j]%5 != 0 && data[i][j]%7 != 0){
				angka[index] = data[i][j];
				index++;
			}
		}
	}
	cout<<"Angka yang tidak bisa dibagi 3, 5, 7 adalah ";
	for(int i = 0; i < index; i++){
		cout<<angka[i]<<", ";

	}
}
```

## Output
Hasilnya akan menampilkan seperti ini :

![nomer2](https://user-images.githubusercontent.com/121169444/209252363-bf6210a3-f78e-4780-bc3a-715fe19ab464.png)
