# Google_Authenticator_Security_Not_Availible
Google Authenticator Gap, Database read via Cat in Cleartext


POC with rooted Android SM-T510 and Google Authenticator App and Android Platform Tools

So hier meine eigene Sicherheits Erkenntnis lookie lookie
so hier ist es gesagt wurden, also Fehlende Sicherheit, beim Google Authentikator vorhanden mit rootrechten kann die Database im Cleartext ausgelesen werden, its Confirmed, by me.
    5 Min.
    Antworten
Steven Schlöffel
Full Text is sended to BSI by Me
    5 Min.
    Antworten
Steven Schlöffel
so hier mal der verfälschte Log, also rück ja nicht meine Originalen raus, also die Cleartext angaben wurden von mir unbrauchbar gemacht, zur Persönlichen Sicherheit meiner seits aber der Rest ist Original in 5min abgehandelt, Google CVE is confirmed, but whats the Number?
    1 Min.
    Antworten
Steven Schlöffel
Microsoft Windows [Version 10.0.26100.3624]
(c) Microsoft Corporation. Alle Rechte vorbehalten.
C:\Users\wg-23>adb devices
* daemon not running; starting now at tcp:5037
* daemon started successfully
List of devices attached
52003bdc4df267bb device
C:\Users\wg-23>adb shell
tdgsi_a64_ab:/ $ su
tdgsi_a64_ab:/ # ls /data/data/com.google.android.apps.authenticator2/databases/
com.google.android.datatransport.events com.google.android.datatransport.events-journal databases
tdgsi_a64_ab:/ # cd /data/data/com.google.android.apps.authenticator2/databases/
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/databases # ls
com.google.android.datatransport.events com.google.android.datatransport.events-journal databases
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/databases # ls databases
databases
s com.google.android.datatransport.events-journal <
com.google.android.datatransport.events-journal
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/databases # ls com.google.android.datatransport.events
com.google.android.datatransport.events
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/databases # cd ..
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2 # ls
cache code_cache databases files no_backup shared_prefs
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2 # ls files
103795117 DefaultAccountData.pb database_migration_proto_data_store.pb phenotype
AccountData.pb accounts first_time_consent.pb phenotype_storage_info
AccountSyncData.pb androidatgoogle_privacy how_it_works_proto_data_store.pb tiktok
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2 # cd files
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/files # ls accounts
1 2
s accounts\1 <
ls: accounts1: No such file or directory
s accounts\2 <
ls: accounts2: No such file or directory
s accounts/2 <
otp_database.db
s accounts/2/otp_database.db <
accounts/2/otp_database.db
tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/files # cat accounts/2/otp_database.db
�H�Hl�!�tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT, otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted INTEGER)1Eindexsqlite_autoindex_otp_table_1otp_tablW--ctableandroid_metadataand��de_DEtadataCREATE TABLE android_metadata (locale TEXT)
at accounts/1/otp_database.db <
�H�Hl�!�tableotp_tableotp_tableCREATE TABLE otp_table(ordering INTEGER PRIMARY KEY, unique_id TEXT UNIQUE NOT NULL, name TEXT NOT NULL, issuer TEXT, secret TEXT, otp_type TEXT, counter INTEGER, timestamp INTEGER, is_deleted INTEGER, algorithm_deleted TEXT NOT NULL, digits_deleted INTEGER)1Eindexsqlite_autoindex_otp_table_1otp_tablW--ctableandroid_metadataand��de_DEtadataCREATE TABLE android_metadata (locale TEXT)
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
q�q����34f400003945754571236ea3c21728768035560360048d17030000031273ae149d1728768135011341b08817287678997513 6f9c391000069666298tdgsi_a64_ab:/data/data/com.google.android.apps.authenticator2/files #
