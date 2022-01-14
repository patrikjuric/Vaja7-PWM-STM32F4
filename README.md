# Vaja7-PWM-STM32F4

Najprej sva aktivirala pri kanal kot PWM Generation CH1.Omogočila sva pin PE9. Poleg pina se izpiše TIM_CH1. Vrednost Perscaler je 16. Ko Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika, vrednost sedaj znaša 10kHz. V PWM Generation Chanel nastaviva Pulse (16 bits value) na 50.Ta parameter pomeni kakšna je širina signala. Prenastavljeni parameter Pulse (ki je 50) v  kodi, ki ga je generiral CubeMX je: sConfigOC.Pulse = 50;. V kodi spremeniva vrednost širine pulza na 25 %, z ukazom ConfigOC.Pulse = 12,5;. 

Pomen ukazov:

htim1.Instance->CCR1 = dutyCycle; - z njim nastavimo spremeljivko dutyCycle.

dutyCycle+=10; - spremeljivki dutyCycle prištejemo 10.

if(dutyCycle>90) dutyCycle=10; - če je spremenljivka večja od 90, ji nastavi vrednost 10.



Komentar na delovanje:
Vaja nama deluje.Bilo je le nekaj težav, kar se tiče same kvalitete signala na osciloskopu zaradi slabega spoja, ki sva jih hitro odpravilia in dobila dokaj čist signal. 
