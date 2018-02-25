# Car-Rental-Management-System

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/desktopphone.png" /></p>

Sistem se sastoji od mobilne i desktop aplikacije.

Mobilna aplikacija omogućava korisniku:
<ul>
  <li>Rezervisanje određenog automobila</li>
  <li>Pregled istorije iznajmljivanih automobila</li>
  <li>Pregled informacija o firmi</li>
</ul>

Desktop aplikacija omogućava korisniku:
<ul>
  <li>Vođenje evidencije o iznajmljivanju i vraćanju automobila</li>
  <li>Pregled slobodnih i zauzetih automobila</li>
  <li>Pregled ugovora iznajmljivanja</li>
  <li>Vođenje evidencije o klijentima</li>
  <li>Vođenje evidencije o servisiranju automobila</li>
  <li>Pregled statistike automobila koji su se najviše kvarili u određenom periodu(na osnovu toga vlasnik može da odluči koji automobil da proda ili kupi)</li>
  <li>Vođenje evidencije o finansijama (moguće je prikazati zaradu po danima,mesecima i godinama)</li>
  <li>Promenu cene iznajmljivanja (pritom da stare cene važe za iznajmljivanja automobila koji su iznajmljeni pre promene cene)</li>
  <li>Vođenje evidencije o radnicima</li>
  <li>Pregled efikasnosti svakog radnika (prikazivanje koliko je radnik iznajmio automobila u određenom periodu i na osnovu toga vlasnik može da nagradi ili otpusti radnika)</li>
  <li>Pregled radnih ugovora</li>
  <li>Pregled statistike iznajmljivanja automobila za određeni period (na osnovu toga vlasnik može da odluči koji automobil da kupi ili da proda)</li>
  <li>Promenu postojanost automobila u firmi (ako je automobil prodat ili iz nekog drugog razloga više ne postoji u firmi, korisnik može to zabeležiti kako automobil ne bi mogao više da se iznajmljuje a da pritom informacije o iznajmljivanju za taj automobili ostanu dostupne ili ako vlasnik firme želi da koristi neki automobil za lične potrebe a da to korišćenje ne evidentira)</li>
</ul>

## Korišćeni alati za razvoj sistema

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/1.jpg" width="380px" /></p>
Mobilna aplikacija je pravljena u cross platformi Xamarin, u programskom jeziku C#. Dostupna je za Android i iOS telefone.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/2.jpg" width="430px"/></p>
Desktop aplikacija je pravljena uz pomoć Windows Forms i .NET Framework-a.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/3.jpg" ></p>
Baza podataka je pravljena u Microsoft SQL Server-u.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/4.jpg" width="400px"/></p>
Baza podataka je postavljena online, na Micrososft Azure cloud-u, da bi moglo da joj se pristupi putem mobilne i desktop aplikacije.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/5.jpg" width="420px"/></p>
Razvojno okruženje koje je korišćeno je Micrososft Visual Studio.

## Relacioni model baze podataka
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/6.png" /></p>

## Mobilna aplikacija

### 1. Login
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/7.png" width="72%"/></p>
Na Login stranici korisnik unosi Korisničko ime I Lozinku kako bi mogao da koristi aplikaciju.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/8.png" width="72%"/></p>
Ukoliko korisnik ne popuni sva polja pojavljuje mu se obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/9.png" width="72%"/></p>
Slika kada korisnik popuni sva polja.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/10.png" width="72%"/></p>
Ukoliko korisnik unese pogrešno Korisničko ime ili Lozinku pojavljuje mu se obaveštenje.

### 2. Rezervisanje automobila
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/11.png" width="72%"/></p>
Kada se korisnik uspešno uloguje, redirektuje se na stranicu za rezervisanje automobila.
Na njoj se prikazuje ime i prezime korisnika i njegov korisnički ID (koji se koristi u Desktop aplikaciji za iznajmljivanje automobila). Ukoliko korisnik želi da se odjavi iz aplikaciji, to će uraditi klikom na dugme Logout.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/12.png" width="72%"/></p>
Kada korisnik odabere model automobila, prikazuje mu se kolika je cena po jednom danu za iznajmljivanje izabranog modela automobila. 
Opcija za Rezervisanje automobila je onemogućena sve dok korisnik ne odabere željeni automobil, kada korisnik odabere automobil, dugme za rezervisanje se omogućuje. 

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/13.png" width="72%"/></p>
Kada korisnik rezerviše automobil, prikazuje mu se obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/14.png" width="72%"/></p>
Ukoliko je korisnik već rezervisao automobil, na početnoj stranici mu se prikazuju informacije o tom automobilu i do kada mu važi rezervacija. Ukoliko korisnik želi da otkaže rezervaciju, to će uraditi klikom na dugme Otkaži rezervaciju.
Korisnik može samo jedan automobil da rezerviše. Rezervacija važi 24h od trenutka kada je automobil rezervisan.

