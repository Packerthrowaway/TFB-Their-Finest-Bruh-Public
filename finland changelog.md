# **Finland Rework Changelog**
#### This is a markdown file, if using VSCode press "Ctrl K" then "V" to view correctly
## Main Finland Winter War changes
### Winter War spirit:
* Changed picture
* No longer reduces Winter Attrition
* No longer grants 10% Core Defense
* Now grants 5% extra Factory Bombing Reduction
* Now grants 5% Division Organisation

### Added new timed spirit "Kollaa Kestää" for 105 days on start of the Winter War granting:
* -1.5% Weekly Balance of Power
* 10% Supply Range
* 10% Core Attack
* 10% Core Defense
* 15% Piercing and 10% Hard Attack to Line AT

### Added new Event "Swedish Volunteers" for Finland 10 days into the Winter War
* Spawns (1) locked 11/4/4 "Swedish Volunteers" Division led by Ernst Linder in Tornio
* Division is deleted after the Winter War (or if Barb starts mid-Winter War)

### During the Winter War a new timeout decision will fire:
* 1 factory from Karjala is automatically relocated to Häme every 7 days
* Evacuating a factory adds 1% Stability
* Fully evacuating the state gives 5% War Support
* Losing control of Karjala or Häme before all industry is evacuated removes 15% Stability and gives the Soviets an event (after the Winter War) to move the remaining mils to Olonets

### Added new events for losing/winning the Winter War as Finland
* Winning now grants +25% Balance of Power 
* Losing now grants +5% Balance of Power, adds state modifier: "Hanko Occupation" to Uusimaa, relocates Salla VP, and re-demilitarizes Åland if focus "Operation Kilpapurjehdus" hasn't been completed

## Comintern Changes
* Sergey Khudyakov (Close Air Support Expert) advisor is now locked behind winning the Winter War

### "Claims in Baltic" focus:
* Now just requires Germany being at war (Was Germany being at war with Poland/Poland not existing)
* Completion Time reduced to 21 days (was 35)

### "Baltic Security" focus:
* Now requires the date to be between November 1st and December 31st 38/39 or past August 1st 1940 (focus continues if requirements are no longer met)

### Added new spirit "Terror Focused Bombing" for Soviets during the Winter War:
* Reduces CAS damage by 90%
* Increases CAS Org damage by 400%
* Reduces Strat Bombing by 15%

### New Winter War related focuses added:
* "Skewer Finland", gives 20% Supply Range and -5% Winter Attrition for 180 days
* "Crush Finland", gives 10% Strat Bombing and 5% Attack and Defense against Finland for 90 days
* The focuses are mutually exclusive
* "Dismantle the Stalin Line" no longer clogs error log, now correctly removes all Stalin Line forts
* "Start Contstruction on the Molotov Line" focus moved below "Secure New Conquests", "Plunder the Baltics" now directly leads to "Prepare to Invade the West"

### "Brothers War" modifier:
* Now reduces CAS damage by 90%
* Now reduces Strat Bombing by 90%

## Winter War decision changes
* Surrender/Victory decision timeout lowered to 5 days (was 7)
* Added new timeout decision for Finland that shows the Soviet time limit
* Time limit for Soviets reduced to 180 days (was 210)
* Soviets no longer get a buff after taking 125k casualties, both casualty timeout decisions no longer visible
* Soviets can now always force Finland to surrender if they control Viipuri
* Casualties required to force Finnish surrender lowered to 65k (was 85k)
* Casualties required to surrender as Finland lowered to 40k (was 65k)
* Casualties required to declare victory as Finland reduced to 275k (was 350k)
* Winter War (and Continuation War) decisions moved to "National Defense" decision category
* Winter War decisions should now dissapear if Barb starts mid-Winter War

## Mannerheim Line Changes
### Karjala starts with new state modifier "Crumbling Fortifications" granting:
* Pillbox effectiveness -15%
* Maximum Pillox level -2

### "Mannerheim Line" focus:
* Removes Crumbling Fortifications modifier
* Instead of 3 levels of Pillboxes now adds 2 levels of Fortresses and 1 level of Pillboxes
* Now adds lvl 2 State AA
* Adds 1 extra Pillbox on the Supply Hub in eastern Karjala
* Adds 1 extra Coastal Pillbox on Viipuri
* No longer adds Pillboxes on Viipuri (was 2)
    #### Mannerheim Line state modifier:
    * Now reduces enemy local supplies by 10%
    * Pillbox Construction speed now works
    * Coastal Pillbox Construction speed removed
    * Now reduces maximum Pillbox level by 1
    * Now removed on state owner change (previously on state controller change)

### If Mannerheim Line was constructed and Winter War was lost:
* Fortresses are removed
* Crumbling Fortifications modifier reapplies
* Unlocks new decision after reintegrating Karjala and Salla:
    * Restores Fortresses to Karjala
    * Removes Crumbling Fortifications state modifier
    * Adds back Mannerheim Line state modifier

