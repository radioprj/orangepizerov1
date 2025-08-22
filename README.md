**Eksperymentalny obraz hotspot FM dla wersji komputera [Orange PI Zero v1.x](http://www.orangepi.org/html/hardWare/computerAndMicrocontrollers/details/Orange-Pi-Zero.html)**

**To jest projekt hobbystyczny i rozwija się w autora własnym tempie.**

Obraz przeznaczony do budowy hotspota domowego z wykorzystaniem modułu radiowego SA818

Obraz o nazwie [hotspotfm-ozpi.img.xz](https://github.com/radioprj/orangepizerov1/releases/download/1.0/hotspotfm-ozpi.img.xz) (jest do pobrania jest na końcu tej strony) nagrać na kartę microSD  przy pomocy: https://etcher.balena.io/

Jeśli masz problem zapisać skompresowany obraz .xz na kartę microSD możesz go dekompresować darmowym narzędziem [7-zip](http://www.e7z.org/free-download.htm) Rozpakowany obraz możesz też zapisać na kartę microSD programem [Win32Image](https://sourceforge.net/projects/win32diskimager/files/Archive/)

Login do konsoli via ssh:

user: root

hasło: fmpoland

Zalecana zmiana hasła poleceniem: **passwd**

Dostęp do dashboard:

http://hotspotfm.local/

lub

http://ip_adres

IP adres możesz znaleźć przy pomocy darmowego narzędzia: https://www.advanced-ip-scanner.com/pl/

Konfiguracja via Dashboard, należy wybrać z menu "Admin" i następnie: 

W pierwszej kolejności sprawdź poprawne ustawienia obsługi SQL i PTT w menu

**SQL PTT**

Po sprawdzeniu / ustawieniu  SQL / PTT dopiero wtedy możesz przejść do konfiguracji:

**SVXCnf** - konfiguracja konta FM POLAND

**NodeInfo** - Informacje o stacji

**WEBCnf** - konfiguracja Dashboard

oraz inne opcje stosownie do potrzeb

CZYTAJ uważnie informacje umieszczone w każdym oknie z serii administracyjnych
w których są istotne informacje do dostępnych ustawień

![Admin Menu](https://github.com/radioprj/orangepizerov1/blob/main/admin-menu.png)

Domyślnie obraz przygotowany do pracy z płytkami radiowymi SA818/SA868 na bazie schematu SPOTNIK lub ROLINK


Można wykorzystać obraz z dowolnym radiem np GMxx, BF-888, UVK5, UV5R itp podłączając go: http://fm-poland.pl/schemat-intrefejsu-dla-orange-pi-zero-anyradio/


Jeśli dashboard będzie dostępny z zewnątrz ( **nierekomendowane z powodów bezpieczeństwa**  - zastanów sie czy jest to ci niezbędne)  to aby dostać się do menu ADMIN należy w Admin -> WebCnf w opcji REMOTEIP zamiast adresu 127.0.0.1 wpisać zdalny zaufany IP adres (ZALECANE: można skorzystać z VPN [Tailscale](https://tailscale.com/) wersja personal zawiera darmową obsługę 3 userów/100 urządzeń). Można też dostać z publicznego adresu do strony dashboard po linkiem

http://ipadresdashboard/svxc/

po podaniu użytkownika i hasła gdzie można wyłączyć lub włączyć zdalnie odbiornik SVXLINK. Jak założyć użytkownika i dla niego hasło patrz opis na swoim hotspot w pliku /etc/svxlink/SVXControl.txt

![Hotspot login](https://github.com/radioprj/orangepizerov1/blob/main/hotspot-login.png)


![OLED-LCD](https://github.com/radioprj/orangepizerov1/blob/main/displays-svx.png)
Możesz podłączyć wyświetlacze LCD 1602, 2004 patrz w katalog /opt/fmpoland/lcdsvx/

lub OLED SSD1306, SH1106 patrze w katalog /opt/fmpoland/oledsvx/

w katalogach tych jest plik **opis.txt** z informacjami o podłączeniu i uruchomieniu wyświetlaczy

Możesz skorzystać z Remote Display zamiast podłączać bezpośrednio do hotspota:

https://github.com/radioprj/remoteoled

https://github.com/radioprj/remotelcd

**Eksperymentalny obraz używasz na własną odpowiedzialność i autor nie ponosi odpowiedzialności za wykorzystane rozwiązanie i wynikające z niego skutki.**
