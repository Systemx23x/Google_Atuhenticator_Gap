## Google Authenticator Security Gap


Commands (Android-Platform-Tools 35.02 Windows 11 x64 24H2) on Rooted S22 (SM-S901B) & Galaxy Tab A (SM-T510)<br>
with Google Authenticator 2 App via Google Play Store<br>

````
adb devices
adb shell
su
cat /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db
````


##  Galaxy Tab A (SM-T510_DBT_T510XXU5CWA1).
########################################<br>

Microsoft Windows [Version 10.0.26100.3624]<br>
(c) Microsoft Corporation. Alle Rechte vorbehalten.<br>

C:\Users\wg-23>adb devices<br>
* daemon not running; starting now at tcp:5037<br>
* daemon started successfully<br>
List of devices attached<br>
5200xxxxxdf267bb        device<br>


C:\Users\wg-23>adb shell<br>
tdgsi_a64_ab:/ $ su<br>
tdgsi_a64_ab:/ # cat<br> /data/data/com.google.android.apps.authenticator2/files/accounts/1/otp_database.db<br>

�H�Hl�!�tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT,<br> otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted<br> INTEGER)1Eindexsqlite_autoindex_otp_table_1otp_tablW--ctableandroid_metadataand��de_DEtadataCREATE TABLE android_metadata (locale TEXT)<br>
�x�3<br>
3�4f46851739457540000308950174IONOSlwU9YkU1nqQvT4NQJXk2v00000jD440+4arrwLTVqAra6iK5sC2cWiGnq3AXziitht12ka36M4cP<br>
Ztwz<br>
3%�6ea3c21700008035560systemxx23xxFacebookKxHOcp2iC22lGMp00000FEuw7mY3oD3qL4f5tYV7hLMaBRkOE7YuCsNgL/2BC2Vowy/FnugOG8q2<br>
lqGX<br>
3!60048d1000084303127Systemx23xGitHub/MnLeNSQ0BwDcOPd8rPOj+0000hCtin9EtHPpumD1ZUb7qFGMxlZ9TV49bg=<br>
totp��7�<br>
3A�ae149d1000068135011stevenschloeffel@gmail.comGooglefv9W+oXJrA0000F+k8AJCAJCDmaApWrtn7waiLF3j/aqRt6KzyWjWw7zPZhWvcyMSnZ2fxlvYPcE<br>
uEyr
3-�41b0881000067899751system23@HiDriveIONOS94NM270000mfzVqTUSDXF7+m6bYqJE6C6W8f/RJhLRJ3RdOeGK3SRW3F6QbjLHW72GW75YzMG6UL<br>
sqw4<br>
3#!6f9c391000069666298 stevenx23xXDA ForumsmQjLrwuvsauJ1z0000fVxYTmVCESU2aheDQ/xIejHUNDLE1Xs2XArc8tBUA=<br>
totp�p�FHmacSHA1<br>
q�q����34f400003945754571236ea3c21728768035560360048d17030000031273ae149d1728768135011341b08817287678997513    6f9c391000069666298<br>


##  Galaxy S22 (SM-S901B_EUX_S901BXXSDEYB1).
########################################<br>



