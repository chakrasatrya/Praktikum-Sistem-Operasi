dbproduk(){
kdbr[0]=0;   nmbr[0]="Mouse Corsair Vengeance MMO          "; hgbr[0]=1240000
kdbr[1]=1;   nmbr[1]="Mouse Logitech Wireless Desktop      "; hgbr[1]=541000
kdbr[2]=2;   nmbr[2]="Mouse Razor Abysus                   "; hgbr[2]=250000
kdbr[3]=3;   nmbr[3]="Prosesor intel core i3 LGA1156       "; hgbr[3]=883000
kdbr[4]=4;   nmbr[4]="Prosesor AMD A-6 FM1                 "; hgbr[4]=1229000
kdbr[5]=5;   nmbr[5]="Hardisk Seagate 1Tb                  "; hgbr[5]=1138000
kdbr[6]=6;   nmbr[6]="Hardisk Hitachi 500Gb                "; hgbr[6]=1038000
kdbr[7]=7;   nmbr[7]="Mainboard Gigabyte (LGA1156,H77,DDR3)"; hgbr[7]=1296000
kdbr[8]=8;   nmbr[8]="Mainboard Asus (LGA1155,DDR3,SATA3)  "; hgbr[8]=1119000
kdbr[9]=9;   nmbr[9]="Monitor LG 23inch                    "; hgbr[9]=2543000
kdbr[10]=10; nmbr[10]="Monitor LG 40inch                   "; hgbr[10]=5238000
kdbr[11]=11; nmbr[11]="Powersupply Corsair 650watt         "; hgbr[11]=1255000
kdbr[12]=12; nmbr[12]="VGA Asus Radeon 2GB DDR5            "; hgbr[12]=2976000
kdbr[13]=13; nmbr[13]="VGA Asus Geoforce 1024MB DDR3       "; hgbr[13]=2180000
kdbr[14]=14; nmbr[14]="Memory RAM corsair 1x4GB            "; hgbr[14]=210000
kdbr[15]=15; nmbr[15]="Memory RAM corsair 2x4GB            "; hgbr[15]=480000
}
echo
clear
echo -e "#************************************************************#"
echo -e "#    P R O G R A M   T O K O  C O M P U T E R  CHAKRASATRY   #"
echo -e "#                 By:CHAKRA SATRYA PRADA                     #"
echo -e "#************************************************************#"
echo "           http.//CHAKRAGANTENGBANGET  "
echo "                    Terimakasih Atas Kunjunganya "
tput cup 9 25
for (( i=1; i <= 20; i++ ))
do
if [ $i -eq 1 ];then
echo  -n "W"
elif [ $i -eq 5 ]
then
echo -n "E"
elif [ $i -eq 10 ]
then
echo -n "L"
elif [ $i -eq 15 ]
then
echo -n "L"
elif [ $i -eq 20 ]
then
echo -n "C"
elif [ $i -eq 25 ]
then
echo -n "O"
elif [ $i -eq 30 ]
then
echo -n "M"
elif [ $i -eq 35 ]
then
echo -n "E"
else
echo -n "*"
fi
sleep 0.09
done


tput cup 20 40
echo
echo -n "          [100%]"
echo -n " CHAKRAGANTENGBANGET  "
menu(){
. load.sh;
. produk.sh;
. out.sh;
load
clear
echo "Toko Komputer chakra tika"
echo "1. Produk"
echo "2. Lihat Struk"
echo "3. Exit"
echo "4. google"
echo -n "Pilihan: "; read pil
case $pil in
 1) produk;;
 2) clear
    cat struk
  
read -p "Tekan Enter untuk kembali ke menu awal"
    menu;;
 3) out;;
 *) echo "Pilihan tidak ada, silahkan ulangi inputan anda";;
 4) google;;
