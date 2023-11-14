---
layout: page
title: NFC Reader Ticket Application
description: NFC reader/writer with complete security implementation  
img: /assets/img/nfccard.jpg
---

Ticketing app that writes and reads NFC enabled card, the application of which can be used in various areas including but not limited to events, transportation, offices, custom service etc.

The features include:

- Unique key for each card, generated using the Serial ID of the card and master secret, that is different that the default password of the card.
- Unique key for MAC generation.
- 2 MACs to validate the integrity of the data in the card: one for static data and other for dynamic data.
- Read and Write protected in all the user memory pages used by the application.
- Multiple taps within 5 seconds (configurable) are blocked.
- 3 tickets (configurable) are issued in each issue action.
- More than 50 tickets (configurable) are not allowed to issue for any card.
- 30 days validity (configurable), are given from the date of first use, while issuing tickets.
- More than 90 days (configurable) of validity period is not given to any card, regardless the number of tickets issued.
- If the card has non-expired tickets, those tickets are added during the new issue.
- If the card has non-expired tickets, the validity duration is added on top of the previous value.

---

[**Access Github repo**](https://github.com/bipinkh/nfc-reader){:target="\_blank"}

---
