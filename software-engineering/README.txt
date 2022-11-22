---
---

Chapter 5 - System modeling 

UML DIAGRAM TYPES

&&Activity diagrams, advanced version of flow chart
Ex: Open word processor -> create file -> save file -> type document -> ...
Use case diagrams summarize the details of the system's users
Ex: 
online shopping system // box // includes 4 circles
c1. view items linked to // customer,idendity provider, auth service
c2. make purchase linked to // customer,idendity provider, auth service
...

Sequence diagrams, you know this 

Class diagrams,  you know this

State diagrams,  you know this also the thing in automata theory


CONTEXT MODELS
illustrate the operational context of a system
System boundaries belirtir gibi?? external internal gibi


INTERACTION MODELS:
Use case diagrams and sequence diagrams may be
used for interaction modeling

Use case models
ex: medical reseptions actor(stickman) -> transfer data (rls) -> patient record system(stickman)

Sequence diagrams
interaction between actors and the objects in the system

STRUCTURAL MODELS:
display organizaiton of a system in terms of the components

class diagrams:
An association is a link between classes that indicates
that there is some relationship between these classes.

Generalazition:
manage complexitiy
doctor -> hospital doctor
doctor -> general practitioner

Object class aggregation models
An aggregation model shows how classes that are
collections are composed of other classes

BEHAVIORAL MODELS:
dynamic behavior of a system it is executing
stimuli :
data:
events:

Data driven modeling
data driven models show the sequence of actions

Event driven modeling
real time systems are often event-driven
based on assumption that a system has a finite number of states

State machine models
These model the behaviour of the system in response to
external and internal events

Model driven enginerring
????





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

Security -> Layered architecture horizontal(
presentation layer Ex-> web interface, terminal interface, announcment interface
businness layer Ex-> authentaticon, form processing, session management
persistance layer Ex -> status management, search, flight management
database layer Ex-> databases?

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

Architectureal patterns structural:


Model-view-Controller(MVC) design pattern:
Model consist only the pure application data(DATA)
View present model's data to user (UI)
Controller lives between view and model it listens to event triggered by view(big brain)
Advantages: multi-developer friendly, models can have multiple views
disadvantages: more code

Example diagram 
controller link to model // state change
view link to model // state query
model link to view // change notification 
controller link to view // view selection
view link to controller // user events

Layered architecture design pattern
horizontally stacked
presentation layer, 
businness layer,
persistance layer, 
database layer
sadece komsu etkileniyor

Advantages: easy simple, Reduced dependency, testing easy, 
disadvantages of layered architecture -> result thightly coupled software components,
and monolithic applications, security become  issue if bypassing layer is allowed


Repository architecture design pattern
large amount data stored single repo
disadvantages: repostiry fails every component that depends on 
repo fails

Client-server architecture design pattern
tek bir computerda birlikte olabilir
advantages: all files stored in central location (server)
disadvantages: server is expensive to purchase and manage, network single point of failure
this type architecture's called as peer-to-peer architecture


pipe-filter architecture design pattern
sisteme verilen inputlarin cesitli fonksiyonel parametrelerle
degisik outputlara cevirmesi?
use case generally batch processing
not really good on interactive systems


APPLICATION ARCHITECTURES

Data processing applications
cok fazla verinin desteler halinde isledigin
batch processing,

Transaction processing applications
kullanicinin requestleri ile ilerleyen process

Event processing applications
enviorementten olusan eventlere gore hareket ediyorlar?

language processing systems
kullanincinin istekleri natural lang olarak veriliyor
farkli bir dilde output

ACID(Atomic, consistency, isolation, durability) database transaction

---
---