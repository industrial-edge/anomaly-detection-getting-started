# Installation of screwing simulation

This installation guide shows how to Configure IE Databus, IE Data Service and the IE Flow Creator run a simulation which is then used to train our Anomaly Detection algorithm. 

- [Installation of screwing simulation](#Installation_ScrewSimulation)
  - [Used Components](#used-components)
  - [Configure IE Databus](#configure-ie-databus)
  - [Configure DataService Adapter](#Configure-DataService-Adapter)
  - [Configure IE Flow Creator](#configure-ie-flow-creator)
    - [Import Flow](#import-flow)
    - [Edit Databus Credentials](#edit-databus-credentials)
  - [Start Simulation and add variables to IE Data Service](#start-simulation-and-add-variables-to-ie-data-sservice)

## Used Components

To run the simulation the folloing components are needed:
- IE Databus V1.6.6
- IE FlowCreator V1.3.8
- IE DataService V1.3.3
 
## Configure IE Databus

First of all make sure that you have created a databus user which has subscription rights with the topic 'ie/#'.

<p align="center"><kbd><img src="graphics/01iedatabus.PNG" /></kbd></p>

## Configure Data Service Adapter

- Open the IE Data Service app and go to the adapter Section. 

- There you have to add an new Adapter with:
  - Adapter name (you are free to choose your own name) 
  - Broker URL: tcp://ie-databus:1883
  - Your own databus credentials
  - Metadata topic ie/m/j/simatic/v1/sim/dp

<p align="center"><kbd><img src="graphics/02AddNewAdapter.PNG" /></kbd></p>

- After that activate the Adapter

<p align="center"><kbd><img src="graphics/03ActivateAdapter.PNG" /></kbd></p>

## Configure IE Flow Creator

After we configured the Data Service Adatper we are now going to configure the actual Simulation which is publishing the data onto the databus. 

### Import Flow

First open the IE Flow Creator application and open the 'burger menue' in the top right cornern. 

There you select 'Import' or you use the shortcut 'ctrl-i'.

<p align="center"><kbd><img src="graphics/04ImportFlow.PNG" /></kbd></p>

Now import the JSON file which can be downloaded [in the src folder](#../src).

### Edit Databus Credentials

## Start Simulation and add variables to IE Data Service

