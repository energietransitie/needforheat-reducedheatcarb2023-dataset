# NeedForHeat REDUCEDHEARCARB 2023 Dataset 

This repository will contain anonymized energy and temperature data from residential buildings in the the Netherlands, collected for the [REDUCEDHEATCARB project](https://edu.nl/gutuc)

Initially, this repository will contain a description what kind of data you may expect. We expect this to be available late 2024.
Before we publish the data, we will do a review to ensure it meet our standards for anonymization. We expect this to be available spring 2025.

## Table of contents
* [General info](#general-info)
* [Subject Recruitment](#recruitment)
* [Inclusion and exclusion criteria](#inclusion-and-exclusion-criteria)
* [Data](#data) 
* [Status](#status)
* [License](#license)
* [Credits](#credits)

## General info

TO DO: Replace this text by general info about the dataset, e.g. generic description of subjects and when the data was collected. 

## Recruitment 

Replace this text that desribes how subjects were recruited, possibly including links to recruitment material used. 

## Inclusion and exclusion criteria

TO DO: describe.

Inclusion criteria were:
* replace with inclusion criterion 1;
* replace with inclusion criterion 2;
* etc.

## Data management

TO DO: Replace this text with (links to) data management plan, privacy policy and (if applicable), DPIA.

## Data

In the sections below, the data pre-processing and data formats used in the data files will be described.

### Subjects 

TODO: describe

### Measurement Source Categories and Source Types

In this section, we will describe the measurement source categories and typesfrom which we collected one or more properties, i.e. monitored time-series data.

### Date and time information

All timestamps were measured in [Unix time](https://en.wikipedia.org/wiki/Unix_time) format, using device clocks regularly synchronized via NTP with the correct UTC time. Setting the local device clock to the proper UTC time via NTP was one of the first steps performed by the measurement devices after they were connected to the internet via the home Wi-Fi network of a subject. Each measurement device synchronized its device clock via NTP every 6 hours. Uploads of measurement data (which could contain more than one measurement) were timestamped both by the measurement device according to the local device clock and by the server. We did not yet check for deviations between the last device timestamp of a measurement upload and the upload timestamp at the server.

Timestamps were converted to a timezone-aware `pandas.Timestamp` value, in the [Europe/Amsterdam](https://en.wikipedia.org/wiki/Time_in_the_Netherlands) timezone. In the csv files we use [ISO 8601 format with time offset](https://en.wikipedia.org/wiki/ISO_8601): `YYYY-MM-DDThh:mm:ss±hhmm`.

### Raw measurements 
 Raw masurements will be available in the folder [/raw-measurements/](/raw-measurements/) as a single [parquet](https://parquet.apache.org/) file with data for all subject ids.

All measurement data is structured according to the table below. By importing the parquet variant using [pandas.read_parquet()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_parquet.html), you automatically get a DataFrame wih the recommended indices and data types. 

| **Index/Column** | **Name** | **Type**     | **Description**                                                                                                                                       |
| ---------- | --------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| index       | `id`            | `Int64`   | unique pseudonym of the home                                                                                                                               |
| index       | `source_category`   | `category`   | e.g. `batch_import`, `cloud_feed`, or `device`                                                                                                                 |
| index       | `source_type`        | `category`   | e.g. [device type name](###measurement-devices) of the measurement device                                                                                  |
| index        | `timestamp`     | `datetime64` | start of the interval (timezone aware) |
| index       | `property`      | `category`   | property name of the measurement                                                                                                                      |
| column      | `value`         | `string`     | (string representation of) the value of the measurement                                                                                                                              |

### Raw propertes 
 In the folder [/raw-properties/](/raw-properties/) we will make various measured properties available in an 'unstacked' format with each property in its own column and an appropriate datatype. Similar to measurements, we will make data availableas a single [parquet](https://parquet.apache.org/) file with data for all subject ids.


| **Index/Column** | **Name**                             | **Type**    | **Description**                                              |
| ---------------- | ------------------------------------ | ----------- | ------------------------------------------------------------ |
| index            | `id`                                 | `Int64`  | unique code of the home                                      |
| index            | `source_category`                             | `category`  | e.g. `batch_import`, `cloud_feed`, or `device` |
| index            | `source_type`                             | `category`  | e.g. [device type name](###measurement-devices) of the measurement device                                                |
| index            | `timestamp`                          | `Timestamp` | start of the interval | (timezone aware)                       |
| column           | property_1; see property table below | data_type_1 | measured value of this property                              |
| column           | property2                            | data_type_2 | measured value of this property                              |
| ...              | ...                                  | ...         | ...                                                          |
| column           | property_n                           | data_type_n | measured value of this property                              |

### Properties 

Below we will include a table that lists all properties that were monitored, the data type in the [raw-properties](#raw-poperties) DataFrame, the measurement unit, the measurement interval, the source device and sensor that measured it, as well as the the property name.

TO DO: Insert table 


### Preprocessed data 

TO DO: add a preprocessing description including the steps taken, the filters applied with their parameters and the number of measurements deleted.

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

We use and gratefully aknowlegde the efforts of the makers of the following source code and libraries:
* [HourlyHistoricWeather](https://github.com/stephanpcpeters/HourlyHistoricWeather), by [@stephanpcpeters](https://github.com/stephanpcpeters), licensed under [an MIT-style licence](https://raw.githubusercontent.com/stephanpcpeters/HourlyHistoricWeather/master/historicdutchweather/LICENSE)