### 3. Istorija iznajmljivanja automobila
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/15.png" width="72%"/></p>
Na ovoj stranici korisnik može videti istoriju iznajmljivanja automobila, hronološki poređanu, počevši od poslednjeg iznajmljivanja pa sve do prvog automobila koji je iznajmio.

### 4. Kontakt Informacije
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/16.png" width="72%"/></p>
Na ovoj stranici korisnik može videti informacije o Rent a car firmi, ulicu gde se nalazi firma i njen broj telefona.


## Desktop aplikacija

### 0. Login
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/17.jpg"/></p>
Na Login formi radnik unosi svoje Korisničko ime i Lozinku kako bi moga da koristi program.
U zavisnosti od vrste radnika koji se prijavljuje za korišćenje programa dobijaju se određene privilegije za pristupanje delova programa.
<br>
Privilegije za korišćenje programa su:
<ul>
  <li>Recepcioner (može da koristi: Iznajmljivanje, Klijenti, Servisi i Nalog)</li>
  <li>Finansijski radnik (može da koristi: Iznajmljivanje, Klijenti, Servisi, Finansije i Nalog)</li>
  <li>Direktor (Ima potpunu kontrolu nad programom, može da koristi: Iznajmljivanje, Klijenti, Servisi,Finansije,Radnici,Automobil i Nalog)</li>
</ul>

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/18.jpg"/></p>
Prilikom prijavljivanja ukoliko se ne popune sva polja izbacuje se obaveštenje korisniku, isto obaveštenje se pojavljuje dalje u svim delovima programa.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/19.jpg"/></p>
Ukoliko korisnik unese nepostojeće Korisničko ime izbacuje mu se obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/20.jpg"/></p>
<p>Ukoliko korisnik unese pogrešnu Lozinku izbacuje mu se obaveštenje.</p>

### 1. Početna
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/21.jpg"/></p>
Izgled aplikacije kada se prijavi **Recepcioner** za korišćenje programa.
Ispisuje mu se na početnoj strani njegovo ime i prezimei i postavlja se određena ikonica za recepcionere na dugme Nalog.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/22.jpg"/></p>
Izgled aplikacije kada se prijavi **Finansijski radnik** za korišćenje programa.
Ispisuje mu se na početnoj strani njegovo ime i prezime i postavlja se određena ikonica za finansijske radnike na dugme Nalog.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/23.jpg"/></p>
Izgled aplikacije kada se prijavi **Direktor** za korišćenje programa.
Ispisuje mu se na početnoj strani njegovo ime i prezime i postavlja se određena ikonica za direktore na dugme Nalog.

### 2. Iznajmljivanje
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/24.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Iznajmi auto</li>
  <li>Vrati auto</li>
  <li>Pogleda slobodne automobile za iznajmljivanje</li>
  <li>Pogleda zauzete automobile koji su već iznajmljeni</li>
  <li>Pogleda ugovore iznajmljivanja</li>
</ul>

#### 2.1 Iznajmi auto
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/25.jpg"/></p>
U ovom delu korisnik iznajmljuje automobile.
Korisniku je prvo onemogućeno da unosi podatke za iznajmljivanje sve dok se na izaberu po redosledu prvo Proizvođač zatim Proizvođačeve model automobila (koji su učitani prilkom odabira u combo box-u Proizvođač) zatim Broj registracije automobila (koji je ućitan prilikom odabira Modela iz combo box-a, svi Brojevi registracije predstavljaju automobile koji su slobodni). 


