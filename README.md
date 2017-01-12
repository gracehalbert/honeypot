# Tech Spec: honeypot
Honeypot is a native, cross-platform application that makes saving money fun. Through in-game microtransactions, users deposit money into their savings account by purchasing supplies for their virtual pet.

The user interface is a pet-care game that triggers ACH transfers between a user’s checking and savings accounts. The happier your pet, the bigger your savings.

## Mockups

## Architecture

## Tech Stack

## Technical investigations done / to do

Animation – Ultimately we would like to implement simple but engaging and dynamic animations for users’ pets to react to user interaction. At this time, we need to investigate what library will best fit our needs.

Bank Connections – Before choosing this project idea, we spent a considerable amount of time researching banking API options. Since we want to facilitate ACH transactions between a user’s accounts, we need a service that would both authenticate bank accounts and handle the actual transfer. We found that this was difficult to find as a single service and ultimately chose a combination of Plaid for authentication and Stripe for performing transactions.

Authentication – Users will log into honeypot using Passport authentication to track in-app savings and pet statistics. They will also need to authenticate their bank account ownership through Stripe. We need to investigate whether there is a secure method for storing tokens from Stripe in our database to prevent users from having multiple log-in requirements each time they use our app.


## Ownership

Server - @marina-cerame
Database - @gonewayword
Bank API - @southcapital
Client - @cdakin1 & @gracehalbert
