# SWT II

## Einleitung
Softwaretechnik (engl. software engineering) ist die Lehre von der Softwarekonstruktion: der systematischen Entwicklung und Pflege von Softwaresystemen

* Anforderungsermittlung
* Spezifikationen
  * Planung, Kostenschätzung
* Entwurf
* Pflege
* Qualitätssicherung / Tests
* Prozessmanagement
  * Organisation von Firma und Abteilungen

### Brook's law
> Adding manpower to a late software project makes it later

### Boehm's 1st law
> Errors more frequent during requirements and design

### Dijkstra's law
> Testing shows the presence, not the absence of bugs

### Lehman's 1st Law
> A system that is used will be changed

### Lehman's 2nd Law
> An evolving system increases its complexity unless work is done to reduce it

### Parnas' Law
> Only what is hidden can be changed without risk

Module sollen alles verstecken (vorher nur "klein und feste API")

### Conway's law
> A system (usually) reflects the organizational structure that built it

### Law of Demeter
> Don't talk to strangers

## Software Development Processes
### Code and Fix
* badly structured code
* non-systematic improvements
* no real team work, as tasks can not be planned
* missing design and documentation
* complications in maintenance
* => Development Processes!

### Components of a Process Model
* activities
* roles
* products/artifacts
* techniques and tools

### Wasserfall
1. Planung
1. Definition
1. Entwurf
1. Implementierung
1. Test
1. Einsatz/Wartung

Problem (Frederick Brooks): Systeme nicht im voraus planbar.

### V-Model
Wasserfall + Tests für jede Phase  
<img src="Zusammenfassung/v-model.png" width=600 />

### Iterativer Prozess
* Wasserfall mit Rücksprüngen
* Inkrementell vs. evolutionär (je nach Sprungziel)

### Spiral Model
<img src="Zusammenfassung/spiral-model.png" width=600 />

### Unified Process Model (UP)
* Nutzt vorige 3 Modelle als Bausteine
* 9 Disziplinen
* <img src="Zusammenfassung/up-model.png" width=600 />
* 4 Phasen
  * Inception (Anfangsphase)
  * Elaboration (Ausarbeitung)
  * Construction (Konstruktion)
  * Transition (Übergabe)

### Rational Unified Process
* Konkrete Implementierung von UP bzgl.
  * Roles
  * Activities/Tasks
  * Artifacts
* 6 best practices
  * Entwickle iterativ
  * Nutze Anforderungsmanagement
  * Component-based Architecture
  * Modelliere visuell
  * Stell Qualität sicher
  * Kontrolliere Änderungen
* Sehr komplex

## Agile Development
### Motivation
Probleme traditionell:
* Design im Vorfeld
* Unflexibel
* Zu viele Artefakte (Noise)

#### Manifest
|Agil|Sonst|
|---|
|Individuals/Interactions|Processes/Tools|
|Working Software|Comprehensive Docs|
|Customer Collaboration|Contract Negotiation|
|Responding to change|Following a Plan|

### XP
<img src="Zusammenfassung/xp-components.png" width=500 />  
<img src="Zusammenfassung/xp-process.png" width=600 />  
Nachteile:
* Kann nicht wiederholt werden
* Keine Docs
* Kunde muss mitarbeiten
* Praktiken teils nicht empirisch belegt:
  * Pair Programming
* Schwer zu lernen
* Qualität wirklich besser?

### Scrum
"Agiles Framework"
* 3 Rollen
  * Product owner
    * represents the customer's interest
    * helps team to clarify questions (and quickly)
    * is responsible for the Team working on the right features
    * changes features and priorities before each sprint (if required)
    * accepts / declines the results
    * release management
    * return on investment (ROI) management
  * Scrum Master
    * removes impediments, buffers conflicts
    * secures that the Team can work productively
    * supports the communication between all stakeholders
    * protects the Team from outside world
    * secures the commitment to Scrum principles and values
  * Team member
    * estimates and commits itself to deliver the features
    * clarifies the sprint goal with the Product Owner and commits itself to it
    * supports the product owner in coarse-grained estimation of Product
    * Backlog items
* 4 Zeremonien
  * Sprint Planning Meeting
  * Daily Scrum
  * Sprint Review Meeting
  * Retrospective Meeting
* 3 Artefakte
  * Product Backlog
    * A high-level collection of all features, etc. prioritized by business value
    * A living document that can be changed any time
    * Priorisierte Feature List/User Stories
  * Sprint Backlog
    * Priorisierte Burn-down Chart (TODO, IN PROGESS, FINISHED)
    * updated on a daily basis
  * Product Increment
* 3 Planungstypen:
  * Release-Planung, basierend auf Product Backlog
  * Sprint-Planung
    * Each activity must not take longer than roughly 16 hours
    * Only add activities as long as 85% of the net capacity of the team is not reached
  * Arbeitstag-Planung
* 30-Tage Iterationen
* Chicken roles:
  * Kunden
  * Manager

