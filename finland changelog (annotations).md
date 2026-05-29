# **Finland Rework Changelog (with annotations)**
#### This is a markdown file, if using VSCode press "Ctrl K" then "V" to view correctly
## Main Finland Winter War changes
### Winter War spirit:
* Changed picture
* No longer reduces Winter Attrition
* No longer grants 10% Core Defense #Moved to "Kollaa Kestää"
* Now grants 5% extra Factory Bombing Reduction #Kinda compensating for reduced bombing from "Sisu" doesn't rly matter though
* Now grants 5% Division Organisation #Half of this is compensation for reduced stats from "Jaeger Movement"

### Added new timed spirit "Kollaa Kestää" for 105 days on start of the Winter War granting:
* -1.5% Weekly Balance of Power #Should be enough to eventually nerf Sisu stats by 1 level to make Soviets breaking the line more likely
* 10% Supply Range
* 10% Core Attack
* 10% Core Defense
* 15% Piercing and 10% Hard Attack to Line AT

### Added new Event "Swedish Volunteers" for Finland 10 days into the Winter War #A Cry For Help doesn't spawn a bugged event anymore
* Spawns (1) locked 11/4/4 "Swedish Volunteers" Division led by Ernst Linder in Tornio #Is meant as a boost to finnish fighting strength even for unoptimized builds (there is like a 5% chance this can cause issues due to the way it uses 3D model and support companies, probably fine tho)
* Division is deleted after the Winter War (or if Barb starts mid-Winter War) #There is like 3 seperate checks trying to avoid being able to keep the division after Winter War ends (Doesnt spawn if at peace with SOV, is removed on GER being at war with SOV, is removed by Winter War ending events)

### During the Winter War a new timeout decision will fire:
* 1 factory from Karjala is automatically relocated to Häme every 7 days #Mils are evacuated before civs
* Evacuating a factory adds 1% Stability
* Fully evacuating the state gives 5% War Support #This should take 105 days due to the changed starting industry (10 mils, 5 civs)
* Losing control of Karjala or Häme before all industry is evacuated removes 15% Stability and gives the Soviets an event (after the Winter War) to move the remaining mils to Olonets #No event if no mils

### Added new events for losing/winning the Winter War as Finland #Mainly just to clean up the code and tooltips and other minor stuff
* Winning now grants +25% Balance of Power #Helps negate some BoP lost from Kollaa Kestää
* Losing now grants +5% Balance of Power, adds state modifier: "Hanko Occupation" to Uusimaa, relocates Salla VP, and re-demilitarizes Åland if focus "Operation Kilpapurjehdus" hasn't been completed #This means you can do "Operation Kilpapurjehdus" after the Winter War if you forget it before

## Comintern Changes
* Sergey Khudyakov (Close Air Support Expert) advisor is now locked behind winning the Winter War #This is mostly to make CAS damage calculations easier, shouldn't affect balance in any way

### "Claims in Baltic" focus:
* Now just requires Germany being at war (Was Germany being at war with Poland/Poland not existing) #This is done because I want to avoid cucking soviets out of their tree by not declaring on Poland, also the Winter War focus is timegated now
* Completion Time reduced to 21 days (was 35) #This is done to give enough time to ensure Romania/Finland wars happen on schedule

### "Baltic Security" focus: #Not super clean but Winter War actually happening around Winter is desirable and creates some sense of urgency to select focus for Soviets
* Now requires the date to be between November 1st and December 31st 38/39 or past August 1st 1940 (focus continues if requirements are no longer met) #Its August 40 to give Soviets enough time to do Romania war ##That should probably be removed anyways imo

### Added new spirit "Terror Focused Bombing" for Soviets during the Winter War: #Idea is to reduce IC loss from Cas and Logi strikes to make it less punishing to fight, without significantly affecting the org performance of Cas bombing
* Reduces CAS damage by 90% #This also affects Logistics Strike
* Increases CAS Org damage by 400% #This should bump cas org damage back up to normal (if using air doctrine modifiers) ##You can stack up to 20% ground attack for CAS and 15% for Tacs ((1.0 - 0.9 + 0.2) x 4 = 1.0 + 0.2) CAS deals same org damage as before if modifiers are stacked (technically 4% less due to doctrine 5% org damage modifier), tacs deal only base org damage ((1.0 - 0.9 + 0.15) x 4 = 1.0)
* Reduces Strat Bombing by 15%

