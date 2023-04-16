---
title: "Name Entity Recognition System"
excerpt: "<br/><img height= '1in'  width='1in' src='/images/ner.png'>"
collection: portfolio
---
# NER-pipeline
This repo contains an Name Entity Recognition pipeline for 9 entities. The project goal is to extract and parse entity
using a sequence of components processing the text. 

## Description
The current pipeline is developed for these entities:
1- Person name
2- Date-time
3- Money
4- Cardianl Number
5- Ordinal Number
6- Phone Number
7- Email
8- URL
9- Address

The pipeline consists of parser services, components, models, and tracker steps that stores and passes entity information to the next component.
The components order in the config file specify their order in the pipeline. 
Each component tags one or more entity types and passes the processed text to the next one.
The active components are mentioned in the config file. Commenting a component turns it off. 
In each component, the active entity types can be turned off as well.
he list of available entities, the corresponding component and the parser:

| Entity Name     | Component         | Parser     |

|-----------------|-------------------|------------|

| Money           | 1) Money <br> 2) Flair | duckling   |

| URL             | url               | duckling   |

| Phone           | regex             | duckling   |

| Email           | regex             | duckling   |

| Address         | address           | usaddress  |

| Person          | flair             | -          |

| Ordinal Number  | flair             | duckling   |

| Cardinal Number | cardinal          | duckling   |

| Datetime        | flair             | dateparser |


<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->