<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/26.jpg"/></p>
Kada korisnik izabere automobil koji želi da iznami odobrava mu se unošenje podataka.
Korisnik unosi ID klijenta kome želi da iznajmi automobil.
Već je zabeležen ID radnika prilikom prijavljivanja na program.
Ispisuje se koja je trenutna cena iznajmljivanja u dinarima (kasnije Finansijski radnik može da promeni cenu iznajmljivanja za taj model ali se u ugovoru beleži ID cene koja je bila u tom trenutku) za izabrani model automobila.
Ispisuje je se tačno vreme od kada je iznajmljen automobil (trenutno vreme)
Unosi se datum do kada se iznajmljuje automobil (ukoliko korisnik prekorači taj datum mora da plati dvostruko za te prekoračene dane iznajmljivanja)
Unosi se način plaćanja (keš ili kartica)

Kada se kligne na dugme Iznajmi prvo se proverava da li je automobil rezervisan. Ukoliko je automobil rezervisan onda se proverava da li je izabrani klijent baš taj koji je rezervisao automobil, ukoliko nije on rezervisao, korisniku se prikazuje obaveštenje:

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/27.jpg"/></p>

Ukoliko automobil nije rezervisan ili je klijent baš taj koji je rezervisao, automatski se postavlja da je automobil zauzet, pravi se ugovor i pravi se istorija iznajmljivanja (u toj istoriji će se beležiti kada je automobil vraćen, koji radnik je vratio automobil. kolika je zarada, pre toga je upisana u istoriji zarada koju je kupac platio prilikom iznajmljivanja a ukoliko se prekorače dani ta zarada se povećava).
Kada se iznajmi automobil izbacuje se korisniku obaveštenje i uklanjaju se podaci iz forme i onemogućuje se unošenje podatka sve dok se ponovo istim redosledom ne odabere automobil.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/28.jpg"/></p>

#### 2.2 Vrati auto
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/29.jpg"/></p>
U ovom delu korisnik vraća iznajmljeni automobil.
Učitava se korisnikov ID koji je zapamćen prilikom prijavljivanja u program.
Ukoliko se unese nepostojeći broj registracije automobila prikazuje se korisniku obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/30.jpg"/></p>
Ukoliko se unese broj registracije za automobil koji nije iznajmljen korisniku se prikazuje obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/31.jpg"/></p>
Kada se vrati automobil korisniku se prikazuje obaveštenje i beleži se kada je automobil vraćen i koji radnik ga je vratio.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/32.jpg"/></p>

#### 2.3 Slobodni automobili
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/33.jpg"/></p>
U ovom delu se prikazuju slobodni automobili i njihov ukupan broj.

#### 2.4 Zauzeti automobili
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/34.jpg"/></p>
U ovom delu se prikazuju zauzeti automobili i njihov broj.

#### 2.5 Ugovori iznajmljivanja
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/35.jpg"/></p>
U ovom delu se prikazuju ugovori iznajmljivanja koji sadrže:
<ul>
  <li>Broj ugovora</li>
  <li>Broj registracije automobila</li>
  <li>Klijenta</li>
  <li>Radnika</li>
  <li>Datim kada je iznajmlje automobil</li>
  <li>Datum do kada je iznajmljen automobil</li>
  <li>Cena iznajmljivanja koja je bila na dan iznajmljivanja</li>
  <li>Način plaćanja</li>
</ul>

### 3. Klijenti
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/36.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Doda klijenta</li>
  <li>Pretraži klijenta</li>
  <li>Izmeni klijenta</li>
</ul>

#### 3.1 Dodaj klijenta
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/37.jpg"/></p>
U ovom delu korisnik dodaje nove klijente.
Ukoliko se pokuša dodati klijent koji već postoji pojavljuje se upozorenje (u bazi se prvo proverava da li već postoji JMBG kod klijenata).

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/38.jpg"/></p>
Ukoliko se pokuša dodati Username klijenta koji već postoji pojavljuje se upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/39.jpg"/></p>
Kada se doda klijent pojavljuje se obaveštenje da je uspešno dodat i ispisuje se njegov korisnički ID.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/40.jpg"/></p>
Nakon dodavanja klijenta brišu se sva polja sa forme.

#### 3.2 Pretraga klijenata
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/41.jpg"/></p>
U ovom delu korisnik pretražuje klijente.
Prilikom ulaženja u ovaj deo programa, učitavaju se svi klijenti iz baze podataka.
Moguće je pretraživati klijente po njihovom ID-ju, Imenu, Prezimenu, preko JMBG-a, broja telefona, email-a, datuma rođenja i datuma učlanjenja.

