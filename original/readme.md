Original topic:

https://forum.myrcon.com/showthread.php?6698-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-2

# Description

This plugin is used to log player chat, player GUID's, player Stats, Weaponstats and Mapstats.
This includes: Chat, PBGUID, EAGUID, IP, Stats, Weaponstats, Dogtags, Killstreaks, Country, ClanTag to be continued.. ;-)
Please post errors if get some.
You can adjust the debug level to a lower value to get less Console Spam. High -> Low (Trace, Info, Warning, Error).
Error only will show critical errors.
Feel free to post feedback and suggestions.

# Requirements

**The plugin Sandbox needs to be disabled!!! if you are not using PRoCon 1.4.1.2 or later**
Access to a MySQL database that accepts remote connections is required so you need to create a user and database if not exists.
It requires the use of a MySQL database with INNODB engine that allows remote connections.(MYSQL Version 5.1 or greater is required!!!)
No ODBC Driver is needed!!!.

Pleases also read the changelog

# Installation

Extract the content of Zipfile into plugin directory.
Set DB Server Settings and the Plugin Settings
Add the machine running the plugin to the remote mysql access host list.
Will throw a permissions error if not done
Enter the correct details for your database connection in the plugin settings tab. You don't need to create tables, the plugin will do that.
The Standard MySQL Port is 3306

# Supported Games

- Battlefield 4
- Battlefield 3
- Battlefield Bad Company 2 & Vietnam
- MOH
- MOHW

# Whats new

- New Databasedesign only one Set of tables needed for multiply gameserver even with different games. Stats are not mixed up!!
- The new Databasedesign allows easy deletion of playerentries.
- Some Code improvements.
- one table for all Weaponstats
- You can create Servergroups

# Working

- Guidlogging
- Statslogging
- Chatlogging
- Weaponstatslogging
- Autotable creation
- Ingame commands
- Welcomestats
- Ingame commands for Dogtags
- Merged stats from all Server

# Maybe Working

- Ingame Weaponstats

# Not Working

- ClanTag coz the server don't deliver it to PRoCon thx EA/DICE!!!.
- Stats for tanks and other vehicles. thx EA/DICE!!!.

# Todos

- [ ] Ticketcount for ServerLiveView
- [ ] Join/Leave History <-- next on list
- [ ] Bugfixes(always :-))
- [ ] Code improvements

# Issues/Requests


# Fixed or Implemented

- [x] Deprecated Trace messages: https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83338&viewfull=1#post83338
- [x] Missing columns for AdKats
- [x] tbl_playerdata: column GameID has no default value --> https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83411&viewfull=1#post83411
- [x] Feature request: Error prefix
- [x] Duplicate Weapon entry try: https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83471&viewfull=1#post83471
- [x] Feature request: Simple Stats: https://forum.myrcon.com/showthread....ll=1#post83476
- [x] CountryCode too long for column: https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83485&viewfull=1#post83485
- [x] Weaponname too long for Fullname column: https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83515&viewfull=1#post83515
- [x] Feature Request: Option to disabled weaponstats: https://forum.myrcon.com/showthread.php?6698-_BF4-PRoCon-Chat-GUID-Stats-and-Mapstats-Logger-1-0-0-0&p=83532&viewfull=1#post83532

# Current Version

Stable: 1.0.0.2

# Changelog

### 1.0.0.2
- Bugfixes for column errors.
- Bugfixes for the sessions streaming bug
- Weaponstats working again.
- Bugfix for Identifier name is too long.

### 1.0.0.1
- Bugfixes for value too long for column errors.
- Bugfixes for some other bugs
- Changed deprecated Tracemessages
- Added an error prefix in pluginlog
- New feature: Tickets/teamscores are now tracked in tbl_teamscores
- New feature: Simple Stats (collects playerdata only)
- New feature: Switch for disabling weaponstats

### 1.0.0.0
- First Release

# Extended Keywordlist (BF3)

