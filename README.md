# node-red-contrib-dashboard-average-bars
Calculate and display the average values of msg.payload in a bar chart.

Important :
The average-bars node is simply and necessarily linked to the node-red dashboard template node. The average-bars node create the input msg of the template node and the template node display the chart.


Note :
Average-bars node values can be cleared by sending the string "clear" in the msg.payload. 
Node-red reboot: keep the node values by storing the context values ( see contextStorage attribute in settings.js )


Node properties :

X-axis :
- last hour : 1 bar per minute
- last day : 1 bar per hour
- last week : 1 bar per day
- last month : 1 bar per day
- last year : 1 bar per month
- msg.topic : 1 bar for each msg.topic
  
Y-axis : is calculated according to the msg.payload received.

Bar style :
- rectangle : classical bar
- equalizer : equalizer bar style

Bar colors : choice the color gradient of the bars

Display values : check boxes to display or hide values :
- bar values : value above the bar
- x-axis values : period values (or msg.topic if x-axis = msg.topic )
- last value : the last msg.payload received
- chart average : the average of all values received
- chart minimum : the minimum of all values received
- chart maximum : the maximum of all values received

Unit : unit to display behind values

Decimals : number of decimals to display

Font color : color of the scale and the values