#### 3.3 Izmeni klijenta
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/42.jpg"/></p>
U ovom delu je moguće izmeniti informacije o klijentu.
Korisnik prvo unosi ID klijenta da bi pronašao klijenta. Ukoliko se unese neispravan ID klijenta korisniku se prikazuje upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/43.jpg"/></p>
Kada se unese ispravan ID klijenta., ispisuju se njegovi podaci i omogućava se njihovo menjanje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/44.jpg"/></p>
Klikom na dugme Izmeni menjaju se podaci (sva polja sa * moraju biti popunjena da bi se izmenili podaci) klijenta.
Klikom na dugme Promeni klijenta omogućava se unošenje ID klijenta i brišu se sva ostala polja na formi kako bi moglo da se pretraži ponovo klijent.

### 4. Servisi
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/45.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Vidi statistiku najservisiranijih automobila</li>
  <li>Pošalje automobil na servis i time onemogući njegovo iznajmljivanje</li>
  <li>Vrati automobil sa servisa</li>
  <li>Prikaže istoriju servisiranja</li>
  <li>Doda servisera</li>
</ul>

#### 4.1 Najservisiraniji automobili
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/46.jpg"/></p>
U ovom delu korisnik može videti statistiku najservisiranijih automobila.
Prilikom otvaranja ovog dela programa učitava se statistika za sve vreme poslovanja. Moguće je i odabrati period za koji korisnik želi da vidi statistiku.
Prelaženjem miša na deo grafika prikazuje se ToolTip sa informacijama o automobilu i brojem servisiranja.

#### 4.2 Pošalji automobil na servis
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/47.jpg"/></p>
U ovom delu korisnik šalje automobil na servis.
Prilikom otvaranja ovog dela programa učitavaju se serviseri iz baze podataka i ispisuje se datum slanja koji će se zabeležiti u bazi.
Kada se klikne na dugme Pošalji proverava se uneti Broj registracije, ukoliko je unet nepostojeći Broj registracije pojavljuje se upozorenje korisniku.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/48.jpg"/></p>
Ukoliko je uneti automobil iznajmljen pojavljuje se upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/49.jpg"/></p>

Ukoliko uneti automobil više ne postoji u firmi pojavljuje se upozorenje.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/50.jpg"/></p>

#### 4.3 Vrati automobil sa servisa
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/51.jpg"/></p>
U ovom delu korisnik vraća automobil sa servisa i upisuje koliko para je plaćeno serviseru i upisuje se šta je popravljeno na automobilu, takođe se beleži kada je automobil vraćen u firmu sa servisa. kao i u delu  4.2 Pošalji automobil na servis, proverava se da li je ispravno unet Broj registracije, ukoliko uneti automobil nije poslat na servis pojavljuje se upozorenje korisniku (jer sve mora da se beleži i kad je poslat na servis i kad je vraćen), takođe ukoliko se pokuša vratiti automobil koji je iznajmljen pojavljuje se upozorenje.

#### 4.4 Istorija servisiranja automobila
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/52.jpg"/></p>
U ovom delu se prikazuje istorija servisiranja automobila gde korisnik može da vidi sledeće informacije:
<ul>
  <li>ID istorije</li>
  <li>Broj registracije</li>
  <li>Naziv servisera kod koga je poslat automobil</li>
  <li>Da li je vraćen automobil</li>
  <li>Cena koja je plaćena serviseru kada se vratio automobil sa servisa</li>
  <li>Datum slanja na servis</li>
  <li>Datum vraćanja iz servisa</li>
  <li>Opis servisa, šta je popravljeno ili zamenjeno u servisu</li>
</ul>

#### 4.5 Dodaj servisera
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/53.jpg"/></p>
U ovom delu se dodaje serviser kod koga će se kasnije slati automobili na servis.
Prilikom dodavanja servisera prvo se proverava da li uneti serviser postoji, ukoliko postoji prikazuje se upozorenej korisniku.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/54.jpg"/></p>

Kada se doda serviser, ispisuje se obaveštenje korisniku. I polja u formi se resetuju kako bi korisnik ponovo mogao da doda novog servisera.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/55.jpg"/></p>

