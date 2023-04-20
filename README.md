# Vendee-Globe-Business-Case

In 1989, Philippe Jeantot established the Vendée Globe, a yacht race around the world that is solo and non-stop. Held once every four years, it is recognized as an extremely challenging feat of individual perseverance and the ultimate examination of oceanic racing. The most recent edition of the Vendée Globe, the 9th one, was conducted during 2020-2021 and was conquered by Yannick Bestaven, a French sailor who circumnavigated the globe non-stop in slightly over 80 days. Throughout the race, viewers were able to monitor the progress live through an online racing dashboard, thanks to Nokia, which provided the technology for tracking the boats in real-time.

In this business case, we will assume the role of Nokia and build a cloud-based Lambda Architecture on Azure to process telemetry data from sailing boats. Our architecture will include a real-time path for processing sailing boat data in real time, and a batch-processing path for collecting sailing boat data in batches and performing calculations on those batches.

The Lambda Architecture will send all boat data to a PowerBI dashboard. The dashboard will display a world map with the current position of each boat and a table with a ranking of racing teams, sorted by who is currently in the lead.

As we are currently between races, we cannot use the actual data from the boats participating in the race. Instead, we will use a Python simulator that will simulate boat telemetry data from a fleet of 10 race participants.

To complete this business case, we will need to do the following:

  1. Create a Lambda Architecture in Azure with a real-time path and a batch-processing path. Our architecture should include an Event Hub, a Stream Analytics Job, and        an output to PowerBI. Our batch-processing path can use any data storage service we prefer: a Data Lake, a SQL Database, a Cosmos database, or a Synapse Analytics        Workspace.
  2. Create a PowerBI dashboard that displays a world map with the current location of each racing team and a table with the teams ranked by position in the race.
  3. Download the Python race simulation app to our local computer. Configure the app to send data to our EventHub.
  4. Start the Python app. Every 60 seconds, the telemetry of the simulated racing boats will be sent to our Azure cloud.

We will have completed the business case if our PowerBI dashboard correctly shows the position and ranking of each sailing team in the race.