```
870MCS{870,870MCS}
AEK-971{AEK,AEK971,AEK-971}
AKS-74u{AKSU,AKS-74,AKSU-74,AKS-74U}
AN-94 Abakan{ABAKAN,AN94,AN-94}
AS Val{ASVAL,AS-VAL,AS VAL}
DAO-12{DAO12,DAO,DAO-12}
death{DEATH}
Defib{DEFIBRILLATOR,DEFIB,PADDLE,PADDLES}
F2000{F2000}
FAMAS{FAMAS}
FGM-148{JAVELIN,FGM148,FGM-148}
FIM92{STINGER,FIM92,FIM-92}
Glock18{GLOCK,GLOCK18,GLOCK-18}
HK53{HK53,HK-53,G53,G-53,HK-G53}
jackhammer{JACKHAMMER,MK3A1,MK3}
JNG90{JNG-90,JNG90,JNG}
L96{L-96,L96}
LSAT{LSAT}
M416{M-416,M416}
M417{M-417,M417}
M1014{M-1014,1014,M1014}
M15 AT Mine{M15,M15 MINE,AT MINE,ATMINE,ATM,M15-ATM}
M16A4{M-16,M16,M16A3,M16-A3,M16A4,M16-A4}
M1911{1911,M1911}
M240{M-240,M240}
M249{M-249,M249,SAW}
M26Mass{M26,M-26,MASS,M26MASS}
M27IAR{M27,M-27,M27IAR}
M320{M-320,GRENADE LAUNCHER,M320}
M39{M-39,M39}
M40A5{M40,M-40,M40A5}
M4A1{M4,M-4,M4A1}
M60{M-60,M60}
M67{HANDGRENADE,GRENADE,M67,M-67}
M9{M-9,M9}
M93R{M93,M93R}
Medkit{MEDKIT}
MG36{MG-36,MG36}
Mk11{MK-11,MK11}
Model98B{M98,M98B,MODEL98,MODEL-98,MODEL98B,MODEL-98B}
MP7{MP-7,MP7}
Pecheneg{PKP-PECHENEG,PKP,PECHENEG}
PP-19{PP19,PP-19}
PP-2000{PP2000,PP-2000}
QBB-95{QBB,QBB95,QBB-95}
QBU-88{QBU,QBU88,QBU-88}
QBZ-95{QBZ,QBZ95,QBZ-95}
Repair Tool{REPAIRTOOL,TOOL,TORCH,BLOWTORCH}
RoadKill{ROADKILL}
RPG-7{RPG,RPG7,RPG7V2,RPG-7V2}
RPK-74M{RPK,RPK74,RPK-74,RPK74M,RPK-74M}
SCAR-L{SCARL,SCAR-L}
SG 553 LB{SG553,SG-553,SG-553LB}
Siaga20k{SAIGA,SAIGA20K,SIAGA,SIAGA20K}
SKS{SKS}
SMAW{SMAW}
SPAS-12{SPAS12,SPAS,SPAS-12}
Suicide{SUICIDE}
SV98{SV-98,SV98}
SVD{SVD,DRAGUNOV}
Steyr AUG{STEYR,AUGA3,AUG-A3,AUG}
Taurus .44{TAURUS,.44MAGNUM,TAURUS.44,MAGNUM,.44}
Type88{TYPE88,TYPE-88}
USAS-12{USAS,USAS12,USAS-12}
Weapons/A91/A91{A91,A-91}
Weapons/AK74M/AK74{AK74,AK-74,AKM,AK-74M,AK74M}
Weapons/G36C/G36C{G36,G36C,G-36,G-36C}
Weapons/G3A3/G3A3{G3,G-3,G3A3,G3-A3}
Weapons/Gadgets/C4/C4{C4,C-4}
Weapons/Gadgets/Claymore/Claymore{CLAYMORE,LANDMINE,APMINE,AP-MINE,APM,M18,M-18,M18-CLAYMORE}
Weapons/KH2002/KH2002{KH2002,KH-2002}
Weapons/Knife/Knife{KNIFE,MELEE}
Weapons/MagpulPDR/MagpulPDR{PDW-R,PDWR,PDR,PDW}
Weapons/MP412Rex/MP412REX{MP412REX,REX,MP-412,MP412}
Weapons/MP443/MP443{MP-443,MP443,GRACH}
Weapons/P90/P90{P-90,P90}
Weapons/Sa18IGLA/Sa18IGLA{SA18,SA-18,IGLA,SA18IGLA,SA18-IGLA,SA-18IGLA}
Weapons/SCAR-H/SCAR-H{SCARH,SCAR-H}
Weapons/UMP45/UMP45{UMP45,UMP-45,UMP}
Weapons/XP1_L85A2/L85A2{L85,L85A2,L-85,L-85A2,L85-A2}
Weapons/XP2_ACR/ACR{ACWR,ACW-R,ACR,AC-R}
Weapons/XP2_L86/L86{L86,L86A2,L-86,L-86A2,L86-A2}
Weapons/XP2_MP5K/MP5K{MP5,MP5K,M5K,MP-5,MP-5K,M5-K}
Weapons/XP2_MTAR/MTAR{MTAR,MTAR21,MTAR-21}
```
