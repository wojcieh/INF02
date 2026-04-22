## Instrukcja do zajęć praktycznych: Przygotowanie do egzaminu INF.02

**Temat:** Konfiguracja interfejsu sieciowego Ethernet w systemie Ubuntu za pomocą terminala.
**Cel zajęć:** Opanowanie umiejętności statycznej i dynamicznej konfiguracji parametrów sieciowych z wykorzystaniem narzędzia Netplan oraz weryfikacji połączenia sieciowego – kluczowych zadań na egzaminie zawodowym INF.02.

---

### Wstęp teoretyczny i przygotowanie

System Ubuntu do zarządzania siecią od wersji 17.10 domyślnie wykorzystuje narzędzie **Netplan**. Konfiguracja odbywa się poprzez edycję plików tekstowych w formacie YAML, znajdujących się w katalogu `/etc/netplan/`. Zwróć szczególną uwagę na **wcięcia (spacje)** w plikach YAML – są one krytyczne dla poprawnego działania konfiguracji (nie używaj klawisza Tab).

Zanim przystąpisz do konfiguracji, sprawdź nazwę swojego interfejsu sieciowego (np. `enp0s3`, `eth0`) za pomocą polecenia:
```bash
ip addr
```

---

### Część 1: Procedura konfiguracji statycznej (Netplan)

Twoim pierwszym zadaniem jest przypisanie interfejsowi następujących parametrów:
* **Adres IP:** 192.168.1.3
* **Maska podsieci:** /28 *(Zapis CIDR /28 odpowiada masce dziesiętnej **255.255.255.240**)*
* **Brama domyślna (Gateway):** 192.168.1.1
* **Serwer DNS:** 4.4.4.4

**Krok 1: Edycja pliku konfiguracyjnego**
Otwórz plik konfiguracyjny Netplan z uprawnieniami administratora za pomocą edytora `nano`. Nazwa pliku może się różnić (często jest to `00-installer-config.yaml` lub `01-netcfg.yaml`). Użyj znaku gwiazdki, aby otworzyć właściwy plik:

```bash
sudo nano /etc/netplan/*.yaml
```

**Krok 2: Wprowadzenie parametrów sieciowych**
Zmodyfikuj zawartość pliku tak, aby odpowiadała poniższej strukturze. Pamiętaj o zachowaniu odpowiednich wcięć:

```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:                     # Zmień na nazwę swojego interfejsu, np. eth0
      dhcp4: false              # Wyłączenie protokołu DHCP
      addresses:
        - 192.168.1.3/28        # Adres IP wraz z maską podsieci (255.255.255.240)
      routes:
        - to: default
          via: 192.168.1.1      # Adres IP bramy domyślnej
      nameservers:
        addresses:
          - 4.4.4.4             # Adres IP serwera DNS
```
> **Uwaga dla starszych systemów:** W starszych wersjach Ubuntu (przed 22.04) zamiast bloku `routes` i wpisu `to: default`, dla bramy IPv4 stosowano parametr `gateway4: 192.168.1.1`.

Zapisz plik (`Ctrl + O`, `Enter`) i zamknij edytor (`Ctrl + X`).

**Krok 3: Zastosowanie konfiguracji**
Aby system wczytał nowe ustawienia z pliku YAML, wykonaj polecenie:

```bash
sudo netplan apply
```

---

### Część 2: Procedura konfiguracji dynamicznej (DHCP)

Kolejnym zadaniem jest przełączenie interfejsu sieciowego na automatyczne pobieranie adresacji z serwera DHCP i wymuszenie odświeżenia dzierżawy.

**Krok 1: Przywrócenie trybu automatycznego w Netplan**
Ponownie edytuj plik YAML:

```bash
sudo nano /etc/netplan/*.yaml
```

Zmień konfigurację, usuwając statyczne wpisy i ustawiając `dhcp4` na `true`:

```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:                     # Nazwa twojego interfejsu
      dhcp4: true               # Włączenie klienta DHCP
```

Zapisz zmiany i zaktualizuj konfigurację:

```bash
sudo netplan apply
```


### Część 3: Diagnostyka i weryfikacja ustawień

Po każdej zmianie konfiguracji sieciowej powinieneś sprawdzić poprawność jej działania. Użyj do tego podstawowych narzędzi diagnostycznych.

**1. Weryfikacja przydzielonego adresu IP oraz maski:**
```bash
ip addr show enp0s3
```
*Na ekranie poszukaj sekcji `inet`, obok której powinien widnieć Twój nowo skonfigurowany adres IP oraz maska w notacji CIDR.*

**2. Testowanie łączności z bramą domyślną (weryfikacja trasy):**
```bash
ping -c 4 192.168.1.1
```
*Przełącznik `-c 4` oznacza, że zostaną wysłane dokładnie 4 pakiety ICMP Echo Request. Sprawdź, czy wartość `packet loss` wynosi 0%.*

---

### Część 4: Dokumentacja – Wymóg krytyczny na egzaminie INF.02

Podczas egzaminu państwowego samo poprawne wykonanie zadania to tylko połowa sukcesu. Egzaminator ocenia Twoją pracę na podstawie zapisanych zrzutów ekranu.

**Pamiętaj o złotej zasadzie dokumentowania:**
1.  Wpisz polecenie, które rozwiązuje dany punkt zadania (np. `ip addr`, `ping`).
2.  Zatwierdź polecenie klawiszem `Enter`.
3.  **Wykonaj zrzut ekranu w taki sposób, aby na jednym obrazie było wyraźnie widać zarówno WYDANE POLECENIE, jak i ZWRÓCONY WYNIK.**
4.  Zapisz pliki z czytelną nazwą sugerującą krok (np. `konfiguracja_ip.png`). Błędy w zrzutach lub ich brak skutkują utratą punktów, nawet przy sprawnie działającej sieci.

---

### Część 5: Przekazanie wyników pracy

Po prawidłowym wykonaniu wszystkich kroków i skompletowaniu dokumentacji w formie zrzutów ekranu, należy przekazać wyniki pracy do weryfikacji.

1. Spakuj wszystkie wykonane zrzuty ekranu do jednego archiwum (np. `.zip` lub `.rar`).
2. Plik archiwum nazwij według schematu: `Nazwisko_Imie_Klasa.zip` (np. `Kowalski_Jan_3TI.zip`).
3. Gotowe archiwum wyślij jako załącznik na poniższy adres e-mail:
   **marcin.wojciechowski@zs1goleniow.edu.pl**
4. W temacie wiadomości wpisz: *INF.02 - Konfiguracja interfejsu sieciowego - [Twoje Imię i Nazwisko]*