### "Defense in Depth" focus:
* Now adds Pillboxes even if you don't control Karjala (Won't add the ones in Viipuri)
    #### "Fortification Effort" modifier:
    * Pillbox Construction speed reduced to 10% (was 20%)

## Fascist Finland Changes
* "Academic Karelian Society" focus: No longer grants 5% Stability
* "Advanced Jaeger Training Program" focus: Special Forces Cap reduced to 2.5% (was 5%)
* "Mustapaidat" focus: Now gives Militia tech, the template is no longer locked
* "Sotilaalliset Kappalaiset" focus: Now adds additional 0.5% Conscription to the Patriotic Peoples Movement modifier 
* "National Fanaticism" focus: Militia org bonus reduced to 5% (was 10%), no longer gives 5% Militia Speed
* "Maan Turva" focus: No longer adds 5% War Support
* "Intellectual Elite" focus: No longer adds Karelian Irredentist Writer advisor

### "Join Axis" focus:
* Name changed to _Finnish Irredentism_
* Picture changed
* Requirements slightly changed
* No longer bypasses
* Now always adds 5% War Support
* Now unlocks Karelian Irredentist Writer advisor

### "Bring Foreign Armor Experts" focus:
* Now requires having researched BT-42 Chassis, previously Improved Light Tank Chassis
* Now grants 1x 50% Mechanized research bonus

### "Keepers Of The North" focus:
* No longer asks nordic countries for annexation
* Now unlocks decision to seize Finnmark from RK Norway should it exist

## Neutral Finland Changes
### "Lone Wolf" focus:
* No longer unavailable if in faction
* No longer grants 5% Stability
    #### Lone Wolf spirit:
   * No longer gets removed
   * No longer prevents joining the Axis 
   * Now grants 5% Core Attack
   * Now grants 1% Conscription (was 0.5%)
   * Some previous modifiers were removed

### "Cooperation With Germany" focus:
* No longer bypasses if in faction with Germany

### "German Military Advisors" focus:
* Completion time increased to 70 days (was 35)
* No longer grants doctrine cost reductions
* Nikolaus von Falkenhorst advisor buffed
* Now grants 2x 25% research bonus for Special Forces technology
* Now unlocks new paratrooper raid "Operation Hokki" against Olonets:
    * Debuffs Soviet speed, disables Soviet strat redeployment, and causes attrition
    * Executable by 16+ width Paratroopers
    * Requires 5 Transport Planes, 100 Support, and 200 Inf equipment
    * Modifier lasts for 45/60/75 days depending on raid outcome
    * One time usage
    * Is removed on capture of Petrozavodsk/Äänislinna

### "Finnish March Of Conquest" focus:
* Name changed to _To The Urals!_
* Picture changed
    #### Finnish March Of Conquest modifier:
    * Duration increased to 450 days (was 356)
    * No longer gives 5% recovery rate

## Army Focus Changes
* "Suomen Maavoimat" focus: Tension requirement lowered to 20% (was 25%)

### "Operation Kilpapurjehdus" focus:
* Completion Time reduced to 7 days (was 35)
* Tension requirement lowered to 50% (was 80%)
* Now grants 1 less Pillbox, but 1 more Coastal Pillbox

### "Underground Resistance Cells" focus:
* Picture changed
* Completion Time reduced to 21 days (was 35)
* No longer requires being in a defensive war
* Now requires having >10% Surrender Progress and being in a faction with Germany
* Now available if country has capitulated
    #### Underground Resistance Cells modifier:
    * No longer provides Targeted Sabotage modifiers
    * Now grants -20% Compliance Growth Speed in Finnish states 

### "Jaeger Movement" focus:
* Completion Time reduced to 35 days (was 70)
* No longer gives 5% Breakthrough
* Division Organisation modifier reduced to 2.5% (was 5%)
* Special Forces Cap increased to 7.5% (was 5%)

### "Motti Tactics" focus:
* No longer grants 2.5% Attacking Division Speed
* Now grants Mastery bonus (Political Tree Mastery bonuses nerfed)

### "Long-Range Patrols" focus 
* Now unlocks new Land Raid against Soviet controlled states:
    * Grants 5% Attack and 10% Breakthrough in the target state
    * Executable by 20+ width Special Forces (Rangers/Mountaineers)
    * Requires 50 SF equipment
    * Only available in Finnish and Soviet cores north of Moscow (Not in Uusimaa or Leningrad)
    * Modifier lasts for 60/65/70 days depending on raid outcome
    * Can be done multiple times (60 day cooldown per state)
    * Limited to 3 raid attempts per game

### "Sissi" focus:
* No longer gives 5% Recon Bonus While Entrenched
* No longer gives 10% Attack and Defense to Long Range Patrol Company support
* Now grants 3% Attacking Division Speed

