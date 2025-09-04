# NeedForHeat REDUCEDHEATCARB 2023 Dataset 

Dataset containing anonymized energy and temperature data from residential buildings in the the Netherlands, collected for the [REDUCEDHEATCARB project](https://edu.nl/gutuc).

*The dataset is currently in review to ensure it meet our standards for anonymization. We are currently in the process of describing metadata, so you know what you may expect.*

## Table of contents
* [General info](#general-info)
* [Subject Recruitment](#recruitment)
* [Inclusion and exclusion criteria](#inclusion-and-exclusion-criteria)
* [Data](#data) 
* [Status](#status)
* [License](#license)
* [Credits](#credits)

## General info

This repository will contain anonymized energy and temperature data from residential buildings in the the Netherlands, collected for the [REDUCEDHEATCARB project](https://edu.nl/gutuc)

Initially, this repository will contain a description what kind of data you may expect. Before we publish the data, we will do a review to ensure it meet our standards for anonymization.

## Recruitment 

Subjects were recruited via [Remeha](https://www.remeha.nl/) via an e-mail invite to fill out this [online recruitment survey](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/recruitment/REDUCEDHEATCARB_intake.pdf). This recruitment mail was sent to about 3350 customers with a Remeha gas-firec boiler and an eTwist connected thermostat in the Netherlands, in three waves, from November 2023 until February 2024.

## Inclusion and exclusion criteria

### Inclusion criteria

Participants must:

* Be a Remeha customer with a gas fired boiler and an eTwist connected thermostat.
* Provide informed consent.
* Live in a single-family dwelling.
* Have a smart meter installed at home.
* Have internet and Wi-Fi at home.
* Ensure all occupants have a smartphone and are willing to keep Bluetooth enabled.

The first criterion was verified by Remeha before sending the recruitment mail.

### Exclusion criteria:

Participants must not:

* Frequently or always charge an electric vehicle (EV) at home.
* Frequently or always use heating sources other than a gas boiler (like wood pellets)
* Have kids at home younger than 12 living at home.
* Live in a tiny home (A<sub>g</sub> < 50 m<sup>2</sup>)
* Live in a huge home (A<sub>g</sub> > 250 mm<sup>2</sup>)

The recruitment survey assessed all inclusion and exclusion criteria except the last two. Of the 171 respondents 45 met all criteria. A subsequent manual check via [Kadaster's Basisregistratie Adressen en Gebouwen (BAG)](https://bagviewer.kadaster.nl/) confirmed that all 45 also satisfied the final two criteria.


## Data management

We documented our [Data Management Plan](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/REDUCEDHEATCARB_data_collection_winter_2023-2024.pdf) online. The privacy policy (in Dutch and English) was available online as well, both in the recruitment survey and in the NeedForHeat GearUp app, in two languages and in a layered structure: 
* Dutch: [short summary](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/privacy/nl-NL/Privacyverklaring%20NeedForHeat.html), [summary](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/privacy-summary/nl-NL/Privacyverklaring%20NeedForHeat.html) and [full version](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/privacy-full/nl-NL/Privacyverklaring%20NeedForHeat.html);
* English: [short summary](./data_management/privacy/en-US/NeedForHeat%20Privacy%20Policy.html), [summary](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/privacy-summary/en-US/NeedForHeat%20Privacy%20Policy.html) and [full version](https://www.energietransitiewindesheim.nl/needforheat-reducedheatcarb2023-dataset/data_management/privacy-full/en-US/NeedForHeat%20Privacy%20Statement.html).

## Data

In the sections below, the data pre-processing and data formats used in the data files will be described.

### Subjects 

TODO: describe

### Measurement Source Categories and Source Types

In this section, we will describe the measurement source categories and typesfrom which we collected one or more properties, i.e. monitored time-series data.

### Date and time information

TODO: describe

### Raw measurements 

TODO: describe

### Raw propertes 

TODO: describe

### Properties 

TODO: describe

### Preprocessed data 

TODO: describe

## Status
Dataset is: _collected_, _anonimization-to-be-started_

## License
This data is made available under the [CC BY 4.0](./LICENSE.md) by the [Research group Energy Transition, Windesheim University of Applied Sciences](https://windesheim.nl/energietransitie) 

## Credits

Data collection was a joint effort of:
* Henri ter Hofte · [@henriterhofte](https://github.com/henriterhofte) · Twitter [@HeNRGi](https://twitter.com/HeNRGi)
* Nick van Ravenzwaaij · [@n-vr](https://github.com/n-vr)
* <contributor name 3> · [@Github_handle_3](https://github.com/<github_handle_3>) · Twitter [@Twitter_handle_3](https://twitter.com/<twitter_handle_3>)
* etc. 

Data description, anonimyzation and re-identification analysis was performed by:

* <name> · [@Github_handle_4](https://github.com/<github_handle_4>) · Twitter [@Twitter_handle_4](https://twitter.com/<twitter_handle_4>) 


Thanks go to those who are the ultimate source of this dataset:
* all anonymous subjects who volunteered to make their measurement data available
