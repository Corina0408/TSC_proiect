link diagrama bloc: https://files.fm/u/eejnjsv4u4 

link Bill of Materials: https://docs.google.com/spreadsheets/d/1bhhom45KiLlfx5yxiHwmtoe4DynNoX60qw5_dlvZoLE/edit?usp=sharing 



Descrierea functionalitatii: 

	dispozitiv smart, construit in jurul microcontrollerului ESP32-C6, care integreaza senzori de afisaj OLED, LED RGB pentru vizual, control tactil si un potentiometru.

	Module si componente utilizate

    ESP32-C6: microcontroller principal, care gestioneaza toate componentele, comunicarea si logica dispozitivului

    BME280: senzor de temperatura, umiditate si presiune

    Display OLED (SSD1306): afiseaza informatii de la senzori si statusul sistemului

    LED RGB WS2812B: ofera feedback vizual configurabil

    TTP223: buton tactil folosit pentru interactiuni simple, cum ar fi pornirea luminii sau schimbarea modului de afisare

    Potentiometru: permite reglarea unui parametru analogic

    Reed switch: senzor magnetic digital, detecteaza apropierea unui magnet

	Interfete si comunicatie

    I2C: folosita pentru a conecta atat senzorul BME280, cat si display-ul OLED pe acelasi bus. ESP32-C6 gestioneaza ambele componente fara conflicte.

    PWM/One-wire: pentru LED-ul WS2812B, controlat prin semnal digital specific.

    Digital input: pentru butonul capacitiv si reed switch.

    Analog input (ADC): pentru citirea potentiometrului.

Procesare si comportament

ESP32-C6 colecteaza datele de la senzori si le afiseaza pe ecran. In plus, permite interactiuni tactile si vizuale cu utilizatorul





Descrierea pinilor ESP32-C6:

BME280 (I2C)

    GPIO8 (SDA) – Bus I2C partajat cu display

    GPIO9 (SCL)

OLED SSD1306 (I2C)

    GPIO8 (SDA) – Partajare eficienta de pini

    GPIO9 (SCL)

WS2812B (PWM)

    GPIO7 – Output digital cu timing precis

TTP223 (Digital)

    GPIO6 – Pin liber, ideal pentru input

Potentiometru (Analog)

    GPIO4 (ADC1) – Suporta ADC, masoara tensiune

Reed switch (Digital)

    GPIO5 – Citire stare logica simpla
	
