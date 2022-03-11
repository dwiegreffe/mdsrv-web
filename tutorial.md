---
title: MDsrv
---

# Tutorials

<a name='t-import'></a>
<details>
    <summary>Importing structures and trajectories</summary>
<p><div markdown="1">

You can import a structure or trajectory by:
- providing the files from your local machine
    1. Open the _Home_ panel on the left-hand side.
    2. Open the _Open Local Files_ menu in the Home panel.
    3. Select _Select files..._ to choose which of the files you have stored locally to upload.
        - ou can import multiple files at once.
        - If you are importing multiple files at once, that do not have the same format, the Format option should be set to Auto.
        - If you are importing only one file at a time, or if all files have the same format, you can also specify the format of the file. However, in most cases, this is not necessary.
    4. Select the _Apply_ button.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_local_files.png'>
            <source src='./videos/import_local_files.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using one of the common public servers (like PDB)
    1. Open the _Home_ panel on the left-hand side.
    2. Open the _Open Remote Structure_ menu in the Home panel.
    3. Select the server you want to download the structure or trajectory from as the _Source_.
    4. Enter the ID of the structure or trajectory you want to import from the selected server.
    5. Select the _Apply_ button.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_structure_id.png'>
            <source src='./videos/import_structure_id.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- using the URL of a structure or trajectory file that is publicly available on another server:
    1. Open the _Home_ panel on the left-hand side.
    2. Open the _Open Remote File_ menu in the Home panel.
    3. Enter the _URL_ of the file.
    4. Select the correct format of the file for the _Format_ parameter.
    5. Set the _Binary_ parameter to On, if the file is binary.
    6. Select the _Apply_ button.
    
<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/import_via_url.png'>
            <source src='./videos/import_via_url.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

**Note**: When you import a trajectory file, like an xtc, you must also import a structure to which the trajectory can be matched. Otherwise you will not be able to play the trajectory. To match the trajectory to a structure, see FAQ: How can I assign a trajectory to a structure?

</div></p></details>

<a name='t-assign-traj'></a>
<details>
    <summary>Assign a trajectory to a structure</summary>
<p><div markdown="1">

To match a trajectory to a structure, you must first import both (<a href="#t-import">Importing structures and trajectories</a>).
1. Open the _Home_ panel on the left-hand side.
2. Open the _Assign Trajectory_ menu in the Home panel.
3. Select the structure and trajectory you want to match:
    - _Model_: the structure to which the trajectory should be matched
    - _Coordinates_: the trajectory you want to match to the structure
4. Select the _Apply_ button.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/assign_trajectory_to_structure.png'>
            <source src='./videos/assign_trajectory_to_structure.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</div></p></details>

<a name='t-play'></a>
<details>
    <summary>Play trajectory</summary>

<p><div markdown="1">

You first need to import your trajectory (<a href="#t-import">Importing structures and trajectories</a>).
After you imported your trajectory, a play button will appear in the top left corner of the white canvas where the structure is displayed.

In case you provided the coordinate file of the trajectory yourself, you must first match it with a structure (<a href="#t-assign-traj">Assign a trajectory to a structure</a>).

After matching the trajectory, you need to clean up the visualization:
1. Open the _State Tree_ panel on the left-hand side.
2. Toggle the visibility for the two imported files (same name as the original files).
    - The visibility toggle is the outermost button on the right side and has an eye symbol.

Now only the matched result is visible in the representation.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/play_trajectory.png'>
            <source src='./videos/play_trajectory.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</div></p></details>

<a name='t-share-session'></a>
<details>
    <summary>Sharing a session</summary>

<p><div markdown="1">

You can share your your in two ways:

- Through our server:
    1. Import the structures and trajectories you want to share
        See Tutorials
        - <a href="#t-import">Importing structures and trajectories</a>
        - <a href="#t-assign-traj">Assign a trajectory to a structure</a>
    2. Prepare your session as desired.
    3. Open the _Remote Session_ menu in the _Extensions_ panel at the bottom.
    4. Name your session.
        - Optional: Enter a description by opening the _Options_ area.
        - Optional: Change the server address.
    5. Select the _Upload_ button.
    6. To share your session with others, right-click your session to open it in a new tab with its URL.
    7. Share this URL.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/share_session_our_server.png'>
            <source src='./videos/share_session.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

- Setting up your own MDsrv, see <a href="install.html#install">How do I install a MDsrv server on my machine (Setting up your own server and viewer)?</a>.

</div></p></details>

