---
title: MDsrv
---

### FAQ:

#### How can I import a structure?

You can import a structure by

- providing the structure from your local machine
1. Open the Home panel on the left-hand side.
2. Open the Open Files menu in the Home panel.
3. Select Select files... to upload the files you have stored locally.
4. Select Apply.

- using one of the common public servers
1. Open the Home panel on the left-hand side.
2. Open the Download Structure menu in the Home panel.
3. Select the server you want (Source).
4. Enter the id of the structure you want to import from the selected server.
5. Select Apply.

- using any URL of servers where data is available
1. Open the Home panel on the left-hand side.
2. Open the Download Structure menu in the Home panel.
3. Select URL as the Source.
4. Enter the URL of the file you want to import.
5. Select Apply.


#### How can I import a trajectory?

You can import a trajectory by
- importing it from a public server (see FAQ "How can I import a structure?")
- providing the trajectory file yourself (see FAQ "How can I import a structure?") 
However, you also need to import a structure so that the trajectory can be matched to it. To match the trajectory to a structure, see FAQ "How can I assign a trajectory to a structure?".

#### How can I assign a trajectory to a structure?

To match a trajectory to a structure, you must first import both (see FAQs "How do I import a structure?" and "How do I import a trajectory?"). 
1. Open the Home panel on the left-hand side.
2. Open the Add Trajectory menu in the Home panel.
3. Select the structure and trajectory you want to match:
- Model: the structure to which the trajectory should be matched
- Coordinates: the trajectory you want to match to the structure
4. Select Apply.

#### How can I visualize my trajectory?

To visualize your trajectory follow the following steps in the FAQs
- "How can I import a trajectory?"
- "How can I assign a trajectory to a structure?"
- "How do I play my trajectory?"

#### How do I play my trajectory?

You first need to import your trajectory (see FAQ "How can I visualize my trajectory?").
After you imported your trajectory, a play button will appear in the top left corner of the white canvas where the structure is displayed.

#### How can I share the session I have prepared?

You can share your session in several ways:

Through our server:
1. Import the structures and trajectories you want to share (see FAQs "How can I import a structure?", "How can I import a trajectory?", and "How can I assign a trajectory to a structure?").
2. Prepare your trajectory as desired. 
3. Open the Remote Session drop-down menu in the Extensions panel at the bottom.
4. Name your session
5. Optional: Enter a description by opening the Options area.
6. Optional: Change the server address.
7. Click the Upload button
8. To share your session with others, right-click your session to open it in a new tab with its URL and share that URL.

A guide with screenshots can be found at [Remote Sessions](remote.html)

Setting up your own MDsrv, see FAQs "How do I install a MDsrv server on my machine".

#### How can I share my trajectory?

See FAQ: "How can I share the session I have prepared?"

#### My trajectory is too large to be displayed and the viewer crashed.
	
To share large trajectories, you need to set up your own server. 
See FAQs 
- "How do I install a MDsrv server on my machine"
- "How do I add a trajectory to my own MDsrv server?"
- "How do I stream a trajectory from the MDsrv server?"

#### How do I install a MDsrv server on my machine (Setting up your own server and viewer)?

See: [https://github.com/dwiegreffe/mdsrv](https://github.com/dwiegreffe/mdsrv) README.md

#### How do I add a trajectory to my own MDsrv server?

1. Add your trajectory into the trajectory folder of your server.
2. Update the trajectory_index.json. 
An entry has the following format:
{
    "timestamp": 123,
    "id": "example_id",
    "name": "example_name",
    "description": "example_description"
 }
Whereas the id (example_id) must be the name of the trajectory file in the trajectory directory, and the id must be unique.
Currently, only trajectories in the XTC format can be streamed.
	
#### How do I stream a trajectory from the MDsrv?

1. Open the Extensions panel at the bottom.
2. Open the XTC Stream Trajectory menu in the Extensions panel.
3. Enter the Server URL where the trajectory is stored (Must be an MDsrv instance).
4. Select the trajectory you want to stream via the Trajectory parameter.
5. Import the structure corresponding to the trajectory (see FAQ "How can I import a structure?")
6. Select this structure via the Model parameter. 
7. Select Add Xtc Stream Trajectory.


#### Do I need a public IP to share data with the world?
	
To make your server globally visible you need a public IP. Otherwise it is only visible to devices within your local network.

#### I developed a really nice representation and perspective on my trajectory. How do I save this and make it available for others?
	
See FAQ: "How can I share the session I have prepared?"

#### How to align two or more structures?

1. Import a Clustal alignment and the corresponding structures. 
2. Match the sequences of the alignment with the structures using the Match Sequence Alignment menu in the Extension Panel at the bottom. For each sequence in the alignment, you must specify which sequence of the structure should be matched to it (structure, entity, chain, and instance).
3. Click Apply Matching.
4. If the structures are correctly aligned, they will be overlaid according to the alignment.
5. If the matching is not correct, it is indicated which sequences of the alignment were not matched correctly in the Log at the bottom.

A guide with screenshots can be found at [Alignment View](alignment.html)

#### How can I import an alignment?

Import the Clustal file (.als, .aln, or .clw) using the Open Files drop-down menu in the Home panel on the left-hand side. 

A guide with screenshots can be found at [Alignment View](alignment.html)

#### How can I plot distances/angles/dihedrals of selected atoms throughout my trajectories?
	
1. Import your trajectory.
2. Open the Structure Tools panel on the right side.
3. Open the Measurements menu in the Structure Tools panel.
4. Select the Add button in the Measurements menu.
5. Activate the selection mode by clicking the last button of the buttons on the right side of the white canvas where the structure is displayed (Toggle selection mode). 
6. An additional menu appears at the top of the white canvas.
7. Select the button labeled Residue to change the granularity of the selection.
8. Select the desired elements to add a measurement (two for distance, three for angle, four for area angle). The selected elements will be displayed in the Measurements menu. 
9. Select the desired measurement in the Measurements menu to add it. 
10. Open the Extensions field at the bottom.
11. Open the Measurement Line Plot menu in the Extensions panel. 
12. Select the measurement you just added to display its plot throughout the trajectory.

A guide with screenshots can be found at [Distance Plots](distances.html)

#### How can I visualize trajectories that are stored on another server that is not an MDsrv?

You will need to download the trajectory to have it locally available on your computer. Then you can follow the steps in FAQ “How can I visualize my trajectory?” to import it locally, or follow the steps in FAQs "How do I add a trajectory to my own MDsrv server?" to add the trajectory to your own MDsrv for streaming.
	
#### Can I upload both my own and public data?

Yes, you can upload your own and public data, see FAQ "How can I import a structure?"

#### How to upload local data (from my computer) to a running server?

To upload the data you have locally stored on your computer you first have to import the data into the client and prepare it to your desires. Then you can store this session on a running server by following the steps in FAQ "How can I share the session I have prepared?"

#### How to upload data from other public servers (such as the Protein Data Bank)?

See FAQ: "How can I import a structure?"

#### Do I have to install MDsrv myself to visualize and share my trajectories?
	
No, you can use our server to visualize and share your trajectories. See FAQ: "How can I share my trajectory?"