esac
}
 out(){
. menu.sh
clear
echo "Apakah anda yakin akan keluar(y/n)? "; read pil
if [ $pil == "y" ]
then
exit
else
menu
fi
}
 produk(){
. dbproduk.sh
. menu.sh
dbproduk
clear
echo -e "Kode\tNama Barang\t\t\t\tHarga Barang"
for (( x=0; x<=15; x++ ))
do
echo -e "${kdbr[x]}\t${nmbr[x]}\t${hgbr[x]}"
done
while [ $pil != "tot" ]
do
echo -n "masukkan kode barang (ketik tot untuk selesai transaksi): "; read pil
if [ $pil != "tot" ]
then
echo -n "masukkan jumlah dari produk ${nmbr[pil]}: "; read qtbr[pil]
fi
done
clear
echo "=============================================================================" >> struk
echo -e "Kode\tNama Barang\t\t\t\tHarga Barang\tQty\tTotal"
echo -e "Kode\tNama Barang\t\t\t\tHarga Barang\tQty\tTotal" >> struk
for (( x=0; x<=15; x++ ))
do
    if [ ${qtbr[x]}>0 ]
    then
    ttbr[x]=$((hgbr[x]*qtbr[x]))
    echo -e "${kdbr[x]}\t${nmbr[x]}\tRp.${hgbr[x]},-\t${qtbr[x]}\tRp.${ttbr[x]},-\t"
    echo -e "${kdbr[x]}\t${nmbr[x]}\tRp.${hgbr[x]},-\t${qtbr[x]}\tRp.${ttbr[x]},-\t" >> struk
    fi
    total=$((total+ttbr[x]))
done


echo "Totalnya: Rp.$total,-"
echo "Totalnya: Rp.$total,-" >> struk
read -p "Tekan Enter untuk kembali ke menu awal"
menu
}

##Program Toko Komputer: ""
##Pemprograman Shell
##copy-rigth:
##http.//CHAKRAGANTENGBANGET
## Terimakasih Atas Kunjunganya

#include
. menu.sh


#program
menu
 ===============================================================================
Kode    Nama Barang                Harga Barang    Qty    Total
1    Mouse Logitech Wireless Desktop          Rp.541000,-    1    Rp.541000,-  
2    Mouse Razor Abysus                       Rp.250000,-    2    Rp.500000,-  
Totalnya: Rp.1041000,-
===============================================================================
Kode    Nama Barang                Harga Barang    Qty    Total
1    Mouse Logitech Wireless Desktop          Rp.541000,-    1    Rp.541000,-  
2    Mouse Razor Abysus                       Rp.250000,-    2    Rp.500000,-  
Totalnya: Rp.2082000,-
===============================================================================Kode    Nama Barang                Harga Barang    Qty    Total
1    Mouse Logitech Wireless Desktop          Rp.541000,-    2    Rp.1082000,-  
3    Prosesor intel core i3 LGA1156           Rp.883000,-    2    Rp.1766000,-  
Totalnya: Rp.2848000,-
===============================================================================Kode    Nama Barang                Harga Barang    Qty    Total
0    Mouse Corsair Vengeance MMO              Rp.1240000,-    2    Rp.2480000,-  
1    Mouse Logitech Wireless Desktop          Rp.541000,-    3    Rp.1623000,-  
Totalnya: Rp.4103000,-
===============================================================================Kode    Nama Barang                Harga Barang    Qty    Total
2    Mouse Razor Abysus                       Rp.250000,-    3    Rp.750000,-  
3    Prosesor intel core i3 LGA1156           Rp.883000,-    tot    Rp.0,-  
4    Prosesor AMD A-6 FM1                     Rp.1229000,-    3    Rp.3687000,-  
Totalnya: Rp.4437000,-
===============================================================================Kode    Nama Barang                Harga Barang    Qty    Total
Totalnya: Rp.0,-
===============================================================================Kode    Nama Barang                Harga Barang    Qty    Total
Totalnya: Rp.0,-

