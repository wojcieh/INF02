1. Zamiana netplanu na network-manager
   # utworzenie nowego pliku konfiguracyjnego dla netplanu
   touch /etc/netplan/01-er-netplan-fix.yaml
   # edycja nowego pliku
    nano /etc/netplan/01-er-netplan-fix.yaml
   # zawartość pliku
   network:
    version: 2
    renderer: NetworkManager
   # instalacja Network Manager
      sudo apt install network-manager
  # wyłączenie NetPlan poprzez zmianę nazwy domyślnego pliku konfiguracyjnego
    mv /etc/netplan/00-installer-config.yaml /etc/netplan/00-installer-config.yaml.bak
  # przeładowanie NetPlan
    netplan apply
  # reboot dla spokojności umysłu
    reboot
