# Visual-Representation-of-UN-CO2-data-public
(This is the public facing version with no source code, Please email/message for source code!)

This Program is an assignment from my Advanced Python Programming Course, which is why it is a private repository. This assignment demonstrates my ability to develop a concurrent python program that can obtain data from an XML file, store that said data in a SQL database, then, access that database by controlling a server layer through the utilization of WebSockets, and lastly, plot the data received as a medium to display the data.

When the program starts it scrapes an XML file and stores data in an SQLite Database. it produces a Tkinter Gui that has a pull-down menu with a list of Countries. When a country is requested, the server layer which controls access to SQLite Database has launched and waits for a request from Client Socket. The Client socket takes in the parameter of Country and sends a request for data from Server Layer. Server Layer sends Data back from SQLite as JSON string to Client Socket, which produces XY plot of the requested country using Matplotlib. Upon closing of GUI window, the Server Layer is turned off and the SQLite Database is emptied.

Here is what the Tkinter Gui looks like.
![Screen Shot 2022-07-18 at 12 02 41 PM](https://user-images.githubusercontent.com/54960376/179603438-3213bdee-a280-42e9-b8d4-711c26893386.png)

The scroll down menu contains all the countries listed in the xml. My cursor was hovering over Australia.

![Screen Shot 2022-07-18 at 12 02 49 PM](https://user-images.githubusercontent.com/54960376/179603873-a53672e8-1e3e-42c4-9d72-78a50ebf4627.png)

Upon Selecting Australia, the Client socket sends a request for Australia's CO2 data from the Server Layer, where the server Layer searches and returns the Country's information from SQLite Database to the Client Socket. Once the information is received, the CO2 data is plotted using Matplotlib as CO2 data over the years. The graph can be closed and another Country can be selected.
![Screen Shot 2022-07-18 at 12 32 12 PM](https://user-images.githubusercontent.com/54960376/179605013-5bd9cf24-7ef3-4466-bf5a-2d26febb593e.png)

Thank you for viewing my project!