### Allgemeine Tipps
#### Große Projekte
* Brook's Law -> Späte Neuankömmlinge verringern Geschwindigkeit
* Klein Anfangen, natürlich wachsen (Teams splitten und Neulinge einführen)
* Minimiere Abhängigkeiten zwischen Teams
* "Scrum of Scrums": Daily Scrum mit Repräsentanten der Teams

#### Verteilte Projekte
* Am besten vermeiden
* Scrum Master nicht von Team trennen
* Am Anfang zusammen, danach erst Trennen
* Teams mischen von Zeit zu Zeit

### Zusammenfassung
* No Silver Bullet
* Architektur/Design und Dokumentation schwach

## Requirements Engineering
Probleme:
* Requirements are missing
* Requirements are wrong or misunderstood
* Stakeholders are not involved

Probleme später beheben teurer: Faktor 10x pro Entwicklungsphase

### Definition Requirement
1. Zustand oder Fähigkeit, die ein Nutzer braucht, um ein Problem zu lösen/Ziel zu erreichen (*needed*)
1. Zustand oder Fähigkeit, die ein System braucht, um Vertrag, Standard, Spec oder andere Verträge zu erfüllen
1. ein Dokument, das 1. oder 2. festhält

Eigenschaften:
* Konsistent
* Eindeutig
* Verständlich
* Vollständig
* Passend / adequat
* Verifizierbar
* Umfang passt zum Risiko

Typen:
* Funktional
* Qualitativ
* Einschränkungen

### Prozess
* Gewinnung
* Dokumentation
* Übereinstimmung
* Validieren und verwalten

### Definition Stakeholder
* Person oder Organisation, die direkt oder indirekt die System-Requirements beeinflussen
  * Nutzer
  * Betreiber
  * Käufer/Sponsor/Auftraggeber
  * Devs oder SW-Architekten
  * Tester
* Müssen sehr genau identifiziert werden

### Definition Requirements Engineer
* Vermittler zwischen Benutzern und Devs
* Muss ein Diplomat sein (Empathie, kommunikativ, konfliktlösend...)

### Requirement-Gewinnung
* Befragungstechniken
  * Interview
  * Fragebogen
  * On-Site Kunde
* Kreative Techniken
  * Brainstorming
  * Perspektivwechsel
  * Analogie
* Retrospektive Techniken
  * System-Archeologie
  * Wiederbenutzung
  * Konkurrenzprodukte
* Beobachtende Techniken
  * Feldbeobachtung
  * Anlernen
* Unterstützende und andere Techniken
  * Mind Maps
  * Workshops
  * Audio/Video Aufzeichnung
  * Use-Case Modellierung
  * User Stories
  * Personas
  * Prototypen

### Requirement Klassifikation
#### Concerns: Funktionale vs. nicht-funktionale Requirements
<img src="Zusammenfassung/concern-table.png" width=600 />  
<img src="Zusammenfassung/requirement-types-tree.png" width=400 />  
<img src="Zusammenfassung/requirement-class-facets.png" width=400 />  

|Form|Definition|Type of verification|
|---|
|Operational|Spec of operations or data|Review, test, formal verification|
|Quantitative|Spec of measurable qualities|Measurement|
|Qualitative|Spec of goals|Not directly possible: Stakeholder judgement or derived metrics|
|Declarative|Description of required feature|Review|

Achtung: Beachte Concerns wie in Baum-Grafik um Funktional/Nichtfunktional zu unterscheiden

#### Tips zum Schreiben
* Kurz, 1 Requirement pro Satz
* Kein passiv: Klar, wer was macht
* Schwache Wörter vermeiden (sollte, könnte...)
* Glossar
* Satztemplates

### Gewinnung
* Feature List
* User Stories
* Use cases

### Requirement Validation
> Am I building the right system?

VS.
> Am I building the system right (=> Verification)

* Inspections, Reviews, Walkthroughs
* Simulation
* Prototypen
* System Test Cases
* Model Checking (Formal?)

<img src="Zusammenfassung/re-costs.png" width=300 />

## Modellbasierte Anforderungsermittlung
* Grafiken werden nebenher erstellt

### Blackbox-User Use Cases
* Systemgrenze / Scope
* System-Kontext
  * Relevante Umgebungsdetails
* Context-Grenze
  * Ab wo wird die Umgebung/Außenwelt irrelevant

### Scopes
* Business
* System
* Komponente

Unterscheidung nach black- und whitebox

### Elementary Business Process
Zusammengesetzt aus:
* Aufgabe
* Person (ausführend)
* Zeit und Ort
* Motiviert durch Geschäftsereignis
* Welches messbaren Geschäftswert hat
* und Daten konsistent belässt

### Bewertung von User Goal Usecases
1. Boss Test
  * Wie glücklich wäre Chef mit was ganzen Tag gemacht wurde?
1. Kaffeepausen-Test
  * Wann könnte man etwas für eine Kaffeepause unterbrechen?

### Usecase-Ebenen
* Zusammenfassung (Summary)
* User Goal (= EBP)
* Subfunktion

