# ProgrammingProject

Contents
1 Introduction                                                                    
2 Getting started                                                               
3 Sections                                                                          
4 Language                                                                       
5 Programming                                                                  
 

1         INTRODUCTION                                      
1.1         Purpose/Specification
The goal set out for the project was as follows:
“ to construct an application to explore data on property transactions in processing. The data set we will use is from the UK Land Registry. “
PriceScanner was developed based on this goal - to solve the issues surrounding sifting through massive amounts of UK land registry data in order to find information about properties in various locations across England and Wales. 
1.2         Scope
The program can be used to sift through 1000 entries, 10000(10k) entries, 50000(50k) entries and the 1 month data file (about 94k entries). The application also works when more than one data file is loaded in at the same time into the same file.




 
2         GETTING STARTED                                                                     
2.1         Usage
The program is designed in a way that makes it easy to use. The options are kept simple, to avoid confusing the user. The aim in mind when creating the program was to simplify the handling of thousands of lines of data by presenting it in a more useful, aesthetically pleasing manner. 
2.2         Overview
As described earlier, the options are kept simple through the usage of Widgets that can easily be clicked to access data. The program presents the user with the following information:
The Average Price of the houses in a particular county as compared to two other counties.
A pictogram of the number of houses sold in the county as compared to the same counties as above
A bar chart representation of the Average Price of properties over a range chosen by the user
A pie chart displaying the number of houses  sold of each type for the county.
Some additional statistics taken from Wikepedia (2015 estimates)
These are described in detail below.





3         SECTIONS                                                                                      
                3.1 Map and Other Widgets
When the program is run, the user is brought to a screen with the application logo and presented with a scan widget that leads them to the map screen.
The main widgets that were created for the home screen where the county widgets fashioned specifically to cater for the needs of every single county for which data was provided. Once the widgets were created, the following piece of code was implemented into draw to find the accurate location on screen for each widget :
if( mousePressed)
{
            System.out.println(“ ” + mouseX  + ”,” + mouseY)
}
This piece of code printed out, to the console, the accurate x and y position when that position was clicked on the background image. The county widgets could then easily be positioned correctly and once this was completed, the piece of code was removed from the program.
The data taken from the Land Registry is displayed across a number of screens in the current program. Widgets were created for the tabs that appear once a county has been selected. These widgets, once clicked change colour to allow the user to easily know what tab is currently being displayed. The five widgets created were Average Price, Pictogram, Average Over the Years, Statistics and Pie Chart. These are explained in further detail below.
More widgets were created on the Average Over the Years Screen to permit the user to select the start and end year, i.e the range of years for which they wanted to view data. These widget, again will change colour once clicked to inform the user of what years they have currently selected.
There was also a back widget created that allows users to flick back to the main home screen and switch between counties. 
Alongside the map is a help option. It features an image which can be clicked to toggle the help text to appear as a separate image. The image provides useful information an how to use the application. When the image is drawn an exit (X) button will appear on the top right-corner of the text making it easier for the user to toggle out of it. The help button can be clicked repeatedly as and when help is required.
3.2 Average Price
Average Price was calculated while the data was being read in and sorted into the respective counties. Once the average price was calculated, it was represented in a Bar Chart. The bar chart took the average price of a county and used this to generate a height value, and this was done for each county put into the chart. This was then drawn, labelled and spaced accordingly to lay the data out in an easy to digest and visually appealing way. The Chart class and drawing method is relatively versatile, and as a result of this can be used to represent more or less bars, making is possible to be used for the average price over the years statistics page.
3.3 Pictogram
The Pictogram chart was used to represent the number of houses in a given county, and much like the Bar Chart, displays the value for the selected county, as well as two  
                                            
surrounding counties, for the purposes of comparison and contrast. The number of houses to be displayed was calculated by taking the height value and dividing it by the size of the
image, while the height value itself was taken by comparing the largest value of the three displayed counties to the two other counties, eg. If a county had 400 houses, and another had 200, its height value would be 50% of the height value of the county with the most houses, which would be drawn at the maximum height allowed by the chart. This ensures proper scaling of pictogram and an accurate display of the data for users to understand. Again, like the Bar Charts, this was designed to be relatively versatile in order to use the features in other sections of the program, and although it may not be used outside of representing the number of houses in a county, the program could very easily be adapted in order show more or less bars on a single chart, or to use the pictogram in other areas to represent other data. 
                3.4 Average price over the Years
This part of the program allows the user to investigate and look into the average prices for properties sold within a county within a certain time period. It allows them to select a Start Year and an End Year and in turn the program creates a Bar Chart displaying the average prices within the given time range. This allows users to research and predict trends in property prices throughout the years.

The bar chart itself was implemented using previous code written by Daniel that was originally used for the Average Price bar chart. It was then adjusted to allow it to be interactive and allow the user to change the time range instantly and have the chart adjust accordingly.

                3.5 Pie Chart
The Pie Chart screen allows the user to investigate the types of properties that are most frequently sold within a region. It allows them to gather clear demographics and distribution models for each county.

For example, when looking at Greater London’s pie chart you see that the majority of properties sold are Flats and Terraced houses. Whilst in the North of London you can see that the most common property types are Detached houses. This allows the user to establish things such as a direct correlation between a county’s population density and the types of properties sold.

                3.6 Statistics
Wikipedia provided estimates for Population, Area and Density and the ranking for those estimates for the year of 2015 for the counties of England and Wales. These were taken from the wikipedia page and used in the program to allow a user to estimate roughly the type of place they were looking at in terms of crowding.
                                                       
                3.7 Method for screens
The bulk of the program resides on the home screen, where all the county widgets are drawn. Once a county is selected, the user can choose between 5 different screens on which our graphs are drawn. Tabs are created along the top of the program, and it constantly checks if any are clicked. If the mouse is pressed, a series of booleans are changed to determine which screen should be displayed. For example if Pie Chart is clicked(made true), average price, pictogram, average over the years and statistics are all false. This allows only the Pie Chart to be displayed, as required, rather than displaying all five of the screens at the same time. An advantage of this system is that if you want to compare a certain aspect of different counties, the final screen you were on is still set to true, meaning you will open to the last screen you were on, allowing the user to quickly switch between counties for the same screen. 

4         LANGUAGE                                                                                    
The program was written with simplicity in mind, yet still aimed to produce quality results. The team decided to use a more stable development environment - Eclipse, however, no external libraries other than Processing were used in the production of the program. The core library file for processing was imported to the folder of our project and used as before in processing with the exception of the PApplet.

5         PROGRAMMING                                                         
The design choice to avoid external libraries may have potentially hurt the overall aesthetic or ‘wow-factor’ of the program, however, our final product was completely produced through the skills we have acquired across first year, through both the Programming Project and Introduction to Programming modules.

