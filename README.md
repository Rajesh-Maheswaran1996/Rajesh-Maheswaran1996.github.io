## CS 416 Data Visualization- Project Essay

By Rajesh Maheswaran; rajeshm2
Summer 2021


View visualization by clicking here : [Final Project for CS 416 - Vehicle properties affecting CO2 emissions](https://rajesh-maheswaran1996.github.io/)

The dataset provided is from the Environment Protection Agency. It contains detailed descriptions of 4,411 vehicles manufactured in 2015 that were used for fuel economy testing. The variables in the dataset are:  
 
- `Make` - manufacturer
- `Model` - model of vehicle
- `ID` - manufacturer defined vehicle identification number within EPA's computer system (not a VIN number)
- `disp` - cubic inch displacement of test vehicle
- `type` - car, truck, or both (for vehicles that meet specifications of both car and truck, like smaller SUVs or crossovers)
- `horse` - rated horsepower, in foot-pounds per second
- `cyl` - number of cylinders
- `lockup` - vehicle has transmission lockup; N or Y
- `drive` - drivetrain system code
    - A = All-wheel drive
    - F = Front-wheel drive
    - P = Part-time 4-wheel drive
    - R = Rear-wheel drive
    - 4 = 4-wheel drive
- `weight` - test weight, in pounds
- `axleratio` - axle ratio
- `nvratio` - n/v ratio (engine speed versus vehicle speed at 50 mph)
- `THC` - total hydrocarbons, in grams per mile (g/mi)
- `CO` - Carbon monoxide (a regulated pollutant), in g/mi
- `CO2` - Carbon dioxide (the primary byproduct of all fossil fuel combustion), in g/mi
- `mpg` - fuel economy, in miles per gallon

## Project Essay

# Introduction
This project focuses on creating a narrative visualization for understanding the major factors that affect CO2 emissions released by vehicles. This dataset provided by the Environmental Protection Agency contains detailed descriptions of 4,411 vehicles manufactured in 2015 that uses for fuel economy testing. The end goal for the user viewing this narrative visualization is to understand which factors in a vehicle (car, truck, or crossover, etc.) contribute more to its carbon emission.

# Narrative Structure
The chosen narrative structure for this project was an interactive slideshow. In an interactive slideshow, the user follows an author-directed path through the slideshow and allows the user to investigate information in the slide if the user requires it. The main difference from a drill-down story structure is that in an interactive slideshow, a user can examine details in a given slide and is asked to go to the next slide to drill down on other information. Similarly, in this project, the user is first presented with a question asking which factors in a vehicle affect CO2 emission while subsequently displaying the first slide. The user then progresses through the slides by clicking on the following visualization buttons to view and CO2 emission rate compared with other factors while finally arriving at the final slide where the user could make a conclusion.

# Visual Structure
The narrative visualization uses a more user directed ordering where the user is presented a scene and then given the option to jump to a scene of choice. To help navigate through this slideshow, the visual structure is set up where the user is given an explicit instruction to click on a specific button to move from one slide to the next. The button is also highlighted to let the user know which slide is currently being viewed. The direction on top of the visualization container instructs the user to hover over data points to understand individual trends for that specific type of vehicle so that the user can get a better understanding of the correlation between the vehicle factors and CO2 emission.
There are three scenes in this narrative visualization, and they all follow a specific template and layout for visual consistency. The project title and direction for interaction are fixed above the visualization container for the duration of the narrative visualization. The visualization container which displays the data, is consistent with a height of 510px, width of 980px, and background color "grey" throughout narrative visualization.  The plot axes and legend are consistent. The axes are also linear which extend to the range of the data. The marks are circular and uniform in size and color. The scenes were designed for consistency to keep the viewer from getting disoriented through transitions. The ordering is such that the viewer is first presented with a vehicle factor and graph is drawn to between that factor and CO2 emissions. This is displayed for all categorical types. Users can then drill down on each type if necessary, to gain more insights. This style of displaying data is repeated in scene two and scene three with other factors, while scene three also reveals a conclusion that asks the user to reflect on the various trends.

# Annotations
Annotations are used to highlight a trend in the data, direct the user to further investigate the data, and ask the user to draw a conclusion from the data. The annotations used are consistent for font size and bolded style. Annotations are mainly used in this narrative visualization to first give a title or one lined message explaining what the given scene is about. This one liner changes when the user moves from one visualization to the other. The other annotation that is presented is when the user drills down and hovers over a specific type of vehicle, a prompt explaining the data and helping the user understand the trend is shown which disappears after the user mouse’s out. The last slide has a concluding message that appears to make the user recall the scenes and make a decision regarding what really contributes to the CO2 emission.

# Parameters
Parameters are used to engage the user in the narrative visualization and further explore the data. The parameter used is the categorical variable “type”. The user has the ability to drill down one vehicle type at a time by mousing over the data point belonging to that particular vehicle. This allows the user to gain more information about the relationship between the various factors and CO2 output, not only as an overall trend, but based on vehicle type as well. The current state is controlled by this parameter vehicle "type". When mousing over a data point belonging to a particular vehicle type, the current state changes and the data points belonging to the other vehicle types are set to opacity = 0.01. When mousing off the data point the current state changes again and opacity for all data points for all vehicle types returns to 1. The second parameter is slideNumber which controls which scene the user is currently viewing. This parameters is crucial for pulling the right data and annotations.

# Triggers
Triggers are utilized in two ways for this visualization. The buttons along the top of the visualization container are triggers to change scenes. The buttons are labelled such that their scenes are made to be obvious: "Weight", "Mileage", "Horsepower" and "About the Visualization". The user event of clicking one of these buttons changes the current state of the visualization by changing the visualization scene. Affordance is used such that the button that represents the current state of the visualization is displayed with an increased brightness. When the user mouses over the other buttons they become temporarily highlighted which indicates to the user that they may be clicked. Upon clicking a button this triggers a change to the corresponding scene being displayed. Triggers are also utilized with the data points. The user event of "mouse over" a data point changes the current state of the chart by applying an opacity of 0.01 to all data not part of the vehicle type that is currently moused over. The user event of "mouse off" changes the current state of the chart by returning the opacity of all data points back to 1. 







