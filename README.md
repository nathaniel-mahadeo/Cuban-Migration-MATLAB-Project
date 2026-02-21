Cuban Migration Analysis Project
This project explores the waves of Cuban immigration to the United States, specifically focusing on the period between 1961 and 1963. 
It utilizes MATLAB to visualize the geographical distribution of refugees across the U.S. and analyzes the rates of registration versus resettlement over time.

The project is contextualized by a qualitative analysis (found in Cuban Data Analysis) involving interviews with first-generation immigrants like Marcello Santana-Aubert, 
bridging the gap between "big data" and individual lived experiences.

Project Structure
1. Data Visualizations
CubanMap.m: The primary mapping script. It generates a choropleth map of the United States, shading states based on refugee population density.
It uses a custom 8-step blue gradient (from light to deep blue) to represent counts ranging from <100 to >20,000.

CubanRegistration.m: Analyzes resettlement efficiency. 
It plots time-series data comparing the number of persons registered versus those successfully resettled on a weekly and monthly basis for 1961, 1962, and 1963.

2. Data Sources
CubanMapData.xlsx: Contains state-level refugee counts (e.g., New York: 21,411; Florida: 903—based on specific historical snapshots).

CubanResettlementfigures.xlsx: Detailed monthly and weekly breakdown of "Persons Registered," "New Arrivals," and "Persons Resettled."

3. Mapping Utilities
The project relies on a suite of mapping functions (originally developed by Chad A. Greene) to render geographical boundaries without requiring the full MATLAB Mapping Toolbox for all operations:

borders.m / bordersm.m: Standard and map-projection-based boundary plotting.

labelborders.m / labelbordersm.m: Functionality for adding state/country labels.

borderdata.mat: The coordinate data required to draw the U.S. and state lines.

4. Qualitative Research
Cuban Data Analysis: A research paper providing the historical and personal context for the data.
It discusses the "common threads" identified in the immigration and assimilation process of Caribbean subgroups in Florida and beyond.

Getting Started
Prerequisites
MATLAB: The scripts were developed for a standard MATLAB environment.

Mapping Toolbox (Optional but Recommended): bordersm.m and CubanMap.m utilize map projections that function best with the toolbox, though borders.m is provided as a fallback.

Instructions
Map Visualization: Run CubanMap.m. Ensure CubanMapData.xlsx and borderdata.mat are in the same directory. This will produce:

A color-coded map of the U.S.

A separate legend figure defining the "Refugee Count" brackets.

Trend Analysis: Run CubanRegistration.m. This will generate three figures (1961, 1962, 1963) comparing registration and resettlement trends.

Data Legend (Geographical)
Light Blue: < 100 refugees

Medium Blue: 1,000 - 4,999 refugees

Deep Blue: > 20,000 refugees

Credits
Mapping Functions: Based on the Borders script by Chad A. Greene.

Research & Analysis: Data compiled for the Metoyer Lab RAG Project, focusing on Caribbean immigration trends.
