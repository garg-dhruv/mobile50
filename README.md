# mobile50
Notes for CS50's  App Development course

**Any sort of edits and contributions are highly appreciated (even grammer nazis can help :P).**
echo "sudo fdisk -l
dc3dd if=/dev/sdb hash=md5 log=dc3ddusb of=test.dd
dc3dd if=/dev/sdc hash=md5 log=dc3ddusb of=data/code/Forensics/test.dd
sudo dc3dd if=/dev/sdc hash=md5 log=dc3ddusb of=data/code/Forensics/test.dd
sudo md5sum /dev/sdc
sudo md5sum data/code/Forensics/test.dd 
sudo dc3dd if=data/code/Forensics/test.dd of=/dev/sdc log=drivecopy.log
sudo dc3dd if=/dev/sdc ofs=meh.img.000 log=wowkam ofsz=1G
sudo dc3dd wipe=/dev/sdc
guymager
foremost -i Downloads/11-carve-fat.dd -o foremost_recovery
foremost -i Downloads/11-carve-fat.dd -o foremost_recovery2 -t jpg
scalpel
cd /etc/scalpel/
code scalpel.conf 
scalpel -o scalpelOutput Downloads/11-carve-fat.dd
bulk_extractor -o bulk_output ~/Downloads/terry-work-usb-2009-12-11.E0
volatility -f Downloads/cridex.vmem imageinfo
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem pslist
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem pstree
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem psscan
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem psxview
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem connections
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem connscan
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem sockets
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem verinfo
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem dlllist
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem getsids
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem hivescan
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem hivelist
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem timeliner
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem malfind
volatility --profile=WinXPSP3x86 -f Downloads/cridex.vmem malfind -p 608"