<a name='t-upload-traj'></a>
<details>
    <summary>Upload a trajectory to the MDsrv</summary>
<p><div markdown="1">

The trajectory you want to store on our server must be publicly available on another server.

1. Open the _Extensions_ panel at the bottom.
2. Open the _Add Trajectory to Stream Server_ menu.
3. Optionally, if you want to upload the trajectory to another MDsrv instance, adjust the _Server_ parameter accordingly.
4. Enter the _URL_ of the trajectory file.
5. Name the trajectory. (If there is already a trajectory with the same name, a message will appear in the Log panel. Please change the name.)
6. Add a more detailed description for your trajectory.
7. Select the _Upload Trajectory to Server_ button.
8. When the trajectory is successfully uploaded, a message appears in the Log panel.
9. To visualize the uploaded trajectory, see the Tutorial <a href="#t-stream-traj">Stream a trajectory from the MDsrv</a>).

Currently, only trajectories in the XTC format can be uploaded.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/upload_trajectory_server.png'>
            <source src='./videos/upload_trajectory_server.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</p>
</details>

<a name='t-stream-traj'></a>
<details>
    <summary>Stream a trajectory from the MDsrv</summary>
<p><div markdown="1">

1. Open the _Extensions_ panel at the bottom.
2. Open the _Match Trajectory Stream_ menu.
3. Enter the _Server_ URL where the trajectory is stored (Must be an MDsrv instance).
4. Import the structure corresponding to the trajectory (see Tutorial <a href="#t-import">Importing structures and trajectories</a>).
5. Select this structure via the _Model_ parameter.
6. Select the trajectory you want to stream via the _Trajectory_ parameter.
7. Select _Add Stream Trajectory_.
8. You can now play your trajectory.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/match_stream_trajectory.png'>
            <source src='./videos/match_trajectory_stream.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</div></p></details>

<a name='t-alignment'></a>
<details>
    <summary>Superpose structures based on a sequence alignment</summary>
<p><div markdown="1">

1. Import a Clustal alignment (_.aln_) using the _Open Local Files_ menu.
2. Import the structures corresponding to the sequences in the alignment.
3. Match the sequences of the alignment with the structures using the _Match Sequence Alignment_ menu in the _Extension_ panel at the bottom.
    - For each sequence in the alignment, you must specify which sequence of the structure should be matched to it.
    - Each sequence needs its own structure.
    - Match the following parameters for each sequence in the alignment:
        - Structure
        - Entity
        - Chain
        - Instance (if available)
4. Select the _Apply Matching_ button.
    - If the structures are correctly matched, they will be superposed according to the alignment.
    - If the matching is not correct, it is indicated which sequences of the alignment were not matched correctly in the Log at the bottom.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/alignment.png'>
            <source src='./videos/alignment.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</div></p></details>

<a name='t-plot'></a>
<details>
    <summary>Add a time-trace plot of a measurement for a trajectory</summary>
<p><div markdown="1">

1. Import the trajectory you want to calculate the measurement for.
    See Tutorials
    - <a href="#t-import">Importoing structures and trajectories</a>
    - <a href="#t-assign-traj">Assign a trajectory to a structure</a>
2. Clean up the visualization by toggling the visibility for the importet files in the _State Tree_ panel on the left side.
3. Open the _Structure Tools_ panel on the right side.
4. Open the _Measurements_ menu in the Structure Tools panel.
5. Select the _Add_ button in the Measurements menu.
6. Activate the selection mode by clicking the last button of the buttons on the right side of the white canvas where the structure is displayed (_Toggle Selection Mode_).
7. An additional menu appears at the top of the white canvas.
8. Select the button labeled _Residue_ to change the granularity of the selection.
9. Select the desired elements to add a measurement (two for distance, three for angle, four for area angle). The selected elements will be displayed in a list in the _Measurements_ menu on the right side.
10. Select the desired measurement in the _Measurements_ menu to add it. 
11. Click the _Toggle Selection Mode_ button again, to exit the selection mode.
12. Open the _Extensions_ panel at the bottom.
13. Open the _Time-trace Plot_ menu.
14. Select the measurement you just added to display its plot throughout the trajectory.

There are various interaction possible:
- Skipping to a specific frame by clicking on the value
- Sorting the values by frame, ascending, and descending
- Filtering the values
- Switching the display to RMSD for the whole model
    - Instead of a filter, it is now possible to change he comparison frame for the RMSD

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/plot.png'>
            <source src='./videos/plot.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

</div></p></details>