### 5. Finansije
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/56.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Vidi zaradu na dnevnom nivou</li>
  <li>Vidi zaradu na mesečnom nivou</li>
  <li>Vidi zaradu na godišnjem nivou</li>
  <li>Promeni cenu iznajmljivanja automobila</li>
</ul>

#### 5.1 Zarada na dnevnom nivou
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/57.jpg"/></p>
U ovom delu korisnik može videti zaradu na dnevnom nivou, odnosno zaradu po danima za određeni mesec i godinu.
Prilikom biranja meseca i godine za prikazivanje statistike, moguće je odabrati statistiku minimum za godinu i mesec kada je iznajmljen prvi automobil pa maksimum sve do današnjeg datuma.
Prelaskom mišem na određeni deo statistike pojavljuje se ToolTip sa ostvarenom zaradom u dinarima.

#### 5.2 Zarada na mesečnom nivou
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/58.jpg"/></p>
U ovom delu se prikazuje zarada na mesečnom nivou, odnosno prikazuje se zarada po mesecima za izabranu godinu.
Minimum godina koja može da se izabere je godina u kojoj je iznajmljen prvi automobil.
Maksimalna godina je trenutna godina.
Prelaskom mišem na određeni deo statistike pojavljuje se ToolTip sa ostvarenom zaradom u dinarima.

#### 5.3 Zarada na godišnjem nivou
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/59.jpg"/></p>
U ovom delu se prikazuje zarada na godišnjem nivou, odnosno zarada koja je ostvarena za sve godine poslovanja firme.
Prelaskom mišem na određeni deo statistike pojavljuje se ToolTip sa ostvarenom zaradom u dinarima.

#### 5.4 Promeni cenu iznajmljivanja
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/60.jpg"/></p>
U ovom delu korisnik može da postavi novu cenu iznajmljivanja za određeni model automobila.
Menjanje se omogućava tek ada se odaberu određeni Proizvođač i Model automobila.
Kada se odabere model automobila, prikazuje se i trenutna cena iznajmljivanja za izabrani model.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/61.jpg"/></p>
Kada se promeni cena pojavljuje se obaveštenje korisniku.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/62.jpg"/></p>


### 6. Radnici
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/63.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Vidi statistiku efikasnosti radnika (najefikasnije radnike)</li>
  <li>Doda radnika</li>
  <li>Pretraži radnika (pogleda informacije o određenom radniku)</li>
  <li>Izmeni informacije radnika</li>
  <li>Doda radni ugovor</li>
  <li>Pretraži radne ugovore (pogleda informacije o radnim ugovorima)</li>
</ul>

#### 6.1 Efikasnost radnika
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/64.jpg"/></p>
U ovom delu korisnik može videti efikasnost radnika, odnosno koliko puta su određeni radnici napravili ugovora, tj. Koliko puta su iznajmljivali automobile.
Kada se otvori ovaj deo programa učitava se statistika za sve vreme poslovanja.
Moguće je odabrati određeni period za koji želimo da prikažemo statistiku.
Prelaskom mišem na određeni deo statistike pojavljuje se ToolTip sa informacijama o radniku i brojem ugovora koje je napravio radnik.
Minimalni datum koji može da se izabere je datum u kojem je iznajmljen prvi automobil.
Maksimalna datum je trenutni datum.

#### 6.2 Dodaj radnika
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/65.jpg"/></p>
U ovom delu korisnik dodaje radnika i kreira nalog za korišćenje programa.
Kada se otvori ovaj deo programa, u combo box-u se ubacuju radna mesta.
Ukoliko se dodaje već postojeći radnik pojavljuje se upozorenje korisniku (u bazi se radnici proveravaju putem JMBG-a).

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/66.jpg"/></p>

Ukolko se dodaje već postojeći Username za radnika pojavljuje se upozorenje korisniku.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/67.jpg"/></p>

Kada se doda novi radnik pojavljuje se obaveštenje korisniku i polja u formi se resetuju kako bi korisnik mogao da ponovo doda novog radnika.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/68.jpg"/></p>

