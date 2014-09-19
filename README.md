Cryptocurrency-faucet-script
============================
* You are completely free to use/modify this script in any way. Credit is not required.
* At this point a big thank you to a friend who asked not to be named.

DEMO: http://wow.bitcoinproject.net/


Faucet features:

- Can be used for the most cryptocurrencys
- You can set minimum and maximum payouts
- Payment system for staged,timed or direct payouts
- Recaptcha integrated (http://www.google.com/recaptcha/)
- Proxies filter option
- Promocodes possible for extra payouts
- Useable with encrypted wallets
- Easy editable template system


Installation:

1. Download or clone this repository
2. Upload the files to your ftp folder
3. Create a database and import faucet.sql
4. Open the config.php and edit all settings to suit your needs
5. Create a .htaccess and .htpasswd for the cronjob folders /cron/ and /lib/proxy_filter/cron/, so just you can fire them!
6. Create cronjob(s):

If you set "stage_payments" => true and "staged_payment_cron_only" => true you have to create a cronjob for /cron/run.php and /lib/proxy_filter/cron/tor.php

If you set "stage_payments" => true and "staged_payment_cron_only" => false you just have to create a cronjob for /lib/proxy_filter/cron/tor.php

// IMPORTANT: The tor proxy list gets downloaded from https://www.dan.me.uk/torlist/ - He just allow to download it only once the hour! Otherwise you will be banned from the service! //


How to add promo codes:

Go to your database and find the sf_promo_codes table.
Add a new line and set your code, minimum_payout, maximum_payout and uses.

- uses = -0 // Promo code disabled
- uses = -1 // No limit on using this code
- uses = 50 // The code counts down until 0 and works e.g. 50 times



Feel free to donate :)
- BTC: 1Av1sFhiWVzhcgxPMsZXni4q5fYCMtR2jE
- DOGE: DLoveeefqGPuEqZvc7PXNt2mvu36YPXcGb
