## Mansion Mod

Main mod file is under game\overworld-town\Mansion and is running on an old version of the game, however that should not be an issue as the mansion is completely separate from the main game.

For a list of what is completed, and some other notes, see CompletedWork.txt

The file structure of the mod is simple, and I've compartmentalized everything pretty well, so it should be easy to work with it. Each chore, room, event, etc has its own file, so seeing what has or has not been done should be easily done by looking at the files. Honestly, looking at the file structure should go a long way in explaining what’s going on.

For now, you have to make a new save when testing the mod, however I have not found this to be an issue. This is because the mod uses new variables, and I have not figured out how to initialize new variables in an old save automatically. The link to entering the mansion is in the PCs bedroom.

When the player enters the main hall of the mansion, the list of chores is created, this is just for testing and will be done each morning. The main hall is also the only room with random movement events set up, but adding that to other rooms is simple. There is a link to a test room where you can begin some of the events and chores manually. 

If anyone wants to help, feel free to go over what I've written and give feedback/find misspellings. There will certainly be some of those. 
Or, if somebody wants to expand on, edit or write a new event, that would be appreciated too. Adding a chore event shouldn't be too hard. My goal for each chore event is to have sub events where the player can interact with each of a guard, guest or another servant while doing each chore.

My main goal right now is to complete all of the chores, daily events and morning events. Getting those done doesn’t require much else done. Then I can move on to refining the layout of the mansion, getting random events firing while navigating the mansion and getting guest rooms sorted out.

### Super Short TLDR:
The player is in a mansion doing work, possibly against their will. They are given a list of chores to do each day. Chores are things like cleaning a room or doing laundry. There are other events like serving or cooking dinner, one happens each day. There are rare events like a servant escaping that will happen some mornings.

# General Overview

There is a mansion in the woods about halfway between the lake and the town. The mansion is a sort of clubhouse where guests/club members go to relax and live for a while away from prying eyes.

The player is able to work there for money by signing a contract, or may be sent there by Bailey. If a contract is signed, the player determines how long they will be working at the mansion (longer = better pay rate), however you will not be allowed to leave before your contract is up.

There are three groups within the mansion, the mansion staff, the guests, and the servants. Each has its own “popularity” stat. More information can be found under *Popularity Stats*

Each day, the player is assigned a number of chores. The goal of the player is to complete these chores before the day ends. These chores are anything from cleaning specific rooms to cooking, to servicing guests. A few events will be locked by time and have to be done before a specific time. IE, the player cannot visit a guest after 1am if that is a chore. The list of chores can be seen under *Chore List*

In addition to these chores, each day the player will be given one daily task to perform at a specified time. Most days this is cooking but there are other events as well. These events can be found under *Daily Events*

Finally, on some mornings, a special event will fire. These events will have drastic changes on how that day professes. These events can be found under *Morning Events*

If the player misses a chore or task, they will be punished and get -mansion trust. Then depending on their overall mansion trust, they will be punished in a number of ways ranging from being forced into the dungeon or having their clothes privileges revoked. Missing chores or tasks also deducts from the pay the player will receive at the end of their contract. If that number goes to 0, they will not be allowed to leave even after the contract ends. The list of punishments can be found under *Punishments*

Once a player completes their list of chores for the day, they will have free time. The list of free time activities can be found under *Free Time Activities*

There are a number of ways for the player to escape the mansion. These ways can be found under *Escape Routes*

## Bedroom levels
Two different bedrooms the player can sleep in, which one they have access to depends on the mansion trust stat.
- dormitory, small single rooms
  - Access to shower, sometimes
  - Decent sleep, sometimes woken up
  - Hard to hide items
- Servant Suite
  - Access to limited wardrobe
  - Personal bathroom
  - Normal sleep
  - Easy to hide items
  - Can read books
  

## Popularity Stats
Popularity/social stat within the guests and servants. Will have to choose between increasing/decreasing relationships between guests and servants sometimes, or can trade time to better the relationship with either group.
- Guest relations effects
  - Starting trust when entering guest room
  - Less likely to be assaulted if the player expresses disinterest
  - More likely to get a good tip, or a tip at all
  - Might approach the player while working and strike up a conversation. The player can choose to interact or not