### New Winter War related focuses added: #Choice to push for Oulu or break the South
* "Skewer Finland", gives 20% Supply Range and -5% Winter Attrition for 180 days
* "Crush Finland", gives 10% Strat Bombing and 5% Attack and Defense against Finland for 90 days
* The focuses are mutually exclusive
* "Dismantle the Stalin Line" no longer clogs error log, now correctly removes all Stalin Line forts
* "Start Contstruction on the Molotov Line" focus moved below "Secure New Conquests", "Plunder the Baltics" now directly leads to "Prepare to Invade the West"

### "Brothers War" modifier:
* Now reduces CAS damage by 90%
* Now reduces Strat Bombing by 90%

## Winter War decision changes
* Surrender/Victory decision timeout lowered to 5 days (was 7) #Less risk of clicking victory but losing anyways
* Added new timeout decision for Finland that shows the Soviet time limit #Just cosmetic, but quite useful
* Time limit for Soviets reduced to 180 days (was 210) #210 days feels too long, making it 180 makes it feel more like you're on an actual timer
* Soviets no longer get a buff after taking 125k casualties, both casualty timeout decisions no longer visible #These are "The structure is Rotten" and "Learn from our Failures" time out decisions ##They still exist but now its the lowtiergod impassable country that gets them (this shouldnt affect anything gameplay wise)
* Soviets can now always force Finland to surrender if they control Viipuri #People always thought this was a thing for some reason, it is now
* Casualties required to force Finnish surrender lowered to 65k (was 85k) #War is shorter and CAS should kill much less ##Ideally casualty limit could be even lower, IDM Sov players winning by casualties since it should allow Finland some industry evacs
* Casualties required to surrender as Finland lowered to 40k (was 65k)
* Casualties required to declare victory as Finland reduced to 275k (was 350k) #War is shorter, still dont expect people to actually reach this number unless soviets giga troll
* Winter War (and Continuation War) decisions moved to "National Defense" decision category #Was "War Measures" before, this should make it easier to locate the decisions ##Soviet decisions are still in "Operations" category
* Winter War decisions should now dissapear if Barb starts mid-Winter War #Attempt to fix existing exploits/weird interactions, may still cause issues ##Industry Evacuation doesnt dissapear, thats semi-intentional and semi-idk how to make it happen considering how loaded that decision already is with conditions

## Mannerheim Line Changes
### Karjala starts with new state modifier "Crumbling Fortifications" granting:
* Pillbox effectiveness -15%
* Maximum Pillox level -2

### "Mannerheim Line" focus:
* Removes Crumbling Fortifications modifier
* Instead of 3 levels of Pillboxes now adds 2 levels of Fortresses and 1 level of Pillboxes #Mainly to make the Mannerheim Line more significant as a fortified position, the Forts should still not be a huge issue
* Now adds lvl 2 State AA
* Adds 1 extra Pillbox on the Supply Hub in eastern Karjala
* Adds 1 extra Coastal Pillbox on Viipuri
* No longer adds Pillboxes on Viipuri (was 2)
    #### Mannerheim Line state modifier:
    * Now reduces enemy local supplies by 10% #This is to counteract the 10% local supply buff it gives, technically that buff shouldnt apply to Soviets since its a modifier scoped for Finland only, but this modifier is broken and applies to everyone, fixing would be much harder
    * Pillbox Construction speed now works #Previously did not
    * Coastal Pillbox Construction speed removed
    * Now reduces maximum Pillbox level by 1 #Pillbox maximum is slightly reduced because of the Fortresses
    * Now removed on state owner change (previously on state controller change) #Essentially what this means is that the modifier is only removed if Finland loses the Winter War or is full annexed

### If Mannerheim Line was constructed and Winter War was lost:
* Fortresses are removed #This is to make it harder for Soviets to use the Mannerheim line against Finland, since its unbombable anyways it would be kinda busted
* Crumbling Fortifications modifier reapplies #Same as with the Fortresses, Sov debuff
* Unlocks new decision after reintegrating Karjala and Salla: #This decision costs 50pp and uses 5 civs for 90 days, is cancelled if you lose control of Viipuri
    * Restores Fortresses to Karjala
    * Removes Crumbling Fortifications state modifier
    * Adds back Mannerheim Line state modifier

### "Defense in Depth" focus:
* Now adds Pillboxes even if you don't control Karjala (Won't add the ones in Viipuri)
    #### "Fortification Effort" modifier:
    * Pillbox Construction speed reduced to 10% (was 20%)

