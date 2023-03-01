# Krag_Unreal_Zadanka_Wstepne
Repo na zadania wstępne do Kręgu Unreal na KNTG Polygon

Krąg unreal - zadanie wstępu
Poniżej znajdują się zadania. Należy wybrać jedno, wykonać i wysłać mi - Swarogowi (projekt, nie build). Zadania lepiej wykonywać na Unreal 5.1
Oceniane będzie wszystko, łącznie ze sposobem pakowania projektu. Nie super rygorystycznie, można też wysłać częściowo wykonane zadanie, jeśli nie będziecie mieli pomysłu na resztę, a włożycie w to już kupę czasu. Oczywiście, im lepiej zrobicie, tym większa szansas na akceptację do Kręgu. Zwracajcie uwagę czytelność waszych rozwiązań, będę ucinał mnóstwo punktów za spagetti.
Jeśli już pracujecie, albo pracowaliście, w Unrealu, możecie mi napisać, wtedy najprawdopodobniej uda się pominąć zadanko 🙂 
Zadanie nie powinno zająć więcej niż jeden wieczór - max 4h.
Na wykonanie zadania jest tyle czasu, ile zapragniecie.
W razie pytań piszcie na discordzie - Swaróg#0001


Przy użyciu Unreala spróbuj odtworzyć prosty projekt w którym będzie zawarta następująca funkcjonalność:
spawnowanych jest 10 agentów w różnych częściach poziomu
jeden z agentów jest berkiem, pozostali są uciekający
berek goni najbliższego uciekającego
berka i uciekających da się odróżnić: kolor mesha albo jakaś czapka
uciekający przemieszczają się w miejsce najdalej od uciekającego, bądź punkt którego berek nie widzi
gra śledzi ile zaszło wymian, oraz który agent był najczęściej berkiem i na koniec gry jest to w stanie wyświetlić
gra kończy się po 10 wymianach


Bonus:
na koniec gry, agenci ustawiają się w rządku, od agenta który był berkiem najwięcej razy do tego który był nim najmniej razy, do tego, który był nim najmniej


Tipy:
[Unreal posiada system do AI oparty na drzewach behawioralnych](https://docs.unrealengine.com/5.0/en-US/behavior-trees-in-unreal-engine/)

[Unreal posiada system do sprawdzania terenu na około aktora - EQS](https://docs.unrealengine.com/4.26/en-US/InteractiveExperiences/ArtificialIntelligence/EQS)

Linki:
Behavior Trees in Unreal Engine
Environment Query System | Unreal Engine Documentation


Wykorzystując Niagarę stwórz system latających ptaków. Ptaki można zastąpić czymkolwiek latającym: motylami, dronami, samolotami itd. Dla uproszczenia będę mówił na cząsteczki “ptaki”
Ptaki powinny być rysowanie tak, aby można było rozpoznać ich kształt.
Ptaki powinny unikać kolizji ze sobą (rzadkie kolizje są ok, najlepiej jakby ich nie było w ogóle)
Ptaki powinny móc łączyć się w grupy i podążać w tym samym kierunku, zachowując poprzedni warunek
Ptaki powinny unikać kolizji z widocznymi przeszkodami.
Bonus:
Ptaki powinny machać skrzydłami podczas latania. Jeśli nie robisz ptaków, tylko jakieś inne latające obiekty, wybierz im część modelu, która będzie się ruszać podczas lotu.  (Jeśli nie znasz lekkiego rozwiązania tego problemu, możesz użyć skeletal mesha z animacją, ale nie będzie za to punktów i zabije performance systemu)
Podpowiedzi:
Zachowanie ptaków to prosty boids/flocking system
Istnieje prosty sposób na odczytanie odległości od powierzchni rysowanego static mesha dla cząstek rysowanych na GPU.


Zaimplementuj dociąganie ręki modelu postaci do przełącznika (do dowolnego punktu, do którego postać jest w stanie sięgnąć bez zginania się, ani skakania - przełącznik jest używany jako uproszczenie, pomagające wizualizacji problemu)
Dociągnięcie powinno się zaczynać jak gracz podejdzie do przełącznika i naciśnie odpowiedni przycisk
Żadne kości nie powinny wyginać się w nienaturalny sposób podczas przełączania
Ręka powinna się przyciągać możliwie blisko celu.
Bonus 1:
Po przyłożeniu ręki do przycisku, musi ona narysować podany symbol (wystarczy jeden, zawsze ten sam)
Bonus 2:
Zmodyfikuj system, aby obsługiwał dowolną liczbę kończyn
Wskazówki:
Szablon trzecioosobowy zapewnia wszystkie potrzebne assety do wykonania zadania
Unreal posiada system “dociągania” kości do wybranego punktu
Linki:
 https://docs.unrealengine.com/5.1/en-US/unreal-engine-ik-rig/


Napisz prosty system ekwipunku gracza.
Przedmioty na lvl można podnieść, co usunie je z lvl i doda do ekwipunku.
Po naciśnięciu odpowiedniego przycisku, na ekranie wyskakuje okno ekwipunku, gdzie gracz może obejrzeć wszystkie posiadane przedmioty
Takie same przedmioty powinny być reprezentowane jako jeden element w oknie ekwipunku, z zaznaczoną ich ilością 
Ekwipunek powinien móc mieć dużą pojemność - jeśli wszystkie posiadane przedmioty nie mieszczą się na ekranie, powinna być możliwość przewijania.
Gracz może wyrzucić lub usunąć przedmiot z ekwipunku (wyrzucanie oznacza usunięcie z ekwipunku i dodanie odpowiedniego obiektu na level, można to traktować jako bonus)
Bonus:
Każdy przedmiot powinien mieć wartość, wagę i typ (albo inne 3, dowolne, cechy). Dodać możliwość sortowanie ekwipunku po każdej z zaimplementowanych cech.
	Wskazówki:
Czym jest przedmiot i jak się go podnosi nie będzie punktowane, chyba że ktoś zrobi super implementację
Do trzymania wielu przedmiotów scrollbox jest niewydajny. Istnieje w Unrealu specjalny widget do takich rzeczy.
	Linki: 
https://docs.unrealengine.com/5.1/en-US/BlueprintAPI/ListView/
Googlać ListView, albo TileView
