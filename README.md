Markdown jest dostosowany pod [Obsidian](https://obsidian.md/), więc w podglądzie Githuba część rzeczy może się psuć

---

### Liczby zespolone
Moduł liczby zespolonej a+bi = odległość od punktu (0, 0)
Argument liczby zespolonej = kąt, który tworzy z osią części rzeczywistych. Argument główny = argument należący do <0*, 360*>.

Postać trygonometryczna (Gaussa) = moduł \* (cos(argument) + sin(argument) \* i)

Argument możemy wyznaczyć za pomocą dwóch równań. Najpierw rysujemy pomocniczy szkic położenia liczby od (0, 0), następnie SOH/CAH/TOA i otrzymujemy wartość cos/sin. Następnie: w pierwszej ćwiartce same plusy, w drugiej tylko sinus, w trzeciej tanges i cotangens, a w czwartej cosinus.

Dzielenie liczb zespolonych = musimy pomnożyć licznik i mianownik przez sprzężenie.
Pierwiastek z liczby zespolonej = do potęgi i układ równań.

##### Działania na postaci trygonometrycznej
$z1 * z2 = r1 * r2 * (cos(a1 + a2) + i * sin(a1 + a2))$
$z1 / z2 = r1 / r2 * (cos(a1 - a2) + i * sin(a1 - a2))$
$z ^ n = r^n * (cos(n * a) + i * sin(n * a))$

Postać Eulera liczby zespolonej: $z * e^{i*modul}$

### Wyznacznik macierzy

Wyznacznik dla macierzy 3x3 otrzymujemy przez dopisanie dwóch wierszów / dwóch kolumn -> suma przekątnych od lewego górnego w dół minus suma przekątnych od prawego górnego w dół.

Dla większych macierzy wykorzystujemy zasadę -1^(wiersz+kolumna) * liczba pod tą pozycją * wyznacznik z macierzy bez wybranego wiersza/kolumny. Wybieramy kolumnę / wiersz z jak największą liczbą zer, aby jak najszybciej zmniejszyć rząd macierzy.

Macierz osobliwa <-> wyznacznik == 0

##### Zasady
- transpozycja oraz operacje elementarne nie zmieniają wyznacznika
- zamiana miejscami 2 kolumn/wierszy zmienia znak wyznacznika
- det(A \* B) = det(A) \* det(B)
- det(A^-1) = A^-1
* pomnożenie wiersza/kolumny przez x = pomnożenie wyznacznika przez x
* Wyznacznik macierzy, której wiersz/kolumna jest kombinacją liniową innych ww. jest równy 0!

### Macierze
Macierz symetryczna: a_ij = a_ji
Macierz antysymetryczna: a_ij = -a_ji
Macierz górnotrójkątna: pod główną przekątną są same zera
Macierz dolnotrójkątna: nad główną przekątną są same zera

Mnożenie macierzy = szerokość pierwszej = wysokość drugiej

Liczenie układu równań - przyjmijmy, że macierz A to macierz współczynników, natomiast A^u to macierz uzupełniona - tj. ma dodatkową kolumnę z wynikami. Układ ma rozwiązanie <=> R(A) = R(A^u). Jeśli równość nie zachodzi, to układ jest sprzeczny.

Ogólny układ rozwiązań -> normalnie podajemy parametry
Fundamentalny układ rozwiązań -> pod parametry podstawiamy 0
Szczególny układ rozwiązań -> pod parametry podstawiamy dowolną liczbę

#### Kilka pojeć wprowadzających
Idempotent - samo potęgujący się, np a \* a = a
Dzielniki zera - a i b różne od 0, ale a * b = 0
Kongruencja - gdy w zbiorze A ustalono relacje równoważności ~ i działanie wewnętrzne \* to:
Przyjmijmy, że są dwie klasy abstrakcji t i s, oraz każdy element t \* s = k sprawia, że wynik należy do konkretnej klasy abstrakcji k. Wtedy działanie \* jest kongruentne z relacja równoważności 

### Algebry binarne
Algebry binarne - jedno działanie dwuargumentowe

Grupoid - działanie wewnętrzne 
Półgrupa - działanie wewnętrzne i łączne 
Monoid - działanie wewnętrzne, łączne i istnieje element neutralny 
Grupa - działanie wewnętrzne, łączne, istnieje element neutralny i przeciwny 

Dla grupy: można skracać 
a \* b = a \* c to b = c
Oraz istnieje tylko jedno rozwiązanie 
a \* x = b

Podstruktury:
Jeśli mamy <G,\* , e> oraz <H, \* , e> oraz H należy do G, to druga grupę nazywamy podgrupa pierwszej grupy. 

### Homomorfizm
Niech będą dane 2 grupy: $<G, * , e1> i <P, +, e2>$
oraz funkcja $h: G -> P$
Jeśli $h(g1 * g2) = h(g1) + h(g2)$
oraz $h(e1) = e2$
to h nazywamy homomorfizmem grup.

Rodzaje homomorfizów:
endomorfizm - homomorfizm w siebie: P = G, \* = +
monomorfizm - 1-1 (różnowartościowe)
epimorfizm - "na", h(G) = P
izomorfizm = epi_ + mono_
automorfizm = izo_ + endo_

Grupa czwórkowa Kleina to grupa utworzona na podstawie przeksztalcania prostokata przez identyczność / symetria Ox / obrót o 180\* / symetria Oy

Z dokładnością do izomorfizmu istnieją tylko 2 grupy 4-elementowe: grupa czwórkowa Kleina oraz grupa Z4 z dodawaniem modulo 4

### Pierścienie 
Pierścieniem abstrakcyjnym nazywamy algebrę, w której istnieją 2 działania:
1. <S, +, 1> - grupa abelowa
2. <S, \*> - grupoid
.. oraz zachodzi rozdzielność + względem \*: x \* (y + z) = (x \* y) + (x \* z)

Jeśli dodatkowo \* jest przemienne (x \* y = y \* x), to pierścień nazywamy przemiennym / abelowym.

2a. Jeśli <S, \*> jest półgrupą, to algebrę nazywamy pierścieniem łącznym.
2b. Jeżeli <S, \*> jest monoidem, to algebrę nazywamy pierścieniem z jednością / pierścieniem unitarnym.

Jeśli w pierścieniu nie ma dzielników zera, to nazywamy go pierścieniem całkowitym.

Przykładem pierścienia może być pierścień wielomianów R\[x].

Ideał pierścienia:
Niech będzie dany pierścień <P, +, \* , 0> oraz zbiór A należący do P.
A nazywamy ideałem, jeśli:
1. dla każdych a, b należących do A: (a + b) należy do A
2. dla a należącego do A, c należącego do P: (a \* c) należy do A

przykład: zbiór liczb parzystych jest ideałem, ale zbiór liczb nieparzystych już nie (1 + 3 jest parzyste)

Ciałem nazywamy pieścień przemienny, w którym każdy niezerowy element jest odwracalny: przykładowo (Z, +, \*, 0, 1).

### Zasadnicze twierdzenie algebry
Każdy wielomian stopnia dodatniego o współczynnikach zespolonych ma w ciele liczb zespolonych co najmniej jeden pierwiastek.
Ciało liczb zespolonych nazywamy algebraicznie domkniętym. Co więcej, jest to najmniejsze ciało algebraicznie domknięte.

### Przestrzenie wektorowe (liniowe)
Niech będzie dane ciało K (zazwyczaj R/C/S) zwane ciałem skalarów.
Niech będzie dany niepusty zbiór V.

W zbiorze V określamy dwie funkcje:
funkcja +: V x V -> V
funkcja \* : K x V -> V

Theta - $\theta$ - to wektor zerowy.
1. <V, +, $\theta$> - grupa abelowa
2. $\forall r,s \in K, \forall v \in V$: 
2a. 1 \* v = v
2b. r \* (s \* v) = (r \* s) \* v
3. $\forall r,s \in K, \forall u,v \in V$: 
3a. (r + s) \* v = (r \* v) + (s \* v)
3b. s \* (u + v) = (s \* u) + (s \* v)

Wówczas system <V, K, +, \*, $\theta$> nazywamy przestrzenią wektorową nad ciałem K, a elementy zbioru V nazywamy wektorami.

Przykłady wektorów: wektory, macierze, wielomiany, ogólnie funkcje, ciągi skończone, ciągi nieskończone.

Własności przestrzeni wektorowej:
- 0 \* v = $\theta$
- dla każdego v (V) istnieje u (V) taki, że u \* v = $\theta$: 
   wektor przeciwny u = -v
- dla s (K), v (V): jeśli s \* v = $\theta$ to wtedy s = 0 lub v = $\theta$ 

Niech będzie dana przestrzeń wektorowa <V, +, \*> i zbiór U zawierający się w V.
Jeżeli <U, +, \*> jest również przestrzenią wektorową, to U nazywamy podprzestrzenią przestrzeni V. 

### Kombinacje liniowe
Przyjmijmy, że v1, v2, ..., vn należą do V (wektory), s1, s2, ..., sn należą do K (skalary).

V_x = (s1 \* v1) + (s2 \* v2) + ... + (sn \* vn)
V_x to kombinacja liniowa układu (v1, v2, ..., vn)

Zbiór wszystkich kombinacji liniowych układu u = (v1, v2, ..., vn) nazywamy powłoką liniową rozpiętą nad tym układem.

span(U) = powłoka liniowa rozpięta nad U

### Liniowa niezależność wektorów
Jeśli z równania (s1 \* v1) + (s2 \* v2) + ... + (sn \* vn) = $\theta$ 
wynika, że s1 = s2 = ... = sn = 0
to mówimy, że układ wektorów (v1, v2, ..., vn) jest liniowo niezależny.

Jeśli nie jest linowo niezależny, to jest liniowo zależny.

Relacja równoważności tzw. liniowa równoważność:
Układ X jest w relacji z Y (X \~ Y) <=> span(X) = span(Y)

Dzieli zbiór wszystkich układów wektorów na klasy abstrakcji. W jednej klasie abstrakcji znajdują się wektory, które rozpinają tą samą powłokę liniową.

Jeśli X \~ Y oraz X i Y są liniowo niezależne, to oznacza że są równoliczne - czyli mają tyle samo elementów. 

### Baza przestrzeni
Baza to układ wektorów B taki, że B jest liniowo niezależny i span(B) = V.

Inna definicja, równoważna:
Baza(B) - maksymalny układ wektorów liniowo niezależnych. Maksymalny, czyli dodanie dowolnego innego wektora powoduje utratę liniowej niezależności tego układu.

Liczność bazy jest stała dla przestrzeni V i nosi nazwę wymiaru. 
|B| = n, będziemy nazywać dim(V) = n.

Dla każdego wektora v (V) i dla każdej bazy b (B):
wektor v można przestawić jako liniową kombinację bazy b w sposób jednoznaczny. 
v = a1v1 + a2v2 + ... + anvn

O współczynnikach a1, a2, ..., an mówimy, że są to współrzędne wektora w danej bazie:
v = \[a1, a2, ..., an]

Baza naturalna:
e1 = \[1, 0, ..., 0]
e2 = \[0, 1, ..., 0]
...
en = \[0, 0, ..., 1]

Aby sprawdzić, czy wektory b1, b2, b3, b4 są bazą, to musimy utworzyć z nich macierz. Jeśli sa bazą, to rząd utworzonej macierzy jest równej n. 

Przykładowo: [1, 1, 0, 0], [1, 1, 1, 0], [1, 1, 1, 1], [1, 0, 0, 1]
Tworzymy macierz, każdy wektor daje nam wiersz.
```
1 1 0 0
1 1 1 0
1 1 1 1
1 0 0 1
```
Po przekształceniach wychodzi macierz jednostkowa => rząd jest równy 4 => wektory (b1, b2, b3, b4) są bazą.
Wymiar zapisujemy jako dimspan(b1, b2, b3, b4) = 4.

#### Zmiana bazy wektora v
Należy utworzyć macierz przejścia z bazy do bazy - uwaga, kolumnami!
```
1 1 1 1
1 1 1 0
0 1 1 0
0 0 1 1
```
A: E -> B

Przyjmijmy V (baza e) = [3, 4, 2, 0]
zgodnie z powyższą macierzą,
y1 + y2 + y3 + y4 = 3
y1 + y2 + y3 + 0 = 4
0 + y2 + y3 + 0 = 2
0 + 0 + y3 + y4 = 0

Więc tworzymy macierz i liczymy układ równań - można tak zmienić kilka liczb na nowa bazę jednocześnie! Możemy policzyć układ także tradycyjnie, bez wykorzystania macierzy.
finalnie:
```
1 1 1 1  3 ~ 1 0 0 0  2
1 1 1 0  4 ~ 0 1 0 0  1
0 1 1 0  2 ~ 0 0 1 0  1
0 0 1 1  0 ~ 0 0 0 1 -1
```

I zliczamy od góry, czyli V (baza B) = [2, 1, 1, -1]

#### Zmiana z bazy na bazę
x1 = \[1, 3, -2, 2]
x2 = \[2, -1, 3, -1]
x3 = \[-3, 5, -8, 4]
x4 = \[-4, 9, -13, 7]
Przyjmijmy, że mamy bazę $\alpha$ = (x1, x2) i chcemy zmienić z $\alpha$ na $\beta$ = (x3, x1).

Najpierw ustalamy współrzędne x3 i x1 w bazie $\alpha$:
x3 = \[1, -2]
x1 = \[1, 0]

Zapisujemy wektory nowej bazy w starej bazie kolumnami:
```
A =  1 1
    -2 0
```

Niezależność wektorów jest niezmienna w stosunku do bazy. Należy zbada wyznacznik w celu sprawdzenia osobliwości.
det(A) = 2 =/= 0, więc jest nieosobliwa, więc można zmienić.

Macierz A przejścia z bazy alfa do beta
A: $\alpha \rightarrow \beta$

Następnie wyznaczamy macierz odwrotną:
```
A^-1  = 0 -1/2
       -1  1/2
```

Przyjmijmy, że chcemy zmienić X.
X w normalnej bazie: \[1, 10, -9, 7]
X w bazie alfa: \[3, 1]

X w bazie beta: A^-1 \* X w bazie alfa
Uwaga, zapisujemy znowu kolumnami!
```
|0  -1/2| * |3| = |1/2|
|1   1/2|   |1|   |5/2|
```

X w bazie beta: \[1/2, 5/2]

### Przekształcenie liniowe
Niech będą dane dwie przestrzenie liniowe
<P, K, +, \*> oraz <Q, K, +, \*> określone nad tym samym K.

Odwzorowanie f: P -> Q, które przypisuje każdemu elementowi dokładnie jeden element drugiej przestrzeni nazywamy przekształceniem liniowym, jeżeli:
- f($\alpha$ \* x) = $\alpha$ \* f(x)
- f(x + y) = f(x) + f(y)

Każde przekształcenie liniowe można zapisać jako macierz.

#### Zagadnienie własne macierzy
Czy też zagadnienie własne przekształcenia liniowego:
```
2 1 1 * 2 =  2
1 2 1  -1 = -1
1 3 0  -1 = -1
```

A \* v = $\lambda$ \* v
Jak widać na powyższym przykładzie = wektor pozostał niezmieniony. Niestety nie można zawsze idealnie dobrać, stąd lambda po prawej stronie równania.

v - wektor własny
$\lambda$ - wartość własna

A \* v - $\lambda$ \* v = $\theta$
(A - $\lambda$\*E) \* v = $\theta$

E to macierz jednostkowa (jedynka przy mnożeniu)

[Tutaj jest mądrze wytłumaczone w okolicach 1:27:00](https://www.youtube.com/watch?v=6-lEeEoOjW4) ale w tempie x10, więc pomijam powód, ale:

det(A - $\lambda$\*E) = 0, to musi być macierz osobliwa
mianowicie macierz:
```
a11-lambda a12        a13
a21        a22-lambda a23
a31        a32        a33-lambda
```
Po stworzeniu równania (=0) wyjdzie wielomian zmiennej lambda, nazywamy go wielomianem charakterystycznym macierzy (a równanie nazywamy charakterystycznym).

Przykładowo dla macierzy:
```
2 1 1
1 2 1
1 3 0

2-l  1   1
 1  2-l  1
 1   3  -l

det = (l-4)(1-l)(1+l)
lambda = 4 v 1 v -1
```
Podstawiamy jakas lambde pod wyznacznik i tworzymy uklad rownan:
tutaj dla przykladu lambda = -1
```
3 1 1 | 0
1 3 1 | 0
1 3 1 | 0
```
Musi dać się później jeden wiersz skreślić, jeśli tak nie wyjdzie to znaczy, że gdzieś był błąd w obliczeniach (z własności macierzy osobliwej)
```
4  0 1 | 0
1 -1 0 | 0
```
4x + z = 0
x - y = 0

Więc wychodzi:
z = -4x
x = y

Tu mamy nieskończenie wiele rozwiązań, więc podstawiamy jakąś wartość pod parametr - np. 1 lub 0 

Dla 1 wychodzi nam x = 1, y = 1, z = -4x
Zatem wychodzi lambda = -1 oraz wektor własny = \[1, 1, -4]
