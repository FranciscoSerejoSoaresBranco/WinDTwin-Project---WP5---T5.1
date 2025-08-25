# WinDTwin-Project---WP5---T5.1
Interactive map for end-user location and needs for the Portuguese, UK and German coasts 



------ Offshore Wind Scouting Tool (OWST) ------


--- Objective ---

The OWST arises from the HORIZON project WinDTwin (https://windtwinproject.eu/), namely, task T5.1 – End user main requirements and overall prediction for long-term electricity prices and demand. 
The OWST is meant to output a comprehensive and high-level map which lists and responds to the main location requirements of relevant end-users in the offshore wind sector – such as operators, promoters and Engineering, Procurement, and Construction (EPC) companies –, in particular, for the specific geographies of Portugal, the United Kingdom (UK) and Germany. In this manner, it will help conduct the preliminary planning of novel offshore wind projects.


--- Software Requirements ---

- Python 3.11.9
- Python packages (can also be found in the "requirements.txt" file):
	- xarray==2024.1.1
	- requests==2.32.2
	- pydantic==2.6.0
	- numpy==1.26.4
	- netCDF4==1.7.2
	- pandas==2.2.0
	- h5netcdf==1.6.3
	- fastapi==0.109.0
	- cdsapi==0.7.3
	- uvicorn


--- Installation Steps ---

1) Download the windtwint51-api folder, which has the windtwint51-api.tar file inside
2) Open Docker Desktop (if software is not yet installed, install it via https://www.docker.com/products/docker-desktop/)
3) Open the Command Prompt and type: \
cd [windtwint51-api folder directory]
4) Load the Docker image: \
docker load < windtwint51-api.tar
5) Run the Docker container: \
docker run -d -p 8000:8000 windtwint51-api
6) Open the OWST in your browser, by typing the following link: 
localhost:8000

The OWST should now be up and running.


--- Layout ---

Inside the OWST, one can find:

- Brief description of the tool.
- Tool's modules "Post" methods.
- Input and output data schema for each of the tool's modules.
  
The OWST encompasses the following modules:

1) Offshore wind farm information.
2) Underwater power cable information.
3) Nearby ports.
4) Capital expenditure and levelised cost of energy.
5) Support schemes.
6) Legal and regulatory information.
7) Electricity demand, renewable curtailment and hybridization.
8) Electricity price.
9) Wind speed.
10) Seabed depth.

Each module is comprised of:

- Introductory section:
	- Title (e.g., 1. Offshore Wind Farm Information).
	- Application Programming Interface (API) endpoint path (e.g., /offshore_wind_farm_information/)
	- Summary description (e.g., Acquire offshore wind farm information for a user-selected range).
	- Extensive description, including bounding box constraints (e.g., Acquire the region, name, power output, status, distance to coast and coordinates of offshore wind farms in a user-selected range. The module's bounding box is [min_lon, max_lon, min_lat, max_lat] = [-10.32, 24.9, 39.72, 65.59]).
- Request body:
	- List of example requests (e.g., North Sea (Segment), Baltic Sea (Segment), Mediterranean Sea (Segment), Portugal, UK (Segment), Germany).
	- Value for the selected example request.
	- Input data schema.
	- Description of the selected example request.
- Response list:
	- Response command Uniform Resource Locator (URL).
	- Request URL.
	- Response code, body and headers.
	- Successful response code and example value.
	- Output data schema.

In the specific case of the "Legal and regulatory information" module, there are vast possible combinations for the domain, sub-domain and sub-sub-domain, which are shown here:

- Germany:
	- Players:
		- Government Ministry / Department:
			- Energy
		- Industrial / Professional Association:
			- Health and Safety
			- Maritime
		- Public Agency / Authority:
			- Environment
			- Health and Safety
			- Maritime
		- Regulator:
			- Energy
		- Standardization & Technical Body:
			- Energy
			- Health and Safety
			- Maritime
	- Consenting:
		- Certifications & Requirements:
			- Electrical & Control Systems
			- Offshore Logistics & O&M
			- Safety and Security
			- Structural Design & Materials
			- Procurement
		- One-Stop Shop 
		- Standards & Technical Brochures:
			- Electrical & Control Systems
			- Offshore Logistics & O&M
			- Procurement
			- Safety and Security
			- Structural Design & Materials
	- Laws & Regulation:
		- Guidelines & Recommendations:
			- Energy
			- Environment
			- Health and Safety
			- Maritime
		- Legally Binding Instruments:
			- Energy
			- Environment
			- Health and Safety
			- Maritime
			- Procurement
     
- Portugal:
	- Players:
		- Government Ministry / Department:
			- Energy
			- Maritime
		- Industrial / Professional Association:
			- Energy
			- Maritime
		- Public Agency / Authority:
			- Energy
			- Environment
			- General
			- Maritime
		- Regulator:
			- Energy
		- Standardization & Technical Body:
			- Energy
			- Health and Safety
			- Maritime
	- Consenting:
		- Certifications & Requirements:
			- Procurement
		- Licenses:
			- Energy
			- Maritime
		- One-Stop Shop 
		- Standards & Technical Brochures:
			- Electrical & Control Systems
			- Offshore Logistics & O&M
			- Procurement
			- Safety and Security
			- Structural Design & Materials
	- Laws & Regulation:
		- Guidelines & Recommendations:
			- Energy
			- Environment
			- Maritime
		- Legally Binding Instruments:
			- Energy
			- Environment
			- Health and Safety
			- Maritime
			- Procurement

- UK:
	- Players:
		- Government Ministry / Department:
			- Energy
			- Environment
		- Public Agency / Authority:
			- Energy
			- Environment
			- Maritime
		- Regulator:
			- Energy
			- Health and Safety
		- Standardization & Technical Body:
			- Energy
			- Health and Safety
			- Maritime
	- Consenting:
		- Certifications & Requirements:
			- Offshore Logistics & O&M
			- Quality, Asset & Environmental Management
			- Safety and Security
			- Structural Design & Materials
			- Procurement
		- Licenses:
			- Energy
			- Maritime
		- One-Stop Shop 
		- Standards & Technical Brochures:
			- Electrical & Control Systems
			- Offshore Logistics & O&M
			- Procurement
			- Safety and Security
			- Structural Design & Materials
	- Laws & Regulation:
		- Guidelines & Recommendations:
			- Energy
			- Environment
			- Health and Safety
			- Maritime
		- Legally Binding Instruments:
			- Energy
			- Environment
			- Health and Safety
			- Maritime
			- Procurement


--- Navigation ---

To use the tool, carry out the following steps:

1) Expand the module you intend to use by clicking on the downwards arrow corresponding to said module.
2) Open the request body by clicking on the "Try it out" button.
	2.1) Should you wish to use one of the predefined example requests, click on the downwards arrow within the "Examples:" list, then click on the example request you wish to activate.
	2.2) Should you wish to introduce a custom request body, you can alter it manually by writing over the displayed request body.
3) Carry out the request by clicking on the "Execute" button. You should now be responded with a "Loading" message.
4) Copy or download the response body by clicking on the Clipboard icon or the "Download" button, respectively (note that you can also copy the API endpoint path and command URL by clicking the Clipboard icon in their respective sections).
