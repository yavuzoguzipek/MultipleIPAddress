# MultipleIPAddress
How to Add Multiple IP Addresses to Windows
 
;   Created by Yavuz Oguz Ipek									 
;   Date : 03/09/2016 - 20:14:26								 
;	  Content: How to Add Multiple IP Addresses to Windows	 
 


Win8&10: Press the Windows key + X and click Command Prompt as Administrator.
If you want to see your ip address, enter 'ipconfig'. 

Then You can add multiple ip address with this script.

- Sample Script -
for /L %a in (start,step,end) do netsh in ip add address "Local Area Connection" 2.1.1.%a 255.255.255.0


- You can create 2.1.1.1 ... 2.1.1.254  ip address with this script -
for  /L %a in (1,1,254) do netsh in ip add address "Local Area Connection" 2.1.1.%a 255.255.255.0


- You can create 2.1.1.1 ... 2.1.254.254  ip address with this script -
for  /L %a in (1,1,254) do for  /L %b in (1,1,254) do netsh in ip add address "Local Area Connection" 2.1.%a.%b 255.255.255.0