## Fascist Finland Changes
* "Academic Karelian Society" focus: No longer grants 5% Stability
* "Advanced Jaeger Training Program" focus: Special Forces Cap reduced to 2.5% (was 5%) #Overall the cap stays the same because Jaeger movement gives more, just done to make Neutral Finland more appealing
* "Mustapaidat" focus: Now gives Militia tech, the template is no longer locked #Should make garrisoning easier, may be too strong depending on doctrine meta
* "Sotilaalliset Kappalaiset" focus: Now adds additional 0.5% Conscription to the Patriotic Peoples Movement modifier 
* "National Fanaticism" focus: Militia org bonus reduced to 5% (was 10%), no longer gives 5% Militia Speed
* "Maan Turva" focus: No longer adds 5% War Support
* "Intellectual Elite" focus: No longer adds Karelian Irredentist Writer advisor

### "Join Axis" focus:
* Name changed to _Finnish Irredentism_
* Picture changed
* Requirements slightly changed
* No longer bypasses #More focus time to justify making Jaeger Movement a 35 day focus
* Now always adds 5% War Support #Previously added conditional War Support from event
* Now unlocks Karelian Irredentist Writer advisor

### "Bring Foreign Armor Experts" focus:
* Now requires having researched BT-42 Chassis, previously Improved Light Tank Chassis
* Now grants 1x 50% Mechanized research bonus

### "Keepers Of The North" focus:
* No longer asks nordic countries for annexation #This was always weird anyways since it only worked on AI Denmark and probably just better to have it removed fully
* Now unlocks decision to seize Finnmark from RK Norway should it exist #Finnmark is cored by "Greater Finland" focus so this helps you actually get that core state while Germans can still get RK benefits

## Neutral Finland Changes
### "Lone Wolf" focus: #New faction system basically makes joining Axis essential and this should finally stop faction joining softlocking
* No longer unavailable if in faction
* No longer grants 5% Stability
    #### Lone Wolf spirit:
   * No longer gets removed
   * No longer prevents joining the Axis 
   * Now grants 5% Core Attack  #Neutral Finland should have slightly more of a bite now
   * Now grants 1% Conscription (was 0.5%)
   * Some previous modifiers were removed

### "Cooperation With Germany" focus:
* No longer bypasses if in faction with Germany

### "German Military Advisors" focus:
* Completion time increased to 70 days (was 35) #More focus time justify making Jaeger Movement a 35 day focus
* No longer grants doctrine cost reductions
* Nikolaus von Falkenhorst advisor buffed #Paratrooper stats (AA Attack, Org After Dropping) increased, but Command Power Increase removed (was 60)
* Now grants 2x 25% research bonus for Special Forces technology
* Now unlocks new paratrooper raid "Operation Hokki" against Olonets: #Mainly larp but should provide slight help in capturing Olonets if you went for Paratrooper SF
    * Debuffs Soviet speed, disables Soviet strat redeployment, and causes attrition
    * Executable by 16+ width Paratroopers
    * Requires 5 Transport Planes, 100 Support, and 200 Inf equipment
    * Modifier lasts for 45/60/75 days depending on raid outcome
    * One time usage
    * Is removed on capture of Petrozavodsk/Äänislinna

### "Finnish March Of Conquest" focus:
* Name changed to _To The Urals!_
* Picture changed
    #### Finnish March Of Conquest modifier: #Having to worry less about ideas expiring makes Neutral Finland more attractive to non-optimized builds (which is where I want them)
    * Duration increased to 450 days (was 356)
    * No longer gives 5% recovery rate

## Army Focus Changes
* "Suomen Maavoimat" focus: Tension requirement lowered to 20% (was 25%) #Winter War being more important requires low-tension games to be less unplayable

### "Operation Kilpapurjehdus" focus: #Now relevant focus to guard against invasions
* Completion Time reduced to 7 days (was 35)
* Tension requirement lowered to 50% (was 80%)
* Now grants 1 less Pillbox, but 1 more Coastal Pillbox

### "Underground Resistance Cells" focus: #More historically accurate and should make Finnish resistance more of a problem for Sov players that occupy Finland
* Picture changed
* Completion Time reduced to 21 days (was 35)
* No longer requires being in a defensive war
* Now requires having >10% Surrender Progress and being in a faction with Germany
* Now available if country has capitulated
    #### Underground Resistance Cells modifier:
    * No longer provides Targeted Sabotage modifiers
    * Now grants -20% Compliance Growth Speed in Finnish states 

### "Jaeger Movement" focus: #More pre-Winter War time for important focuses
* Completion Time reduced to 35 days (was 70)
* No longer gives 5% Breakthrough
* Division Organisation modifier reduced to 2.5% (was 5%)
* Special Forces Cap increased to 7.5% (was 5%) #This only matters for Neutral Finland, since Fascist Finland had its Special Forces Cap reduced