- Servant relations effects 
  - More likely to randomly get help with chores, reducing the time taken to complete it
  - Somebody starts the new load for you while you sleep in laundry
  - Servants come by and help/talk while you’re doing a chore
  - More likely to be saved when accosted by a guest
- Mansion Relation effects
  - Bedroom level
  - Leeway when making mistakes
  - Amount of punishment given to the player when they get in trouble
  - Specific events locked behind high trust


## Chores
During the week, the player is given a list of tasks they must complete throughout the day, shown by a widget at the top of each page. The player tries to complete tasks while being accosted and possibly while trying to find time to plan an escape. If a player doesn't complete a chore by the end of the day, they will be punished in some way.
 - Clean 
   - Kitchen
   - Dungeon
   - Private rooms
   - Strip Club
   - Guest rooms
   - Main hall
   - Dormitory
   - Garden
   - Library
 - Do laundry
 - Tend plants
 - Take care of guests on the patio
 - Deliver items between rooms
 - Clean empty guest rooms in between stays 
 - Bartend in club
 - Service Guest in their room

## Daily Events
Each weekday there will be an activity for the player to take part in at night. M/W/F that activity will be cooking. The activity will start at 7, unless otherwise stated, and last an hour. 
- Cook for dinner: The default daily activity. The player will cook food for the guests, choosing from a list of three food choices for the three courses of the meal. The player will be told how well the guests like the meal overall, and will have to guess at what choices they made that were correct. Each week the correct meal choices change. The player may be able to get info about the meals from overheard conversation after the first day of dinner, once per day. Or from talking with the guests while in their room.

- Masquerade ball: All the guests wear masks and get much more aggressive thanks to their anonymity. The servants must wait on the guests and provide food and drink. Gets more dangerous as the night goes on. Different rooms become more populated and more dangerous as the night goes on, forcing the player to move between rooms while working. They might meet Avery here, who might be willing to save you from the mansion.

- Garden Maze game: The player must attempt to run and hide from hunters, you are given a small head start to hide in the hedge maze. Don’t get caught. The maze is random, however going the right direction when coming to landmarks is how to advance in the maze. If the player hides well enough, they may be able to slip away.

- Dinner Party: 
The player is told to be a hostess for a dinner party, the player needs to wait on guests who might want a taste of something more than food.
  - You may be able to slip something into drinks, causing a panic that allows you free reign of the mansion for a short time.
  - You may be able to regulate the amount of drinking guests do.
  - After some parties (cumulative random chance, at most every other), the servants will be lined up and guests will pair off with them. If a guest is sufficiently drunk, they might just go right to sleep after picking you, letting you leave the room in peace. If the pair off does not happen, drunk guests can be dangerous.

- Mud Wrestling: While cliche, some members enjoy seeing two servants duke it out in the mud. Winner gets to be cleaned off, the loser gets mobbed. This event would happen in the day.

- Be a dancer in the club: Self explanatory

## Morning Events
On some mornings, an event will fire that does not have to do with chores or the daily event. These events have a drastic effect on how the day will progress.

- Escapee: Another servant has escaped, if you have high trust, you may be asked to help find them (new option added to each menu within quest widget). If you find them and turn them in, you will gain max trust. If you find them and don’t, they will tell you how to escape. Or you could just ignore them.

- Know your place: If the player gets too comfortable by having too much free time, they are reminded of where they are and what they are in an unsavory way. You are sufficiently traumatized, lose all sense of control and your daily tasks increase by 1 (system of dynamic difficulty)

- Player is rented out, yacht: An especially rich guest has “rented out” the player for a couple of days, you will be spending a lot of time with them on their yacht. 

- Player is rented out, room: A wealthy guest has requested, and paid a large sum, to have you visit their room at least once a day. Not doing so will anger the guest and the player will be punished until 7pm the next day and be sent off to the guests room with no chores.

