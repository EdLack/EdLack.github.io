# ENG1 Cohort 3 Group 2
## Contents
<p>

Assessment 1/2 Deliverables (Old & New) <br/>

<details>
  <summary>Click to see Assessment 1 updated and old deliverables</summary>
  - <a href="https://EdLack.github.io/#requirements">Requirements</a> <br />
  - <a href="https://EdLack.github.io/#architecture">Architecture</a> <br />
  - <a href="https://EdLack.github.io/#method-selection--planning">Method Selection & Planning</a> <br />
  - <a href="https://EdLack.github.io/#risk-assessment">Risk Assessment</a> <br />
  - <a href="https://EdLack.github.io/#implementation">Implementation</a> <br />
</details>
<details>
  <summary>Click to see Assessment 2 deliverables</summary>
  - <a href="https://EdLack.github.io/#change-report">Change Report</a> <br />
  - <a href="https://EdLack.github.io/#implementation2">Implementation</a> <br />
  - <a href="https://EdLack.github.io/#testing">Testing</a> <br />
  - <a href="https://EdLack.github.io/#user-evaluation">User Evaluation</a> <br />
  - <a href="https://EdLack.github.io/#continuous-integration">Continuous Integration</a> <br />
</details>
<br/>
- <a href="https://EdLack.github.io/#github-repository">Github Repositories</a> <br />
- <a href="https://EdLack.github.io/#executable-jar">Executable JARs</a> <br />
- <a href="https://EdLack.github.io/#google-drive">Google Drives</a> <br />
</p>


## Documentation


### Change Report
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <a href="https://drive.google.com/file/d/1vykJayrxhYvukxs3_O3Kos0aUdv98GTu/view?usp=drive_link">Change2.pdf</a>
  <br/>
</div>

### Implementation2
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <a href="https://drive.google.com/file/d/1rnt2niWqDyOWN49nkGCZyOa-i3gyXwzu/view?usp=drive_link">Impl2.pdf</a>
  <br/>
  <a href="https://github.com/KyberCrys/Team-2-Assessment-2-Engineering-Project/releases/tag/untagged-df7a6eb590a3cb672585">Source Code</a>
  <br/>
</div>

