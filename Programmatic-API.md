The API is designed to control the your station from a script running on your computer. You can control all the parameters of your station and even get data from the API.

We are still testing this feature and it will be released in the next weeks.

## * **Why I cannot cannot access to the MQTT server as I did before?**
The access to the mqtt server like we did previously was a really bad hack. It's essentially a man in the middle in the server-station protocol. In the new version, the server has way more awareness of the station status in order to be able, for example, of continuously change the parameters of the stations with "AutoTune" enabled to receive the most probable satellite based on TLEs and also to show all the station information on the web application in real time.

These new features open a lot of very interesting posibilites, but the server needs to be always in sync with the info in the stations. If there is other mqtt clients injecting traffic on the same channel that the server uses to communicate to the stations it all becomes chaotic. 

**What is the alternative?**
First, provide an user friendly interface to visualize all the parameters of the station in real time (including junk packets, errors, etc.). The web panel: https://tinygs.com/stations This panel also allow editing all the possible parameters of the station when you are logged in on the panel.

Second, provide a proper programmatic API so that it is possible for anyone to make an script to get the data and interact with the system. This API runs against the server and makes it aware of the changes so it can take them into account. For example if the the frequency of a sation is changed, it knows it and adjusts accordingly.