#### 6.3 Pretraga radnika
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/69.jpg"/></p>
U ovom delu korisnik može da pretražuje radnike i da vidi sledeće informacije o njima:
<ul>
  <li>ID radnika</li>
  <li>Ime</li>
  <li>Prezime</li>
  <li>JMBG</li>
  <li>Broj telefona</li>
  <li>Email</li>
  <li>Datum rođenja</li>
  <li>Datum prvog zaposlenja</li>
  <li>Radno mesto</li>
  <li>Opis radnog mesta</li>
</ul>

Korisnik može pretražiti radnike po:
<ul>
  <li>ID radnika</li>
  <li>Imenu</li>
  <li>Prezimenu</li>
  <li>JMBG-u</li>
  <li>Broju telefona</li>
  <li>Email-u</li>
  <li>Datumu rođenja</li>
  <li>Datumu prvog zaposlenja</li>
  <li>Radnom mestu</li>
</ul>

Kada se učita ovaj deo program prikazuju se svi radnici.

#### 6.4 Izmeni radnika
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/70.jpg"/></p>
U ovom delu programa je moguće izmeniti informacije o radniku.
Prvo se unosi ID radnika, ukoliko se unese nepostojeći ID radnika korisniku se pojavljuje upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/71.jpg"/></p>
Kada se unese ispravan ID radnika, učitavaju se podaci o radniku i moguće je izmeniti ih.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/72.jpg"/></p>
Na dugme Promeni radnika se resetuju sva polja u formi i potrebno je da korisnik ponovo udese ID radnika.
Kada se klikne na dugme Izmeni, menjaju se podaci o radniku i korisniku se pojavljuje obaveštenje da su podaci izmenjeni.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/73.jpg"/></p>

#### 6.5 Dodaj radni ugovor
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/74.jpg"/></p>
U ovom delu se dodaje radni ugovor za radnika.
Ukoliko korisnik unese nepostojeći ID radnika pojavljuje se upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/75.jpg"/></p>
Kada se doda novi radni ugovor, pojavljuje se obaveštenje korisniku i polja na formi se resetuju kako bi korisnik mogao da ponovo doda novi radni ugovor.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/76.jpg"/></p>

#### 6.6 Pretraga radnih ugovora
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/77.jpg"/></p>
U ovog delu korisnik može da vrši pretragu radnih ugovora i da vidi o njima sledeće informacije:
<ul>
  <li>Broj radnog ugovora</li>
  <li>ID radnika</li>
  <li>Ime radnika</li>
  <li>Prezime radnika</li>
  <li>JMBG</li>
  <li>Datum rođenja</li>
  <li>Radno mesto</li>
  <li>Opis radnog mesta</li>
</ul>

Pregraga se vrši unošenjem jedgnog od gore navedenih podataka ugovora.


### 7. Automobili
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/78.jpg"/></p>
U ovom delu korisnik bira da li želi da:
<ul>
  <li>Pogleda statistiku najiznajmljivanijih modela automobila</li>
  <li>Doda automobil</li>
  <li>Doda model automobila</li>
  <li>Doda proizvođača automobila</li>
  <li>Vrši promenu postojanosti automobila u firmi (npr. ako je automobil prodat ili iz nekog drugog razloga više ne postoji u firmi korisnik može to zabeležiti kako automobil ne bi mogao više da se iznajmljuje a da pritom informacije o iznajmljivanju za taj automobili ostanu dostupne ili ako vlasnik firme želi da koristi neki automobil a da to korišćenje ne upisuje u bazu podataka...)
</li>
</ul>

#### 7.1 Najiznajmljivaniji automobili
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/79.jpg"/></p>
U ovom delu korisnik može pogledati statistiku najiznajmljivanijih modela automobila, kako bi mu pomoglo u odluci koji model automobila da kupi kako bi unapredio svoje poslovanje.
Kada se učita ovaj deo programa, korisniku se prikazuje statistika za sve vreme poslovanja
Korisnik može odabrati period za koji želi da vidi statistiku.
Kada se pređe mišem na određeni deo statistike pojavljuje se ToolTip sa informacijama o modelu i broju iznajmljivanja.

#### 7.2 Dodaj automobil
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/80.jpg"/></p>
U ovom delu korisnik dodaje automobile koji će kasnije biti iznajmljivani.
Da bi se omogućilo dodavanje automobila potrebno je da korisnik odabere Proizvođača i Model za željeni automobil.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/81.jpg"/></p>

