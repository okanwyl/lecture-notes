---
---
Chapter 6 - Architectureal Design

early stage of the system design process.
specificication and design process linking
involves major system components and their communcations

Architectureal abstraction 
-> architecture in the small -> indivual programs concerned
-> architecture in the large -> concerned about complex enterprise systems
that include other systems

explicit architecture (acik bir sekilde belirtilmesi?)
stakeholder ile daha iyi iletisim saglar 
system analysis -> requirementlarin karsilanabilmesi fark edilir
cart curt ne dedigi anlasilmiyor derste
large scale re-use -> tanimlanan mimari bir dizi sistemde yeniden kullanilabilir

Hangi Architectureal design non-fucntional requirementlari saglar

non functional implemantasyonlar Architectureal

Performance -> Localise critical operations and minimize
communcations. 

Security -> Layered architecture horizontal(presentation layer, 
businness layer,
persistance layer, 
database layer)

disadvantages of layered architecture -> result thightly coupled software components,
and monolithic applications, security become  issue if bypassing layer is allowed

Safety -> safety-critical small sub-systems

Availability -> Arttirmak icin o islevi yerine getiren redundant ve mekanizmalar eklenir

Maintainbility -> use replaceble components


4+1 view model 
different view models of different stakeholders
Logical view -> UML class diagram object or class
Process view -> runtime interacting process this is a concern about dynamic aspect of the
system sequence diagram modeli kullanilabilir
Development view  ->  decomposoed view of development package diagram
veya software diagram kullanilabilir
Physical view aka deployment view -> donanim yazilim processorlara nasil dagitildi olarak modellenebilir
system engineers pov'dur. physical layer and communaciton concern
use cases view -> all of them requires use case and scenarios 

Architectureal patterns:



---
---