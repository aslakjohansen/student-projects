# The Social Garden

**Tags:** social network, prediction, energy conservation, embedded, iot

## Introduction

Many facilities pay companies to properly water plants. This enforces a strict tradeoff between the number of plants an the financial cost of "operating" the plants. It also serves to position the plants as a passive element of the context of the occupants. Would it be possible to introduce a form of common feeling ownership amongst the occupants?

## Problem

Can we build a system for crowdsourcing the watering of plants using an IoT device that measures soil humidity?

## Approach

Make an app that users install. Whenever a plant needs water it looks for nearby users. It then picks a user and displays a notification on the the users phone. If the user doesn't react within a reasonable time the notification is removed and displayed on another users phone. This way the notification jumps from phone to phone until a user reacts.

Points are awarded when a watering operation is confirmed. Special points are awarded when watering a plant as a "guest". A user is a guest when they are visiting a facility operating the system, but are not associated with the user.

Several parameters can be optimized:
- How to prolong the battery life of a device?
- How to avoid pestering users with notifications?
- How to pick the next user to display the notification for?
- How to engage users through gamification?
- What incentives are necessary to make this successfull?
- How can a 2d-barcode on the device be used to introduce new users to the social community?

## Related Work

- Potential platform: [ESP32 soil humidity sensing spear](https://www.amazon.de/diymore-Temperatur-Luftfeuchtigkeit-Hygrometer-Feuchtigkeitserkennung/dp/B07HRD1VR9/ref=sr_1_15?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=esp32+soil+humidity&qid=1608661028&sr=8-15) (there are a few slightly different versions)