## Escape Routes
 - Skullduggery + laundry: using a coat hanger stolen from the laundry room, build a lockpick. Use to unlock window or doors.
 - Athletics + garden: escape over a weak section of the garden wall, found while roaming in the garden maze. The path can be told to the player, navigation from landmarks is all that matters.
 - Library + dungeon: Find an old, locked secret tunnel while looking for books, have to find the key, which is in the dungeon. Each room will have a “search for library trapdoor key” in it. ExtraOptions widget.
 - Athletics + skulduggery: steal a butterknife, find sandpaper in a storage room.
 - Avery: find Avery using the mansions services or attending a dinner party, offers to get you out if his love or endearment is high enough.
 - Paperwork event: can find plans for the building, including secret passages and escape routes that only the manager knows about.
 - Time + eden encountered: purchased by eden 
 - Too much disobedience: sold to underground dungeon or farm

## Punishments
There are three categories of punishments, dungeon punishments, non-dungeon punishments, and daily event related punishments. If a punishment would prevent the player from completing chores, they will not be given chores for that day. There are three catagories of punishments; dungeon punishments, non-dungeon punishments, and daily event punishments 
### Dungeon Punishments
- Chained up in dungeon for a long period of time in different poses
 - Forced orgasms for camera
 - Accosted for camera

### Non-Dungeon Punishments
- Forced bondage while roaming, makes chores harder
- Forced vibrators while roaming, makes cleaning randomly fail and assaults more likely
- Removal of clothing privileges
- Harper experiments
- Tied up in personal room and accosted

### Daily Event Related Punishments
- Serve dinner
  - While naked
  - With vibrators
  - Before pair off, be completely bound
  - While drugged
- Garden Maze game
  - While feet chained
  - While nakes
  - With vibrators
  - While bound
- Masquerade party
  - While bound
  - With vibrators
  - While naked

## Free Time Activities
Once the player is done with their chores, they can do activities with their free time.
- Bedroom
  - Bathe
  - Read

- Library
  - Study subject

- Kitchen
  - Cook for self
  - Cook for others

- Garden
  - Sunbathe
  - Exercise
  - Plant for tending skill

- Dormitories
  - Console new servants
  - Discuss escape (can give hints for how to escape)
  - General chatting


## Guest Rooms
The Guest room mechanics are the least fleshed out. The general idea is that the player will be stuck in a guest room until a condition is met. They may be stuck for hours, but never more than a day. The guests opinion of the player is persistent and effects what they do to the player and what they allow the player to do. 

Often the player will have the chore of visiting a guest in their room ot service them. While in the room, they are expected to stay until the guest gives them permission to leave. While in the room, the guest anger, trust, etc will be persistant. Guests may keep the player in their room for a very long time (but never longer than a day), preventing the from doing other chores. To avoid getting in trouble, players can ask for the guest to get the player excused from their chores. Players may do a number of things while in a guest room, including things like:
- Ask to leave
- Ask for excuse note
- Talk with guest
- Take a bath
- Sleep in guest bed
- Sleep on floor

### Guest Room Descriptions
Guest rooms will have multiple different layouts, some layouts have an effect on what can happen to the player and what the guest does.

- The room is clean and well kept, a bed sits in the corner and across from a TV. 
- This room is cluttered, but otherwise clean. It looks like this guest has lived here for a while, with some personal effects strewn about on various tables.
- This room is more barren than others you’ve seen, there is just a single bed in the center of the room and nothing else.
- Entering this room, you get a shiver down your spine. Chains dangle from the ceiling, and a small metal loop sits underneath it. There is a small bed in the corner. The guest pushes you in and shuts the door behind you.
- This room seems normal enough, a bed sits in the usual corner and there is a small table on the other side of the room. As you walk further in, your heart drops as you see small specks of something red on the wall near the bed.

### Guest Quirks
When the player enters a room, the guest will be assigned a list of quirks that interact with what the player is doing, and the guest will say and do different things depending on those quirks.
- Wants a specific act preformed
- Wants the player to leave immediately
- Refuses to let the player leave, but will sign an excuse note if the player doesn’t push it
- Refuses to let the player clean themselves
- Doesn’t want the player to make a sound
- Silent guest hurts the player when they talk
- Stops before player cums, gets angry when player does. 
- Uses toys during sex.
- Chokes or beats the player, player passes out after encounter. Wakes up in same guest room. Maybe alone, maybe tied up, maybe with toys.
- Leaves the player alone in the room, maybe tied up, maybe with toys.
