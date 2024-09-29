[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/VuODydzp)

## Systems and Toolchains Course Project – Option 1

Contributors: Jiayi Liu(andrew ID: jiayili5) & Kitiyaporn Takham(andrew ID: ktakham)

### Dataset
In this project, we use FIFA Dataset available on Kaggle https://www.kaggle.com/stefanoleone992/fifa-22-complete-player-dataset/.
This dataset contains Soccer player statistics for 2015-2022. Male player data start in 2015 while Female player statistics start in 2016.
#### Features (110 features)
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

> ### :speech_balloon: The benefit of using PostgreSQL DB table compared to a NoSQL Database in this project
>  - excel at combing tables with similar features using JOIN and UNION operations
>  - allowing better organization, and validation of data which means that we can separate the big table into samll tables and relate them with the key
>  - better supporting complex SQL queries than NoSQL DB