### "Motti Tactics" focus:
* No longer grants 2.5% Attacking Division Speed
* Now grants Mastery bonus (Political Tree Mastery bonuses nerfed)

### "Long-Range Patrols" focus 
* Now unlocks new Land Raid against Soviet controlled states: #Attempt to make Finnish pushing power more specialized
    * Grants 5% Attack and 10% Breakthrough in the target state
    * Executable by 20+ width Special Forces (Rangers/Mountaineers)
    * Requires 50 SF equipment
    * Only available in Finnish and Soviet cores north of Moscow (Not in Uusimaa or Leningrad)
    * Modifier lasts for 60/65/70 days depending on raid outcome
    * Can be done multiple times (60 day cooldown per state)
    * Limited to 3 raid attempts per game #Mostly to make the raid alert less annoying for Soviets

### "Sissi" focus: #Want a more meaningful choice between the two focuses
* No longer gives 5% Recon Bonus While Entrenched
* No longer gives 10% Attack and Defense to Long Range Patrol Company support #As far as I can tell this was broken and useless anyways
* Now grants 3% Attacking Division Speed

### "Nation Armor Focus" focus: 
* No longer gives 1x 50% Armor research bonus
* Completion Time reduced to 42 days (was 70)
* Now adds Land Warfare Facility to Häme #This shouldnt matter too much since its a focus you will usually do pretty late anyways

### "Salvaged And Retooled" focus: 
* No longer gives 1x 50% Mechanized Armor research bonus #Moved to "Bring Foreign Armor Experts"
* Number of 50% Armor research bonuses reduced from 2 to 1
* Now gives 1x 100% research speed for BT-42 Chassis #BT-42 Chassis is now the tech needed for Fascist focus "Bring Foreign Armor Experts"

## Air Focus Changes
* "National Aircraft Production" and "Expand Producton Lines" focuses: No longer randomly select Karjala for spawning factories
* "Pilot Training" focus: No longer gives 10% Ace Generation Chance, Now gives -25% Air Manpower Requirement
* "Naval Air Force" focus: Completion Time shortened to 35 days (was 70)

### "Foreign Aircraft" focus:
* Replaced with new "Purchase Blenheims" focus
    * Gives research bonus for Tactical Bombers #1x 150% bonus normally but reduced to 1x 50% bonus if you already researched Tac Bomber 1
    * Grants 84 Tactical Bomber 1s if Tac 1 tech is researched (otherwise on research complete) #Keep in mind Finland now starts with Bomber 0 tech so only 1 research is needed
    * Adds timed spirit for 60 days that transfers 15% of civ industry to the Uk #Same way Romania tree does it, just kinda larp

### "Modernize Production Lines" focus:
* Now grants 5% Production Efficiency Base and 15% Production Efficiency Retention #I still dont expect people to actually bother with picking this over the Mil focus but its not giga useless like before

## Naval Focus Changes
### "Suomen Merivoimat" focus: #This exists to prevent a supply routing bug after capturing Leningrad due to port level difference
* Now adds 5 levels of Port to Helsinki
* Completion time reduced to 35 days (was 70)
* No longer adds 1 Dockyard

### "Strengthen the Naval Bases" focus:
* No longer adds Ports and Coastal Pillboxes to Helsinki #By the time you get to this focus you already have level 10 Port and you can get level 6 Coastal Pillboxes through other effects
* Now adds Ports and Coastal Pillboxes to Petsamo

### "Coastal Defense" focus:
* Now adds 1 extra Dockyard
* Spawn ins from decision no longer locked, now use Garrison Battalions #6 width slop

## Other Focus Changes
* "Arm the Lotta Svärd" focus: Now adds level 2 State AA to Uusimaa #They operated an AA Searchlight Battery historically, also less bombing reduction from Sisu
* "Union of Finnish Brothers in Arms" focus: Now grants 1.5% Conscription (was 1%), Conscription Factor removed (was 10%) #This should make Finland have more manpower early but less lategame
* "Found Pohjolan Voima" focus: Will not select Karjala even if infrastructure level is 3 or above
* "Greater Finland" focus: Now changes Victory Point names in Olonets and Murmansk
* "Weapon Caches" focus: Completion Time reduced to 21 days (was 35), no longer cancels if invalid #Still bad
* Some focuses had their bypasses and available conditions changed to account better for Barb starting mid-Winter War

