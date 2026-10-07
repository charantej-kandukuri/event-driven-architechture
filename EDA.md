# Event Driven Architure (EDA)

## Source
https://www.geeksforgeeks.org/system-design/event-driven-architecture-system-design/

---

In **Event Driven Architechture (EDA)** all action as tread as **"events"** (e.g. a button click, swipe of a credit card, a temperature change). The movement an event occurs, the system instantly catches it, process it, and triggers the next step - usually in milliseconds.

## How It Looks in Daily Applications

- Ride-Sharing (e.g., Uber): The moment a driver updates their GPS location, riders near them see the car move on their map in real time.

- Fraud Detection: When you swipe your credit card, the bank's system checks for suspicious activity and approves or declines the transaction in under a second before you even take your card back.

- E-Commerce: As soon as you purchase the last item in stock, the website updates immediately to show "Out of Stock" for all other shoppers.

## Defination
**Event-Driven Architechture (EDA)** is a **system design** approach where system **components communicate** by _producing or responding_ to **events**. Such as user actions or system state changes.

Components are **loosely coupled**, allowing the to operate independently while reacting to events in real time.

```
Example:

In an e-commerce system, when a customer places an order, an Order Placed event is generated. Different services like payment processing, inventory management, and email notifications don’t constantly check the order system; instead, they independently respond when the event occurs.
```

## Important compoents in EDA

### Events
Events carry informations such as type of event and payload.
eg: a "PaymentReceived" event might detiail the payment amount.

## Event Source
An event source is any component that generates an event when a significant action or state changes occur.

They act as the staring point of the event flow.

## Event Broker/Event Bus
The event broker acts as a central hub for managening event communication.

- Receives events from publishers.
- Filters and routes events to appropriate subscribers.

## Publisher
A Publisher is responsible for emmiting events to event bus.
- A Pubsliher do not need to know who will consume the events.
- Sends events asynchronously
- convents system actions/changes into events.

## Subscriber
A subscriber registers interest in specific type of events.
- listens for relavent events in event bus.
- reads dinamically when then the event occurs.



