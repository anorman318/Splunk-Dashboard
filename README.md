# Splunk-Dashboard
Designed a single dashboard to view all the data visualizations in a single location
  
**Background**  
Assuming the role of SOC manager at Omni Medical Products  
* The Networking team notified you about performance issues that OMP's public-facing website experienced over the weekend.
* The team discovered that these issues were caused by an attacker flooding the web server with POST requests.
* As the SOC manager, you would like to build visualizations that your SOC team can use to determine the severity of the attack. These visualizations will help your SOC quickly and accurately respond to attacks.
* Your networking team provided you with a log file of two hours of normal activity for you to analyze.

Single Value Visualization:  
1. Within Splunk design a search to view the POST events for the time range of "All TIME", using the following fields:  
    * source="radialgauge.csv"
    * http_method=POST
    * stats count as total

2. Design a radial gauge to visualize the data.  
  * Your Networking team notified you that they received approximately 1,200 POST requests during a 2 hour period of the attack.
  * Design a radial gauge with the following criteria:  
      * Count of total POST requests  
      * Three different color settings: green, yellow, and red.  
      * Select the appropriate ranges for each color setting, use your best judgement!  
      
 3. Save your visualization as a report titled: "Radial Gauge - POST request monitor.":   
 <img width="920" alt="radial_guage_source" src="https://user-images.githubusercontent.com/106919343/200923445-d3e4da58-01b4-40b7-847b-cc1ba4b5dae5.png">  
 
Multiple Value Visualization:  
* Your team would like you create a visualization that displays the exact URL paths being targeted by attacks.  
* You are tasked with designing a multiple value visualization to display the URL paths being targeted by the POST requests.  

1. Design an SPL query with the following fields:  
    * source="radialgauge.csv"  
    * http_method=POST  

2. Add the top command to display the top 10 URI paths (uri_path).  

3. Visualize the data in a pie chart.  

4. Save your visualization as a report titled: "Pie Chart - Top 10 URI_PATH."  
<img width="913" alt="pie_chart_source" src="https://user-images.githubusercontent.com/106919343/200923859-8379263d-3701-4400-8425-f6b5c7388baf.png">  

Geographic Map Visualization:  
* OMP would like you to expand your visualizations to provide more geographic information about the attacks.  
* The Security team can use this information to create firewall rules that restrict traffic from certain geographic locations.  
* You are tasked with designing a geographic map visualization to help your SOC team understand where attacks are originating.  

1. Design a geographic map that displays a visualization of source IP address locations. Use the following fields:  
    * source="radialgauge.csv"  
    * http_method=POST  

2. Save your visualization as a report titled: "Geographic Map - POST request monitor by Source IP."  
<img width="913" alt="map_source" src="https://user-images.githubusercontent.com/106919343/200924297-57231544-36ce-4054-bf1a-9f2d5e6f2867.png">  

Dashboard: 
1. Design a dashboard that contains the previously created radial gauge, pie chart, and map.  

2. Add a fourth visualization that contains a statistical report representing the data from the pie chart.  
    * Place this report directly next to the pie chart.  
    
    <img width="909" alt="dashboard1" src="https://user-images.githubusercontent.com/106919343/200924487-0083db27-ac7e-43ea-979b-dc5835378d9c.png">  
    <img width="903" alt="dashboard2" src="https://user-images.githubusercontent.com/106919343/200924509-00a9888a-e8cb-447a-a143-1e14d40616d5.png">  


 
