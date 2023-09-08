Setup Ubuntu 22.04.3 LTS with NAT TYPE:Bridge Adapter, with 8-16GB ram and 2TB SSD, keep in mind I used "humble" as my Ubuntu username for all the formatting of these python scripts, so use humble unless you want to change every single username in these scripts.
Run the following commands "sudo apt install python3-pip"
"pip3 install wget" or "sudo apt install python3-wget"
Download BitcoinCore python script and move to your home directory with command "mv BitcoinCore ~"
Edit the RPC "Username" and "Password" by "nano BitcoinCore"
Then execute the script with command "python3 BitcoinCore"
Check the bitcoin.conf file by opening a new terminal and "nano /.bitcoin/bitcoin.conf" ensure your rpcusername and password match then type "done"
Verify bitcoin core is working by entering the command "sudo systemctl status bitcoind.service"
Once bitcoincore is fully downloaded (approximately 2 days) verify bitcoincore is fully synced with "bitcoin-cli getblockchaininfo"
Only then run the "Fulcrum" python script ensuring you edit and move the script to your home directory with command "mv Fulcrum ~"
Edit RPC username and password and IP address with "nano Fulcrum" then run the script with "python3 Fulcrum".
Verify the fulcrum is working with "sudo systemctl status fulcrum.service".
Ensure fulcrum is fully downloaded approximately 12 hours with "journalctl -u fulcrum.service".
If both bitcoin core and fulcrum are fully synced download sparrowwallet and torbrowser.
Run both scripts, download Dockermempool and nano the script to edit rpc username and password, ipaddress.
Once the mempool is launched in docker with "docker-compose up" verify in firefox browser with "ipaddress:4080"
If mempool is fully synced download Samourai and edit the rpc username, password, ip address etc.
Run the script and verify in the tor browser that you can access samourai wallet dojo.
