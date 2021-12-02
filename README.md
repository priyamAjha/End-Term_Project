# End-Term_Project

Description:

- Tick stack is used to handle time-series data. 
- Data are sent to Telegraph and stored in an InfluxDB database. Chronograf can query the database through a web interface. Kapacitor can process, monitor, and raise alerts based on the data.
- Created tick.yml file and it explains about the components of the stack and also about there connection. 
- For Telegraf port 8186:8186 was configured and used to ingest data.  
- For chronograf port 8888:8888 was configured which is used to visualize the data and is available through a web interface on local port 8888.


- Configuration of Telegraf was provided through a Docker Config object which was created in telegraf.conf file and it has following specifications:
  - It defines an agent that gathers host CPU metrics on a regular basis.
  - It defines an additional input method allowing Telegraf to receive data over HTTP.
  - It specifies the name of the database where the data collected will be stored.

 Used Swarm to deploy the Tick Stack
- First I Setup the local swarm environment to deployed the TICK stack as a Docker stack. It created a network for communication between the application containers, a Config object containing the Telegraf configuration and the 4 services composing the TICK stack.

- I used lucj/genx Docker image to generate data and then send the data to the Telegraf HTTP endpoint. 


Link : https://youtu.be/y5tBsaMrRHA 