## Map Changes
* Karjala now starts with 8 more mils
* Kuopio starts with 5 less mils, 1 less civ, and Vaasa starts with 2 less mils
* Häme starts with a state modifier providing 42 coal and -10% local factory energy consumption #Finland has gained 1 mil and 42 coal but lost 1 civ
* Åland is now a Strait blocking the Gulf of Bothnia
* Åland Base Suppy increased
* Port added to Tornio
* Naval Tiles in the Baltic adjusted #Makes borders fit with new strait, no changes to which tiles border which have been made but 2 tiles have swapped seazones
* One Province from Troms moved to Finnmark state #This is only to make borders prettier
* Removed/Reduced some VPs in southern and northern Finland #Idea is that VP snipe naval invasions don't work and to win the Winter War you need to conquer either Viipuri or Lappi+Oulu
* Impassable borders changed #This is to further separate the North and South as possible directions of attack for Soviets
* Added Tulemajoki river in Karjala 
* Base Supply in the northern Finnish states adjusted slightly #Realistically can be ignored
* Petrozavodsk is now a Town tile, the Plains tile next to it is now a Forest tile  #Should make the state more interesting to fight over
* Kirkenes is now a Plains tile #Works better for continuation war combat
* Kirkenes now starts with level 2 Coastal Pillboxes #Increased Naval Penalty to make it not as easy to invade

## Other Changes
* Changed Finland's starting templates and increased their starting division strength #Finland starts with 4183 more Inf Equipment (464 of these are Gun 0s), 542 more Squad Equipment, and 192 more Support Equipment
* Finland starts with Interwar Bombers researched #Pretty much only so that the Blenheim focus is cleaner
* Sisu modifier Factory Bombing Reduction reduced to 50% (was 75%)
* General Aarne Juutilainen now has the "Winter Specialist" trait #He is still not good enough to warrant using normally (Matti Aarnio and others are just better in comparison) ##He was historically important in the Winter War and being able to get Adaptable should also make him better for actual Mountain warfare, which makes using him for fighting in Narvik more appealing
* Field Marshal Mannerheim no longer has "War Hero" trait, now has the "Winter Expert" trait (he still has 2 open trait slots) #Technically I gave Mannerheim 1 Extra Trait Slot, but this doesnt matter since its taken up by Winter Expert ##The reason for this change is to make Mannerheim slightly more unique (people kinda dont like using him for the Continuation War), but also to actually make the Winter Expert trait something players get to see/use for once ###War Hero trait removal is literally just to clog the UI less, it did basically nothing
* Unique Operative "Vilho Tahvanainen" added to Finland (Infiltrator, Well Groomed) #This guy existed historically, although its like 90% confirmed he was just lying about being a bond level spy ##I do think its a good idea to have a unqiue spy ##Well Groomed doesn't actually do anything but its a cool trait
* Unique Propaganda Campaigns added to Finland
* Unique Tank Chassis "BT-42" added to Finland #This is just a BT-7 that can mount the Light Casemate Turret, but ONLY the Light Casemate ##I expect it to be pretty mid or even useless but is added for funny larp ###Useless doesnt mean researching doesnt have a purpose, since its a requirement for "Bring Foreign Armor Experts" focus
* Added equipment textures to Finnish tech tree and changed names of Finnish equipment #Changed Infantry and Artillery tab to be mostly unique and added Blenheim sprite to Air tab
* Applied MIOs to starting production lines #NOT to the equipment itself, just the production line
* Changed order of Finnish starting production lines
* Winter War event now triggers its effect immediately, tooltip only for show #Most events added by the rework also do this, it just gives people time to read effects while already having the benefits + removes event holding trolls
* Added "Fall of Helsinki" and "Fall of Moscow" (Finland) events #I noticed noone gets an event if Finland is the one to take Moscow, this is bad since allies seeing that event often makes them hurry up on DDays ##The Fall of Helsinki event is just cuz why not
* Countries no longer get the "Finnish Motti Tactics" event #The event wasnt relevant anyways, less mid-war popups is good for Soviets
* New Player Help events for Winter War updated
* Some Broken/Unusable/Redundant decisions and events removed for QoL
* Mannerheim has his normal portrait again, you get a decision until Jan 3rd 1936 to give him the movie portrait back
* Finnish Continuous Focuses moved down slightly (Greater Finland focus no longer gets obstructed)
* An effort was made to increase legibility of some effects
* 3D Unit positions updated to fit naval map changes
* 3D Buildings adjusted in Karjala, Åland, Turku and Uusimaa
* 3D Trees added to some forest tiles that lacked them