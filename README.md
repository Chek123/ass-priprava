# Zoznam vzorov

1. Model View Controller
2. Microkernel
3. Reflection
4. Messaging
5. Message Channel
6. Message Endpoint
7. Message Translator
8. Message Router
9. Publisher - Subscriber
10. Broker
11. Client Proxy
12. Requestor Invoker
13. Client Request Handler
14. Server Request Handler
15. Reactor
16. Proactor
17. Acceptor-Connector
18. Assynchronous Completion Token
19. Explicit Interface
20. Extension Interface
21. Introspective Interface
22. Dynamic Invocation Interface
23. Proxy
24. Business Delegate
25. Facade
26. Combined Method
27. Iterator
28. Enumeration Method
29. Batch Method 
30. Encapsulated Implementation
31. Whole-Part
32. Composite
33. Master-Slave
34. Half-Object plus Protocol
35. Replicated Component Group
36. Page Controller
37. Front Controller
38. Application Controller
39. Command Processor
40. Template View
41. Transform View
42. Firewall Proxy
43. Authorization
44. Observer
45. Mediator + class diagram
46. Command + class diagram
47. Memento
48. Context Object
49. Data Transfer Object
50. Message
51. Bridge + class diagram
52. Object Adapter + class diagram
53. Chain of Responsibility
54. Interpreter + class diagram
55. Interceptor
56. Visitor + class diagram + sequence diagram
57. Decorator + class diagram
58. Execute-Around Object
59. Template Method
60. Strategy
61. Null Object
62. Wrapper Façade 
63. Objects for States
64. Abstract Factory + class diagram
65. Builder + class diagram + sequence diagram
66. Database Access Layer
67. Data Mapper
68. Row Data Gateway
69. Table Data Gateway
70. Active Record

# Štýly

## Pipes and Filters
- scenare
- implementácia
- pros & cons

## Layers
- scenare
- implementacia
- pros & cons

## Klient-server
- pros & cons

## Black Board
- implementacia
- pros & cons

## Štýly riadenia
- rozdelenie
- definicie
- obrazok


# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# .
# Odpovede
## Pipes and Filters
### scenare
- zdroj údajov tlačí údaje, filtre sú pasívne
- spotrebič údajov ťahá údaje, filtre sú pasívne
- kombinácia tlačenia a ťahania
- filtre sú aktívne, t.j. ťahajú,spracúvajú a tlačia údaje, synchronizácia dátovodom medzi nimi (vyrovnávacia pamäť)

### implementacia
1. rozdeľ úlohu systému do postupnosti spracovateľských krokov
2. definuj formát údajov pre každý dátovod
3. rozhodni o spôsobe implementácie každého spojenia
4. navrhni a implementuj filtre
5. navrhni spôsob ošetrenia chýb
6. zostav spracovateľský reťazec

### pros & cons
- pomocné súbory netreba, hoci môžu byť
- pružnosť výmenou filtrov
- pružnosť rekombináciou
- znovupoužitie filtrov
- rýchle prototypovanie spracovateľských reťazcov
- efektívnosť paralelného spracovania

## Layers

### scenare
- komunikácia zhora nadol
- komunikácia zdola nahor
- komunikácia zhora čiastočne nadol
- komunikácia zdola čiastočne nahor
- komunikácia dvoch vrstvených systémov

### implementácia
1. definuj kritérium abstrakcie
2. urči počet úrovní abstrakcie
3. pomenuj úrovne, priraď úlohy
4. zjemni členenie úrovní
5. stanov rozhrania úrovní
6. štrukturuj jednotlivé úrovne
7. urči spôsob komunikácie medzi jednotlivými úrovňami
8. navrhni spôsob ošetrenia chýb

### pros & cons
- znovupoužitie vrstiev (+)
- podporuje normalizáciu (+)
- lokalizácia závislostí (+)
- zameniteľnosť (+)
- reťazenie zmien (-)
- nižšia efektívnosť (-)
- nadbytočná práca (-)
- ťažkosť pri stanovovaní vrstiev (-)

## Klient-server
### pros & cons
- Distribúcia dát je priamočiara (+)
- Robí využívanie sieťových systémov efektívnym. Môže vyžadovať lacnejší hardvér(+)
- Jednoduché pridať nové servery alebo ich vynoviť (upgrade) (+)
- Neposkytuje model pre spoločné požívanie dát, čiže podsystémy používajú rozličné spôsoby organizovania dát. Vzájomná výmena dát môže byť neefektívna.(-)
- Nadbytočné manažovanie v každom serveri (-)
- Nejestvuje centrálny register mien a služieb – môže byť ťažké zistiť aké servery a služby sú dostupné (-)

## Black Board
### implementacia
1. definuj problém
2. definuj priestor riešenia
3. rozdeľ proces riešenia na kroky
4. navrhni špecializované podúlohy
5. navrhni štruktúru tabule
6. špecifikuj spôsob riadenia systému
7. implementuj špecializované programové podsystémy

### pros & cons
- Experimentovanie
- podpora zmien a udržovateľnosti
- znovupoužiteľné podsystémy
- odolnosť voči poruchám a robustnosť
- ťažké testovanie
- nezaručuje sa dobré riešenie
- ťažko sa stanoví riadiaca stratégia
- nízka efektívnosť
- vysoké nároky na vývoj
- nebráni, ale ani nepodporuje paralené vykonanie

## Štýly riadenia
### rozdelenie
- Centralizované riadenie (Model volanie-návrat, Model s manažérom)
- Riadenie založené na udalostiach (BroadCast, Interrupt-driven)

### definicie
- **Model volanie-návrat** (model podprogramov „zhora nadol“ kde riadenie začína na vrchu hierarchie podprogramov a pohybuje sa volaním akoby smerom dole, návratmi sa neskôr vracia späť nahor. Dá sa použiť na sekvenčné systémy)
- **Model s manažérom** (Dá sa použiť na súbežné systémy. Jeden systémový komponent ovláda zastavovanie, štartovanie a koordináciu ostatných systémových procesov. V sekvenčných systémoch sa dá implementovať pomocou príkazu case. )
- **BroadCast** ( Udalosť (informácia o nej) sa vysiela všetkým podsystémom. Ktorýkoľvek podsystém, ktorý dokáže vybaviť/ošetriť udalosť, tak môže učiniť.)
- **Interrupt-driven** ( Používa sa v systémoch reálneho času, kde sa prerušenia rozpoznajú správcom prerušení (interrupt handler) a odovzdajú sa určenému komponentu na spracovanie)

### obrazok
to sa mi uz nechce