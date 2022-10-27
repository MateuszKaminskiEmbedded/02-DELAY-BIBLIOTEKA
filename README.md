# 02-DELAY-BIBLIOTEKA

Bibloteka "delay" służy do odmierzania czasu. Zawiera dwie funkcje. Pierwsza z nich to "delay_us(us)". Odmierza czas podany w argumecie. Wielkość odmierzango czasu to mikrosekundy.
Druga funkcja to "delay_ms(ms)". Odmierza ona czas tak samo jak pierwsza, z tą różnicą, że wielkość odmierzango czasu to milisekundy. Obie funkcje bazują na wewnętrznym liczniku
mikrokontrolera, działającego zaraz po uruchomieniu mikrokontrolera i inkrementowanego co drugi takt zegara systemowego.

W celu wykorzystania funkcji odmierzających czas, należy:
1) Dodać pliki do folderu z projektem
2) Do pliku głównego programu lub innego pliku wykorzystującego odmierzanie czasu dołączyć biblioteke #include "delay.h"
3) W pliku nagłówkowym biblioteki (delay.h) lub w pliku głównym programu dodać definicję stałej #define SYS_FREQ 120000000, która przechowywać będzie częstotliwość pracy mikrokontrolera
(wymagane do przeliczneia wartości podanej w argumencie na odpowiadający mu czas).
4) Funkcje odmierzające czas są dostępne dla użytkownika