<img src="Zusammenfassung/use-case-diagram.png" width=500 />  
`SUD`: System under Discussion

* Stakeholder
* Actor: Person außerhalb des Systems
* Primary Actor: Initiiert die Interaktion
* Use Case Model: Menge aller Use-Cases und Diagramme


### Vorgehen:
1. Systemgrenze auswählen
1. Akteure bestimmen
1. Ziele der Akteure bestimmen
1. Usecases bestimmen, die Akteure befriedigen

Tipps: 
* Keine UI-Elemente in Usecases, 
* Präzision:
  1. Datenfeldname
  1. Name und Feldtyp
  1. Name, Typ und Validierung

### Iterative Verfeinerung
* Breite zuerst
* Zerteilen, Vereinigen

### Fully dressed
1. Preface
  * Scope
  * Level
  * Primary Actor
1. Stakeholders und Interessen
1. Vorbedingungen
1. Nachbedingungen
1. Erfolgsscenario
1. Erweiterungen/Alternative Vorgehen
1. Sonderanforderungen
  * z.B. Touchscreen, i18n...
1. Technologie- und Datenvariationen

Außerdem in den Folien: Dokumentstruktur

### Anforderungs-Management
* Zentrales Repo
* Requirements verknüpfen
* Taggen für bessere Durchsuchbarkeit

=> Tolle Spezialtools

## Model driven Development
* Goals
  * better platform independence and interoperability
  * increased development speed with code generation
  * better software quality through working and analysing models
  * reuse MDSD infrastructure in SPL
  * optimized separation of concerns using different models (views)
  * better maintainability as redundancy avoided & technological change managed
  * manage complexity through abstraction
* Expected benefits
  * cost reduction
  * shorter time-to-market
  * variability through the use of software product lines
  * use of domain knowledge in models

Hier fehlt Zeug, weil VL MDSD besucht wurde...

### CIM, PIM, PSM
* Computation independent models
  * requirements for the system and its environment
* Platform Independent Models
* Platform Specific Models

=> Wird immer spezifischer / beinhaltet mehr Plattform-Details

### Weitere Themen
* UML 2.0 4-Ebenen Hierarchie
* Domain Specific Languages
* Transformationen
  * Model-2-Text
  * Model-2-Model
  * QVT

### Tools
* Eclipse Modeling Framework
  * EMOF -> Ecore
* OCL
* XText
  * Xtend als Generator-Engine (Model-2-Text)
  
## Analyse
Analysis
* Emphasises an investigation of the problem and requirements
* Rather than a solution
* Do the right thing
* E.g. requirements analysis (investigation of the requirements)
* E.g. object-oriented analysis (investigation of the domain objects)

Design
* Emphasises a conceptual solution (in software and hardware )
* Rather than its implementation
* Do the thing right
* E.g. object-oriented design (designing the software objects)
* E.g. database design (designing the database schema)

### System Sequence Diagrams
* System Boundary wieder wichtig
* System Events: external events that directly stimulate the software system
* System Operations: operations that the system as a black box offers
  * Definieren gemeinsam `public system interface`
* Descr:
  * List events to be handled by system
  * Define system interface as starting point for design

<img src="Zusammenfassung/system-diagram.png" width=600 />

### Operation Contracts
* Beschreiben Systemoperationen im Detail
* Schema:
  * <img src="Zusammenfassung/op-contract.png" width=400 />
  * Postconditions:
    * Instanziierung und Loeschung
    * Auf- und abgebaute Beziehungen/Verbindungen
    * Attributveraenderungen
    * Bzgl. Domain-Model Objekte
    * Deklarativ
    * Past-tense
    * Komische Theater-Metapher
* Contracts vs. Use Cases: Use Cases sind sehr wichtig, aber Contracts koennen mit post-conditions mehr Komplexitaet beherrschen
* Vorgehen:
  * System Operationen identifizieren 
  * Fuer solche, die komplex und subtil sind, mache Contract
  * Schreibe Post-Conditions wie oben beschrieben
* Descr:
  * If required state change of domain model is complex
  * More precise than trying to express this in use cases
  * Helps to uncover additional domain model attributes
  * Also useful for unexperienced team members

<img src="Zusammenfassung/up-artifacts.png" width=600 />

## Architektur
Problemstellungen:
* Wie wird dokumentiert?
* Was muss eingekauft werden?
* Wie wird mit bestehender Software umgegangen? (Einbindung, Anbindung)
* Wie wird mit bestehenden Daten umgegangen?
* Wie passt die SW in das Portfolio?
* Was wird wiederbenutzt?
* Was soll wiederbenutzbar werden?
* Ist eine Produktlinie angemessen fuer eine Plattform?

### Definition
* Ergebnis von Design-Entscheidungen
* Beinhaltet die Systemstruktur
  * Komponenten
  * Beziehungen
  * Abbildung auf Ausfuehrungsumgebung
  
### Vorteile explizite Architektur
* Stakeholder communication
* System analysis
* Large-scale reuse
* Project Planning

