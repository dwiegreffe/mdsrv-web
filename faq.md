---
title: MDsrv
---

### FAQ:

- [How can I import a structure?](#import-str)
- [How can I assign a trajectory to a structure?](#assign-str)
- [How can I visualize my trajectory?](#vis-tr)
- [How do I play my trajectory?](#play-tr)
- [How can I share the session I have prepared?](#share-session)
- [How can I share my trajectory?](#share-tr)
- [My trajectory is too large to be displayed and the viewer crashed.](#tr-large)
- [How do I install a MDsrv server on my machine (Setting up your own server and viewer)?](#install)
- [How do I add a trajectory to my own MDsrv server?](#import-tr-md)
- [How do I stream a trajectory from the MDsrv?](#stream)
- [Do I need a public IP to share data with the world?](#public) 
- [I developed a really nice representation and perspective on my trajectory. How do I save this and make it available for others?](#share) 
- [How to align two or more structures?](#align) 
- [How can I import an alignment?](#import-align) 
- [How can I plot distances/angles/dihedrals of selected atoms throughout my trajectories?](#distance-plot) 
- [How can I visualize trajectories that are stored on another server that is not an MDsrv?](#vis-other) 
- [Can I upload both my own and public data?](#data) 
- [How to upload local data (from my computer) to a running server?](#upload) 
- [How to upload data from other public servers (such as the Protein Data Bank)?](#upload-pdb) 
- [Do I have to install MDsrv myself to visualize and share my trajectories?](#install-myself) 

<details style=' border-style:solid border:2px '>
    <summary style='color:#159957'><big>
    How can I import a structure or trajectory? 
    </big></summary>

<p>
You can import a structure or trajectory by:
- providing the files from your local machine
    1. Open the Home panel on the left-hand side.
    2. Open the Open Local Files menu in the Home panel.
    3. Select Select files... to choose which of the files you have stored locally to upload.
        - You can import multiple files at once.
        - If you are importing multiple files at once, that do not have the same format, the Format option should be set to Auto.
        - If you are importing only one file at a time, or if all files have the same format, you can also specify the format of the file. However, in most cases, this is not necessary.
    4. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_local_files.png'>
            <source src='./videos/import_local_files.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using one of the common public servers (like PDB)
    1. Open the Home panel on the left-hand side.
    2. Open the Open Remote Structure menu in the Home panel.
    3. Select the server you want to download the structure or trajectory from as the Source.
    4. Enter the ID of the structure or trajectory you want to import from the selected server.
    5. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_structure_id.png'>
            <source src='./videos/import_structure_id.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using the URL of a structure or trajectory file that is publicly available on another server:
    1. Open the Home panel on the left-hand side.
    2. Open the Open Remote File menu in the Home panel.
    3. Enter the URL of the file.
    4. Select the correct format of the file for the Format parameter.
    5. Set the Binary parameter to On, if the file is binary.
    6. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_via_url.png'>
            <source src='./videos/import_via_url.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

**Note**: When you import a trajectory file, like an xtc, you must also import a structure to which the trajectory can be matched. Otherwise you will not be able to play the trajectory. To match the trajectory to a structure, see FAQ: How can I assign a trajectory to a structure?

</p>
</details>

<a name="import-str"></a>
## How can I import a structure or trajectory?

You can import a structure or trajectory by:
- providing the files from your local machine
    1. Open the Home panel on the left-hand side.
    2. Open the Open Local Files menu in the Home panel.
    3. Select Select files... to choose which of the files you have stored locally to upload.
        - You can import multiple files at once.
        - If you are importing multiple files at once, that do not have the same format, the Format option should be set to Auto.
        - If you are importing only one file at a time, or if all files have the same format, you can also specify the format of the file. However, in most cases, this is not necessary.
    4. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_local_files.png'>
            <source src='./videos/import_local_files.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using one of the common public servers (like PDB)
    1. Open the Home panel on the left-hand side.
    2. Open the Open Remote Structure menu in the Home panel.
    3. Select the server you want to download the structure or trajectory from as the Source.
    4. Enter the ID of the structure or trajectory you want to import from the selected server.
    5. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_structure_id.png'>
            <source src='./videos/import_structure_id.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using the URL of a structure or trajectory file that is publicly available on another server:
    1. Open the Home panel on the left-hand side.
    2. Open the Open Remote File menu in the Home panel.
    3. Enter the URL of the file.
    4. Select the correct format of the file for the Format parameter.
    5. Set the Binary parameter to On, if the file is binary.
    6. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_via_url.png'>
            <source src='./videos/import_via_url.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

**Note**: When you import a trajectory file, like an xtc, you must also import a structure to which the trajectory can be matched. Otherwise you will not be able to play the trajectory. To match the trajectory to a structure, see FAQ: How can I assign a trajectory to a structure?

<a name="assign-tr"></a>
## How can I assign a trajectory to a structure?

To match a trajectory to a structure, you must first import both ([How can I import a structure or trajectory?](#import-str)). 
1. Open the Home panel on the left-hand side.
2. Open the Assign Trajectory menu in the Home panel.
3. Select the structure and trajectory you want to match:
    - Model: the structure to which the trajectory should be matched
    - Coordinates: the trajectory you want to match to the structure
4. Select Apply.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/assign_trajectory_to_structure.png'>
            <source src='./videos/assign_trajectory_to_structure.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

<a name="vis-tr"></a>
## How can I visualize my trajectory?

To visualize your trajectory follow the following steps in the FAQs
- [How can I import a structure or trajectory?](#import-str)
- [How can I assign a trajectory to a structure?](#assign-str)
- [How do I play my trajectory?](#play-tr)

<a name="play-tr"></a>
## How do I play my trajectory?

You first need to import your trajectory ([How can I import a structure or trajectory?](#import-str)).
After you imported your trajectory, a play button will appear in the top left corner of the white canvas where the structure is displayed.

In case you provided the coordinate file of the trajectory yourself, you must first match it with a structure ([How can I assign a trajectory to a structure?](#assign-tr)).
After matching the trajectory, you need to clean up the visualization:
1. Open the State Tree panel on the left-hand side.
2. Toggle the visibility for the two imported files (same name as the original files).
Now only the matched result is visible in the representation.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/play_trajectory.png'>
            <source src='./videos/play_trajectory.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

<a name="share-session"></a>
## How can I share the session I have prepared?

You can share your your in two ways:

- Through our server:
    1. Import the structures and trajectories you want to share (see FAQs [How can I import a structure or trajectory?](#import-str), and [How can I assign a trajectory to a structure?](#assign-str)).
    2. Prepare your session as desired. 
    3. Open the Remote Session menu in the Extensions panel at the bottom.
    4. Name your session
        - Optional: Enter a description by opening the Options area.
        - Optional: Change the server address.
    5. Click the Upload button.
    6. To share your session with others, right-click your session to open it in a new tab with its URL.
    7. Share this URL.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/share_session_our_server.png'>
            <source src='./videos/share_session.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- Setting up your own MDsrv, see FAQs [How do I install a MDsrv server on my machine (Setting up your own server and viewer)?](#install).

<a name="share-tr"></a>
## How can I share my trajectory?

See FAQ: [How can I share the session I have prepared?](#share-session)

<a name="tr-large"></a>
## My trajectory is too large to be displayed and the viewer crashed.
	
To share large trajectories, you either need to set up your own server:
See FAQs 
- "How do I install a MDsrv server on my machine"
- "How do I add a trajectory to my own MDsrv server?"
- "How do I stream a trajectory from the MDsrv server?"

Or you can upload the trajectory to our server, so you can stream it frame by frame:
The trajectory you want to store on our server must be publicly available on another server.
1. Open the Extensions Panel at the bottom.
2. Open the Add Trajectory to Stream Server menu.
3. Optionally, if you want to upload the trajectory to another MDsrv instance, adjust the Servre parameter accordingly.
4. Enter the URL of the trajectory file.
5. Name the trajectory. (If there is already a trajectory with the same name, a message will appear in the Log panel. Please change the name.)
6. Add a more detailed description for your trajectory.
7. Select Upload Trajectory to Server.
8. When the trajectory is successfully uploaded, a message appears in the Log panel.
9. To visualize the uploaded trajectory, see FAQ: [How do I stream a trajectory from the MDsrv?](#stream).
Currently, only trajectories in the XTC format can be uploaded.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/upload_trajectory_server.png'>
            <source src='./videos/upload_trajectory_server.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

<a name="install"></a>
## How do I install a MDsrv server on my machine (Setting up your own server and viewer)?

See: [https://github.com/dwiegreffe/mdsrv](https://github.com/dwiegreffe/mdsrv) README.md

<a name="import-tr-md"></a>
## How do I add a trajectory to my own MDsrv server?

1. Add your trajectory into the trajectory folder of your server.
2. Update the trajectory_index.json. 
An entry has the following format:
```
{
    "timestamp": 123,
    "id": "example_id",
    "name": "example_name",
    "description": "example_description"
}
```

Whereas the id (example_id) must be the name of the trajectory file in the trajectory directory, and the id must be unique.
Currently, only trajectories in the XTC format can be streamed.

<a name="stream"></a>
## How do I stream a trajectory from the MDsrv?

1. Open the Extensions panel at the bottom.
2. Open the Match Trajectory Stream menu.
3. Enter the Server URL where the trajectory is stored (Must be an MDsrv instance).
4. Import the structure corresponding to the trajectory (see FAQ [How can I import a structure or trajectory?](#import-str)).
5. Select this structure via the Model parameter. 
6. Select the trajectory you want to stream via the Trajectory parameter.
7. Select Add Xtc Stream Trajectory.
8. You can now play your trajectory.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/match_stream_trajectory.png'>
            <source src='./videos/match_trajectory_stream.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

<a name="public"></a>
## Do I need a public IP to share data with the world?
	
To make your server globally visible you need a public IP. Otherwise it is only visible to devices within your local network.

<a name="share"></a>
## I developed a really nice representation and perspective on my trajectory. How do I save this and make it available for others?
	
See FAQ: [How can I share the session I have prepared?](#share-session)

<a name="align"></a>
## How to align two or more structures?

1. Import a Clustal alignment and the corresponding structures. 
2. Match the sequences of the alignment with the structures using the Match Sequence Alignment menu in the Extension Panel at the bottom. For each sequence in the alignment, you must specify which sequence of the structure should be matched to it (structure, entity, chain, and instance).
3. Click Apply Matching.
4. If the structures are correctly aligned, they will be overlaid according to the alignment.
5. If the matching is not correct, it is indicated which sequences of the alignment were not matched correctly in the Log at the bottom.

A guide with screenshots can be found at [Alignment View](alignment.html)

<a name="import-align"></a>
## How can I import an alignment?

Import the Clustal file (.als, .aln, or .clw) using the Open Files drop-down menu in the Home panel on the left-hand side. 

A guide with screenshots can be found at [Alignment View](alignment.html)

<a name="distance-plot"></a>
## How can I plot distances/angles/dihedrals of selected atoms throughout my trajectories?
	
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

<a name="vis-other"></a>
## How can I visualize trajectories that are stored on another server that is not an MDsrv?

You will need to download the trajectory to have it locally available on your computer. Then you can follow the steps in FAQ [How can I visualize my trajectory?](#vis-tr) to import it locally, or follow the steps in FAQs [How do I add a trajectory to my own MDsrv server?](#import-tr) to add the trajectory to your own MDsrv for streaming.

<a name="data"></a>	
## Can I upload both my own and public data?

Yes, you can upload your own and public data, see FAQ [How can I import a structure?](#import-str)

<a name="upload"></a>	
## How to upload local data (from my computer) to a running server?

To upload the data you have locally stored on your computer you first have to import the data into the client and prepare it to your desires. Then you can store this session on a running server by following the steps in FAQ [How can I share the session I have prepared?](#share-session)

<a name="upload-pdb"></a>	
## How to upload data from other public servers (such as the Protein Data Bank)?

See FAQ: [How can I import a structure?](#import-str)

<a name="install-myself"></a>
## Do I have to install MDsrv myself to visualize and share my trajectories?
	
No, you can use our server to visualize and share your trajectories. See FAQ: [How can I share my trajectory?](#share-tr)