### Testing
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <a href="">Test2.pdf</a>
  <h3>Manual Test Table</h3>
  <table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>ID</th>
      <th>Description</th>
      <th>Requirement</th>
      <th>Method</th>
      <th>Expected Outcome</th>
      <th>Actual Outcome</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>TEST_STARTSCREEN_RENDER</td>
      <td>Tests that the starting screen is loaded correctly upon starting the game with the background, intro text, and leaderboard</td>
      <td>UR_CLEAR_DESIGN, UR_LEADERBOARD</td>
      <td>Load the game</td>
      <td>Correct background and text is loaded, text is legible and easy to understand</td>
      <td>Background and text is loaded correctly, and the text is legible</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_WINSCREEN_RENDER</td>
      <td>Tests the win screen loads correctly upon winning the game, with the background, congratulatory text, and achievements</td>
      <td>UR_CLEAR_DESIGN, UR_ACHIEVEMENTS</td>
      <td>Play through the game until the win condition is met</td>
      <td>Correct background and text is loaded, text is legible and easy to understand</td>
      <td>Background and text is loaded correctly, and the text is mostly legible</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_PLAYER_RENDER</td>
      <td>Tests that the correct animation is played for each of the players inputs</td>
      <td>UR_MOVEMENT, UR_CLEAR_DESIGN</td>
      <td>
        Press each of the keys w,a,s,d checking that the animation changes correctly on each keypress.
        Stop after pressing each key, checking that the animation is correct once the key is no longer pressed
      </td>
      <td>
        Press W: up walking animation is used, when stopped, the facing up animation is used<br><br>
        Press A: left walking animation is used, when stopped, the facing left animation is used<br><br>
        Press S: down walking animation is used, when stopped, the facing down animation is used<br><br>
        Press D: right walking animation is used, when stopped, the facing right animation is used
      </td>
      <td>Pressing each key plays the correct animation whilst the key is pressed and once the player stops moving</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_DOOR_AND_KEY_RENDER</td>
      <td>Tests that exactly three doors and three keys are drawn on the map in the correct orientation</td>
      <td>UR_ITEMS, UR_MAP, UR_CLEAR_DESIGN, FR_LOCKED_DOOR</td>
      <td>Load and start a game</td>
      <td>Three doors and three keys will be clearly visible on the map</td>
      <td>Three doors and three keys are visible on the map</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_WARP_RENDER</td>
      <td>Tests that a warp panel is correctly rendered </td>
      <td>UR_HIDDEN_EVENTS</td>
      <td>Load and start a game, then move the player until they collide with the warp panel</td>
      <td>The warp panel is initially not visible, once the player collides with it, it will then become visible</td>
      <td>The warp panel is not initially visible, then becomes visible once it is collided with</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_POWERUP_RENDER</td>
      <td>Tests that each powerup is correctly rendered</td>
      <td>UR_MAP, UR_ITEMS, UR_POSITIVE_EVENTS, UR_NEGATIVE_EVENTS, UR_HIDDEN_EVENTS</td>
      <td>
        Load and start a game, check that all the visible events are rendered with the correct image.
        Move the player to collide with the remaining hidden events
      </td>
      <td>
        There are two speed up events, then one of each a:<br>
        chest; charge; hole; drink, sleep; slow down; time boost; and score divider
      </td>
      <td>
        All visible events are shown on the map and are mostly clear to see, both hidden events are not visible when starting the game,
        however the charge event doesn’t then become visible once it is activated
      </td>
      <td>Fail</td>
    </tr>

    <tr>
      <td>TEST_ACTIVE_POWERUP_RENDER</td>
      <td>Tests the active powerups are shown on the UI bar</td>
      <td>UR_CLEAR_DESIGN</td>
      <td>Load and start a game, then collect a speed up powerup, check that it is active for 10 seconds</td>
      <td>The icon for the active powerup should appear and stay visible for the amount of time that it is active</td>
      <td>Upon collecting the speed up, it becomes visible in the active powerup section, disappearing after 10 seconds</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_EVENTCOUNTS_RENDER</td>
      <td>Tests that the counters for each event are shown on the UI bar with the correct counts</td>
      <td>UR_EVENT_COUNTER</td>
      <td>Load and start a game, then collect a powerup of each type: positive, negative and hidden</td>
      <td>The counters should be rendered and legible, then upon each powerup being collected, the respective counter should increase</td>
      <td>
        The counters are initially rendered to 0, and are clearly visible, upon collecting a good, bad and hidden event,
        the respective counters all incremented by 1
      </td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_PAUSE</td>
      <td>Tests that the Pause menu renders correctly</td>
      <td>UR_PAUSE, UR_CLEAR_DESIGN, UR_GAME_DESIGN</td>
      <td>Load and start a game, then press esc to activate the pause menu, press esc again to return to the game</td>
      <td>The pause menu will be rendered with a transparent background and legible text, with the game timer pausing</td>
      <td>
        The pause menu is rendered correctly, and the text is quite legible, and the game timer visibly pauses
      </td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_GAME_OVER</td>
      <td>Tests that the Game Over screen renders correctly</td>
      <td>UR_CLEAR_DESIGN, UR_GAME_DESIGN</td>
      <td>Load and start a game, wait until the timer runs out</td>
      <td>The game over screen will be rendered with a transparent background and legible text</td>
      <td>The game over screen is rendered correctly, the text is relatively legible</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_TIMER</td>
      <td>Tests that the timer is correctly rendered on the UI bar, accurately depicting the time</td>
      <td>UR_COUNTDOWN, UR_CLEAR_DESIGN</td>
      <td>Load and start a game, watch the timer and check it decreases every second</td>
      <td>The timer is rendered in the top corner in the format MM:SS, and decreases by 1 every second</td>
      <td>The timer is correctly rendered and decreases at the correct rate</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_GAME_RENDER</td>
      <td>Tests that the game map is rendered correctly</td>
      <td>UR_MAP, UR_CLEAR_DESIGN</td>
      <td>Load and start a game</td>
      <td>The map is correctly rendered and easy to understand </td>
      <td>The map is correctly rendered, the pixel art graphics making it clear what areas can be accessed</td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_MOVEMENT</td>
      <td>Tests that the player can move and collide with objects in order to complete the game</td>
      <td>UR_MOVEMENT, UR_ITEMS, UR_GAME_DESIGN</td>
      <td>Load and start a game, play through the game until the win condition is met</td>
      <td>All entities are rendered correctly, the player can move, collide with items to progress, and end the game</td>
      <td>
        All entities were rendered correctly, and the player was able to collide with items to complete the game
      </td>
      <td>Pass</td>
    </tr>

    <tr>
      <td>TEST_RESIZE</td>
      <td>Tests that the game window can be resized accurately</td>
      <td>UR_GAME_DESIGN</td>
      <td>
        Load and a game, press F11 to resize the game to fullscreen,
        press F11 again to return to original window size
      </td>
      <td>
        The graphics adapts to fullscreen without loss of quality, and then revert back to the initial state
      </td>
      <td>
        From the start screen, pressing F11 will not resize the game, doing so once the game has started however,
        will resize the screen correctly. Pressing F11 again does not revert the screen size
      </td>
      <td>Fail</td>
    </tr>
  </tbody>