Ausserdem:
* come to a common vision

### Structures, Views, and View Points
* View:
  * Architekturelemente und Relationen
  * Geschrieben und gelesen von Stakeholdern
  * SW Architelktur Dokumentation
* Structure:
  * SW-Elemente, die als SW oder HW existieren
  * = SW Architektur
* Viewpoint:
  * Gruppen von Views je nach Concern

=> SW-Architektur immer vorhanden, aber nicht immer dokumentiert und up-to-date

#### Views nach Kruchten
* Logical view
  * Funktionalitaet fuer Endnutzer
  * Class diagram, Communication diagram, Sequence diagram
* Development view (implementation view)
  * Programmierer-Perspektive
  * UML Component diagram, Package diagram, andere UML Diagramme
* Process view
  * runtime behaviour of the system
  * concurrency, distribution, integrators, performance, and scalability
  * Aktivitaetsdiagramm
* Physical view (deployment view)
  * system engineer's point of view
  * topology of software components on physical layer + connections
  * Deployment diagram
* Scenarios (use case view)
  * small set of use cases or scenarios
  * identify architectural elements
  * illustrate and validate the architecture design
  * starting point for tests of an architecture prototype

#### Views aus UP
* Logical
* Process
* Deployment
* Data
* Security
* Implementation
* Development
* Use Case

#### Palladio View-Points
* Structural: Statische Eigenschaften des Systems
  * `repository` view Type
  * `assembly` view Type
* Behavioral: Funktionale und extrafunktionale Systemsemantik, User behavior
  * Sequenzdiagramme
  * SEFF (?)
  * Usage models
* Deployment:
  * `allocation`
  * `environment`
  * `resource environment`

### Entscheidungen dokumentieren
* Vor allem WARUM eine Entscheidung getroffen wurde

### Einfluesse auf die Architektur
* Anforderungen
  * **Quality Requirements** wie z.B.
    * Performance
    * Security
    * Safety
    * Availability
    * Maintainability
    * Scalability
  * Koennen gegengerichtet sein: Balance!
* Wiederverwendbarkeit
  * Komponenten
  * Pattern
  * Architectural Pattern: crosses the boundaries of architectural elements (Domain Model, MVC)
    * domain/business logic
    * data sources and O/R mapping
    * (web) presentation and session handling
    * distribution and concurrency
  * Architectural Style (z.B. OO, modular)
    * eases system understanding, maintenance and evolution
    * Kommunikation (Service-Orientiert)
    * Struktur (OOP)
    * Deployment (z.B. Client/Server)
  * Reference Architecture
    * derived from a study of the application domain
