[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/VuODydzp)

## Systems and Toolchains Course Project – Option 1

Contributors: Jiayi Liu(andrew ID: jiayili5) & Kitiyaporn Takham(andrew ID: ktakham)

### Dataset
In this project, we use FIFA Dataset available on Kaggle https://www.kaggle.com/stefanoleone992/fifa-22-complete-player-dataset/.
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
      
      body_type  *Note: dataset has height&weight*
      
      real_face
      
      release_clause_eur
      
      player_tags
      
      player_traits
      
      ls: player that is playing as LS
      st: player that is playing as ST
      rs: player that is playing as RS
      lw: player that is playing as LW
      lf: player that is playing as LF
      cf: player that is playing as CF
      rf: player that is playing as RF
      rw: player that is playing as RW
      lam: player that is playing as LAM
      cam: player that is playing as CAM
      ram: player that is playing as RAM
      lm: player that is playing as LM
      lcm: player that is playing as LCM
      cm: player that is playing as CM
      rcm: player that is playing as RCM
      rm: player that is playing as RM
      lwb: player that is playing as LWB
      ldm: player that is playing as LDM
      cdm: player that is playing as CDM
      rdm: player that is playing as RDM
      rwb: player that is playing as RWB
      lb: player that is playing as LB
      lcb: player that is playing as LCB
      cb: player that is playing as CB
      rcb: player that is playing as RCB
      rb: player that is playing as RB
      gk: player that is playing as GK
      
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

- **SparkML version**

  - linear regression
  - redom forest regression

- **Pytorch version**

  - linear regression
  - MLP


> [Note] explain why you chose the classifiers/regressors and
> provide comments on the impact of the tunable parameters on the
> accuracy. Also, compare the selected models