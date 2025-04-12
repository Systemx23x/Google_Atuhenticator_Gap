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

## Notepad++ otp_database.db.
#############################<br>

````
SQLite format 3   @                                                                   .CÂ
Ÿ H §Hl                                                                                                                                                                                                                                    ‚!„tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT, otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted INTEGER)1E indexsqlite_autoindex_otp_table_1otp_table       W--ctableandroid_metadataandroid_metadataCREATE TABLE android_metadata (locale TEXT)                                                                                                                                                                                                                                                                                                                                                                                                                                     
   ÷ ÷                                                                                                                                                                                                                                                                                                                                                                                                                                                de_DE
   ~ xÛ3
°
~
 31 4f4685100007545712308950174IONOSlwU9YkU00000T4NQJXk2v+ndnkjD440+4arrwLTVqAra6iK5sC2cWiGnq3AXziitht12ka36M4cP
Ztwz
totp•É\k€HmacSHA1
 3%1 6ea3c21728700000560systemxx23xxFacebookKxHOcp2iC22l00000t1TFEuw7mY3oD3qL4f5tYV7hLMa000007YuCsNgL/2BC2Vowy/FnugOG8q2
lqGX
totp•ÐQñ—HmacSHA1 
 3! 6004800000784303127Systemx23xGitHub/MnLeNSQ000000Pd8rPOj+7YYqhCtin9EtHPpumD1ZUb7qFGMxlZ9TV49bg=
totp•É7È
HmacSHA1%
 3A1 ae149d0000068135011stevenschloeffel@gmail.comGooglefv9W+oXJr00000F+k8AJCAJCDmaApWrtn7waiLF3j/aqRt6KzyWj00000ZhWvcyMSnZ2fxlvYPcE
uEyr
totp–ÇoHmacSHA1
 3-1 41b0000008767899751system23@HiDriveIONOS94NM2700000fzVqTUSDXF7+m6bYqJE6C6W8f/RJhLRJ3Rd00000SRW3F6QbjLHW72GW75YzMG6UL
sqw4
totp•É,Ä§HmacSHA1
 3#! 6f9c300000769666298 stevenx23xXDA ForumsmQjLrwuvsauJ1z00000VxYTmVCESU2aheDQ/xIejHUN00000s2XArc8tBUA=
totp–pÍFHmacSHA1
   q Ñq¡‰é¹                                                                                                                                                                                                                                 ae14900000768135011341b08810000078997513	6f9c391000009666298
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
3�4f46851739457540000308950174IONOSlwU9YkU1nqQvT4NQJXk2v00000jD440+4arrwLTVqAra6iK5sC2cWiGnq3AXziitht12ka36M4cP
Ztwz
3%�6ea3c21700008035560systemxx23xxFacebookKxHOcp2iC22lGMp00000FEuw7mY3oD3qL4f5tYV7hLMaBRkOE7YuCsNgL/2BC2Vowy/FnugOG8q2
lqGX
3!60048d1000084303127Systemx23xGitHub/MnLeNSQ0BwDcOPd8rPOj+0000hCtin9EtHPpumD1ZUb7qFGMxlZ9TV49bg=
totp��7�
3A�ae149d1000068135011stevenschloeffel@gmail.comGooglefv9W+oXJrA0000F+k8AJCAJCDmaApWrtn7waiLF3j/aqRt6KzyWjWw7zPZhWvcyMSnZ2fxlvYPcE
uEyr
3-�41b0881000067899751system23@HiDriveIONOS94NM270000mfzVqTUSDXF7+m6bYqJE6C6W8f/RJhLRJ3RdOeGK3SRW3F6QbjLHW72GW75YzMG6UL
sqw4
3#!6f9c391000069666298 stevenx23xXDA ForumsmQjLrwuvsauJ1z0000fVxYTmVCESU2aheDQ/xIejHUNDLE1Xs2XArc8tBUA=
totp�p�FHmacSHA1
q�q����34f400003945754571236ea3c21728768035560360048d17030000031273ae149d1728768135011341b08817287678997513    6f9c391000069666298
````


##  Galaxy S22 (SM-S901B_EUX_S901BXXSDEYB1).
###########################################<br>

````

````

<br>

````

````

