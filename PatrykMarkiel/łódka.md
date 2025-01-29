# Game Design Document: Sailing Challenge

# Overview

Sailing Challenge is a 2D sailing game where the player controls a sailing boat navigating the open sea. The primary objective is to avoid obstacles such as boulders, other ships, and reefs while managing the effects of wind on the boat's speed. The challenge comes from the dynamic wind system, which influences the boat's movement based on direction and strength.


---

# Game Mechanics

## Boat Movement

Speed depends of n value which is randomly set by program and is changing in the time

The player can adjust the boat’s angle to optimize speed and avoid obstacles.

Speed is affected by wind direction and strength.

If the boat is in an unfavorable wind condition, it slows down.

The player must strategically adjust their angle to maximize speed and maneuver effectively.

Movement is realistic the sailboat can't turn in place.

---

# Wind Mechanics

The Sailing boat is accelerates til it reaches n value or max speed(it depends of sail position)

If the wind is blowing between the angles of the sail setting, speed is reduced to half of the maximum possible speed.

## Wind Direction and Boat Speed

The wind direction determines how much the boat's speed is affected. The boat's sail position relative to the wind direction categorizes its effectiveness into sailing positions:
<table>
  <tr>
    <th>Angle of blowing (°)</th>
    <th>Position</th>
    <th>Speed %</th>
  </tr>
  <tr>
    <td>&lt; 30° or &gt; 330°</td>
    <td>In Irons</td>
    <td>0%</td>
  </tr>
  <tr>
    <td>30° - 45°</td>
    <td>Close Hauled (Right)</td>
    <td>50%</td>
  </tr>
  <tr>
    <td>45° - 60°</td>
    <td>Close Reach (Right)</td>
    <td>75%</td>
  </tr>
  <tr>
    <td>60° - 90°</td>
    <td>Between Close Reach & Beam Reach</td>
    <td>87.5%</td>
  </tr>
  <tr>
    <td>90°</td>
    <td>Beam Reach (Right)</td>
    <td>100%</td>
  </tr>
  <tr>
    <td>100° - 135°</td>
    <td>Broad Reach (Right)</td>
    <td>90%</td>
  </tr>
  <tr>
    <td>135° - 150°</td>
    <td>Between Broad Reach & Running</td>
    <td>85%</td>
  </tr>
  <tr>
    <td>150° - 180°</td>
    <td>Running</td>
    <td>80%</td>
  </tr>
  <tr>
    <td>180°</td>
    <td>Beam Reach (Left)</td>
    <td>100%</td>
  </tr>
  <tr>
    <td>190° - 225°</td>
    <td>Broad Reach (Left)</td>
    <td>90%</td>
  </tr>
  <tr>
    <td>225° - 270°</td>
    <td>Beam Reach (Left)</td>
    <td>100%</td>
  </tr>
  <tr>
    <td>270° - 300°</td>
    <td>Close Reach (Left)</td>
    <td>75%</td>
  </tr>
  <tr>
    <td>300° - 315°</td>
    <td>Close Hauled (Left)</td>
    <td>50%</td>
  </tr>
  <tr>
    <td>315° - 330°</td>
    <td>Between Close Hauled & In Irons</td>
    <td>25%</td>
  </tr>
</table>

# Use Cases for **Sailing Challenge**

## 1. Use Case: Starting the Game
- **Description:** The player launches the game and starts the sailing challenge.
- **Preconditions:** The game is running, and the player is on the main menu screen.
- **Steps:**
  1. The player presses the “Start” button.
  2. The game loads the initial sailing environment.
  3. The player sees the boat on the water, with wind direction and strength displayed.
- **Expected Outcome:** The game starts, and the player can begin controlling the boat.

---

## 2. Use Case: Controlling the Boat
- **Description:** The player controls the boat’s movement by adjusting the sail angle and steering to align with the wind direction.
- **Preconditions:** The game has started, and the player is actively controlling the boat.
- **Steps:**
  1. The player uses the controls to steer the boat.
  2. The player adjusts the sail angle to optimize speed based on wind direction.
  3. The player maneuvers the boat to avoid obstacles and navigate through the open sea.
- **Expected Outcome:** The boat responds to the player's input, and its speed is affected by wind conditions and sail angle.

---

## 3. Use Case: Adjusting the Sail
- **Description:** The player adjusts the sail to match the wind direction, optimizing the boat’s speed.
- **Preconditions:** The boat is in motion, and the wind is blowing from a certain direction.
- **Steps:**
  1. The player observes the wind direction and the current sail position.
  2. The player adjusts the sail angle (left or right) to get the best sailing position relative to the wind.
  3. The boat’s speed changes based on the angle between the sail and wind direction.
- **Expected Outcome:** The boat’s speed increases or decreases based on the correct adjustment of the sail.

---

## 4. Use Case: Avoiding Obstacles
- **Description:** The player avoids obstacles (rocks, other ships, reefs) while navigating through the water.
- **Preconditions:** The boat is in motion, and obstacles are present in the environment.
- **Steps:**
  1. The player observes the surroundings and detects obstacles.
  2. The player steers the boat to avoid collisions.
  3. The player may need to adjust the sail to gain speed or maneuver more effectively around obstacles.
- **Expected Outcome:** The boat successfully avoids obstacles, or a collision occurs if the player fails to navigate properly.

---

## 5. Use Case: Wind Changes
- **Description:** The wind direction and strength change over time, affecting the boat’s speed and direction.
- **Preconditions:** The game is ongoing, and the boat is already in motion.
- **Steps:**
  1. The wind direction shifts, and its strength may increase or decrease.
  2. The player notices the change in wind and adjusts the sail accordingly.
  3. The player adapts their movement strategy to maintain optimal speed.
- **Expected Outcome:** The boat’s speed and direction adjust dynamically based on the wind’s changes. The player must react to these changes to maintain control.

---

## 6. Use Case: Game Over
- **Description:** The game ends when the boat collides with an obstacle or reaches a goal (if applicable).
- **Preconditions:** The boat is in motion, and the player is actively controlling it.
- **Steps:**
  1. The boat collides with an obstacle or completes the goal (if applicable).
  2. A game over screen or summary appears.
  3. The player is prompted to either restart the game or quit.
- **Expected Outcome:** The game ends, and the player can choose to restart or exit.