Ukoliko korisnik pokuša da doda automobil koji već postoji pojavljuje mu se upozorenje.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/82.jpg"/></p>

Kada korisnik doda novi automobil pojavljuje mu se obaveštenje i polja na formi se resetuju kako bi mogao da ponovo doda novi automobil.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/83.jpg"/></p>

#### 7.3 Dodaj model
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/84.jpg"/></p>
U ovom delu korisnik može da doda novi model za izabranog proizvođača autmobila.
Kada se odabere proizvođač iz combo box-a korisniku je omogućeno da unese podatke.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/85.jpg"/></p>
Ukoliko korisnik pokuša da doda model za izabranog proizvođača koji već postoji, korisniku se pojavljuje upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/86.jpg"/></p>
Kada korisnik uspešno doda model za izabranog proizvođača, pojavljuje mu se obaveštenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/87.jpg"/></p>

#### 7.4 Dodaj proizvođača
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/88.jpg"/></p>
U ovom delu korisnik može da doda proizvođača automobila.
Ukoliko već postoji uneti proizvođač korisniku se pojavljuje upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/89.jpg"/></p>

Kada korisnik uspešno doda novog proizvođača pojavljuje mu se obaveštenje i podaci u formi se resetuje kako bi korisnik moga da doda novog proizvođača.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/90.jpg"/></p>

#### 7.5 Postojanost automobila u firmi
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/91.jpg"/></p>
U ovom delu korisnik vrši promenu postojanosti automobila u firmi, npr. ako je automobil prodat ili iz nekog drugog razloga više ne postoji u firmi korisnik može to zabeležiti kako automobil ne bi mogao više da se iznajmljuje a da pritom informacije o iznajmljivanju za taj automobili ostanu dostupne ili ako vlasnik firme želi da koristi neki automobil za lične potrebe a da to korišćenje ne upisuje u bazu podataka.

Ukoliko korisnik unese nepostojeći Broj registracije prikazuje mu se upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/92.jpg"/></p>
Kada korisnik unese ispravan Broj registracije automobila, dozvoljava mu se menjanje postojanosti i ispisuje mu se da li izabrani automobil postoji u firmi.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/93.jpg"/></p>
Na dugme Promeni automobil, moguće je promeniti automobil.
Na dugme Da, menja se postojanost automobila.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/94.jpg"/></p>
Takođe je moguće i vratiti automobil u firmu (ukoliko gazda ponovo kupi isti automobil ili vrati u firmu automobil koji je koristio za lične potrebe).

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/95.jpg"/></p>

Na dugme DA se vraća automobil u firmu.
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/96.jpg"/></p>

### 8. Nalog
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/97.jpg"/></p>
U ovog delu korisnik bira da li želi da:
<ul>
  <li>Promeni lozinku</li>
  <li>Se odjavi iz programa</li>
</ul>

Ukoliko je korisnik ulogovan kao **Direktor** ikonica dugmeta Nalog je: <img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/98.jpg"/>

Ukoliko je korisnik ulogovan kao **Finansijski radnik** ikonica dugmeta Nalog je: <img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/99.jpg"/>

Ukoliko je korisnik ulogovan kao **Recepcioner** ikonica dugmeta Nalog je: <img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/100.jpg"/>

#### 8.1 Promeni lozinku
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/101.jpg"/></p>
U ovom delu korisnik može da promeni svoju lozinku za korisnički nalog.
Korisniku se prikazuje njegovo korisničko ime.
Da bi promenio lozinku mora prvo da unese trenutnu lozinku, ukoliko ne unese tačnu trenutnu lozinku, pojavljuje mu se upozorenje.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/102.jpg"/></p>
Kada uspešno promeni lozinku, pojavljuje mu se obaveštenje i automatski ga program izloguje i prinuđen je da se ponovo uloguje sa novom lozinkom.

<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/103.jpg"/></p>

#### 8.2 Odjavi se
<p align="center"><img src="https://raw.githubusercontent.com/kovacevic-marko/Car-Rental-Management-System/master/Pictures/104.jpg"/></p>
Klikom na dugme odjavi se, korisnik se odjavljuje iz programa i ponovo je moguće da se drugi korisnik prijavi u program.

<br><br><br>
Datum proizvodnje: Februar 2018.
