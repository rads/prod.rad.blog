---
title: The Life of an Event
---

## 1. User Event → DOM Event Handler → Re-frame Dispatch

When the user clicks something or types in a form field, the browser dispatches a DOM event. We write callbacks for these DOM events as `on-*` attributes in our Reagent components. Inside these callbacks we call `(rf/dispatch)` which creates an event in Re-frame.

## 2a. Re-frame Event Handler → HTTP Request → RPC Message

The Re-frame event is handled by a function we registered using `(rf/reg-event-fx)`. Our handler is a pure function that returns a map with an `:http-xhrio` key. The value for this key represents an HTTP request to be sent to the server. The request body is JSON-encoded Transit which represents an RPC message the server will receive.

## 2b. HTTP Server → Kafka Message

The RPC message is received by the server and routed to a Ring handler. Inside the Ring handler we publish a message to Kafka.

## 2c. RPC Message → HTTP Response → Re-frame Event Handler → Re-frame DB

After publishing to Kafka we send back the confirmation to the browser. The Re-frame event handler will be a function registered with `(rf/reg-event-db)`. The handler is a pure function that takes the DB and handles the response.

## 3a. Re-frame Event Handler → HTTP Request → RPC Message

Once we've confirmed that the event was published to Kafka, we want to retrieve the new state that was caused by it. At some point (?) we will trigger an event for a handler registered with `(rf/reg-event-fx)`. This handler will return an `:http-xhrio` key like last time.

## 3b. HTTP Server → PostgreSQL Table Row

The HTTP server receives the message and sends a query to the PostgreSQL database. It returns the rows in the response (which *may or may not* have been updated with effects of the new event).

## 3c. RPC Message → HTTP Response → Re-frame Event Handler → Re-frame DB

The rows are returned in the RPC message and handled by the Re-frame function defined with `(rf/reg-event-db)`. The handler uses the response to update the app state atom with the latest view of the PostgreSQL data.

## 4. DOM Elements → DOM Event Handler → User Event

After every Re-frame event handler finishes, any updated subscriptions will trigger re-renders in the Reagent components. This may update the DOM event handlers which will respond to future user events. Go back to step 1 to complete the loop.
