## Google Authenticator Security Gap


## Google Authenticator Security Gap


Commands (Android-Platform-Tools 35.02 Windows 11 x64 24H2) on Rooted S22 (SM-S901B) & Galaxy Tab A (SM-T510)<br>
with Google Authenticator 2 App via Google Play Store

````
adb devices
adb shell
su
cat /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db

adb shell
su
cp /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db /sdcard
adb pull /sdcard/otp_database.db
notepad++ otp_database.db
````

![Screenshot_20250412_050937_Authenticator](https://github.com/user-attachments/assets/5cb4f026-900b-4ca8-bb80-5c3981be9bc1)
![Screenshot_20250412_050851](https://github.com/user-attachments/assets/8628074d-623b-412a-b181-f39f09055417)
![Screenshot_20250412_050903](https://github.com/user-attachments/assets/6e25c804-3202-4c33-b84a-d81c06b966d1)
![Screenshot_20250412_050649_Google Play Store](https://github.com/user-attachments/assets/4872d7ce-19a9-488c-ba10-71c86201adb3)


## Notepad++ otp_database.db.
#############################<br>

````
SQLite format 3   @                                                                   .CÂ
Ÿ H §Hl                                                                                                                                                                                                                                    ‚!„tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT, otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted INTEGER)1E indexsqlite_autoindex_otp_table_1otp_table       W--ctableandroid_metadataandroid_metadataCREATE TABLE android_metadata (locale TEXT)                                                                                                                                                                                                                                                                                                                                                                                                                                     
   ÷ ÷                                                                                                                                                                                                                                                                                                                                                                                                                                                de_DE
   ~ xÛ3
°
~
 31 4f46851000075454IO000T4NQJXk2v+ndnkjD440+4arK5sC2cWiGnq3AXziitht12ka36M4cP
Ztwz
totp•É\k€HmacSHA1
 3%1 000008751FacebookKxHOcp2iC22l00000t1TFEuw7mY3oD3qL4f5tYV7hLMa000007YuCsNgL/2BC2Vowy/FnugOG8q2
lqGX
totp•ÐQñ—HmacSHA1 
 3! 000008751GitHub/MnLeNSQ000000Pd8rPOj+7YYqhCtin9EtHPpumD1ZUb7qFGMxlZ9TV49bg=
totp•É7È
HmacSHA1%
 3A1 000008751@gmail.comGooglefv9W+oXJr00000F+k8AJCAJCDmaApWrtn7waiLF3j/aqRt6KzyWj00000ZhWvcyMSnZ2fxlvYPcE
uEyr
totp–ÇoHmacSHA1
 3-1 000008751@HiDriveIONOS94NM2700000fzVqTUSDXF7+m6bYqJE6C6W8f/RJhLRJ3Rd00000SRW3F6QbjLHW72GW75YzMG6UL
sqw4
totp•É,Ä§HmacSHA1
 3#! 000008751XDA ForumsmQjLrwuvsauJ1z0VCEQ/xIejHUN008tBUA=
totp–pÍFHmacSHA1
   q Ñq¡‰é¹                                                                                                                                                                                                                                 ae149005011341b088197513	6f9c3910000298
````




##  Galaxy Tab A (SM-T510_DBT_T510XXU5CWA1).
########################################<br>

Microsoft Windows [Version 10.0.26100.3624]<br>
(c) Microsoft Corporation. Alle Rechte vorbehalten.<br>

````
C:\Users\wg-23>adb devices
* daemon not running; starting now at tcp:5037
* daemon started successfully
List of devices attached
5200xxxxxdf267bb        device
````

<br>

````
C:\Users\wg-23>adb shell
tdgsi_a64_ab:/ $ su
tdgsi_a64_ab:/ # cat /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db

<
�H�Hl�!�tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT,<br> otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted<br> INTEGER)1Eindexsqlite_autoindex_otp_table_1otp_tablW--ctableandroid_metadataand��de_DEtadataCREATE TABLE android_metadata (locale TEXT)
�x�3
3�4f44575400000087511nqv0arrwLTVqAra6iK5sC2citht12ka36M4cP
Ztwz
3%�000008751FacebookKxHOcp2iC22lGMp00000FEuw7mY3oD3qL4f5tYV000008751YuCsNgL/2BC2Vowy/FnugOG8q2
lqGX
3!000008751GitHub/MnLeNSQ0BwDcOPd8rPOj+0000hCtin9EtHPpu000008751GMxlZ9TV49bg=
totp��7�
3A�000008751@gmail.comGooglefv9W+oXJrA0000F+k8AJCAJCDmaApWrtn7waiLF3j/aqRt6K000008751vcyMSnZ2fxlvYPcE
uEyr
3-�000008751@HiDriveIONOS94NM270000mfzVqTUSDXF7+m6bYqJE6C6W8f/RJhLRJ3RdOeGK3S000008751bjLHW72GW75YzMG6UL
sqw4
3#!000008751XDA ForumsmQjLrwuvsauJ1z0000fVxYTmVCESU2aheDQ/xIej000008751XArc8tBUA=
totp�p�FHmacSHA1
q�q����34f400003945754571236e728768035560360048d17030000031279d17135088172897513    6f9c39100000875166298
````


##  Galaxy S22 (SM-S901B_EUX_S901BXXSDEYB1).
###########################################<br>

````
C:\Users\wg-23\Desktop>adb devices
List of devices attached
R5CTC1YDKYF     device
````

<br>

````
C:\Users\wg-23\Desktop>adb shell
r0s:/ $ su
r0s:/ # cat /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db-wal

3-�000008751@HiDriveIONOSa5IDGW6h904sRUOL9Wo6
totp��,ħHmacSHA1�_!�����+�L���;
3#!000008751XDA Forums6SQlxzDyKi862a+cqF+6ewgwXN5X4=
3-�000008751@HiDriveIONOSjYnZP+Rh906xSs+b9D+gwRU3HDmCpl5OubM1
WtPO
totp��,ħHmacSHA1�_!�����߼/Om�1
3!000008751GitHub8tdYBmboDyhFg8tqb4/FTCDnlrb/cbqJ04Z2x9zMPSGo=
totp��7�
3#!000008751XDA Forums6SQamePnZJbOIlxzDyKkilzBfhGh+cqTtm6ewgwXN5X4=
3-�000008751@HiDriveIONOSjYnZP+Rba5IDGW6h904sRo69D+gwRU3Hp3a3L8Tm5OubM1
WtPO
totp��,ħHmacSHA1�_!�����F��>|�
3�000008751IONOSSuqzfqVuQSFlLwfXRF1lrb1l67g54W6R6VVtjLB/20/qgWKr5oRfD988prqXEleN4P00000
YveL
3!000008751GitHub8tdYBmboDyhFg8tqp4/FTCDnlrb/clZ2RXbqJ04Z245HMPSGo=
totp��7�
3#!000008751XDA Forums6SQamePnZJbDyKi862atuDXikilzBfhGh+cqTt+6ewgw00000XN5X4=
3-�000008751@HiDriveIONOSjYnZP+Rba5IDG4sRUOL9WoFC6GhkPoDa+gwRU3Hp3azNFDo3L8TmCpl5OubM1
WtPO
totp��,ħHmacSHA1�_!�����A���Ӌ
�����34f4685173945750000087517037843031200000736f9c39172872983      41b088000008751899751�_!����nW>�3%�000008751Facebookkv3V400000Gf8SdgOYiZ+00000Xf2B5ZHzJGJU7qFp62z9twMH0000087518bNUVVXWmGmc
jWTO
3�000008751IONOSSuqzfqVuQSFlLw00000lrb1l67g54W6R6VVtjLB/20/qgWKr5o00000sFt888ls1P1QeN4P
YveL
3!000008751GitHub8tdYBmb00000tqp6nhDb4/FTCDnlrb/clZ00000J04Z2x5HMPSGo=
totp��7�
3#!000008751XDA Forums6SQamePn00000lxzDyKi86200000ikilzBfhGh+cqTtmbBZFwXN5X4=
3-�000008751@HiDriveIONOSjYnZP+Rba000006h904sRUOL9Wo6xSs00000hkPoDaN+b9D+gwRU3Hp3a3L8TmCpl5OubM1
WtPO
totp��,ħHmacSHA1�_!�����.'�K��
������36ea3c2100000803556034f468500000575457128d170370000012736f9c3917287696662983 41751�_!����C
�z6(��
&c�X
3A�000008751@gmail.comGooglecLeITQ/DUcYwPTgj/XdIj//jWgKF00000lr8Pkzx00000jBbLHNOvZuq000004LCfCt5Ovm
kccd
3%�000008751Facebookkv3V400000Gf8SdgOYiZ+x00000f2B5ZHz00000qFp62z9twMHkFMAqF3sx8bNUVVXWmGmc
jWTO
3�000008751IONOSSuqzfqVu00000wfXRF1lrb1l67g54W6R6VVtjLB/20/qg00000sFt88800000ls1P1QeN4P
YveL
3!000008751GitHub8tdY00000yhFg8t00000Db4/FTCDnlrb/cl00000qJ04Z2x9zIPSGo=
totp��7�
3#!000008751XDA Forums6SQamePnZJbOIlxzDyKi862atu00000lzBfhGh+00000bBZF+6N5X4=
3-�000008751@HiDriveIONOSjYnZP+Rba5I00000904sRUOL9Wo6xSsOFC6GhkPo000009D+gwRU3Hp3azNFDmCpl5OubM1
WtPO
totp��,ħHmacSHA1�_!����m�>���J

q�����q3ae149d172870000001136ea3c21728757545712360000017037736f62983  41b08800000751
````