* Organisation (Conway's law)

### The Logical Architecture
* large-scale organization of classes into packages and subsystems
* Haeufig in Ebenen unterteilt

### Architektur-Zeugs
#### Prinzipien
* Separation of concerns
* Single Reponsibility
* Information Hiding
* Priciple of least knowledge (don't talk to strangers)
* Don't repeat yourself
* Minimize upfront design

#### Layered (Reference) Architecture
Benefits:
* reduces "accidental" complexity
* improves modifiability
* clear separation of concerns
* independent exchangeability
* compatible to SOAs
* simplified testing

Drawbacks:
* usually increases the amount of classes
* through facades or data transfer objects
* however, these are patterns in their own right that help to better deal with complexity

Ebenen:
* UI (View)
* Application (Controller)
* Domain (Model)
  * Buendelt Applikations-spezifisches => Macht den Rest universeller
* Business Infrastructure
* Technical services
* Foundation

#### Package Diagrams
#### Facades
* Viele Klassen in einem Paket/Ebene durch gemeinsames Interface buendeln/zentral organisieren

#### Observer

## Software Components (Component Based Software Engineering CBSE)
Definition:
* unit of composition
* contractually specified interfaces
* explicit context dependencies
* can be deployed independently
* subject to composition by third parties
* without understanding its internals

Warum sind Objekte keine Components?  
**=> Inheritance**

### Component Model
Wie mappt man das Componenten-Prinzip auf eine Programmiersprache?
* Was ist eine Komponente?
* Wie werden Dienste angeboten?
* Wie werden Componenten verknuepft/zusammengesetzt?
* Wie kommunizieren Componenten?
* Wie werden Componenten aufgefunden/gelistet?

Wichtige Teile:
* Plattform
* Framework
* Hilfswerkzeuge
* Repository
* Componenten

### Bestehende Standards
* CORBA, CCM, OMA, Java, JavaBeans, EJB, COM, OLE/ActiveX, COM+, .NET CLR
* Aehnlich: Late binding, encapsulation, interface inheritance
* Unterschiedlich: Memory management, evolution and versioning, ...

### OSGi (Open Service Gateway Initiative)
* basically JAR files defining a public interface via a manifest
* consumer bundles need to explicitly require services
* Eclipse integration

### Web Services
* self-contained (has api, hides information)
* self-describing (machine readable description)
* modular (composable to higher-level functionality)
* published (registered in registry)
* located (has global unique location)
* invoked (can be used using standard internet protocol)

#### Service-Oriented Architecture (SOA)
* 3 Rollen
  * service requestor
  * service provider
  * service broker (repository)
  
<img src="Zusammenfassung/soa.png" width=300 />

#### Core Web Service Technologies
* Simple Object Access Protocol `SOAP`
* Web Service Description Language `WSDL`
* Universal Description, Discovery and Integration `UDDI`

### Research-based Component Models
* SOFA
* ROBOCOP
* KobrA
* Palladio
  * performance prediction at design time
  * support of CBSE role model
  * mapping to EJB possible

#### Palladio Component Model (PCM)
* DSL
* early performance predictions
  * Alle Einfluesse werden explizit aufgefuehrt (Hardware, Nutzerzahl, Perf. von externen Abhaengigkeiten)
* Ganz dolle component-orientiert

### Palladio
* Designed to support independent developer roles

Modellierung ist wichtig fuer 
* Erweiterung von bestehenden Systemen
* Performance Predictions
* Analyse von Systemeigenschaften
* Simulation

<img src="Zusammenfassung/palladio-views.png" width=600 />

Input:
* Usage
* Hardware
* External Dependencies
* Code

Output:
* Antwortzeit
* Durchsatz
* Resourcenausnutzung

#### Service Effect Specification (SEFF)
* Beschreibt nach aussen sichtbare Aktionen eines Komponenten-Dienstes
* Abstraktion des internen Verhaltens
* Beschreibt Relation zwischen angebotenen und angeforderten Koponenten
* Kann parametrisiert werden (nachtraegliches Variablenaendern)

#### Parametrisierung von
* Resourcen Umgebung
* Nutzungsverhalten

#### Aufgaben von Componenten-Entwicklern
PCM:
* Specifies components & interfaces
* Specifies data types
* Builds composite components
* Creates parameterised service effect specifications
* Stores modelling & implementation artefacts in repositories

Allgemein:
* Implements components
* Tests components
* Maintains components

#### System-Modell
* Benutzt Componenten von verschiedenen Repos
* Bietet eine Nutzerschnittstelle
* Verbindet und vereinfacht Dienste (z.B. durch weglassen)
* Ist Vorbedingung fuer den System-Deployer

#### Aufgaben von Software Architekten
* Spezifiziert die Architektur anhand von bestehenden Componenten/Schnittstellen
* Spezifiziert neue Componenten/Schnittstellen
* Benutzt Styles und Patterns
* Analysiert die Spezifikation und macht Design-Entscheidungen
* Macht Performance-Prediction
* Delegiert Implementierungsarbeit an Entwickler
* Leitet den Entwicklungsprozess

#### System Deployer
Resourcenbeschreibung:
* CPU, Netzwerk, HDD, RAM

Aufgaben:
* Modelliert die Resourcenumgebung
* Setzt sie auf
* Modelliert Allokation von Componenten auf Umgebung
* Deployt Componenten
* Pflegt das laufende System

#### Nutzungsmodell -> Domaenenexperte
* Models user behaviour (z.B. Anzahl)

#### Abhaengigkeiten aufloesen
<img src="Zusammenfassung/pcm-jobs.png" width=600 />

<img src="Zusammenfassung/cbse-process.png" width=600 />

## Enterprise Application Architecture
Enterprise:
* software that supports businesses
* mainly about display, manipulation, storage of data
  * Persistent data
  * Large amount of data
  * Gleichzeitiger Datenzugriff
  * Verschiedene Anzeige-Bildschirme
  * An andere Systeme angebunden
  * "Conceptual dissonance" - Versdchiedenes Verstaendnis fuer gleiche Terme
  * Business "illogic"

Business Information Systems:
* support of business processes
* process business transactions and data

Beispiele:
* Web shop
  * Scalability, Performance
* Leasing Management System
  * Complexity, Maintainability
* Expense Tracking
  * Time to Market, Extensibility

### Ebenen der EA
* Presentation (front-end)
* Domain (Middle, Business)
* Data Source

### Domain Logic Patterns
#### Transaction Script
* Eigene Prozedur fuer jede Art von Request/Transaktion

#### Domain Model
Mischt Daten und Verhalten in einem OO-Modell

Advantages
* Better organizes complex domain logic

Problems
* Steeper learning curve if not familiar with OO
* Mapping to data source more complex

#### Table Module
Ein Modul (ein Objekt), dass alle Daten einer Tabelle verwaltet

Advantages
* Straightforward mapping to data
* Separates logic for different concepts
* Useful if used technology supports it (COM, .NET)

Problems
* No object instances: can be bad for complex logic

### Data Source Architecture
Wie bekommt man die Datenbank mit dem (OO-) Code kombiniert?

#### Record set (JDBC ResultSet)
* "in-memory representation of tabular data"
* Data Transaction Object (`DTO`)

Strongly typed record sets

#### Table Data Gateway
Gateway: "An object that encapsulates access to an external system or resource"

#### Active Record
* "wraps one row in a database table or view, encapsulates the database access, and adds domain logic on that data"
* OO: Bringt Daten und Funktionalitaet zusammen
* "Active Record is a domain model object in which the classes match the database schema very closely"

Probleme:
* Vererbung
* Objekt-Relationen

#### Row Data Gateway
* Wie Active Record, aber Duplikaten werden mittels Identity Map verhindert
* Code-Gen moeglich (attraktiv)
* Nachteil: Bis zu 3 Datenrepraesentationen: Domain Model + Row Data Gateway + DB

#### Data Mapper
> moves data between objects and database while keeping them independent of each other

* Herausforderung: Aggregationen und Vererbung mit relationalen DBs
  * => Object Schema + DB Schema
* Metadaten-Mapping (z.B. Annotationen) statt explizitem Code
* Nicht selber bauen

<img src="Zusammenfassung/domain-data-summary.png" width=500 />

### Object-Relational structural Patterns
#### Single Table Inheritance
Pros
* simple database schema: only one table
* no joins required
* refactoring that moves fields up or down does not require database changes

Cons
* direct use of tables can be confusing because of unused fields
* tables can get very large
* many indexes & frequent locking => loss of performance
  * solution: introduce additional index tables
* only one namespace for all fields exists (Konventionen: z.B. CLASSNAME_FIELDNAME)

#### Class Table Inheritance
Pros
* all columns are relevant for every row
  * tables are easier to understand
  * tables do not waste space
* easier to map a legacy, pre-existing schema using this strategy
* straightforward relationship between domain model and database schema

Cons
* loading an object in most cases means touching multiple tables
  * Joining multiple tables, multiple queries => Performance decreases
* refactoring: Moving fields up and down in the hierarchy implies changing the database schema
* supertypes can become bottlenecks
  * has to be accessed frequently
* high normalisation makes schema harder to understand

#### Concrete Table Inheritance
Nur nicht-abstrakte Klassen bekommen eigene Tabelle

Pros
* each table is self-contained; no irrelevant fields
  * useful, if applications directly access the database
* no joins required when reading from concrete mappers
  * concrete subclasses
* only local access to tables can increase performance
  * Each table is usually accessed by one domain object only

Cons
* refactoring: Pushing fields up / down required database schema changes
* changes of field of supertypes influence all subtype tables
* a find on the superclass forces to check all subclasses (subtables) or a complex join

<img src="Zusammenfassung/table-inheritance-summary.png" width=500 />

## Software Design
* Wie wird Funktionalitaet auf Objekte gemappt?

### Responsibility Driven Design
* Echtwelt-Aufgaben auf die modellierten Instanzen uebertragen
* `doing` vs. `knowing` Responsibilities

Vorgehen:
* Beginne mit Operation Contracts um Objektinteraktionen zu bestimmen

### Agile Modeling
* Whiteboard

### Dynamic Design Model
* Interaction diagrams
* Kombiniere system operations/contracts + domain model + architectural guidelines

#### Design Class Diagram
* Typen von SW klassifizierbar
* specifications for software classes and interfaces in an application
* Beinhaltet
  * classes, associations and attributes
  * interfaces with their operations and constants
  * methods
  * attribute type information
  * navigability
  * dependencies

Vorgehen:
1. Teilnehmende Klasen identifizieren
1. Klassendiagramm malen
1. Adding Method Names
  * Durch analyse des Interaktionsdiagramms
  * Bennenung:
    * Create Operation?
    * Accessor/Mutator?
    * Collections?
    * Avoid Language-dependent Syntax
    
### Static Design Model

### General Responsibility Assignment Software Patterns (GRASP)
* (Information) Expert
  * Look for the object that has the information to do something
  * Wenn existent: Zuerst betrachten
  * Danach: Bestehendes erweitern
  * Sonst: Pure Fabrication oder Controller
* Creator: Choose an object C, such that –
  * C contains or aggregates X  
     i.e. X is a part of C
  * C closely uses X  
     i.e. C calls a lot of operations of X
  * C has the initializing data for X
* Controller
  * Behandelt System Event Nachrichten
  * Implementierung: Subsystem Facade oder pro Usecase 
* Low Coupling + High Cohesion
  * Verringere den Effekt, den Aenderungen auf System haben
  * High Coupling: Viele interagierende Klassen
  * Low Cohesion: Klasse macht viel zusammenhangsloses
* Polymorphism
  * Alternativen auf Typen basierend auswaehlen
  * ABER: Composition ueber Vererbung!(Verebung = whitebox)
* Pure Fabrication
  * Sich etwas kuenstlich aus den Fingern saugen, um fehlenden Verantwortlichen zu erschaffen
* Indirection
  * Wenn eine weitere Responsibility bei einem Expert zu Low Cohesion fuehrt, baue Mediator-Objekt ein
* Protected Variations (open/closed principle)
  * Basierend auf Parna's Law
  * information hiding
  * Polymorphismus
  * Interfaces
  * Law of Demeter: Don't talk to strangers
  * service lookup
  * use of reflection
  * use of standards such as SQL

## Clean Code
* elegant and efficient
* straightforward logic
* minimal dependencies
* does one thing well
* simple and direct
* reads like well-written prose
* never obscures the designer‘s intent
* easily enhancible by others
* code that has been taken care of

### Object-Oriented Design

### SOLID Principles
* Single Responsibility
* Open Closed
  * open for extension, but closed for modification
* Liskov Substitution Principle
  * Man muss mit abgeleiteten Klassen-Instanzen genauso gut klarkommen wie mit den original Super-Klassen
  * Verwandt: Design by Contract
* Interface Segregation
  * Clients should not be forced to depend upon interfaces that they do not use
* Dependency Inversion
  * "Don't call us, we call you" (Observer Pattern)
  * Oder allgemeiner: Nicht direkt Referenzieren, sondern Interface bereitstellen, um den Referenzierten zu abstrahieren
* Command-Query-Separation
  * Basic Bsp.: Getter und Setter
* Law of Demeter: Clean Apis, keine Innereien
* Boy Scout Rule
  * "Leave the campground cleaner than you found it"
  * Nicht am Code rumhacken, sondern clean erweitern
* Principle Of Least Surprise
  * Keine unerwarteten Seiteneffekte

### Code Conventions
* Naming
* Commenting
  * Erklaerend
  * Warnend
  * Informativ (z.B. TODO)
* Auskommentierten Code direkt loeschen (Version Control)
* Formatting

### Don't Repeat Yourself
### Keep It Simple, Stupid (KISS)
### You Ain't Gonna Need It (YAGNI)
* Nichts Programmieren, was nicht in absehbarer Zeit notwendig ist
* Featurism

### Single Level of Abstraction (SLA)
* z.B.: Nicht in selber Methode wild zwischen Assembly und Dependency-Injection wechseln

## Real-time Development & Patterns
* Resultat nur korrekt, wenn funktionale und zeitliche Anforderungen eingehalten werden

Soft vs Hard real-time
* Soft: Degraded wenn nicht in korrekter Zeit
* Hard: Inkorrekt wenn nicht in korrekter Zeit

=> Definiert durch
* possible stimuli
* expected responses
* timing constraints

* Interrupts vs. Periodische Prozesse
* Monitoring Systems vs. Control Systems vs. Data Acquisition Systems
* Sensor-Aktuator Schema

### RT-OS
Benoetigt
* real-time clock
* interrupt handler
* scheduler
* resource manager
* dispatcher

Prozessmanagement:
* Interrupt level priority: Wer zuerst auf Event reagieren soll
* Clock level priority: Wer die meiste Rechenzeit bekommt

### Scheduling Strategien
Grobe Kategorisierungen:
* static vs dynamic
* non-preemptive vs pre-emptive
* mit/ohne statische/dynamische Priorities

Strategien:
* FIFO
* Fixed Priorities
* Earliest-Deadline First (EDF)
* Least-Laxity-First (LLF)
  * Laxity = deadline - now - remaining required CPU-time
* Time Slice Scheduling

### JamaicaVM: Real-Time JVM
Java Probleme:
* Indeterministisches Thread starting
* garbage collection
* JIT
* Sandboxing der Hardware

### System Design
* hardware software co-design
* simulation and prototyping

Prozess:
* Stimuli identifizieren
* Timing constraints
* Plattform waehlen
* Concurrent Processes
* Stimulus Processing entwerfen (State machines)
* Scheduling System entwerfen

### Thread vs. Process
* Hier gleichbedeutend benutzt
* Arrival Pattern: Periodisch/Aperiodisch
* Ausfuehrungszeit: Worst case oder average

#### Kommunikation
* Shared Memory
  * hat Konistenzprobleme
* Messageing
  * Blocking vs. non-blocking send
  * Sync/Async receive

#### Petrinetze

### Dependability
* Verfuegbarkeit
* Verlaesslichkeit
* Versagens-Sicherheit
* Angreifer-Sicherheit

Fehlerstufen
* Fault
  * defect in a system
  * Systematic vs. Random
  * Random: Transient (einfach nochmal probieren) vs. Persistent (Eingreifen noetig)
* Error
  * discrepancy between the intended behaviour of a system and its actual behaviour inside the system boundary
* Failure
  * displays behaviour that is contrary to its specification

* Mit oder ohne Fail-Safe State

#### Protected Single Channel
* Mit Data Validation  Unit koennen Fehler erkannt werden

#### Homogenous Redundancy (Switch to Backup)
* Faellt ein Channel aus, wird der andere benutzt

#### Triple Modular Redundancy
* Comparator der nach der Mehrheit entscheidet

#### Heterogeneous Redundancy
* independent design and implementation of versions

#### Monitor-Actuator
* Actuator Monitor Sensor um Aktuator-Zustand mit gegebenem Befehl zu vergleichen

#### Sanity Check
* Wie Monitor-Actuator, plus Ueberpruefung, ob Systemzustand sinnvoll

#### Watchdog
* Heartbeats von verschiedenen Komponenten

#### Safety Executive Pattern
* Watchdog + Safety-Coordinator + Safety-Measures + Saefety-Policy
* Optional: Fail-Safe Processing CHannel

## Testing
* Nach uebergabe durchschnittl. 3 bugs per 1000 LOC
* ~50% haben noch nichttriviale Fehler
* 7% von Fixes bringen neue Bugs
* Reliability = probability of failure-free operation
* Probability of failure on demand (`POFOD`)
* Rate of occurrence of failures (`ROCOF`)
* Mean time between failures (`MTBF`)
* Mission time: Zeit, in der System bereit fuer Eingaben sein sollte
* Availability = (MTBF/(MTBF+MTTR)

### Typen von Tests
* Functional testing
* Coverage testing
* Random testing
* Partition testing
* Statistical testing

### Testing is Sampling
Test-Modell
* Model for the expected operational use
* Test environment that simulates the operational environment
* Protocol for analysing the test data

```
R = (n - k) / n    // Sampling reliability
p = 1 - n-th-root(1 - beta) = 1 - R
```

* `k` Fehler in `n` Wiederholungen = `(n ueber k) R^(n-k) (1-R)^k` (Binomialverteilung)
* Konfidenz: Abstand zwischen 1 und 10 erfolgreichen Tests

### Voraussetzungen fuer statistische Tests
* Tests generated according to a probabilistic model
* any test run is statistically independent
* Outcome des Tests muss klar als "korrekt" oder "Fehlschlag" feststellbar sein

### Statistical Usage Model
* Markov-Kette

## Software Security
Goals
* Confidentiality
* Availability and integrity
* User authentication
* Traceability & auditing
* Monitoring
* Anonymity

Attacks
* network sniffers and proxies
* viruses and worms, Trojan horses, hacked download
* rootkits, port scanner
* insider attacks
* theft
* burglary
* social engineering attacks

### Formulating Security Requirements
* identify what needs to be protected
* Generische Aussagen vermeiden ("es muss sicher sein")

### Design
* Misuse Cases
* Konfligiert mit anderen Anforderungen

### Prinzipien
* Secure the weakest link
* Practice defence in depth: Mehrere Sicherheitsmassnahmen hintereinander
* Fail Securly
* Secure Default
* Least Privilege
* No Security by Obscurity
* Minimize Attack Surface
* Privileged Core
* Input Validation und Output Encoding
* Don't Mix Data and Code

### Pattern
* Federated Identity Management (LDAP)
* Falls doch passwoerter: Stark! Salted! Nicht be CLient validieren!
* Session handling bei Webapps

### Implementierung:
* Sich gut um kritischen Code kuemmern (dokumentieren, hohe Awareness, sicher Coden)

### Security Testing
* Focus on identified risks
* Code coverage metric
* Code and system reviews
* Evaluate security in each phase resp. iteration
* Various sources for test cases
* Standard security testing environment to check basics (Port Scanner etc)
* Security experts check your system as black box or white box
* Fehlerdatenbanken fuer Dependencies ueberwachen
* Fuzzing

### Issues
* Race Conditions
  * Z.B. Abfrage, ob Partner abgesichert, dann schnell "entsichern", ungesichert arbeiten
* Buffer Overflows
  * Stack
  * Heap
* SQL Injection

### Kryptografie
* Confidentiality
* Integrity
* Authenticity
* Non-repudiability

### Pseudo Randomness
* cryptographically secure: Naechste Zahl nicht in polynomieller Zeit erratbar
* Sehr gute Seeds verwenden

## CI
Probleme ohne CI:
* Software defects can pile up due to conflicting changes
* Large overhead, worst case: Roll back large set of changes
* Magical Machine: "It works on my machine!"

Def:
> team integrate their work frequently. Verified by automated build

### Prozess
Manual
1. Change code/development artefacts
1. Test locally
1. Commit change

Automated
1. Materialisation of dependencies
1. Compilation
1. Testing
  1. Functional testing
  1. Quality tests (performance, documentation/code coverage)
1. Bundling of deployment entities (e.g. WAR files for Java EE)
1. Provide meaningful developer feedback

Manual
* Fix broken builds immediately

Vorteile:
* Reduces risks
* Reduces repetitive manual processes

### Repo
* Version all relevant development artefacts
  * Code
  * Tests
  * Build-Automatisierung
  * Build Job Description
    * Fail early
  * Deployment Description
* Vermeide Duplikate => Parametrisierte Builds
* Aufteilen in kleinere Deployment Units fuer bessere Build-Performance
* Continuous Feedback: Lavalampe

### Studie
Effect of CI on productivity
* Teams using CI are significantly more effective at merging pull requests of
  * core members
  * external contributors

Effect of CI on code quality
* Core developers discover significantly more bugs
* External contributors do not encounter more defects => CI does not negatively impact software quality
