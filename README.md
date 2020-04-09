# At the Hour of Annihilation

## Forward
November 2019, as a lark, a small collection of amateur theatre enthusiasts unwittingly began drafting [an original stage-play](https://docs.google.com/document/d/1M_bp2vOEIlvXp-hv4aCaoiU3qeLlvKdlyH81C5zF2lw/edit?usp=sharing) featuring a world being destroyed by a coronavirus. The script was declared “ready” and casting began in February 2020, planning to unleash the premiere upon an unsuspecting Berlin audience in April 2020.

How do you make a God laugh?
Tell him your plans.

By March 2020, it became evident that we were not just casting characters but casting prophecy. What we wanted to put on a small stage, was in fact to be played out upon all the world!

The original production was set to hit the stage on 2018 April 18.  While lockdowns forced us to postpone the theatrical production, some members of Lost Thespians agreed the show must go on.  Thus we are adapting the play for "radio" presentation.

## Workflow and Branch Naming Conventions

1. The `dev` branch contains an empty Reaper project with placeholders to keep certain common directories (e.g. "voiceovers", "scenes", "acts", etc.) available for each branch (because git does not like empty directories).

2. For each scene, create/modify a branch called something like `scene/1-6` which will be editted to the best of our ability for the specific scene.

3. As/When all the scenes within each act become available/ready, we create/modify a branch called something like `act/1` which would contain each scene as a single track (each having been exported from the appropriate branch).

4. As/When all the acts within the production become available, we update the `master` branch to have an end-to-end copy of the production which would contain each act as a single track (each having been exported from the appropriate branch).

* For scenes were we want to experiment with multiple possibilities (different actors, different timing, different effects, whatever), we could use names like `scene/1-5/johnny-as-president` or whatever makes it meaningful. And we could do similiar for the acts or the master branch (e.g. `master/johnnys-cut`).

NOTE: Because most of the files are binary, because support for merging XML-like files is lacking, and because every merge would mean manually repositioning an ever increasing number of tracks, we won't ever actually merge branches.


## How to prepare your workstation.
1. Download and install [Reaper](https://www.reaper.fm/download.php).

2. [Download](https://git-scm.com/downloads) and [install](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) git.
    (GUI options are available, but instructions for use won't be provided here.)

3. [Configure username and password](https://www.shellhacks.com/git-config-username-password-store-credentials/) for git.

4. Open git bash.

5. In the git console, using bash commands, navigate to where you would like to store this project on your computer.

6. Clone this project from the command line using `git clone https://github.com/nilvon9wo/at-the-hour-of-annihilation.git`

## How to work on a new scene.

1. Open git bash.

2. In the git console, using bash commands, navigate to this git project.

3. Make sure you are in the `dev` branch with `git checkout dev`.

4. Make sure the project is up to date with `git pull`.

5. Create a new branch for the scene with `git checkout -b <some-branch>`, example: `git checkout -b scene/7-1`.
    Notice there is a `-b` here.

6. Download [voiceover recordings](https://cp.sync.com/files/1329940731) needed for your scene into the `voiceovers` directory.

7. Open this project in Reaper (`File` >> `Open project...`)

8. Import the voiceovers into Reaper (`Insert` >> `Media file...`)
    If importing multiple voices at once, when prompted, choose "Separate tracks"

9. Create the scene with the audio tracks.
    [Reaper Daw: The Complete Beginner's Guide](https://www.musicgateway.com/blog/how-to/reaper-the-complete-beginners-guide)

10. Open git bash.

11. In the git console, using bash commands, navigate to this git project.

12. Add your files to the git project with `git add <path-to-file>`, example: `git add voiceovers/john-smith-7-1.mp3`.
    If you know you want to add all the new files in the project, you can use `git add .`

13. Push your changes to Github with `git push`.
    Depending how you have git configured on your machine, you may get an error telling you this didn't work and how to correct it.
    If this happens, follow the instructions provided.

## How to work on an existing scene.

1. Open git bash.

2. In the git console, using bash commands, navigate to this git project.

3. Open the existing branch with `git checkout <some-branch>`, example: `git checkout scene/7-1`.
    Notice there is no `-b` here.

4. Make sure the project is up to date with `git pull`.

5. (Optional) If you wish to create an alternative verson of the scene, create a new branch for it, `git checkout -b scene/7-1/johnnys-preferred-actors`.

6. Modify the project as required/desired.

    [Reaper Daw: The Complete Beginner's Guide](https://www.musicgateway.com/blog/how-to/reaper-the-complete-beginners-guide)

7. Open git bash.

8. In the git console, using bash commands, navigate to this git project.

9. Add your files to the git project with `git add <path-to-file>`, example: `git add voiceovers/john-smith-7-1.mp3`.
    If you know you want to add all the new files in the project, you can use `git add .`

10. Push your changes to Github with `git push`.
    Depending how you have git configured on your machine, you may get an error telling you this didn't work and how to correct it.
    If this happens, follow the instructions provided.
    



