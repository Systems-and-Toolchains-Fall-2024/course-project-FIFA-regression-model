[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/VuODydzp)

## Systems and Toolchains Course Project – Option 1

Contributors: Jiayi Liu(andrew ID: jiayili5) & Kitiyaporn Takham(andrew ID: ktakham)

**walkthrough videos:** 
- [cloud_walkthrough](https://www.dropbox.com/scl/fi/aj3daxi994r1bgtzrrx7b/walkthrough_cloud.mov?rlkey=ud9mq4ca3meb3938usfi6gq8x&st=h06glo4o&dl=0)
- [local_walkthrough](https://www.dropbox.com/scl/fi/uqksf4d3bswonlmyqhq5k/walkthrough_local.mov.mp4?rlkey=4x1r1bopar7zecc300wymceo5&st=mmpgso9r&dl=0)
- [Bonus walkthrough](https://www.dropbox.com/scl/fi/ac2rcozmrc9if5yseseoi/bonus_walkthrough.mov?rlkey=pj25zurwhx28n8wvq8l8xdqdo&st=kd69nngd&dl=0)

**demo videos:** 
- [cloud demo](https://www.dropbox.com/scl/fi/jsz8aimzclr64864vwy17/running_on_cloud.mov?rlkey=yq5zem09uirkjzqm37oui3m53&st=kpas6e7m&dl=0)
- [local demo on task I](https://www.dropbox.com/scl/fi/wpdt8rwltr1sy3je58lyc/local_running_taskI.mov?rlkey=gz8fy63zyyrp9ekon5szyr61m&st=9e369lw5&dl=0)
- [Bonus demo](https://www.dropbox.com/scl/fi/48ac1pupei8gcax17lu7u/bonus.mov?rlkey=ofe746wny3365gyuwlpv771vi&st=zcyqdopa&dl=0)

### Dataset
In this project, we use FIFA Dataset available on Kaggle [here](https://www.kaggle.com/stefanoleone992/fifa-22-complete-player-dataset/).
This dataset contains Soccer player statistics for 2015-2022. Male player data start in 2015 while Female player statistics start in 2016.

#### Features (110 features)
<details> 
<summary> Expanded </summary>

- sofifa_id: player unique key 
- player_url: player information link
- short_name: player short name
- long_name: player full name
- player_position: player position with the role in the club and the national team
- overall: the number of matches that the player plays
- potential: player performance rate (0-100)
- value_eur: player value (in EUR)
- wage_eur: player weekly wage (in EUR)
- age: player weekly wage (in EUR)
- dob: player date of birth
- height_cm: player height (in cm)
- weight_kg: player weight (in kg)
- club_team_id: club team_id on Sofifa where the player plays
- club_name: club name where the player plays
- league_name: league name of the club
- leaue_level: league rank of the club (e.g. English Premier League is 1, English League Championship is 2, etc.)
- club_position: player position in the club (e.g. SUB means substitute, RES means reserve)
- club_jersey_number: player jersey number in the club
- club_loaned_from: club loaning out the player
- club_joined: the date when the player joined his current club
- club_contract_valid_until: player contract expiration date
- nationality_id: player nationality id on Sofifa
- nationality_name: player nationality name
- nation_team_id: national team_id on Sofifa where the player plays
- nation_position: player position in the national team
- nation_jersey_name: player jersey number in the national team
- preferred_foot: player preferred foot
- weak_foot: player weak foot (1-5)
- skill_moves: player skill moves (1-5)
- internation_reputation: player international reputation (1-5)
- work_rate: player work rate attributes (attacking / defensive)
- body_type: player body type ??
- real_face: player real face ??
- release_clause_eur: player release clause (in EUR)
- player_tags: player tags
- player_traits: player traits
- pace: player pace
- shooting: the number of a player's shooting
- passing: the number of a player's passing
- dribbling: the number of a player's dribbling
- defending: the number of a player's defending
- physic: the number of a player's physic
- attacking_crossing: the number of a player's crossing
- attacking_finishing: the number of player's finish attacking
- attacking_heading_accuracy: player heading attack accuracy
- attacking_short_passing: the number of a player's short passing
- attacking_volleys: the number of a player's volleys
- skill_dribbling: the number of a player's skill dribbling
- shill_curve: the number of a player's skill curve
- skill_fk_accuracy: player free-kick accuracy
- skill_long_passing: the number of a player's long passing
- skill_ball_control: player ball control
- movement_acceleration: player acceleration
- movement_sprint_speed: player sprint speed
- movement_agility: player agility
- movement_reactions: player reactions
- movement_balance: player balance
- power_shot_power: player shot power
- power_jumping: player jumping
- power_stamina: player stamina
- power_strength: player strength
- power_long_shots: player long shots
- mentality_aggression: player mentality aggression
- mentality_interceptions: player interceptions
- mentality_positioning: player positioning
- mentality_vision: player vision
- mentality_penalties: player penalties
- mentality_composure: player composure
- defending_marking_awareness: player marking awareness
- defending_standing_tackle: player standing tackle
- defending_sliding_tackle: player sliding tackle
- goalkeeping_diving: player GK diving
- goalkeeping_handling: player GK handling
- goalkeeping_kicking: player GK kicking
- goalkeeping_positioning: player GK positioning
- goalkeeping_reflexes: player GK reflexes
- goalkeeping_speed: player GK speed
- ls: player that is playing as LS
- st: player that is playing as ST
- rs: player that is playing as RS
- lw: player that is playing as LW
- lf: player that is playing as LF
- cf: player that is playing as CF
- rf: player that is playing as RF
- rw: player that is playing as RW
- lam: player that is playing as LAM
- cam: player that is playing as CAM
- ram: player that is playing as RAM
- lm: player that is playing as LM
- lcm: player that is playing as LCM
- cm: player that is playing as CM
- rcm: player that is playing as RCM
- rm: player that is playing as RM
- lwb: player that is playing as LWB
- ldm: player that is playing as LDM
- cdm: player that is playing as CDM
- rdm: player that is playing as RDM
- rwb: player that is playing as RWB
- lb: player that is playing as LB
- lcb: player that is playing as LCB
- cb: player that is playing as CB
- rcb: player that is playing as RCB
- rb: player that is playing as RB
- gk: player that is playing as GK
- player_face_url: URL of the player face
- club_logo_url: URL of the club logo
- club_flag_url: URL of the club nationality flag
- nation_logo_url: URL of the national team logo
- nation_flag_url: URL of the national flag
</details>

> ### :speech_balloon: The benefit of using PostgreSQL DB table compared to a NoSQL Database in this project
>  - excel at combing tables with similar features using JOIN and UNION operations
>  - allowing better organization, and validation of data which means that we can separate the big table into samll tables and relate them with the key
>  - better supporting complex SQL queries than NoSQL DB

## Steps and Notes for running project.ipynb

**Table of contents**
- [Task I](#task-i)
- [Task II](#task-ii)
- [Task III](#task-iii)
- [Task IV](#task-iv)
- [Bonus](#bonus)

### Task I
- All of 15 .csv data files with 110 original features & 2 columns of `year` and `gender` have been uploaded in the Postgres table named `fifa`
- Total male+female players: 144323 (distinct w.r.t. 111 features)

### Task II

*Note:* "use only male player data for your analysis tasks (Tasks 2 and 3)"

**Question 1**
- Defined function `query_no_clubs(X, Y, Z)` to finish the task of "find the Y clubs with the highest number of players in year X with contracts ending in year Z"
  - input required: year as `X`, the number of clubs (positive integer) that want to display as `Y`, year of a contract ending as `Z`
  - output: the `Y` clubs' name and there players number in year `X` with contracts ending in year `Z`
    
  <details> 
  <summary> Function testing </summary>
    
  - Possible value for year X: [2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022]
  - Possible value for contract ending year Z (hold the value of 2023 or after): [2031, 2026, 2028, 2025, 2023, 2024, 2027]
  </details>

**Question 2**
- Defined function `top_avg_age_clubs(X, Y, filter)` to finish the task of "list the X clubs with the highest (or lowest) average player age for a given year Y"
  - input required: club ranking as `X`, year as `Y`, option to choose from "highest" or "lowest" ranking as `filter`
  - output: list of `X` clubs with the `filter` average player age for a given year `Y`

**Question 3**
- Defined function `display_popular_nation()` to illustract the most popular nationality in the dataset for each year
  - input: nothing
  - output: list of popular nationality for each year

### Task III

#### Data Engineering

Prediction target: `value_eur`

 - **Data Cleaning & Data Preprocessing**

    - player_position,club_name,preferred_foot -> one-hot
    - club_contract_valid_until - club_joined -> contact time period 
    - work_rate -> split into attacking / defensive -> one-hot
    - drop columns that are not of interest
    
      <details> 
      <summary> Expanded </summary>
      
      sofifa_id
      
      player_url
      
      short_name
      
      long_name
      
      club_name
      
      club_postion
      
      dob
      
      club_team_id
      
      leuage_name
      
      club_jersey_number
      
      club_loaned_from
      
      nationality_id
      
      nationality_name
      
      nationality_team_id
      
      nation_position
      
      nation_jersey_name
      
      body_type  **Note: dataset has height&weight**
      
      real_face
      
      release_clause_eur
      
      player_tags
      
      player_traits
      
      ls
      
      st
      
      rs
      
      lw
      
      lf
      
      cf
      
      rf
      
      rw
      
      lam
      
      cam
      
      ram
      
      lm
      
      lcm
      
      cm
      
      rcm
      
      rm
      
      lwb
      
      ldm
      
      cdm
      
      rdm
      
      rwb
      
      lb
      
      lcb
      
      cb
      
      rcb
      
      rb
      
      gk
      
      player_face_url
      
      club_logo_url
      
      club_flag_url
      
      nation_logo_url
      
      nation_flag_url
      
      year
      
      gender
      </details> 

  - **Handle missing value**

    - value_eur: drop the rows with "NULL" 
    
    - wage_eur, league_level, pace, shooting, passing, dribbling, defending, physic, mentality_composure: fill missing vale with medium value  
    
    - goalkeeping_speed, contract_duration: fill missing value with "0"
  
#### Modeling (Regression)

> ### :speech_balloon: Explain why you chose the classifiers/regressors
> **Answer:** Because the prediction target is a value of player in EUR (numerical), the models should be regression models.

- **SparkML version**

  - **Linear Regression**

    Experiment on: regParam, maxIter

    - if the model has high regularization (regParam = 100) and minimal iteration, the model is simple and less flexible resulting in underfitting.

    - if the model does not have regularization (regParam = 0) and maximal iteration, the model fully fits the data resulting in overfitting.
    
    **Results: MSE of test = 0.427**
    
  - **Random Forest Regression**
 
    Experiment on: maxDepth, numTrees
 
    - if the model is too small in-depth and has fewer trees, the model is simple resulting in underfitting.

    - if the model is too deep and has more trees, the model is complex resulting in overfitting.
    
    **Results: MSE of test = 0.079**

- **Pytorch version**

  - **Linear Regression**
 
    Experiment on: learning rate, epochs
    
    - if the model has a small learning rate with large epochs, it may stuck into the local minimum
    - if the model has a larger learning rate with small epochs, in our experiment, the model gets a smaller loss than a smaller learning rate
    
    **Results: MSE of test = 0.451**
    
  - **MLP**
 
    Experiment on: learning rate, epochs
 
    - We changed the lr and number of epochs together and found for our MLP model, a smaller lr=0.01 with larger epochs=2000 gives the best result.
    
    **Results: MSE of test = 0.158**

  > **Summary**
  > 
  > The Random Forest model in SparkML is the best model for this data with the lowest MSE loss at 0.079, followed by the MLP model in Pytorch with 0.158 and Linear Regression in SparkML and in Pytorch for 0.427 and 0.451 respectively.
  
### Task IV

Deploy 3 tasks above on the Cloud will refer to cloud running video & project_on_cloud.ipynb

> **Summary**
> 
> Training models on cloud gives different loss values to local training for each models. However, the random forest model with SparkML still be the best model with the different ranking; MLP with Pytorch, linear regression with SparkML, and Linear regrssion with Pytorch respectively.

### Bonus

Run the PostgreSQL on the cloud:

> Code: bonus.ipynb
> 
> Explanation and code running recording: Bonus walkthrough & Bonus demo videos