</table>

  <br/>
  <h2>For each of the following files you will be taken to a google drive, where you will need to download the main folder and then unzip it. From there you can open the corresponding index.html / main.html from your device.</h2>
  <br/>
  <a href="https://drive.google.com/drive/folders/1m9kK-Yr092WOa7RAWlj8ju0mcEOUoHcd?usp=drive_link">Checkstyle Report Link </a>
  <br/>
  <a href="https://drive.google.com/drive/folders/1f65CbQjS7mlk6cSh3zZCjipFZjrNeAgX?usp=drive_link">JaCoCo Coverage Report Link </a>
  <br/>
  <a href="https://drive.google.com/drive/folders/1K0dwUzp_6oYqCBK_mKgJ_lNYohiH3P1Y?usp=drive_link">JaCoCo Test Report Link </a>
  <br/>
</div>

### User Evaluation
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <a href="https://drive.google.com/file/d/164R2vcPc9YHRCVEuHDl3SnW9Am0IygLX/view?usp=drive_link">Eval2.pdf</a>
  <br/>
</div>

### Continuous Integration
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <a href="https://drive.google.com/file/d/1nqvOZjXFrRvhVQsyATP18eIQLIqPz2fo/view?usp=drive_link">CI2.pdf</a>
  <br/>
</div>

### Requirements
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>Updated Assessment 1 Requirements PDF</p>
  <a href="https://drive.google.com/file/d/13uhUjVx7PIffPOfPYGdHgOFZvdo-RLJT/view?usp=drive_link">Team 2 Req1.pdf</a>
  <br/>
  <br/>
  <p>Old Assessment 1 Requirements PDF</p>
  <a href="https://drive.google.com/file/d/11Bx9VRTYPCfj8bXo6u9mI7ReFgbd0k88/view?usp=drive_link">Old Req1.pdf</a>
  <br/>
  <br/>
  Other Files:
  <br/>
  <a href="https://docs.google.com/document/d/1PW_X5c8_erpyhJr1A2UBc4y99jOvTr5_0AJ8lF1-oBU/edit?tab=t.0#heading=h.ver9vukz1rzm">Client Interview</a>
</div>

### Architecture
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>Updated Assessment 1 Architecture PDF</p>
  <a href="https://drive.google.com/file/d/1NNg7ovKc4ouWQzEhXrDNHR1S94auQUsD/view?usp=drive_link">Team 2 Arch1.pdf</a>
  <br/>
  <br/>
  <p>Old Assessment 1 Architecture PDF</p>
  <a href="https://drive.google.com/file/d/1jfcNZlO0-KP5iMbTfysFoU-16XQcxtFD/view?usp=drive_link">Old Arch1.pdf</a>
  <br/>
  <br/>

  Previous Iterations
  <details>
    <summary>Click to see updated Assessment 1 architecture diagrams</summary>
    <img width="736" height="1321" alt="Assessment2_Behaviour_of_Game" src="https://github.com/user-attachments/assets/43567578-3f49-4688-a113-cf01ea066f7c" />
    <img width="1057" height="1965" alt="Assessment2_Behaviour_of_Game_V2" src="https://github.com/user-attachments/assets/fe8f3009-f656-4eeb-9ed0-008bb3c6ac57" />
    <img width="635" height="610" alt="InvertedControls" src="https://github.com/user-attachments/assets/8bfdbaf5-be9f-4f65-a3e6-b412e6afd7d4" />
    <img width="591" height="477" alt="TimeDecrease" src="https://github.com/user-attachments/assets/031280d6-fa9e-495b-90ff-c97d262fc1cd" />


  </details>
  <details>
    <summary>Click to see original Assessment 1 architecture diagrams</summary>
    <img width="926" height="711" alt="image" src="https://github.com/user-attachments/assets/6fada868-1d1f-42c3-9eab-dce23af878bb" />
    <img width="991" height="693" alt="image" src="https://github.com/user-attachments/assets/acdfb748-2049-4796-9ed5-f8b3db69f24a" />
    <img width="986" height="598" alt="image" src="https://github.com/user-attachments/assets/fe2fbfec-6573-41f3-9547-0d066612e1e8" />
    <img width="720" height="673" alt="image" src="https://github.com/user-attachments/assets/1a2ba6ae-e65f-44a5-b432-9508dcd061fb" />
  </details>
</div>

