White paper: 

# Location-based entertainment
Developing a large-scale multiplayer VR experience

![Players enjoying an LBE experience](https://www.roadtovr.com/wp-content/uploads/2015/05/2player-thevoid.jpg)
Figure 1: Players enjoying an LBE experience


# Introduction

Location-based entertainment (LBE) continues to grow as a popular form of immersive gameplay and role-playing. Players, wearing virtual reality headsets and motion capture sensors, explore a virtual environment, interact with each other or in-game characters, and perform game tasks such as walking a maze, solving puzzles, and even fighting enemies. Players sometimes carry prop weapons and other items. Examples of LBE experiences are Star Wars: Secrets of the Empire and Ralph Breaks VR.
[IMAGE]
LBE experiences offer exciting opportunities for creativity, entertainment, and business investment. An LBE experience is run on powerful hardware and software in a fixed physical space, presenting real-time motion and graphics to players through their VR headsets. The experience often includes physical enhancements such as wind, heat, and sound. 
Such a setup offers developers, artists, and storytellers the chance to create rich, complex VR experiences that take place in universes outside our own. THE VOID, for example, has produced many such experiences that can immerse up to four players in the worlds of Star Wars (Star Wars: Secrets of the Empire), Marvel comics (Avengers: Damage Control), the colorful, light-hearted cartoon world of Wreck-It Ralph (Ralph Breaks VR), and even the gritty streets of a dystopian 19th-century Chicago (Nicodemus: Demon of Evanishment), just to name a few. The experiences are housed at shopping centers and theme parks around the globe as well as at THE VOID’s own office in Santa Monica, CA.
Corona beer even got into the game with their promotional Paraiso Secreto experience in Mexico City, working with The Mill and Wieden+Kennedy to combine live theater and VR and immerse visitors in a “secret paradise”. The experience sent them through a magical doorway to a dense, full-sensory jungle—including real foliage they could touch, and virtual flying birds and fluttering butterflies—to reach a sunny, sandy beach complete with real-life bottles of ice-cold Corona for visitors to enjoy.


# Business opportunities

Virtual reality is fast becoming big business, with entertainment at the forefront. According to the Tractica Report Virtual Reality for Enterprise and Industrial Markets published in Q2 2018, a diverse range of 100+ companies operate in the enterprise VR ecosystem, including tech giants (Facebook, HTC, Intel), technology enablers (Tobii, Leap Motion), and content developers.
The report estimates that the amusement sector will be the most important category for enterprise VR hardware and content in the year 2021. Here are the key industries and their estimated 2021 spending on VR hardware and software:
Location-based entertainment (attractions): $4.5 billion
Training and simulation: $2.2 billion 
Education: $1.6 billion 
Medical therapy: $357 million 
Virtual prototyping / 3D modeling: $349 million 
The item with the highest estimated spend is location-based entertainment (LBE). 
Why this paper?
Advances in real-time rendering and programmable controls, typically through a game engine running on advanced graphics hardware, are what make LBE possible now. But with LBE being a fairly new form of entertainment, there is no turnkey LBE kit one can order. 
All the hardware and software components needed to develop and run an LBE experience are readily available, but the design, creation, and running of such a system, if not done correctly, can result in cost overruns or a poor player experience. To construct a smoothly functioning LBE system within budget, you’ll need to choose your hardware wisely and set up all the controls correctly.
With this in mind, in this paper we explore a tried-and-true approach to designing an LBE experience, including the selection of modestly priced hardware that supports true player immersion. This paper focuses on a technical solution that includes the real-time game engine Unreal Engine (UE) from Epic Games.
LBE versus home-based VR
LBE is a cousin to the home-based VR experience, but there are significant sharp differences that affect the relative scopes of these types of entertainment. 
LBE strives for true immersion, which requires a fixed, open space with room for multiple players, mocap equipment, and physical cues like props, wind, or heat, none of which are part of a home-based experience. The hardware, which sits onsite at the venue, can consist of multiple servers, high-end graphics cards, and other hardware that consumers wouldn’t ordinarily have at home. The high-end setup means that LBE can include scenarios that are far richer and more complex than those you might find in home-based VR.
With any VR experience, developers must pay close attention to how the complexity of the virtual scene affects real-time performance, and make compromises to keep the frame rate high. While this is true for both home VR experiences and LBE, the fact that LBE can use customized hardware means that fewer sacrifices are necessary to create a rich environment with engaging gameplay.
Part I: LBE planning
Before you dive into creating a virtual world and putting together hardware and software, a few planning tasks are in order.
Resources
An important first step is taking stock of resources available to your team, now or in the near future. Important questions to ask yourself are:
What kinds of spaces are available for housing the LBE experience, and what are the dimensions and costs of each?
What kinds of mocap suits and VR headsets are readily available?
What information is tracked in the Wi-Fi zone, and what are the needs for the LBE network?
Who on the team will produce the assets, and who will create the experience in Unreal Engine?
How will the investment be recouped?
Scope of experience
Determining the scope of the experience often entails working back and forth between the story, the proposed virtual action, available hardware, and other factors like the duration and number of players, until all are aligned in a cohesive plan.
Story
Crafting the story for your LBE is a task in itself. What does the virtual location look like? What activities and challenges will the players face?
A study of all the factors for a good LBE story is outside the scope of this paper. However, learning about all the other setup considerations will help you form an LBE story that will work within your chosen framework. 
Also, realize that the story will likely shift and change as you develop and test the experience. It is not uncommon for a team to adjust the experience during development due to poly count, VFX or hardware limitations, and tester feedback.

Figure 3: Scene from LBE experience by Normal Studio. ICARE: Canne XR Experience
[Image from Normal studio]
Duration
Most LBE experiences are between 5 and 20 minutes long. Too short, and users feel shortchanged. Too long, and you’ll need to develop a lot of content and activities to keep users engaged. Choose a duration for which you can reasonably produce engaging content with your resources. 
Number of players
How many users will participate in the experience at any given time? The number of players will determine the hardware and network—a two-player experience will require less installation than an eight-player experience.
You will also need to consider the maximum number of player groups you’d like to roll through in a day, which will tell you how much time you’ll need between groups. This decision will also inform your choice of hardware and player gear.
Virtual portals
In most cases, you will want players to feel as though they are visiting a space much larger than the physical space. The construction of a story and VR environment that achieves this goal is a key component in an engaging LBE experience.
One way to do this is to occasionally open up a virtual portal that displays a new room to players, basically a virtual door that starts out as closed or solid but opens up or becomes transparent when players come near it or perform a specific task. Participants will feel like they are entering an entirely new space while they are really just doubling back through the same physical space they were in a moment earlier. The newly entered space can be made to feel quite different through mechanisms like virtual ceiling height and sensory cues for indoor versus outdoor environments. 
The Corona Paraiso Secreto experience includes an excellent example of an indoor-to-outdoor virtual portal, as does the project ICARE from 4DART.

Figure 5: What the player sees when looking up in the 4DART project ICARE from Normal Studio after going through a virtual portal
[Need permission from Normal Studio / 4DART project ICARE]
https://4dart.com/fr/creation/2020/icarus-realite-virtuelle-mixte/

Virtual interaction
It is also at this first stage that you need to determine the desired level of virtual interaction related to storytelling. Within the story, the player must receive enough sensory feedback to feel that he or she is actually present in the environment. In general, the more sensory feedback you plan to provide to players, the more sensors you will need for both player gear and your fixed hardware setup. More sensors means higher cost as well as more setup and maintenance, so you will need to balance the needs of your story with these factors.
At a minimum, the system will need to track the locations of players as they move around the space so it knows which part of the environment to show them in their VR headsets. This will require motion capture gear, which is discussed in more detail in a later section. 
Beyond this minimum requirement, you will need to decide whether players will be able to see other players, and their own bodies, as avatars within the experience. With avatars, in general, many more sensors are required than for non-avatar experiences. However, certain tricks can be put in play to minimize processing time for the data received by these sensors. We will discuss these tricks in Part II of this paper.
You can also include non-visual cues to enhance the sensory experience such as physical lamps or fans that activate during certain scenes of the story, and sound effects or animated sequences that play at specific times. 
Usually, triggers that depend only on overall timing, or on general player proximity to a known location, do not require additional sensors. A trigger such as “Activate fans eight minutes after the experience starts” can be simply programmed into the experience, while the trigger “Activate fans when at least one player is within two feet of wall #3” can be set off from location data already coming from motion capture sensors on players’ bodies. 
However, cues that depend on specific types of player motion might require additional gear such as haptic sensors worn or held by players. These sensors track finer motions and locations of a specific player’s arms and hands, such as those involved in wielding a weapon or grabbing a virtual object. Haptic sensors add expense and complexity to an LBE experience, but can also make the experience far richer for players. These systems are discussed in more detail in the Feedback systems section.
A good first step in planning your LBE experience is to determine the ideal amount of virtual interaction, and also the minimum that you would consider. Then you can look at your options with regard to cost and practicality within that range.
Physical space
How much space is the right amount? A 2000-square-foot arena offers a superior experience, and can allow more players at the same time. However, such a large space is more expensive to use and maintain than a smaller room.
Any large space will require tracking mechanisms placed at intervals around the room. Due to budget considerations, a number of LBE operators have chosen to use smaller spaces of 30' x 30' or even 20' x 20’. With such a small space, the setup can use a less expensive tracking mechanism. The VR space can be made to feel much larger than the physical space through cleverly designed 3D environments and the use of virtual portals,

Figure 1: 
[Image from Dark Slope]
Spaces that are more than 50’ x 50’ in size require more powerful capture systems. Also, the higher the number of players, the higher the hardware and server requirements. 
Motion capture system
An LBE experience, by nature, requires some form of motion capture system. A motion capture system records and transmits the motion of players during the experience. The players wear sensors on their bodies, and stationary mechanisms (cameras, base stations, computers) continually capture the motion data from the sensors. Props and weapons may also be tracked with motion capture.


[6 DOF setup for LBE with Optitrack Motive. Could also use this image: https://optitrack.com/public/images/motive-active-vr.jpg]
This captured data is used for a variety of purposes during gameplay: 
Sensing the location of each player (minimum dataset for LBE) - The system computes and displays each player’s view of the environment in the player’s VR headset.
Sending avatar visuals to players’ headsets - The system can retarget each player’s movements to a digital avatar, render the visuals showing this movement, and transmit the visuals to other players’ headsets so each player can “see” the others.
Triggering environmental changes - The system can use the player’s location to determine when to change the visible environment, open a virtual portal, or play an audio clip.
Triggering feedback - The system can use location and motion data to determine when to deliver haptic (tactile) feedback to add to the sensory experience. This mechanism is described in more detail in the Feedback systems section of this paper.
Mocap gear
While you have likely seen imagery of film actors wearing close-fitting mocap suits, such suits are impractical for an LBE experience—besides the fact that your players will likely come in many shapes and sizes, the suits would need to be cleaned between each wearing.
With LBE, the more usual solution is to provide wearable gear that players can put over their own clothes, such as a vest or backpack. Some gear, such as headsets and gloves, can be worn against the player’s skin, with easy solutions for maintaining hygiene from one session to another. These measures are similar to those used by gyms and exercise classes, where equipment is often handled by many patrons. For example, players can be provided with a disposable soft silicon face cover to wear under the headset, or the headset can be quickly cleaned with disinfecting wipes between sessions. 
Optical versus inertial
Most body motion capture systems can be categorized as using optical or inertial sensors or markers. Optical sensors and markers, as the names suggest, make use of light to capture motion data. 
Passive optical markers reflect light, while active optical sensors transmit infrared (IR) light to provide signals to the cameras or base stations. When multiple players are involved, active markers can be set up to transmit a different ID for each player. Active markers help the server separate the motion data coming from different players.

Figure 8: Hybrid inertial/optical glove
Image source: https://manus-vr.com/manus-vr-and-optitrack-partner-up-for-hybrid-mocap-glove/
To effectively track motion, both passive and active markers rely on the design and placement of rigid bodies, which are fixed configurations (or “constellations”) of three or more markers. The tracking system uses the known distances between these markers to help track motion. 
A rigid body of passive markers relies on the relative locations of the markers in the pattern, while active markers’ rigid bodies rely directly on the ID light pattern. 

Figure 8: OptiTrack Active Puck with rigid body
[Image from OptiTrack website.]

Optical systems really have only one serious limitation: the camera or base station must be able to “see” a sensor in order to get its position. This means that characters in close proximity to one another are likely to block each other’s sensors, causing the system to “lose” the character’s limbs or torso from time to time. Multiple cameras or base stations can help, but can’t remove the risk of occlusion completely.
Conversely, inertial sensors use gyroscopes, accelerometers, and magnetometers to calculate the current position of the sensor in XYZ space and transmit this data to a base station, with a signal that traverses around players and obstacles. 
Inertial systems also have a serious limitation: Because the player’s XYZ position is inferred from data like the acceleration of the sensor rather than from the physical location of the sensor itself, the data can be slightly inaccurate. Such a discrepancy can easily amplify and cause the avatar to “drift” from the player’s actual location, leading to problems with avatars’ locations not matching the player’s location in the physical space.
Because of the limitation in inertial systems, most LBE experiences utilize optical motion capture systems, and make use of software mechanisms that infer player positions when markers are occluded from cameras. 

Equipment possibilities
Unreal Engine works with motion capture tracking integration from many vendors, including:
Vicon
Mo-sys
Art
OptiTrack
Manus VR
As with any mocap system, calibration for players will be required before each LBE session. Each system has its own calibration method.
For more detailed information on motion capture systems and how to select the right one for your needs, see our white paper Choosing a real-time performance capture system.
Room considerations
A smaller room can make use of a relatively inexpensive solution such as the VIVE Lighthouse system, which can handle motion capture in a space up to 900 square feet in size. Combining the VIVE Headset with five VIVE trackers yields a decent setup for a 6DoF (six degrees of freedom) full body tracking setup.
For spaces over 2000 square feet in size, one solution is the OptiTrack optical motion capture system, which boasts high data transfer speeds to accommodate a large number of players. Vicon and ART systems are also viable options for a large space.
Roll-through time
If you’d like to minimize downtime between groups, you might need to go with a smaller number of motion sensors on users for faster changeover. One example of a fast-turnaround system consists of OptiTrack Active Pucks (one for each player) coupled with the latest version of OptiTrack Motive software and the OptiTrack plugin for Unreal Engine, which provides fast 6DoF tracking and initial solving with 240 fps of latency.

Device latency
When choosing a mocap system, one must also consider the mocap system’s latency, the delay between the time the user makes a motion and the time when the motion registers with the system. 
It’s important to distinguish between latency and frame rate:
Latency is a measure of the time it takes for motion data to go from the player’s body to the system, which in turn determines how fast the view in each headset is updated. The speed of data transfer is largely dependent on the capabilities of your chosen mocap system, but can also be affected by the speed of your network and your settings in Unreal Engine. Latency is expressed in milliseconds (ms), the lower the better.
The frame rate is how fast each frame of the visuals is refreshed (displayed) in the player’s VR headset. The frame rate is largely dependent on the headset’s capabilities, but can be affected by scene complexity (speed of rendering in Unreal Engine). Frame rate is expressed as frames per second (FPS), the higher the better.
Let’s look at a simple example of a player turning his head while in the LBE experience. The tracker on the player’s head transmits a stream of data about where the player’s head is positioned in space and the direction in which he is looking at each consecutive moment. If latency is low, each piece of data will reflect the player’s head position no more than a few milliseconds before. Then Unreal Engine renders the environment from those consecutive viewpoints, and a high frame rate displays the consecutive renderings fast enough (without stuttering) to make it seem real to the player.
High latency will lead to player discomfort, as what the players expect to see changing in their VR views won’t match what their bodies are doing.
In general, an LBE experience requires a latency of no more than 8ms. When choosing trackers and sensors for your setup, check the manufacturer’s specifications to ensure the equipment has an advertised latency within this range.
Note that it is possible that even with low latency, you can still have stuttery or otherwise poor visuals in players’ VR headsets due to other issues. Low latency isn’t a guarantee of a high FPS refresh rate—it just guarantees that once the data is displayed in headsets, that data will be up to date.
Feedback systems
Feedback systems provide visual or sensory feedback to augment the visuals in VR goggles. While these systems can add a lot of realism to the LBE experience, they also add setup time and cost.
Haptic feedback
Haptics provide a connection between the virtual and real worlds, delivering physical sensations to enhance the experience beyond what the player sees. Such sensations can add greatly to the player’s sense of immersion in the LBE experience.
Examples of the haptic devices and the sensations they provide:
Gloves that give a sense of pressure on the hand when a player picks up a virtual object
A vest that vibrates in specific spots when the player is struck by a virtual weapon
A fan that turns on when a player moves through a virtual portal to an outdoor environment, to simulate wind blowing on the player’s skin

Figure 4: Weapons, sword and shield haptic devices that track motion and senses vibration in the hand.
[Images from Haply.co. Permission form sent via email.]
A haptic device worn on the body delivers sensation to the player via either a simple vibration, or through force in the form of directed pressure. External devices use forces (fans) or heat (lamps) to simulate environmental conditions like wind and sun.
Haptic devices require significant setup to work properly. In addition, devices worn on the body will be subject to significant wear and tear as players put them on and remove them for each session. To stay within your budget, you will need to balance the cost and robustness of such devices with the level of immersion they provide for your story.
Motion sensors
If the players are to use their hands to pick up virtual objects, the system will need a method for representing the gripping or holding motion visually within the virtual experience, both for the player handling the object and the other players observing him.
When using mocap tracker data for hands, one solution for better visuals is to use more precise hardware that provides haptic signals and hand tracking with inertial sensors, which can help reduce occlusion issues.  
Also, the data can be optimized in Unreal Engine using the hand’s location (as gleaned from tracker data) to occasionally trigger pre-rendered hand and finger animation sequences. For example, when a player’s hand comes close to a virtual object (especially one that the story or game requires him to pick up), the player is probably, in real life, curling his fingers to grab the object. However, the crude sensor arrangement doesn’t pick up this finer motion. Instead, when the hand comes close to the object, the system responds by playing a pre-rendered animation of the avatar’s fingers curling around the object in every player’s VR headset, including the person doing the grabbing.
With this technology under constant development, more accurate hand trackers are very likely coming soon to the market. However, such systems might not be practical for your LBE project, because of both the cost and the increased processing required. 
Part II: Technical setup
Since Part I was about planning elements for creating a LBE experience, it is now time to focus on the technical aspects of creating a virtual world and linking external components together. In the spirit of creating a multiplayer LBE experience with VR headsets, external motion tracking, and haptics, Part II will go through the process of setting up the network and building the VR game system in Unreal Engine.
Network
Creating a network-shared LBE experience allows people to blend into one space. While many possible configurations are possible, here we put forth a recommendation for an LBE experience using an external mocap solution with optical cameras, a server, a dedicated mocap machine, HMD headsets, and backpacks.
Basic network setup 
A basic LBE network setup consists of the following:
One client per player, one server, one dedicated mocap machine
Windows OS (most backpack systems run on this OS)
Backpack LBE system (usually included with backpacks), including a display emulator to keep backpacks active
Server, more powerful than backpacks
Remote desktop solution for each backpack client
One POE (power-over-ethernet) switch for optical cameras
Professional high-speed Wi-Fi router dedicated to the LBE and removed from other networks

            Figure 7
To determine the specifics for a network setup, we start with our requirements for output and work backwards from there.
Output rate requirements
The human eye processes an image every 13-20 milliseconds. For HMD headsets, the recommended rate for what we present to the user in a VR headset is 90 fps. 
90 frames / 1 second = 90 frames / 1000 ms
We can flip this over to calculate:
1000 ms / 90 frames = 11.11 ms / frame
This tells us that a frame rate of 90 fps translates to the production of a new image (frame) every 11.11 milliseconds, which is below the 13-20 ms range for the human eye. Ideally, your system will reach 90 fps as a minimum rate, not as the average.
Live and predictive data
To achieve such a frame rate, a real-time motion capture system utilizes two sets of data:
Live data is fed to the network from mocap sensors on the users’ bodies.
Predictive data is calculated by the system. It “fills in the blanks” to replicate a user's live data to show his avatar’s animation to another user. 
Live data has to make a journey to the server where it can then be analyzed, with latency measured in milliseconds. Predictive data, on the other hand, is calculated in Unreal Engine — the latency for predictive data is typically a fraction of a millisecond. Using a combination of live and predictive data smooths out the avatar’s motion and generally provides a better visual experience for the user. This mixing of data is called in this context replication (see Replication section).
In an LBE setup, each visible user client requires an update time from the central server of at least 10 ms of real data and another 20 ms of predictive data, interspersed to provide the best visual quality and giving the final output a minimum of 90 fps. 
Network latency
The next problem is that network latency must be limited—the Wi-Fi must provide the lowest possible time for the data’s round-trip journey. A typical time for this trip is about 10 ms, but of course it is desirable to get this time even lower. Make sure to ping Wi-Fi IPs to check round-trip time and check that there is not too much packet loss. 
To keep network latency low, it is necessary to define a closed network with IP statics, called a dedicated server.

Figure 11: XXXX
A good setup would be to have a dedicated server connected by LAN to the mocap computer and the router, and a closed Wi-Fi connection to the backpack computers. Also, take care to remove firewalls, virtual networks, or any other networks not related to the LBE setup. 
Networking issues often come from the priority order from all the different tracking solutions.You can change network priority by customizing the Interface metric value in Advanced TCP/IP Settings. 

Figure 12: Changing priority with Interface metric setting
By typing “route print” in the command prompt of any machine on the LBE network, you can get the metric information for the IP network. The lower the metric value, the higher the priority.

Figure 13: Route print command
Latency reduction
Reducing latency, among other factors, is an important aspect of minimizing the chance of motion sickness in participants.
To improve the LBE experience, you will always need to be aware of the effects of latency, both from the network and your mocap gear. For example, an optical sensor system such as OptiTrack has a latency of 4 ms , which is great for playing a multiplayer LBE in a shared environment.
With the fast refresh rate of an LBE system, you need to make sure you use your capture data with the concept of “late update”. This process sends the player’s position data to the headset at the latest possible moment, which ensures that any HMD transform will be applied to the camera as close as possible to the time the player sees the finished frame. 
You’ll need to define the availability of “late update” with the hardware you use. It is available as a feature in Unreal's native XR plugins and also in the OptiTrack plugin.
If your LBE experience is going to utilize virtual portals, you will most likely need to set up render targets in Unreal Engine, which are basically textures you can write to at runtime. You can, for example, take the depth map of the scene as viewed from the user’s perspective at a specific frame, and before the frame is sent back to the user’s headset, use information from that texture in a Blueprint script to change what the user sees. Using ticking, each frame is updated with this custom information at the tail end of the rendering process for that frame. 
This process adds to each frame’s rendering time, which can introduce more latency. To minimize this latency, you can give part of the computation to the CPU and the other to the GPU, effectively distributing the work over parallel threads. Limit the number of Render Targets in the game is something you might consider to optimise your LBE experience. 

Setup in Unreal Engine
To help keep your setup tasks to a minimum, you should start your project with a template that includes all the network and replication settings already in place. You can also study tutorials that show how to do a multiplayer project, like this Blueprint Multiplayer series. 
You will, of course, need to import assets (3D models) from a DCC package such as Maya or 3ds Max. The import process is the same as for any game, and is covered in great detail in the Importing Content section of the Unreal Engine documentation.
You will then need to integrate specific LBE practices such as those described in this section.
Replication
To connect multiple wireless clients to tracking data in a closed LAN, it is more advantageous for each client to individually establish the connection between the game server and the capture system machine rather than retrieve the data directly through the game server. This is essential for fast transfer of tracking data over a wireless network. 




Figure 14: Setup for UE and 3rd Party Tracking System for two-player LBE system
Figure 14 shows how the system components work together:
LBE Server - The machine that controls the server operations. Including Game Mode, starting cinematics in sequencer to all players to be sync.
Motion tracking is the tracking data in real time by ex: Optitrack. It needs to be sent directly to each client.
LBE Clients are receiving Motion tracking data and LBE server Information and send that back to the game state and player state.
Game State shares data between server and client.

Note that UE uses a standard server-client architecture, where the information needs to be sent from client to server. To make this happen with Unreal Engine, we need to make use of some of the principles of replication. 
To prevent a feeling of motion sickness for each local VR client (and to give all users a smoother experience in general), the motion capture and VR helmet information for a particular user needs to be sent to that user’s client first. After that, the system can tweak the data and movement information and send it back to the server, and then send it on to other clients.
This data flow is part of replication. Each user gets their own data as quickly as possible to reduce the likelihood of motion sickness, and a client doesn’t see the HMD and mocap tracking info from others clients directly, which leads to smoother representations of other players in the experience.
Replication in an Unreal Engine-based LBE system is accomplished through Blueprints or C++. 
To learn how replication works within UE, let’s take a look at the hierarchy of the most important Blueprint classes used for a multiplayer LBE game in UE.
Classes
Creating an LBE experience means you’re essentially creating a game. These basic UE classes are part of the gameplay framework for setting up multiplayer game logic, including the rules of the game, the player’s view and controls, and the avatar’s animations and interaction. 
Game Mode
The Game Mode class defines the general flow and rules of your VR game. This is also where you generate the players and spawn the pawns.
Game and Player State
The Game State and Player State class holds the player states on the server, and are important classes for sharing data from clients to server.  More generally, in LBE, it is used for keeping a list of connected backpack VR players and variable values that pertain to players such as mocap configurations,hardware ID, and game statistics. If any data needs to be passed from one client to another, it will need to go through this class on the server. 

Figure 15: XXXX
Player Controller
Player Controller is an important class for any multiplayer game including VR LBE. A server needs each client to control its respective Pawn class. The Player Controller class accomplishes this by making a direct connection between the client and the server for playing the game with the specific controls. 
In an LBE setup in UE, the client must directly receive external tracker transforms from the tracking system to minimize latency. This means the tracker client origin must first exist on the client, and then it is sent to the Player Controller and then to the server. This means by steps:
Send an event from the server at the beginning of the game to spawn tracker client origin actors on each client build, along with respective UDP Messaging IP info. 
Updated data is sent to the Player Controller each time the player changes position, then the Player Controller sends tracking control information back to the server. 
Pawn
The player controller controls the Pawn class (this control is called “possessing the pawn”). The Pawn class is mostly replicated to all clients by default if you don’t change the Default Game Mode. But to make a LBE game, you need to customize your VR LBE Pawns. After receiving the client tracking data from the Player Controller, the Pawn can then create tracking information and update HMD transforms or to create controllers Inputs. 
Character
Then, you can create a character class to get all the tracking data from the pawn to create new transforms for animating the bones of the Skeletal Mesh.  
Tips: At the end, you replicate moves of the Skeletal Mesh to other clients. 

Figure 16
Tips: Note also that you can auto posses any pawn in a level going on the detail panel in the Editor, choosing Auto Posses Player and set the player id.

Figure 17: [CAPTION]
Multicast function
Multicast is a type of replication function available in UE. This function sends a Multicast event from the server to all clients. For example, If you want to play a cinematic sequence from the server to all clients, you need a Multicast event. 
To do so, create a Custom Event to play on the server and set the Replicates option to Multicast. Note that you can’t run a multicast event from a client.






Tip: Turn on the Reliable option under Graph to cause your replication to be sent as fast as possible, such as cinematics to be synced to all clients. 
You can learn more about the Multicast function in the Unreal Engine help topic Replicating Functions in Blueprints.

Prioritization
In Unreal Engine, and mostly in LBE as latency means everything, you will need to prioritize client replication. The Net Priority setting gives priority on the bandwidth; the higher this number, the more bandwidth that the client variable receives. A Net Priority value of 2.0 will cause updates twice as frequently as a Net Priority value of 1.0. This setting is useful when you need to minimize data latency to reduce the possibility of motion sickness.
Information coming from the server to the client from player tracking should generally have a Net Priority of 1.0, while client-to-client transfer of animation can have a Net Priority of 2.0 or more.

Figure 18

 
 
Motion capture setup
To start off your motion capture setup, you will need to work out the best way to place the markers and sensors on players. Normally, a mocap LBE setup means to have the minimum DOFs markers in your performer. In this paper, we are reviewing the 6 DOF setup with Optitrack.
You will also need to calibrate the mocap system. Each system performs this task differently, so you will need to consult the manufacturer’s documentation.
You should also consider the frequency and speed of calibration.  
Retargeting 

Retargeting is the process of taking animation from one character and applying it to another. If you are displaying avatars in the game, you will need to retarget motion captured from each tracked actor to its avatar.
Retargeting becomes tricky when the player and the avatar do not match closely in height and weight. One way to solve this problem is to have multiple avatars parts available (ex: head, legs, arms, chest), each with a different height and weight, and match them up to players just before the LBE experience begins. Another approach is to retarget the player’s movements to a one-size-fits-all avatar using an automated fudge factor based on the player’s height/weight. While the latter may be simpler to set up, it can lead to some unusual-looking avatar motion.
If the avatars do not follow human skeletal structure (for example, a woodland creature with an extra bone in its leg) then the retargeting process is complicated even further.
Whatever approach you use, you will need to test your retargeting solution on people of different shapes and sizes before considering it ready for play.

Retargeting - Optitrack exemple

Here is an example of MOCAP integration for LBE, using Optitrack Motive. You can use passive or active rigid bodies to establish skeleton tracking. Rigid bodies are attached to the head, torso, both hands, and both feet. This means a 6 DOFs, or 6 rigid bodies setup. 
Then, you can create a retargeting skeleton using the Builder pane when selecting all markers of your selected DOF. A good way to do it would be to put all DOFs on the ground and place them in a way to get all the markers without moves and loose. 

The naming convention of the rigid bodies is very important as it needs to start with the name of your character, followed by the part it represents. The two are combined to form the rigid body name. The tool creator in Optitrack Motive will then use the character name to find all parts of the body to make the skeleton retargeting.
Once the body parts have been created, the next step is to position the pivot point at the appropriate location of the body. Chest and head need to be placed at the brain and hip center.
As a general advice for all the mocap tools, It is really important that the head DOF matches the real pivot and position of the real performer head. As you will use the DOF data transform from Motive Instead of the HDM data transform. Without an accurate pivot and position, you can perform incoherent movements with the head.
After positioning the pivot point, you adjust the orientation of all the DOFs, as the +z axis must direct towards the front of the actor.


OpenVR Driver
 
The OptiTrack VR driver mixes the data transform of the head-mounted display (HMD) and the head DOFs from Motive into SteamVR. It basically changes the configuring streaming settings for you. Using this, the tracking data from Motive can be used to override the tracking of the VR system in any applications that are compatible with SteamVR.

Retargeting - Unreal Engine

In laying out the scene for MOCAP and retargeting, the first step is to set the mocap volume in the UE scene. For that, we attach the live elements under a Root Actor that will receive the transformation data from the mocap origin coming from the tracking software. It is really important to set the root of everything using the mocap data to ZERO in UE. 
A good practice is to set markers in real space. A real rule can be positioned on the real field in a visible location for the operator. During operation of the game, the operator will be able to tell when the two rules are no longer aligned, and can perform an automatic correction to return to the same place of alignment between the world of Unreal Engine and the real world of the user.
This parent Root Actor (often called also the stage origin) and its children are best set up on a sublevel dedicated to the live corrections on stage. 
e
Figure 20: Setting up the volume as a Root Actor
Next, you will need to set up a pawn. Right-click in Content Browser, and from the context menu, select Blueprint → Blueprint Class → Pawn.
Then you will need to create a Camera Component. If you want to play with Head offsets between the view and the mesh, you can put the camera under a root scene component.

 
Figure 21

The “Lock to HMD” property needs to be set to true under the camera component properties in the details pane. Then select the pawn and set the “Base Eye Height” to zero.


Let’s now add a skeletal mesh component to the pawn, and create a new animation blueprint. The skeletal mesh will also need to be positioned to Zero  


Figure 23
Depending on the MOCAP solution, you will set your anim graph with Livelink Pose or the Mocap solution pose. See Livelink Plugin in Unreal for more details.
In the case of Optitrack, they use a custom animinstance class called OptiTrackAnimInstance. If you create a new anim blueprint parented to that class, you then get access to the Optitrack Skeleton Node.

Ether with LiveLink or Optitrack Skeleton, you will need after to remap the bones in the skeleton to the MOCAP skeleton names. This can be done in Livelink via the Livelink remap asset.

Or with Optitrack directly in the Optitrack Skeleton node.

NB: This is a remapping solution. For better retargeting results, you should refer to the Control Rig section in Unreal. 
Haptics setup
Working on a haptics system will certainly add a layer of presence and realism to your LBE experience. While most haptic technology uses vibration to create the sensation of feedback, other haptics systems use interaction with real life mechanisms to simulate ambiance. As there are different ways to virtually mimic these interactions, Unreal Engine enables many solutions for communicating with haptics systems. 
One example of a haptics system comes from the company Haptic using sword and shield props with their custom Arduino-like protocol that creates vibrations sensations. With a UDP protocol, Haptic created a JSON-based communication protocol in UE to communicate between haptic devices and the game. This allowed them to have electronic devices and controlled props telling the game when the players wanted to shoot, or when to activate certain sequences or VFX.
A popular haptics solution is a mechanism driven by an electronic device such as an Arduino-based system. Here, for the purpose of explaining the process of setting up haptics, we will assume the use of Arduino devices, but other solutions are also available. In this example, we open and close an Arduino relay shield for a 110V plug, essentially turning on or off a physical device such as a fan. This example can be directly integrated into Unreal Engine. 
To connect the Arduino device, use the UE Arduino plugin to communicate with the Arduino protocol via USB connection. Source code and binaries for Arduino 4.23 are available on GitHub. 
Before integration with UE, you will need to create the Java code. In this example we created an Java code, like this example, to open an AC light using a Relay:

Int Light = 13

char character

void setup() {
  Serial.begin(9600);
  pinMode(Light, OUTPUT);
  digitalWrite(Light, LOW);
}

void ActiveLight(){
  character == serial.read();
  if (character == 1){
    digitalWrite(Light, HIGH);
    
  } else if (character == 0){
    digitalWrite(Light, LOW);
  }
}

in the Arduino IDE software that you can download here:
https://www.arduino.cc/en/Main/Software

Use the node Open Serial Port function, select the appropriate USB port, and store the result in a variable. Afterwards, you can set/read your variable with the specific event you want. On this specific setup, we used a custom event to execute on the server. If you need to send it to all clients, please check the Replication section for further information.

Then we pass it as a custom event in the game mode executed on the server to set a Boolean variable in the sequencer using multicast custom events. You will then be able to get the variable in the level blueprint where the Arduino is set.



Figure 10: XXXX

Sensor interaction
If you need haptic sensor interaction, you will need to use a UDP/TCP protocol to create a JSON-based communication protocol or a CSV DataTable to communicate between haptic devices and the game. Then you can have props controlled by Arduino boards telling the game when the players want to shoot, or when to activate a certain multisensor experience like a fan blowing air.
To read / write a Json or CSV string from a file or network or the engine can be done at runtime, and can be done in different ways. Mostly you will need to work with a keys and values pair of parameters.
CSV DataTable
Json or CSV data needs a matching structure.(The field name must not be "Name" or a system reserved name). The values in the structure can be all data types supported by UE4.

You first create a CSV file. 

And then, in Unreal, you create a structure blueprint related to the CSV properties.


Then you import your CSV file in Unreal as DataTable and choose the created structure. 

Then, creating a new actor blueprint, you use the Get Data Table Row blueprint node to set your variables.

Figure 10: Settings for DataTable in UE

JSON API
If you want to use JSON with Blueprint, there are many JSON plugins that are available on the marketplace. However, you will maybe need to create a custom C++ JSON parser. As Json is easily workable by C++, you can create your own plugin fast. 

Mainly, you will need to add JSON modules to your ProjectName.Build.cs. "Json" and "JsonUtilities". 


Figure xxxxxx
After, you define pointers to “FJsonObject” and “FJsonValue”. 

Figure xxxxxx
Including the headers "JsonUtilities/Public/JsonUtilities.h" and "Serialization/JsonReader.h", you can define a reader and a writer in your class .cpp.
A demo example of a C++ JSon plugin is available here: https://github.com/Hurtubise-Epic/Json_Plugin.git. 

REST API
Controlling remotely over http is also something you may need when talking about LBE experience. With REST API, you can send commands to the Unreal Engine and Editor remotely over HTTP.

This makes it possible to create your own customized web UIs that trigger changes in your Project’s content. You can control Unreal from any browser or custom app that supports modern web standards, and you can integrate your controls into other custom panels that you use to control other applications in your environment.

Using node.js and vue.js, you can create a remote control that you host on a server with npm. 

With console commands in Unreal, we can start a server that will be automatically hosted on port. Here are the commands:
 WebControl.StartServer
 WebControl.StartServer
 WebControl.EnableExperimentalRoutes
 WebControl.EnableServerOnStartup

IP endpoints
In Unreal Engine, the UDP messaging plugin is enabled by default. But if you are working with dedicated servers and a closed LAN, you will need to consider setting up the IP endpoints for your network.
The UDP Messaging plugin configuration can be accessed in Project Settings. Note that this plugin can be really useful to set up endpoint IPs for any kind of network connection (especially Message Bus connections). To do so, here are the steps:
1- In UE, go to Project settings, and find UDP Messaging in the Plugins section.
2- Look for the setting Unicast Endpoint. Change the IP 0.0.0.0:0 for the IP of the Server machine. Adding : 0 at the end of the IP. ex: 192.168.7.123:0

Figure 19
Another way to set up UDP is to create server/client configurations in an .ini file, and store them in the UE project’s /Config folder using the following settings:
[/Script/UE4LBE.LBEGameInstance]
DefaultServerIP=192.168.120.01
bAutoConnect=true
AutoConnectType=client
bUseHMD=true
StartingLevel=0
OptiTrackHMDID 02
TrackerServerID=192.168.124.20
MeshScale 1.05
To learn more about customizing the .ini file, please refer to the Performance section of this paper.
Player UI 
If you want to send UI or textures that are not affected by post-processes and are part of a separate render pass for each HMD eye, you will need to add a Stereo Layer Component to your Pawn. This will create a shape with a texture that is rendered separately for each eye. 



Performance
Here are some tips to improve your content’s rendering performance, with the goal of achieving the best possible frame rate. You’ll find additional tips in Unreal Engine’s Virtual Reality Best Practices and Virtual Reality Development documentation.Forums are also a rich source of tips; check out the Unreal Engine VR and AR development subforum and the Oculus Community Forums. 
Here are a few specific tips for increasing your system’s performance:
To effectively run VR from a backpack with batteries and Wi-Fi, you will need to disable heavy post-processors. Certain post-processing effects like bloom, ambient occlusion, and Unreal Engine Distance Field Shadows are very costly rendering-wise.
Shaders with transparency add rendering time, so transparency should be used sparingly in your content. 
To improve transparency, anti-aliasing, and render speed, activate Forward Rendering. See the VR Performance Features help topic for more information on how forward rendering relates to VR performance.
To minimize the performance impact of VR, enable the Instanced Stereo option in the project’s VR settings.
To optimize thread syncing between the CPU (RHI commands such as “render to texture”) and GPU (commands such as “frame to capture”), use Execute Console Command to enable r.OneFrameThreadLag for RHI by setting this property to 1. Then you can play around with the r. and rhi. commands to tweak your sync and reach your acceptable frame rate. For more information, see Low Latency Frame Syncing in the Unreal Engine documentation.
You might need to revisit your previous traditional constraints and look at your scene complexity regarding particles, dynamic shadows, atmospheric smoke effects, poly counts, and LODs. Note that for VR, the poly count should be limited to around 15K per model when viewed close up. For more information, see the Virtual Reality Best Practices help topic.
It’s important to minimize overdraw to keep performance at a maximum. To minimize draw calls, create master materials and material instances. In general, creating instances is an effective approach for minimizing overdraw calls.
Customizing VR performance settings
Most VR projects will need to implement their own Global VR settings. You can find some reference settings in the VR Demo Showdown, in the defaultengine.ini file in the project’s configs folder (see below for settings). These settings can also be set individually as command-line commands with the Execute Console Command feature.

The Unreal Engine VR template also contains some great settings for pawns and controllers. 

If you need to change settings on a player-by-player basis, you can set them as individual command-line commands. The performance is then defined relative to the player and the HMD.

Settings in VR Demo Showdown:

vr.PixelDensity=1
r.SeparateTranslucency=0
r.HZBOcclusion=0
r.MotionBlurQuality=0
r.PostProcessAAQuality=3
r.BloomQuality=1
r.EyeAdaptationQuality=0
r.AmbientOcclusionLevels=0
r.SSR.Quality=1
r.DepthOfFieldQuality=0
r.SceneColorFormat=2
r.TranslucencyVolumeBlur=0
r.TranslucencyLightingVolumeDim=4
r.MaxAnisotropy=8
r.LensFlareQuality=0
r.SceneColorFringeQuality=0
r.FastBlurThreshold=0
r.SSR.MaxRoughness=0.1
r.rhicmdbypass=0
sg.EffectsQuality=2
sg.PostProcessQuality=0
r.setres  1920x1080
r.streaming.poolsize 3000
r.ScreenPercentage  120
sg.AntiAliasingQuality 3
sg.ShadowQuality 3
r.Streaming.MipBias 0



Figure 15

The future of LBE, VR, and Unreal Engine
The future of virtual reality and location-based entertainment looks bright. We see the technology being used more and more in theme park rides, VR arcade experiences, art installations, and many other creative, educational, and entertaining experiences.
By nature, the success of LBE requires players to be completely immersed, and that requires compelling graphics and stories processed in real time. And beyond networking and graphics technology, some productions use real sets, props, and one or more LED screens or projectors to simulate the 3D environment. For example, the Millennium Falcon: Smuggler’s Run experience at Disney’s Hollywood Studios perfectly reproduces the virtual experience of flying aboard the famous Star Wars ship by using Unreal Engine nDisplay technology to enable multi-projection on five big screens. 
The main strength of Unreal Engine for LBE and VR is that it provides a robust basis for the development of these experiences, right out of the box. Unreal Engine keeps a stable frame rate beyond 90 frames per second with modern and advanced rendering quality at the level of a AAA game. And the engine is open source, able to handle the demands of the SDKs of most XR and motion tracker solutions. In addition to being free and used by more than 7.5 million developers, Unreal Engine includes a large set of tools for development, prototyping, and optimization of LBE and VR experiences. 
UE is continuing to strive for faster, better graphics and support for motion capture and other technology around LBE. For this reason, we developed some great new tools for 4.25 such as Networking Insights to optimize, analyze, and debug network traffic.

This tool also integrates an animation insight to visualize during gameplay.
Speaking of animation, there is major improvement to the Control Rig tool in UE v4.25. It has been optimized to be up to 20% faster and use up to 75% less memory, and now supports bone, space, and control to create VR IK human rigs.
Some improvements have also been made to the API such as UProperty, which has been refactored to be FProperty. This helps the performance of “garbage collection” and improves memory usage.
Also, Epic’s nDisplay technology is useful for LBE productions that require multi-display screens. In Unreal Engine 4.25, nDisplay now supports frame synchronization and rendering to curved surfaces. 

As for control of lights in the real world, Unreal Engine supports the DMX standard through a plugin released in Unreal Engine 4.25. Or you can use the OSC plugin or middleware solutions for controlling lights in real time that are compatible with the engine. 
All these great Unreal Engine features will continue to be updated in the future to support the latest platforms SDKs. 
In its essence, LBE is making people think it’s real, whatever the technology used. And we will see more next-generation LBE coming from Unreal Engine and from pioneers inventing new solutions, getting ever closer to the ultimate LBE experience. 
About this document

Authors
David Hurtubise
Steve Smith
Nick Whiting

Collaborators
Anthony Tominia

Editor
Michele Bousquet

