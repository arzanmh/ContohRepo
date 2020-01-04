#Example : this is Simply syntax (if - else $ Case statement) in Linux

#!/bin/bash

If  [-z $1]
then
order=”Jenis Aplikasi”
elif [ -n $1]
then
order=$1
fi
		case $order in
			“gojek”) echo “Harga $order Rp.2000/km”;;
“gocar”) echo “Harga $order Rp.6000/km”;;
“grabike”) echo “Harga $order Rp.2500/km + Diskon 5% untuk order >10 km”;;
“grabcar”) echo “Harga $order Rp.7000/km + Diskon 10% untuk order >10 km”;;
*) echo “Maaf, $order belum terdaftar”;;
		esac
    
================================================================================================

#!/bin/bash
konversi () {
read –p “Konversi Rupiah Ke- “  t
		case $t in
“dollar”) read –p “Masukan jumlah uang :” x;;
“pound”) read –p “Masukan jumlah uang :” y;;
“riyal”) read –p “Masukan jumlah uang :” z;;
*) echo “Tidak Tersedia”;;
		esac
			if (($x))
				then
				let hasil=$x/$1
				echo=”$hasil Dollar”
			elif (($y))
				then
				let hasil=$y/$2
				echo=”$hasil Pound”
			elif (($z))
				then
				let hasil=$z/$3
				echo=”$hasil Riyal”
			else
			echo “Maaf yang anda masukan salah”
			fi
}
konversi 14035 18333 3742 

