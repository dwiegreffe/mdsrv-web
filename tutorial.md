---
title: MDsrv
---

# Tutorials

<details markdown='1' style='border:solid; border-color:#159957; border-width:2px; border-radius:5px; padding: 10px 15px 10px 15px;'>
    <summary markdown='span' style='cursor:pointer; display:list-item; color:#159957; '>Importing structures and trajectories</summary>
    <summary markdown='span' style='cursor:pointer; display:list-item; color:#159957'>Importing structures and trajectories</summary>

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

</details>

## Importing structures and trajectories

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

## Assign a trajectory to a structure

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

## Sharing a session

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


## Upload a trajectory to the MDsrv

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

## Stream a trajectory from the MDsrv

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

## Superpose structures based on a sequence alignment

1. Import a Clustal alignment (.aln) using the Open Local Files menu. 
2. Import the structures corresponding to the sequences in the alignment.
3. Match the sequences of the alignment with the structures using the Match Sequence Alignment menu in the Extension Panel at the bottom. 
    - For each sequence in the alignment, you must specify which sequence of the structure should be matched to it.
    - Each sequence needs its own structure.
    - Match the following parameters for each sequence in the alignment:
        - Structure
        - Entity
        - Chain
        - Instance (if available)
4. Select Apply Matching.
    - If the structures are correctly matched, they will be superposed according to the alignment.
    - If the matching is not correct, it is indicated which sequences of the alignment were not matched correctly in the Log at the bottom.

<center>
    <figure class='video_container'>
        <video width='75%' controls='true' allowfullscreen='true' poster='./videos/poster/alignment.png'>
            <source src='./videos/alignment.mp4' type='video/mp4'>
        </video>
    </figure>
</center>

