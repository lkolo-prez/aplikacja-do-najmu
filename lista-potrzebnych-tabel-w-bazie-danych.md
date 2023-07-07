Bazy danych


1. Tabela "Najemcy":
   - ID_najemcy (klucz główny)
   - Imię
   - Nazwisko
   - Miasto 
   - Ulica
   - Numer budynku
   - Numer mieszkania
   - Kod pocztowy
   - Numer Pesel
   - Numer dowodu
   - Numer Paszportu
   - Numer telefonu
   - Adres e-mail
   - Narodowsośc
   - Status (Student, bezrobotny, pracujacy)

2. Tabela "Nieruchomosci":
   - ID_jednostki (klucz główny)
   - Miasto
   - Ulica
   - Numer budynku
   - Numer mieszkania
   - Numer pokoju
   - Typ jednostki (np. mieszkanie, lokal handlowy)


3. Tabela "Umowy najmu":
   - ID_umowy (klucz główny)
   - ID_najemcy (klucz obcy z tabeli "Najemcy")
   - ID_jednostki (klucz obcy z tabeli "Jednostki najmu")
   - Data rozpoczęcia
   - Data zakończenia
   - Warunki umowy (np. wysokość czynszu, opłaty za media)
   - Wysokość czynszu
   - 

4. Tabela "Płatności":
   - ID_płatności (klucz główny)
   - ID_najemcy (klucz obcy z tabeli "Najemcy")
   - ID_umowy (klucz obcy z tabeli "Umowy najmu")
   - Kwota płatności
   - Data płatności
   - Typ płatności (np. czynsz, opłaty za media)
   - Status płatności (np. opłacone, oczekujące)
   - Forma płatności


5. Tabela "Media":
   - ID_media (klucz główny)
   - Nazwa media (np. woda, prąd, ogrzewanie)
   - Jednostka miary (np. m³, kWh)
   - Koszt jednostkowy (np. cena za m³ wody, cena za kWh prądu)
   - Data wpisu wartości
   - 

6. Tabela "Pomiary":
   - ID_pomiaru (klucz główny)
   - ID_najemcy (klucz obcy z tabeli "Najemcy")
   - ID_jednostki (klucz obcy z tabeli "Jednostki najmu")
   - ID_media (klucz obcy z tabeli "Media")
   - Data pomiaru
   - Wartość pomiaru
   - Inne informacje dotyczące pomiaru

7. Tabela "Rozliczenia mediów":
   - ID_rozliczenia (klucz główny)
   - ID_najemcy (klucz obcy z tabeli "Najemcy")
   - ID_umowy (klucz obcy z tabeli "Umowy najmu")
   - ID_media (klucz obcy z tabeli "Media")
   - Okres rozliczeniowy (np. miesiąc, rok)
   - Zużycie mediów (np. ilość m³ wody, ilość kWh prądu)
   - Kwota rozliczenia
   - Status rozliczenia (np. opłacone, oczekujące)
   - Inne szczegóły rozliczenia
