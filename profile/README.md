# Welcome to BrochureUI

## Overview

BrochureUI introduces *Anchor*, a concept that transforms business model canvases into compelling, multilingual stories through a fully responsive landing page, *Anchor* offers a seamless workflow, guiding users from idea to reality, and ensuring a cohesive narrative for your business.

### First, what is a business model

A business model describes how an organization creates, delivers, and captures value in economic, social, cultural, or other contexts. The model outlines how the business operates, spends, and earns money to generate profit. The process of business model construction and modification is also called business model innovation and forms a part of business strategy.

#### It consists of:

  1. **Key Partnerships**
     - Strategic collaborations that enhance capabilities, reduce risks, and drive value creation.
  2. **Key Activities**
     - Core operations and tasks essential for delivering value to customers.
  3. **Key Resources**
     - Critical assets, such as tools, people, or technology, that support business success.
  4. **Value Proposition**
     - The unique benefits and solutions that address customer needs and solve their problems.
  5. **Customer/Client Relationships**
      - Approaches to building and maintaining strong connections with customers/clients.
  6. **Channels**
      - Pathways used to deliver products, services, or messages to customers.
  7. **Customer/Client Segments**
      - Defined groups of customers or clients served by the business.
  8. **Cost Structure**
      - The breakdown of major expenses required to operate the business.
  9. **Revenue Stream**
      - The streams of income generated from products, services, or activities.
  10. **Social Impact**
      - The positive effects the business creates for society and communities.

### Second, how Anchor perceives it

Anchor perceives the business model as a story of two interconnected worlds: the **internal world**, where the business operates and creates value, and the **external world**, where customers and clients exist. The **bridge** connecting these worlds is formed by the channels that deliver the business’s value to customers and clients.

#### The Metaphor

The internal world encompasses the operations, partnerships, and resources necessary for the business to exist and thrive. The external world focuses on the customer-facing side, where the business engages with clients and generates revenue. The bridge connects internal operations to external audiences, facilitating the communication, delivery, and sustainability of the business’s value.

1. The **internal world** is the foundation and it consists of **key partnerships**, **key activities**, **key resources**, and **cost structure**.
2. The **external world** is the audience and it consists of **customer/client segments**, **relationships**, and **revenue stream**.
3. The **bridge** connects both worlds and it consists of **channels**, **value proposition**, and **social impact**.

## The Data

### The Card Structure

Below is the business card details representing the business metadata that summarizes the business, its important to understand that the landing page goal is to encourage the viewrs to take an action and start interacting with the business, so this goal has to be clear. The `CTA` is an abbreviation for *Call to Action*, this should be the text of main button that takes a certain action, for example: navigating to another page, opening a form, making a call or sending a message. In the example below, `en` represents the English version. If there are multiple languages, provide the same structure under their respective language keys, wrapped within the same object. For example: `ar` for Arabic, `it` for Italian, and so on.

```json
"en": {
  "name":"",
  "slogan":"",
  "description":"",
  "CTA":""
}
```

### The Model Structure

Below is a basic example of the data structure for each division. This example covers most common use cases, but keep in mind that the keys and structure can be customized to better fit the final view and business requirements. In the example below, `en` represents the English version. If there are multiple languages, provide the same structure under their respective language keys, wrapped within the same object. For example: `ar` for Arabic, `it` for Italian, and so on.

  1. **Key Partnerships**
```json
"en": {
  "title":"partnerships",
  "list":[
     {
       "name":"",
       "role":"",
       "logo":""
     }
   ]
}
```
  2. **Key Activities**
```json
"en": {
  "title":"activities",
  "list":[
     ""
   ]
}
```
  3. **Key Resources**
```json
"en": {
  "title":"resources",
  "list":[
     ""
   ]
}
```
  4. **Value Proposition**
```json
"en": {
  "title":"offerings",
  "products":[
     {
       "name":"",
       "description":""
     }
   ],
  "services":[
     {
       "name":"",
       "description":""
     }
   ]
}
```
  5. **Customer/Client Relationships**
```json
"en": {
  "title":"relationships",
  "list":[
     ""
   ]
}
```
  6. **Channels**
```json
{
  "title":"channels",
  "contact":{
       "website":"",
       "email":"",
       "phone":"",
       "location":""
     },
  "platforms":[
    {
       "name":"",
       "link":"",
       "icon":""
     }
],
   
}
```
  7. **Customer/Client Segments**
```json
"en": {
  "title":"segments",
  "list":[
     {
       "segment":"",
       "description":""
     }
   ]
}
```
  8. **Cost Structure**
```json
"en": {
  "title":"costs",
  "list":[
     ""
   ]
}
```
  9. **Revenue Stream**
```json
"en": {
  "title":"revenues",
  "list":[
     ""
   ]
}
```
  10. **Social Impact**
```json
"en": {
  "title":"impacts",
  "list":[
     ""
   ]
}
```
## The Storage

It is recommended to store the data in JSON files, as Anchor is a front-end application that does not require a database. Each file should be named after its corresponding division, which makes the process of updating, storing, and deploying easier. Below is an example of the data file system structure:

```bash
.
├── card.json
├── audience
│   ├── relationships.json
│   ├── revenue.json
│   └── segments.json
├── bridge
│   ├── channels.json
│   ├── impact.json
│   └── offerings.json
└── foundation
    ├── activities.json
    ├── cost.json
    ├── partnerships.json
    └── resources.json
```

## The Application

**Anchor** simplifies access to the data by organizing it into JavaScript objects: ***card***, ***audience***, ***bridge***, and ***foundation***. Additionally, it handles toggling between display languages to provide a seamless multilingual experience.

## The Presentation

**Anchor** creates a single page application of four main components: ***Header***, ***AudienceSection***, ***BridgeSection***, and ***FoundationSection***. The ***Header*** acts as the hero section, which is the first thing the viewer sees, displaying the [card](#the-card-structure) content. Each of the other components then displays the corresponding division data responsively.

![Logo](https://github.com/BrochureUI/assets/blob/main/organizations/BrochureUI.png)
