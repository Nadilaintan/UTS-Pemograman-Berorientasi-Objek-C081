#include <cstdlib>
#include <iostream>

using namespace std;

class menu{ //class
      private :
      		  int paket,porsi,Nomormeja;
              float jumlah,jumlah_meja,listrik,perjam,total;
              char nama[100];
              
      public :
      	//atribut yang dibutuhkan
      	/* 
      	paket menu
      	porsi 
      	nomor meja
      	listrik
      	// pilihan fitur pilihan menu
      	pilih paket, pilih meja, hitung jml, tampilan struk
      	*/

             menu();
             void pilih_paket();
             void pilih_meja();
             void hitung_jml();
             void tampil_struk();
      };

menu::menu(){        

		cout<<"\t\t       DAFTAR MENU MAKANAN DEMEN MAKAN RESTO"<<endl;
                 }

void menu::pilih_paket(){
	 cout<<"-----------------------------------------------------"<<endl;
	 cout<<"\t\tPILIHAN MENU :"<<endl;
	 cout<<"-----------------------------------------------------"<<endl;
     cout<<"\n\nPilihlah paket menu yang akan di pesan :\n\n";
 	 cout<<"1. Paket 1 = Nasi Ayam Goreng lv 0-5 + minum "<<endl;
     cout<<"2. Paket 2 = Nasi Ayam geprek lv 0-5 + minum "<<endl;
     cout<<"3. Paket 3 = Nasi ayam lada hitam lv 0-5 + minum "<<endl;
     cout<<"4. Paket spesial = Nasi ayam balado + cheese + minum "<<endl;
     cout<<"pilih paket : ";
     cin>>paket;
     cout<<"Mau beli berapa porsi : ";
     cin>>porsi;
     cout<<"masukan lama fasilitas listrik yang digunakan : ";
     cin>>listrik;
     }

void menu::pilih_meja(){
     cout<<"\n\nBerapa Nomor meja yang dipesan : ";
     cin>>Nomormeja;
     cout<<"pesan berapa lama : ";
     cin>>perjam;
     }


void menu::hitung_jml(){
     if(paket>0 && paket<5){
        if (paket==1){
                                   
        	jumlah=15000*porsi;
            listrik=5000*perjam;
            total=jumlah+listrik;               
               } else if (paket==2){
              
            jumlah=18000*porsi;
            listrik=5000*perjam;
            total=jumlah+listrik; 
               } else if (paket==3){
              
            jumlah=20000*porsi;
            listrik=5000*perjam;
			total=jumlah+listrik;                
              
               } else {
                                 
            jumlah=25000*porsi;
            listrik=5000*perjam;
            total=jumlah+listrik;                 
                                  }
               }
     else{
          cout<<"Pilihan tidak ada!"<<endl;
          }
   }
    
void menu::tampil_struk(){
	char nama[100];
	cout<<"========================================================"<<endl;
   	 cout<<"\t\t   KASIR DEMEN MAKAN RESTO"<<endl;
	 cout<<"\t\tSILAHKAN PESAN & BAYAR DISINI"<<endl;
	 cout<<"========================================================"<<endl;
	 cout<<"Nama Pelanggan           : ";cin>>nama;
     cout<<"total penggunaan listrik : "<<listrik<<"\n";
     cout<<"jumlah pesanan           : "<<jumlah<<"\n";;
     cout<<"total bayar pesanan      : "<<total<<"\n";
       
 
     };
  
 class camilan:public menu {
 	int porsi,meja;
 	float admin,harga,jumlah,total;
 	
 	public:
 		//atribut yang dibutuhkan
 		/*
 		camilan
 		//fitur yang digunakan
 		pilih snack,pilih antrian,hitungjumlah,tampilanstruk
 		*/
 		 camilan();
 		  void pilih_snack();
 		  void pilih_admin();
          void hitung_jumlah();
		  void tampil_struk2();		
 };
camilan::camilan(){
                cout<<"======================================================================================="<<endl;
                cout<<"\t\t\tSilahkan pilih camilan\t\t"<<endl;
                cout<<"=======================================================================================\n\n"<<endl;
                 }
 void camilan::pilih_snack(){
	 cout<<"-----------------------------------------------------"<<endl;
	 cout<<"\t\tPILIHAN CAMILAN :"<<endl;
	 cout<<"-----------------------------------------------------"<<endl;
     cout<<"\n\nPilihlah paket snack yang akan di pesan :\n\n";
 	 cout<<"1. Camilan 1 = sosis bakar "<<endl;
     cout<<"2. Camilan 2 = kentang goreng "<<endl;
     cout<<"3. Camilan 3 = roti bakar "<<endl;
     cout<<"pilih Camilan : ";
     cin>>harga;
     cout<<"berapa porsi : ";
     cin>>porsi;
     }
   
   void camilan::pilih_admin(){
   	 admin=2000;
     cout<<"berapa biaya admin :"<<admin<<endl;
     }
	   
void camilan::hitung_jumlah(){
     if(harga>0 && harga<4){
        if (harga==1){
                                   
        	jumlah=15000*porsi;
            total=jumlah+admin;               
               } else if (harga==2){
              
            jumlah=12000*porsi;
            total=jumlah+admin; 
    
               } else {
              
            jumlah=10000*porsi;
           total=jumlah+admin;   
		}
              
               } else{
          cout<<"Pilihan tidak ada!"<<endl;
          }
}
void camilan::tampil_struk2(){
{
	char nama[50];
	 cout<<"========================================================"<<endl;
   	 cout<<"\t\t   KASIR DEMEN MAKAN RESTO"<<endl;
	 cout<<"\t\tSILAHKAN PESAN & BAYAR DISINI"<<endl;
	 cout<<"========================================================"<<endl;
	 cout<<"\t\tNama Pelanggan              : ";cin>>nama;
     cout<<"jumlah snack yang di pesan      : "<<jumlah<<"\n";
     cout<<"total bayar snack yang di pesan : "<<total<<"\n";
}
     };
   
int main(int argc, char *argv[])
{
	
    menu pilihan;
    	cout<<"\t\t\tSelamat datang di Demen Makan Resto\t\t"<<endl;
                 cout<<"\t\t\t  Tak datang tak kenyang\t\t"<<endl;
                 cout<<"\t\t\t\t   Free Wifi\t\t"<<endl;
                 cout<<"=======================================================================================\n\n"<<endl;

    pilihan.pilih_paket();
    pilihan.pilih_meja();
    pilihan.hitung_jml();
    pilihan.tampil_struk();
    
    camilan pilih;
    pilih.pilih_snack();
    pilih.pilih_admin();
    pilih.hitung_jumlah();
    pilih.tampil_struk2();
    
	cout<<"========================================================"<<endl;
	cout<<"\t\tTERIMA KASIH PELANGGAN SETIA KAMI"<<endl;
	cout<<"\t\t   SELAMAT DATANG KEMBALI"<<endl;
	cout<<"\t\tPassword WIFI: Alhamdulillah"<<endl;
    cout<<"========================================================"<<endl;      
 	return 0;
    
}