### Method Selection & Planning
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>Updated Assessment 1 Method Selection & planning PDF</p>
  <a href="https://drive.google.com/file/d/170GA7l7ohJZw9Rnvt7Rh7utbooll0QvL/view?usp=drive_link">Team 2 Plan1.pdf</a>
  <br/>
  <br/>
  <p>Old Assessment 1 Method Selection & planning PDF</p>
  <a href="https://drive.google.com/file/d/1auxYCpcE32DbexzwlmGxIhwrD-RJoYl7/view?usp=drive_link">Old Plan1.pdf</a>
  <br/>
  <br/>
  Initial Plan:
  <br/>
  <a href="https://docs.google.com/document/d/1CiLiLa8Z827Mq-DgH0Q8jv8Wn1GDovbXgPi0u2z3JoU/edit?tab=t.0#heading=h.f63lrhvh1wkv">To-Do List</a>
  <br/>
  <p>
  <img align="center" width="703" height="336" alt="image" src="https://github.com/user-attachments/assets/7ae28110-0919-4a64-807a-7593293826ba" />
  
  <br />
  <br />
  </p>
  Working Plan:
  <p>
  <details>
    <summary>Click to see Assessment 1 Gantt Chart diagrams</summary>
    <img align="center" width="1627" height="523" alt="image" src="https://github.com/user-attachments/assets/4940d4c2-355b-4195-98c5-bada6c530a39" />
  </details>
  <details>
    <summary>Click to see Assessment 2 Gantt Chart diagrams</summary>
    <img width="962" height="594" alt="Screenshot 2025-12-06 133434" src="https://github.com/user-attachments/assets/5ccf5a95-b50b-458c-a74c-f5b37fa69e5c" />
  </details>
  </p>
</div>

### Risk Assessment
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>Updated Assessment 1 Risk Assessment PDF</p>
  <a href="https://drive.google.com/file/d/1bHjCCFkdH6vQi6cmq_lY5GjtXeMplphr/view?usp=drive_link">Team 2 Risk1.pdf</a>
  <br/>
  <br/>
  <p>Old Assessment 1 Risk Assessment PDF</p>
  <a href="https://drive.google.com/file/d/1DKwnoRbtImQGt3f1-UKzbjqffvHFHFGC/view?usp=drive_link">Old Risk1.pdf</a>
</div>

### Implementation
#### Deliverable:
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>Assessment 1 Implementation PDF</p>
  <a href="https://drive.google.com/file/d/1bE5mqLg-GjwBI3gwtMpksPvTMxCAgt-W/view?usp=drive_link">Old Impl1.pdf</a>
</div>

## Github Repository
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>New Assessment 2 GitHub Repository</p>
  <a href="https://github.com/KyberCrys/Team-2-Assessment-2-Engineering-Project">github.com/KyberCrys/Team-2-Assessment-2-Engineering-Project</a>
  <br/>
  <br/>
  <p>Old Assessment 1 GitHub Repository</p>
  <a href="https://github.com/hanap05/ENG1-Team-6-Game">github.com/hanap05/ENG1-Team-6-Game</a>
</div>

## Executable JAR
<div style="border: 1px solid #ddd; padding: 15px; ">
  <p>New Assessment 2 .jar executables</p>
  <a href="https://drive.google.com/file/d/1rphI45mRU37JYSxk9EjVUXw38Gb3uglG/view?usp=drive_link">Linux (ubuntu) .jar executable</a><br />
  <a href="https://drive.google.com/file/d/10hYqFsrlu4c7AIaWsIvWPN0BEY3qLLcQ/view?usp=drive_link">Apple (macos) .jar executable</a><br />
  <a href="https://drive.google.com/file/d/1QYK15_ZL8fxLP9aWoGQ2g_tEsjEgt_W7/view?usp=drive_link">Windows (windowsos) .jar executable</a><br />
  <br/>
  <p>Old Assessment 1 .jar executable</p>
  <a href="https://drive.google.com/file/d/1QMBXNiztB0TcUS6n2Vf8zyf3TzBQhuqu/view?usp=drive_link">eng1-maze-game.jar</a>
</div>

## Google Drive
<p style="border: 1px solid #ddd; padding: 15px; ">
<a href="https://drive.google.com/drive/folders/1CtLu-3PziEayoKYIXwBJSp9JGyHGROdM?usp=drive_link">New Assessment 2 Eng1 Cohort 3 Team 2</a>
<br/>
<a href="https://drive.google.com/drive/folders/1i6r96fl1IZ4NdzUq33oifIspLvy7vvBL?usp=sharing">Old Assessment 1 Eng1 Cohort 3 Team 6</a>
</p>
