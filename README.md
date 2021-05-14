# Mining-AV-Exceptions
PowerShell script for Windows 10 and Windows Server 2016+ for implementing Antivirus exceptions for mining software executables.
VMAVE.v.x.y.ps1 is the primary PowerShell script for setting antivirus exceptions for Windows Defender in Windows 10 and Windows Server 2016+. "x" and "y" are the major and minor versions respectively.

2021-05-14 - v.1.2: This initial version targets exceptions for the Nicehash mining suite.

The presumption is that Windows Defender is your ONLY Antivirus/antimalware/antispam/privacy application (The new MS Edge adds app blocking as well so watch out as it is NOT scoped in my post.  Other browsers may have similar features).  Additional presumptions:
1. there is no malware/unwanted apps trying to maintain process control of your computer already.
2. drivers are up to date

If you are running Windows 10 and only using Windows Defender:

1. Close all Nicehash instances and miners.
2. Start PowerShell_ISE.exe as an Administrator
3. Open the following PowerShell script; download from https://github.com/V8por5m1n3R/Mining-AV-Exceptions
4. Change this line to match the folder you launch Nicehash from: $RootFolder = "C:\CCMN\Miners" # Replace this with the path to your Nicehash folder
5. Consider removing miners from the $MFLJ variable that you are NOT using.
6. Run the script
7. A reboot may not be necessary, but is recommended before restarting Nicehash.

To verify if any Nicehash suite miners are quarantined by Windows Defender:
1. Start PowerShell_ISE.exe as an Administrator
2. Run ."$ENV:ProgramFiles\Windows Defender\MpCmdRun.exe" -Restore -ListAll


If this script helps you, please send a donation:
USDC - 0xd1d107bcE3F196A612e0e839D2D956f265Ddbf2C

BTC - 3EDXrh16ficV1Q6HmAMr3rXWNCMHbFwRra

LTC - MMbh94XJUY95Gdeo9G7gK1qY6esNbPdaR1 

ETH - 0x4Fe21b7b1178888745F3b53EDc0e22f25D5cd3b1

ETC - 0x852971f07775cB2078b92ffcb2840E218DB0E06a
