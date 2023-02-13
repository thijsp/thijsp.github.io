---
layout: post
title: "Smart Boilers: Shower more Sustainable and more Economical"
date: 2023-02-13T08:45:00Z
authors: "Thijs Peirelinck"
categories: ["Reinforcement Learning", "Demand Response"]
description: "Artificial Intelligence can help to heat our shower water when cheap sustainable energy is abundant, without compromising in comfort."
thumbnail: "/blog/2023/droplet-wide.png"
image: "/blog/2023/droplet-wide.png"
comments: true
locale: "en_BE"
---

In my research I work on artificial intelligence based control algorithms for demand response. The goal of these algorithms is to control appliances, such as heat pumps, boilers and electric vehicles, and use their flexibility to support renewable energy uptake. Here, I would like to discuss the problem setting and solution approach I am investigating.

## "Electrify everything, decarbonise electricity"

The challenges of climate change push our society to electrify our energy needs. At the same time, we are trying to source electrical energy from sustainable resources and, as a result, reduce our reliance on fossil fuels. This combination, the energy transition, brings about some captivating challenges.

One of those challenges relates to the balance between *supply* and *demand* of energy. In Belgium, keeping this balance is currently mainly done by means of flexible gas-fired power plants. As the share of these power plants will reduce in the future, we'll have to look elsewhere for this flexibility. Solar and wind power plants rely on weather conditions for their power output. Hence, they are less flexible. We can counter this reduction in flexibility at the supply side, with an increase in flexibility at the demand side. In short, as the share of intermittent renewable energy resources in our power grid grows, we need novel approaches, such as demand response, to keep the supply-demand balance in our power grid.

Luckily, the electrification of heating and transport comes with promising solutions. Electric vehicles, electric boilers and heat pumps all offer some form of flexibility, by means of storing energy. The hot water buffer of an electric boiler decouples heat and power demand. When we want hot water for our evening shower, we can heat this water in the afternoon with solar energy.

## Artificial intelligence and computer games

Artificial intelligence is broad and encompasses applications from image recognition to chatbots to playing chess. Most applications that deal with artificial intelligence in the context of computer games are belonging to what we call *reinforcement learning*.

Reinforcement learning is a class of algoritms that typically work in a setting as displayed in the below figure. Een *agent* observes the *state* of its *environment*, for example the computer game Breakout. The state consists of everything that is needed to desribe the current status of the environment. In our example, this thus means the position of the ball, the slider and all blocks that should be hit. Based on this state the agent has to choose an *action*. In this case, two actions are possible: shifting the slider to the left or to the right. When the ball hits one of the top blocks, the score goes up. As in most computer games, the goal is to achieve the highest score possible. Our agent thus has to choose actions in such a way that its score, or *reward*, is maximised.

![RL_atari.png](https://f003.backblazeb2.com/file/thijsp-blog/blog/2023/RL_atari.png)
Over the past years, we have seen many great results of reinforcement learning beating human players in difficult games.

While this progress is interesting to see, what does this have to do with boilers and the energy transitions, you might ask.

## Cheaper and more sustainable hot water: gamification

Well, we can formulate the challenge of heating water at the right moment, when prices are low an sustainable energy is abundant, as a game. By means of reinforcement learning we can then learn to increase our score, just as in Breakout.

Unfortunately, it is not all that simple. Two main challenges arise.

First, we need to define our reward. Energy prices can be a good fit. The score of the agent can be the inverse of the energy cost. The more energy you consume, the lower the score. Additionally, we can put to cost of self-produced sustainble energy, for example by means of a rooftop solar installation, to a very small number. As a result, the agent will able to learn that hot water can be made cheaply when the sun is shining.

Second, we need to take into account comfort. We do not want a cold shower in the evening when the sun didn't show up during the day (a common problem in Belgium). Therefore, we need a comfort controller. One approach would be to give our agent a bad score for not statisfying comfort levels. However, the agent will then have to *learn* what the comfort levels are. We would like to enforce a more strict comfort policy. Therefore, our comfort controller will maintain water inside the buffer at a pre-determined minimal comfort level and override agent actions when needed.

Over the past years, we have tested and fine-tuned this approach. This work has been presented at several scientific conferences and in several scientific journals \[1, 2, 3\]. The results show that a reinforcement learning based agent can indeed reduce the cost of electric water heater operation by taking into account energy prices and simultaneously match solar production and boiler power consumption. We have seen cost reductions for the end-consumer up to 15% \[3\], compared to a regular controller as used nowadays.

Given the economical en ecological impact I am confident this technology will eventually find its way to the end-consumer. Would't you like to have boiler which is sustainable wihtout breaking the bank?

---

\[1\] T. Peirelinck, C. Hermans, F. Spiessens, G. Deconinck, *“[__Domain randomization for demand response of an electric water heater__](https://ieeexplore.ieee.org/abstract/document/9201065)“*, IEEE Transactions on Smart Grid 12 (2), 1370-1379, 2020

\[2\] T. Peirelinck, C. Hermans, F. Spiessens, G. Deconinck, *“[__Transfer learning for Demand Response of a Multi-Agent Battery and Electric Water Heater System__](https://ieeexplore.ieee.org/abstract/document/9640081)“*, 2021 IEEE PES Innovative Smart Grid Technologies Europe (ISGT Europe), 1-6, 2021

\[3\] T. Peirelinck, C. Hermans, F. Spiessens, G. Deconinck, *“[__Using reinforcement learning for optimizing heat pump control in a building model in Modelica__](https://ieeexplore.ieee.org/abstract/document/8398832)“*, 2018 IEEE International Energy Conference (ENERGYCON), 1-6, 2018
