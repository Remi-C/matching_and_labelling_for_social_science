# Collaborative Matching and Labelling for Social Science #

## Brief summary ##
  This project is an open source tool for collaborative editing of data. It is intended to assist researchers in disambiguating their data. Thus, it gives them the opportunity to increase the accuracy of and find new connections in the data. 
  
  The program is especially useful for text classification. Researchers will be able to provide text files as input, as well as an intermediate file that includes contextual information (predictions, images, etc.). From there, researchers, along with their teams and colleagues, will be able to use the collaborative match system as leverage for more better informed research.

illustration

## Using this project ##
### Requirements ###
  The application requires Python 3 and a number of packages, which can be found in dependencies.txt. 
  The backbone of the front-end is Plotly's Dash, a Python framework for web applications.
  
  For researchers, the application requires either json files or a connected database with specifications for the input data. Further details are provided below.

  
### How to run the application ###
  Server : go to URL
  
  Locally : users can launch web app locally with one, or a combination, of the command line and a configuration file. They can then open the application in a browser with the specified port.

## How to customize the app to your need ##
### use your own data ###
### change styling ###
### Do more with your data ###
### Custom display ###

## Dev doc ##

### Input / Ouput ###
#### Required Format ####

### Overall Structure and Project Flow ###


[[./docs/images/collabm_architecture.png|Diagram illustrating architecture of project]]

The second diagram, "Project Architecture", provides a more detailed illustration of how the program will be organized.

The program begins with the Lobby database, which contains data on lobby firms, companies, government entities, and lobbyists. Additionally, the database includes tools and methods to clean and prepare the data for the API. The API will serve as a medium between the Python code and the database.
It will first interact with the Python code to know which data is needed, then retrieve the correctly formatted data, for example the predictions, from the database.
The Python code performs three tasks.

- First, in the "Input/Output" section, it sends requests to and receives data from the API in the appropriate format. 
- The "Logic" section reformats and prepares the data to be presented to the user.
- The "GUI" section encodes the interface that the user will interact with.

The final part of the architecture is the UI, which serves to 
1. display contextual information of the current data point which needs a user correction and 
2. receive the user input.

The contextual information will include what information we know about the name.

For example, if the program displays the lobbyist name *"John Doee"*, which was misspelled from *"John Doe"*, the program might note that both names are connected to the same lobby firms.
This information will be displayed in text, graphs, etc. This section also receives user input, which is then processed back into the Python code and is how the program makes updates to names.

#### Data input
#### Data output
#### Processing data
#### displaying data
#### Interaction
#### Submit mechanism
