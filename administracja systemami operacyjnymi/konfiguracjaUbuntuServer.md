### Konfiguracja poinstalacyjna
```
sudo touch /etc/cloud/cloud-init.disabled
```


### Zamiana netplanu na network-manager
1. utworzenie nowego pliku konfiguracyjnego dla netplanu
```
touch /etc/netplan/01-er-netplan-fix.yaml
```
3. edycja nowego pliku
```
nano /etc/netplan/01-er-netplan-fix.yaml
```
3. zawartość pliku
```
network:
  version: 2
  renderer: NetworkManager
 ```
4. instalacja Network Manager
```
sudo apt install network-manager
```
5. wyłączenie NetPlan poprzez zmianę nazwy domyślnego pliku konfiguracyjnego
```
mv /etc/netplan/00-installer-config.yaml /etc/netplan/00-installer-config.yaml.bak
```
6. przeładowanie NetPlan
```
netplan apply
 ```
7. reboot dla spokojności umysłu
```
reboot
```