### "Nation Armor Focus" focus: 
* No longer gives 1x 50% Armor research bonus
* Completion Time reduced to 42 days (was 70)
* Now adds Land Warfare Facility to Häme

### "Salvaged And Retooled" focus: 
* No longer gives 1x 50% Mechanized Armor research bonus
* Number of 50% Armor research bonuses reduced from 2 to 1
* Now gives 1x 100% research speed for BT-42 Chassis

## Air Focus Changes
* "National Aircraft Production" and "Expand Producton Lines" focuses: No longer randomly select Karjala for spawning factories
* "Pilot Training" focus: No longer gives 10% Ace Generation Chance, Now gives -25% Air Manpower Requirement
* "Naval Air Force" focus: Completion Time shortened to 35 days (was 70)

### "Foreign Aircraft" focus:
* Replaced with new "Purchase Blenheims" focus
    * Gives research bonus for Tactical Bombers
    * Grants 84 Tactical Bomber 1s if Tac 1 tech is researched (otherwise on research complete)
    * Adds timed spirit for 60 days that transfers 15% of civ industry to the Uk

### "Modernize Production Lines" focus:
* Now grants 5% Production Efficiency Base and 15% Production Efficiency Retention

## Naval Focus Changes
### "Suomen Merivoimat" focus:
* Now adds 5 levels of Port to Helsinki
* Completion time reduced to 35 days (was 70)
* No longer adds 1 Dockyard

### "Strengthen the Naval Bases" focus:
* No longer adds Ports and Coastal Pillboxes to Helsinki
* Now adds Ports and Coastal Pillboxes to Petsamo

### "Coastal Defense" focus:
* Now adds 1 extra Dockyard
* Spawn ins from decision no longer locked, now use Garrison Battalions

## Other Focus Changes
* "Arm the Lotta Svärd" focus: Now adds level 2 State AA to Uusimaa
* "Union of Finnish Brothers in Arms" focus: Now grants 1.5% Conscription (was 1%), Conscription Factor removed (was 10%)
* "Found Pohjolan Voima" focus: Will not select Karjala even if infrastructure level is 3 or above
* "Greater Finland" focus: Now changes Victory Point names in Olonets and Murmansk
* "Weapon Caches" focus: Completion Time reduced to 21 days (was 35), no longer cancels if invalid
* Some focuses had their bypasses and available conditions changed to account better for Barb starting mid-Winter War

## Map Changes
* Karjala now starts with 8 more mils
* Kuopio starts with 5 less mils, 1 less civ and Vaasa starts with 2 less mils
* Häme starts with a state modifier providing 42 coal and -10% local factory energy consumption
* Åland is now a Strait blocking the Gulf of Bothnia
* Åland Base Suppy increased
* Port added to Tornio
* Naval Tiles in the Baltic adjusted
* One Province from Troms moved to Finnmark state
* Removed/Reduced some VPs in southern and northern Finland
* Impassable borders changed
* Added Tulemajoki river in Karjala 
* Base Supply in the northern Finnish states adjusted slightly
* Petrozavodsk is now a Town tile, the Plains tile next to it is now a Forest tile
* Kirkenes is now a Plains tile
* Kirkenes now starts with level 2 Coastal Pillboxes

## Other Changes
* Changed Finland's starting templates and increased their starting division strength
* Finland starts with Interwar Bombers researched
* Sisu modifier Factory Bombing Reduction reduced to 50% (was 75%)
* General Aarne Juutilainen now has the "Winter Specialist" trait
* Field Marshal Mannerheim no longer has "War Hero" trait, now has the "Winter Expert" trait (he still has 2 open trait slots)
* Unique Operative "Vilho Tahvanainen" added to Finland (Infiltrator, Well Groomed)
* Unique Propaganda Campaigns added to Finland
* Unique Tank Chassis "BT-42" added to Finland
* Added equipment textures to Finnish tech tree and changed names of Finnish equipment
* Applied MIOs to starting production lines
* Changed order of Finnish starting production lines
* Winter War event now triggers its effect immediately, tooltip only for show
* Added "Fall of Helsinki" and "Fall of Moscow" (Finland) events
* Countries no longer get the "Finnish Motti Tactics" event
* New Player Help events for Winter War updated
* Some Broken/Unusable/Redundant decisions and events removed for QoL
* Mannerheim has his normal portrait again, you get a decision until Jan 3rd 1936 to give him the movie portrait back
* Finnish Continuous Focuses moved down slightly (Greater Finland focus no longer gets obstructed)
* An effort was made to increase legibility of some effects
* 3D Unit positions updated to fit naval map changes
* 3D Buildings adjusted in Karjala, Åland, Turku and Uusimaa
* 3D Trees added to some forest tiles that lacked them