---
layout: post
title: "PhD Abstract"
date: 2022-05-04T17:00:00Z
authors: ["Thijs Peirelinck"]
categories: ["Reinforcement Learning", "Demand Response", "Transfer Learning"]
description: "Abstract of my PhD Thesis"
thumbnail: "/blog/2023/tekening_Thijs-wide.png"
image: "/blog/2023/tekening_Thijs-wide.png"
comments: true
locale: "en_BE"
---

*Find the full thesis <a href="https://lirias.kuleuven.be/3700338?limo=0" target="_blank">here</a>*

## Reinforcement Learning with Knowledge Transfer for Residential Demand Response

One of the main challenges of the energy transition is the increasing need for demand flexibility due to the intermittency of renewable energy sources. While electrification of heating and transport further increases the need for sustainable energy sources, it also provides a source of flexibility. Power-to-heat technologies, such as heat pumps and electric water heaters, offer decoupled demand for heat and power, and thus provide a source of flexibility at the residential level.

Demand Response (DR) programs aim to activate demand flexibility by encouraging end-users to adapt their energy consumption based on grid signals. Over the past years, many countries have started to re-organise their electricity market(s) to activate dormant residential flexibility. For example, in the European Union every customer is entitled to an electricity contract with time-varying prices.
To harness this flexibility, researchers have been looking at Reinforcement Learning (RL). The main benefit of this control paradigm is its ability to solve complex control problems without the need for an environment model. This property mitigates several challenges of residential DR. Unfortunately, RL is relatively data inefficient. This manifests itself in extensive training times. During this initial period, the RL agent shows poor performance.

Inspired by recent efforts to improve RL data efficiency, this work builds upon transfer learning algorithms and contributes to their application in DR. This dissertation proposes several knowledge transfer learning approaches that increase data efficiency of RL algorithms, both in single- and multi-agent settings. This work shows how RL agents can be pre-trained in simulation, either to perform the same task in practice or to perform the same task for a different appliance. Furthermore, this work presents a method to incorporate domain knowledge into RL agents, without restricting their applicability. By means of these approaches, RL agents show good control performance immediately after deployment and, consequently, increased user comfort.

___

## Reinforcement Learning met kennisoverdracht voor toepassingen van residentiële vraagsturing

Een van de grootste uitdagingen van de huidige energietransitie is de stijgende behoefte aan flexibiliteit langs de vraagzijde. Deze flexibiliteit is nodig omdat het productieprofiel van hernieuwbare energiebronnen vaak moeilijk te voorspellen is en een wisselend karakter heeft. Bovendien zorgt de stijgende graad van elektrificatie van onze verwarming en ons transport ervoor dat we in de toekomst meer van die hernieuwbare bronnen zullen nodig hebben. Gelukkig bieden elektrische wagens, elektrische boilers en warmtepompen ook een grote mate van flexibiliteit. Dit komt omdat zij, door hun energiebuffer, voor een ontkoppeling van de warmtevraag en elektriciteitsvraag zorgen.

Door middel van verschillende signalen, en met behulp van vraagsturing, kunnen eindgebruikers aangemoedigd worden om hun flexibiliteit actief te gebruiken en hun verbruik aan te passen aan de noden van het elektriciteitsnet. In de voorbije jaren zijn verschillende landen begonnen met het herorganiseren van hun elektriciteitsmarkt. Dit met als doel het activeren van flexibiliteit die tot op heden niet gebruikt werd. Zo werd het binnen de Europese Unie onlangs ingeschreven dat het een recht is van elke consument om een dynamisch contract af te sluiten met zijn energieleverancier.
Om deze flexibiliteit te kunnen exploiteren kijken onderzoekers meer en meer naar Reinforcement Learning (RL). Het grootste voordeel van deze regelmethodologie is de mogelijkheid om complexe regelsystemen op te lossen zonder dit regelsysteem wiskundig te moeten beschrijven. Deze eigenschap biedt een oplossing voor enkele van de grootste uitdagingen op het vlak van residentiële vraagsturing. Jammer genoeg gaat RL vrij inefficiënt om met de beschikbare data. Dit resulteert in lange perioden van slechte sturing omwille van het onvoltooid leerproces.

Geïnspireerd door recente nieuwe ontwikkelingen die de data-efficiëntie van RL verhogen, bouwt dit werk voort op algoritmes die kennisoverdracht mogelijk maken en draagt het bij aan de toepassing van deze algoritmes voor vraagsturing. Dit proefschrift stelt enkele mogelijkheden voor om kennis over te dragen tussen verschillende systemen en zo de data-efficiëntie van RL te verhogen, zowel voor systemen met één enkele agent, als voor systemen met meerdere agenten. De resultaten in dit proefschrift tonen aan dat RL-agenten in een simulatie kunnen worden voorbereid op het regelsysteem dat ze in de praktijk zullen moeten aansturen. Tevens kunnen agenten ook worden voorbereid op het uitvoeren van dezelfde taak, maar voor een ander apparaat. Dit werk toont ook aan dat het mogelijk is om domeinkennis van een expert rechtstreeks in te bouwen in de RL-agent. En dit op een manier waarbij de toepasbaarheid niet gelimiteerd wordt tot één enkel huishouden. Al de hierboven genoemde methoden dragen bij aan het verhogen van de data-efficiëntie van RL-algoritmes. Door middel van de voorgestelde werkwijzen wordt de prestatie van de RL-regeling, tijdens de eerste weken na de installatie, sterk verhoogd. Dit resulteert in verhoogd comfort voor de eindgebruiker en komt tegemoet aan de toenemende noden van de energiemarkt.
