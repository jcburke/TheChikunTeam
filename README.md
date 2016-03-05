# TheChikunTeam
Project Proposal for BIOL519

We will likely be working on a project looking at the CHikungunya virus and environmental transmission factors.

Main Question: 
What are the environmental factors that contribute to the increased probability of local transmission of the chikungunya virus?

Revised Question: 
Given the level of total preciptation and temperature, what is the likelihood that there will be predicted Chikungunya in a given area?

Additional Steps to take:
	1) Find the final source for the Chikungunya virus data - WHO, CDC
	2) Find an environmental data source (EPA, WHO, NOAA, CDC etc.) temperature, humidity, precipitation). - Alexandria 
	3) How do we scale down the amount of geographic information to countries or regions of the world instead of cities?
We also need to scale it down to a time period.  The data for each country has been taken on a month-to-month basis.

Climate data for temperature at the National Oceanic and Atmospheric Administration (NOAA) website: 
http://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCNDMS 

*Note that the climate data has to be requested and downloaded specific to each city we are using in our project.

THe Chikungunya virus information can be found at the Centers for Disease Control and Prevention data website:
https://data.cdc.gov/ . For a direct link to CHikungunya see: https://data.cdc.gov/browse?limitTo=datasets&tags=chikungunya+virus&utf8=%E2%9C%93


Juandalyn Burke and Alexandria Blake
BIOL 419/519
19 February 2016
Project Proposal

The Chikungunya virus, that causes fever and intense muscle pain, is transmitted to humans through bites by infected mosquitos. There is no known cure for this illness today and it is often misdiagnosed as dengue fever, as both diseases share many similar symptoms. The Chikungunya virus has in recent years spread from Africa, Asia, Europe and the Americas. Many of outbreaks of the virus have been in the tropical climates of Latin America and the Caribbean through the Aedes mosquitoes.  However, the Aedes mosquito can be found in any area of the world.  Thus, given the global changes in climate and daily unusual weather patterns, many areas of the world may be susceptible to hosting and spread the disease including areas of Europe and the United States. In our project, we plan to study the likelihood of the Chikungunya virus in select cities of the United States using temperature and precipitation data as predictors in comparison to other areas of the world.   

The datasets we intend to use in our project have been extracted from: (1) the Centers for Disease Control and Prevention (CDC), and (2) the National Oceanic Atmospheric and Administration (NOAA).  These datasets include:  Nowcast_Predictions_for_Local_Transmission_of_Chikungunya and city-wide climate datasets from matched cities in the local transmission of Chikungunya dataset.  The local transmission of Chikungunya dataset include the following parameters: the location, date by month, the probability of the average local transmission, the probability of the minimum local transmission, the probability of the maximum local transmission, and local cases.  The climate datasets, that we have to request and download, include the following parameters: monthly mean temperatures (MMNT) and total precipitation (TCPC).  

Thus, we plan to integrate these datasets to ask the following questions (1): Given the level of total precipitation and temperature, what is the likelihood that there will be predicted Chikungunya in a given area, and (2) Does this information compare to the same likelihoods for the areas of Latin America and the Caribbean?  We intend to use Matlab software to code the analysis portion of our dataset. We will use regression analysis to test for correlation of Chikungunya probability data with the temperature and precipitation data.  We then plan to perform a Principle Component Analysis (PCA) to investigate how well the climate data (i.e. temperature and precipitation) predict the likelihood of forecasting the Chikungunya virus in a given area of the United States. The data visualization for our project will include scatter plots displaying the correlation, and the PCA analysis results.  As a group, we plan to allocate efforts of gathering the information needed for the climate change data, as the data will be requested and downloaded from the NOAA website.  Then, we plan to begin the analysis portion of the project together through a face-to-face meeting, in case initial questions arise. Additional communication efforts will be conducted via GitHub, and face-to-face meetings, if needed. 


Code for Anaylyzing Data in Matlab

%%Barranquillo Columbia Climate Data from NOAA
figure
plot(MNTM,TPCP);
xlabel('Mean Monthly Temperature');
ylabel('Total Precipitation');

%%Sorting Barranquillo Data from Chikungunya Transmission Data
cities = cell2table(location);

%Preliminary Information for the Charleston, South Carolina dataset from NOAA
gscatter (data(:,3), data(:,2)); 
xlabel ('MNTM–Monthly mean temperature'); 
ylabel ('TPCP-Total precipitation amount for the month'); 
