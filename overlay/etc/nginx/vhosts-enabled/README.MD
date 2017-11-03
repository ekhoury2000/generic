testing SSL for riot 

command to make the ssl 
sudo openssl genrsa -des3 -out l3cdn.riotgames.com.key 2048
sudo openssl req -new -key l3cdn.riotgames.com.key  -out l3cdn.riotgames.com.csr



sudo cp l3cdn.riotgames.com.key server.key.org
sudo openssl rsa -in server.key.org -out l3cdn.riotgames.com.key




sudo openssl x509 -req -days 365 -in l3cdn.riotgames.com.csr -signkey l3cdn.riotgames.com.key  -out l3cdn.riotgames.com.crt
