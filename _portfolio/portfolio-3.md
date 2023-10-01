---
title: "Name Entity Recognition System"
excerpt: '<br><img src="/images/ner.png" alt="NER" height="300"  width="300">'
collection: portfolio
---
# NER-pipeline
This project was done as part of my internship at [Got It AI](https://www.app.got-it.ai/). The goal was to develop a pipeline for Name Entity Recognition that can recognize entities like name, address, URL, email, Date, etc. and also parse the infromation of that entity, meaning that for an entity like adress, extract different components like street adress, apartment number and zip code from the tagged text. 

I developed a pipeline that uses a modular approach for each entity. Each module takes care of one or two, if related, entities and calls the parsing service of that module to parse the entity text. A single NER model is expensive to train because of lack of high-quality data that is not based on a single domain, like Books, News, or Wikipedia. I stress-tested available NER models at the time, found gaps and filled the performance gap either by training models from scratch using our in-house datasets for that entity or improved the available performance by fine-tunning or other approaches. 

## Description
The current pipeline is developed for these entities:
1. Person name
2. Date-time
3. Money
4. Cardianl Number
5. Ordinal Number
6. Phone Number
7. Email
8. URL
9. Address

and got the average f1 score of 0.9 over these entities. 
The pipeline consists of parser services, components, models, and tracker steps that stores.
The components and their communications are defined in the config file. The modular approach gives the bot designer the flexibility to turn on desired entities for each client of the company.
I presented this project in the company-wide meeting (70+ audience) at the end of my internship (Was so much fun!). Unfortunately, I don't have the permission to share the code or more details, but will be happy to chat about it if you are interested! 



<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->
