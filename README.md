# ThrowaBall [<img src="https://github.com/JustSleightly/Resources/raw/main/Icons/JSLogo.png" width="30" height="30" alt="JustSleightly">](https://vrc.sleightly.dev/ "JustSleightly") [<img src="https://github.com/JustSleightly/Resources/raw/main/Icons/Discord.png" width="30" height="30" alt="Discord">](https://discord.sleightly.dev/ "Discord") [<img src="https://github.com/JustSleightly/Resources/raw/main/Icons/GitHub.png" width="30" height="30" alt="GitHub">](https://github.sleightly.dev/ "Github") [<img src="https://github.com/JustSleightly/Resources/raw/main/Icons/Store.png" width="30" height="30" alt="Store">](https://store.sleightly.dev/ "Store")

[![GitHub stars](https://img.shields.io/github/stars/JustSleightly/ThrowaBall)](https://github.com/JustSleightly/ThrowaBall/stargazers) [![GitHub Tags](https://img.shields.io/github/tag/JustSleightly/ThrowaBall)](https://github.com/JustSleightly/ThrowaBall/tags) [![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/JustSleightly/ThrowaBall?include_prereleases)](https://github.com/JustSleightly/ThrowaBall/releases) [![GitHub issues](https://img.shields.io/github/issues/JustSleightly/ThrowaBall)](https://github.com/JustSleightly/ThrowaBall/issues) [![GitHub last commit](https://img.shields.io/github/last-commit/JustSleightly/ThrowaBall)](https://github.com/JustSleightly/ThrowaBall/commits/main) [![Discord](https://img.shields.io/discord/780192344800362506)](https://discord.sleightly.dev/)

![TB Gumroad Showcase gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Gumroad%20Showcase.gif)

**ThrowaBall** is a physics-based throwable object system built for **VRChat** users. It streamlines the deceptively difficult task of naturally grabbing and tossing an object with a modular automatic setup tool, allowing for 2 step installation without any VRChat 3.0 or advanced Unity experience whatsoever.

This is a **system** and only includes three default ball prefabs. Please import your own for more variety.

## Available now at [store.sleightly.dev](https://store.sleightly.dev/)

<img src="https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Default%20Settings.png" height="280" alt="TB Default Settings">

### Features

- **Syncs ball position** with other players
- **Drag and drop setup** - works with **any** object, not just balls
- Supports up to **8 balls per system installation**
- Supports **multiple system installations** to use multiple balls at once
- Choose between two different throw force mechanics to suit your needs/preferences
- Options to respawn the ball using a **gesture, menu, or a physical button**
- Controls the throw force using a **radial puppet**
- Allows ball to be **grabbed (and thrown\*) by other players**
- Customizable **drag/bounce** physics
- Extensive modular options and animator API resources for creators to develop compatible prefabs
- **Automatic Write Defaults detection** and compatibility with both on/off

\* *Throws by other players come with their own caveats due to VRChat limitations (See Disclaimer Below)*

| Specifications | Default | Range |
| :--- | :--- | :--- |
| `Memory` | 38 | 2 - 47 |
| `Icons` | 5 | 3 - 14 |
| `FX Layers` | 6 | 3 - 7 |
| `Animation Clips` | 30 | 13 - 40 |

## Showcase / Performance Reel

[<img src="https://img.youtube.com/vi/TODO/0.jpg" width="410" alt="ThrowaBall Showcase">](https://www.youtube.com/watch?v=TODO "ThrowaBall Showcase")

<details>

  <summary> <strong> Full Demo GIF </strong> </summary>
​
<blockquote>

![TB Script Showcase gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Script%20Showcase.gif)

</details>

---

# Requirements

1. Basic Unity experience + VRChat SDK3 uploading experience.
2. A **validated** license key for first time activation.
    1. License keys can be purchased from my [store](https://store.sleightly.dev/).
    2. Keys must be validated by joining my [discord](https://discord.sleightly.dev/) and opening a ticket with my automated discord bot.
3. An active **internet connection** while in Unity in order to use the tool - cannot be used offline.
4. Only compatible with Unity for **Windows** - not compatible with Unity for Mac/Linux at this time.
5. Pre-requisite import - [VRChat Creator Companion SDK](https://vrchat.com/home/download) version `3.2.0` or newer.

---

# Disclaimer

ThrowaBall is a unique throwable system as it is designed to **both** sync its position to other players, **and** allow other players to throw the object.

However, due to limitations with VRChat regarding the way player IK interpolates and delays between player clients, it leads to a sub-par/delayed throwing experience for players other than the avatar wearer who attempt to throw ThrowaBall.

The **Include Remote Tracker** option in the ThrowaBall installer adds complexity to the hierarchy and animator in an attempt to partially mitigate the delay in player IK, but it is far from a robust solution.

The only way to allow for players other than the avatar wearer to throw ThrowaBall seamlessly is to disable/sacrifice syncing the position of the ball, resulting in other players seeing the ball in a different location than the wearer.

The `PhysJoint` force mode has the ability to toggle off **or** omit position syncing entirely, allowing the avatar wearer to trade position syncing to prioritize other players' experience interacting with ThrowaBall.

---

# Throw Force Mode

ThrowaBall supports two different throwing mechanics to choose from to suit your preferences/needs. They both throw with roughly the same range of force, but have slightly different feels to each other.

### `Force Particle`

ThrowaBall will use particle system collision to determine the force of the throw. The thrown object is still a rigidbody with physics collision, and not a particle mesh.

- **Feels more consistent/stable for the average user**
- **Properly scales linearly with VRChat Avatar Scaling**
- *Including Sync is mandatory (+27 memory) and can't be toggled*
- *Ball will not rotate for other players*

### `PhysJoint`

ThrowaBall will use a PhysBone and configurable joint to determine the force and direction of the throw.

- **Including Sync is optional if other users do not need to see where the ball lands (-27 memory)**
- **Sync can be toggled off in-game to allow other users to throw ThrowaBall without any visual delay as if they were the original wearer**
- **Ball will rotate to face the direction of its travel**
- *Throwing takes a little more practice to get used to*
- *Throw force scales with Avatar non-linearly and is especially an issue for other users at drastically different scale than the wearer who try to throw ThrowaBall*

---

# Installation

### Unity Installation Guide Video

[![ThrowaBall Unity Installation Guide](http://img.youtube.com/vi/TODO/0.jpg)](https://www.youtube.com/watch?v=TODO "ThrowaBall Unity Installation Guide")

### Importing The Prefab

<details>

  <summary> <strong> Add to Scene </strong> </summary>
​
<blockquote>

To add ThrowaBall to your scene, click on **JustSleightly** in the top toolbar, and click on the **ThrowaBall** menu option. You can also press **Alt + T** for *ThrowaBall*.

This will add the installer onto the first active loaded Avatar Descriptor in the scene.

<details>

  <summary> Technical Details </summary>
​
<blockquote>

If you have any GameObjects selected in the scene, clicking the Menu Item for ThrowaBall will search all selected objects and parents first for an Avatar Descriptor.

If there are no active Avatar Descriptors found in the scene, the installer will be added to the base scene.

</details>

</details>

<details>

  <summary> <strong>  Activate License </strong> </summary>
​
<blockquote>

If you have never used this on this PC before, you will see a field labeled **Enter your license key**. Make sure you've validated your license key on the [Discord](https://discord.sleightly.dev/) server, then input your license key from your purchase and click activate. This is a one-time-use key that will authorize the current PC for future use of ThrowaBall.

If your license key is not working due to it already being in use, click the *Transfer License* option.

</details>

### Main Settings

![TB Main Settings png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Main%20Settings.png)

<details>

  <summary> <strong> Target to Follow </strong> </summary>
​
<blockquote>

Select a humanoid body bone from the drop-down that ThrowaBall should follow.

Selecting `Custom` will allow for any gameobject on the avatar to be used as a **Custom Follow Target**.

</details>

<details>

  <summary> <strong> Force Mode </strong> </summary>
​
<blockquote>

Select the method ThrowaBall will use to calculate the ball's force between `Force Particle` and `PhysJoint`.

Details regarding both force modes can be found in the **Throw Force Mode** section above.

</details>

<details>

  <summary> <strong> Ball Inputs </strong> </summary>
​
<blockquote>

Select a **Ball Type/Object** for ThrowaBall to use from the drop-down, or select `Custom` to drag in any GameObject/Prefab from your hierarchy or your project assets.

Select a **Physics Preset** for each ball to follow, or select `Custom` to set a specific drag/bounce.

Use the +/- symbol to add/remove additional balls to the system, up to 8 balls. Rearrange them by click/dragging into your preferred order.

Adds +1 Expression Parameter memory per ball.

![TB Ball Add Rearrange gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Ball%20Add%20Rearrange.gif)

<details>

  <summary> Technical Details </summary>
​
<blockquote>

All GameObjects will have their root re-positioned to (0, 0, 0).

If the input GameObject is a prefab, the prefab will be unpacked.

Inputting the Avatar Root or ThrowaBall's own GameObject will automatically be removed.

Any RigidBody, Spring Joint, and Configurable Joint components within any GameObjects/Prefabs inputted will be removed.

Any Sphere, Box, Capsule, and Mesh Collider components within any GameObjects/Prefabs inputted that are not set as Triggers will be removed.

Leaving an input field blank will yield an error.

</details>

</details>

### Advanced Options

![TB Advanced Options png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Advanced%20Options.png)

<details>

  <summary> <strong> Write Defaults </strong> </summary>
​
<blockquote>

Enabling/Disabling this option will enable/disable Write Defaults in all generated animator states for ThrowaBall.

![TB Write Defaults png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Write%20Defaults.png)

If it says Write Defaults **(Auto)**, then this is handled automatically to match the current Write Defaults of your Animator Controller(s).

![TB Write Defaults Auto png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Write%20Defaults%20Auto.png)

<details>

  <summary> Technical Details </summary>
​
<blockquote>

If your FX Animator Controller is set to one Write Defaults mode, the **Write Defaults** option will automatically match and be labeled with **(Auto)**.

If your FX Animator Controller has a mix of Write Defaults On and Off, a warning will appear and the **Write Defaults** option will not be labeled with **(Auto)**. This option will be available to manually enable/disable, and the generated states will follow the manually set status.

States with BlendTrees that are also set to Write Defaults On and have `(WD On)` in the name are omitted from the scan.

</details>

</details>

<details>

  <summary> <strong> Include Collision Parameter </strong> </summary>
​
<blockquote>

Enable this feature to add an animator parameter called `TB/Collision` that will be driven whenever the thrown object collides with a surface for use with custom animations.

The collision detection is not foolproof or perfect, as it depends on world colliders and the detection rate of particle collision death. The parameter fires for a minimum of 10 frames at a time.

</details>

<details>

  <summary> <strong> Include Menu Respawn Button </strong> </summary>
​
<blockquote>

Enable this feature to add a menu control that respawns ThrowaBall.

Adds +1 Expression Parameter memory.

</details>

<details>

  <summary> <strong> Include Gesture to Respawn </strong> </summary>
​
<blockquote>

Enable this feature to respawn ThrowaBall upon a specific gesture or gesture combination.

</details>

<details>

  <summary> <strong> Include Physical Respawn Pedestal </strong> </summary>
​
<blockquote>

Enable this feature to add a Physical Pedestal that respawns ThrowaBall when a squishbone is pressed.

</details>

<details>

  <summary> <strong> Include Throw Force Radial Control </strong> </summary>
​
<blockquote>

Enable this feature to add a radial puppet to dynamically control ThrowaBall's throw force by a default multiplier range of 0.5x - 1.5x.

Adds +8 Expression Parameter memory.

The multiplier range and initial value can be adjusted in the **Debug Options**.

</details>

<details>

  <summary> <strong> Allow Remote Grabbing </strong> </summary>
​
<blockquote>

Enable this feature to allow other players to grab the ThrowaBall.

Be mindful of ball syncing and **Throw Force Mode** caveats.

</details>

<details>

  <summary> <strong> Include Ball Syncing </strong> </summary>
​
<blockquote>

Enable this feature to sync the position of ThrowaBall from you to other players.

Adds +27 Expression Parameter memory.

This option only appears if the **Throw Force Mode** is set to `PhysJoint`, as syncing is mandatory for `Force Particle`.

</details>

<details>

  <summary> <strong> Include Sync Toggle </strong> </summary>
​
<blockquote>

Enable this feature to include a menu control that disables Ball Syncing to allow for smoother throwing for remote throwers.

Adds +1 Expression Parameter memory.

This option only appears if **Allow Remote Grabbing** is enabled and **Include Ball Syncing** is enabled/required.

</details>

<details>

  <summary> <strong> Include Remote Tracker </strong> </summary>
​
<blockquote>

Enable this feature to add a contact tracker to partially counteract network IK lag from remote throwers.

See the **Disclaimer** above for more details.

This option only appears if **Allow Remote Grabbing** is enabled and **Include Ball Syncing** is enabled/required.

</details>

<details>

  <summary> <strong> World Drop When Enabled </strong> </summary>
​
<blockquote>

Disable this feature to not constrain ThrowaBall to the world when the system is enabled, such as for grabbing the ThrowaBall off another moving object like a belt.

This option only appears if **Include Physical Respawn Pedestal** is disabled.

</details>

<details>

  <summary> <strong> Select Respawn Gesture </strong> </summary>
​
<blockquote>

Select the gesture(s)/gesture combination that will respawn ThrowaBall.

This option only appears if **Include Gesture to Respawn** is enabled.

</details>

### Extra Settings

<details>

  <summary> <strong> Save File Path </strong> </summary>
​
<blockquote>

Select where to create the GeneratedTBResources folder which contains all of the generated files.

![TB Save File Path png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Save%20File%20Path.png)

<details>

  <summary> Technical Details </summary>
​
<blockquote>

By default, this path is `Assets/JustSleightly/ThrowaBall`.

Changes made to this path will attempt to be saved to your editor preferences for use in other projects as well.

</details>

</details>

<details>

  <summary> <strong> Debug Options </strong> </summary>
​
<blockquote>

Experimental options for manipulating ThrowaBall behaviour.

It is not recommended to adjust these values without extensive testing.

<details>

  <summary> <strong> Throw Multiplier Min </strong> </summary>
​
<blockquote>

Set the minimum multiplier value of the Force Multiplier Parameter when the parameter float value is 0.

</details>

<details>

  <summary> <strong> Throw Multiplier Max </strong> </summary>
​
<blockquote>

Set the maximum multiplier value of the Force Multiplier Parameter when the parameter float value is 1.

</details>

<details>

  <summary> <strong> Throw Default Multiplier </strong> </summary>
​
<blockquote>

Set the default value of the Force Multiplier Parameter.

The 0 - 1 float range corresponds to a linear min - max force multiplier.

</details>

<details>

  <summary> <strong> Throw Start Lifetime </strong> </summary>
​
<blockquote>

Set the Start Lifetime of the Force Particle System.

This option only appears if the **Throw Force Mode** is set to `Force Particle`.

</details>

<details>

  <summary> <strong> Throw Collider Force </strong> </summary>
​
<blockquote>

Set the Collider Force of the Force Particle System.

This option only appears if the **Throw Force Mode** is set to `Force Particle`.

</details>

<details>

  <summary> <strong> Throw Exit Time </strong> </summary>
​
<blockquote>

Set the exit time of the throw vector, which correlates to how long the force is applied to ThrowaBall before leaving it to inertia.

This option only appears if the **Throw Force Mode** is set to `PhysJoint`.

</details>

<details>

  <summary> <strong> Throw Force Curve </strong> </summary>
​
<blockquote>

Set the curve that controls the throw force relative to an avatar eye height of 1 meter.

The duration of this curve is inversely proportional to the Throw Exit Time.

This option only appears if the **Throw Force Mode** is set to `PhysJoint`.

</details>

<details>

  <summary> <strong> Select Sync Damping </strong> </summary>
​
<blockquote>

Set the strength of the damping interpolation between sync intervals.

This option only appears if **Include Ball Syncing** is enabled/required.

</details>

<details>

  <summary> <strong> Select IK Lag Buffer </strong> </summary>
​
<blockquote>

Set the buffer time to account for IK before releasing a remote throw.

This option only appears if **Include Remote Tracker** is enabled.

</details>

<details>

  <summary> <strong> Select Tracker Size </strong> </summary>
​
<blockquote>

Set the initial tracker size of the remote player contact tracker before attaching.

This option only appears if **Include Remote Tracker** is enabled.

</details>

</details>

<details>

  <summary> <strong> Begin Setup </strong> </summary>
​
<blockquote>

Clicking this button will begin the generation of the ThrowaBall system according to the configuration of the **Main Settings** window, and proceed to **Anchor Positioning**. This button will be greyed out if there are any red errors returned in the Inspector.

![TB Begin Setup png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Begin%20Setup.png)

</details>

<details>

  <summary> <strong> Add Additional System </strong> </summary>
​
<blockquote>

Clicking this button will generate an additional instance of the ThrowaBall system according to the configuration of the **Main Settings** window, and proceed to **Anchor Positioning**. This button will be greyed out if there are any red errors returned in the Inspector.

The system will be generated under the same existing ThrowaBall root, and animator parameters will be suffixed by the index of the installed instance.

This option is only available if an existing instance of ThrowaBall is already detected.

![TB Additional System png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Additional%20System.png)

</details>

<details>

  <summary> <strong> Utilities </strong> </summary>
​
<blockquote>

<details>

  <summary> <strong> Memory Calculations </strong> </summary>
​
<blockquote>

Displays the Required Memory to generate and the Available Memory on the current Avatar's Expression Parameters.

![TB Calculate Memory png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Calculate%20Memory.png)

<details>

  <summary> Necessary Memory can be calculated as: </summary>
  ​
<blockquote>

```math
\Sigma TotalRequiredMemory = CustomBallMemory + \begin{cases}1 + BallCount \\8 & IncludeForceSlider \\1 & IncludeMenuRespawn \\27 & IncludeBallSyncing\|\|UseForceParticle \\1 & IncludeSyncToggle\&AllowRemoteGrabbing\&!UseForceParticle \\1 & IncludeCollisionParameter\end{cases}
```

</details>

</details>

<details>

  <summary> <strong> Warnings/Errors </strong> </summary>
​
<blockquote>

<details>

  <summary> <strong> ERROR: No Avatar Descriptor Detected </strong> </summary>
​
<blockquote>

Triggers if no Avatar Descriptor component can be detected in any parents of the current GameObject.

</details>

<details>

  <summary> <strong> ERROR: No Animator Detected </strong> </summary>
​
<blockquote>

Triggers if no Animator component is found on the Avatar Descriptor GameObject.

</details>

<details>

  <summary> <strong> ERROR: An Error Has Occurred And Interrupted The Installation </strong> </summary>
​
<blockquote>

Triggers for various reason, likely due to going in/out of Play Mode, or sometimes Unity recompiling due to a change in project files via import/deletion.

</details>

<details>

  <summary> <strong> ERROR: Not Enough Memory </strong> </summary>
​
<blockquote>

Triggers if the Expressions Menu does not have enough available memory to satisfy the features configured in **Main Settings**.

</details>

<details>

  <summary> <strong> ERROR: Not Enough Menu Space </strong> </summary>
​
<blockquote>

Triggers if the Expressions Menu in the Avatar Descriptor already has 8 controls.

</details>

<details>

  <summary> <strong> ERROR: Animator Missing Avatar </strong> </summary>
​
<blockquote>

Triggers if the Animator component on your Avatar Root does not have an Avatar mapped.

![TB Error Animator No Avatar Example png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Error%20Animator%20No%20Avatar%20Example.png)

</details>

<details>

  <summary> <strong> ERROR: Model Not Humanoid </strong> </summary>
​
<blockquote>

Triggers if the model's FBX is not set to Humanoid rig configuration.

</details>

<details>

  <summary> <strong> ERROR: Chest Not Mapped </strong> </summary>
​
<blockquote>

Triggers if the model's humanoid rig configuration does not have the chest mapped.

</details>

<details>

  <summary> <strong> ERROR: Empty Custom Target </strong> </summary>
​
<blockquote>

Triggers if the custom target GameObject field is left blank.

</details>

<details>

  <summary> <strong> ERROR: Empty Ball Inputs </strong> </summary>
​
<blockquote>

Triggers if any custom Ball Object fields are left blank.

</details>

<details>

  <summary> <strong> WARNING: Avatar Not At Origin </strong> </summary>
​
<blockquote>

Triggers if the Avatar is currently not at origin (0,0,0 Position and Rotation). If continued, the ThrowaBall system may spazz out for remote players.

</details>

<details>

  <summary> <strong> WARNING: Mixed Write Defaults </strong> </summary>
​
<blockquote>

Triggers if both Write Defaults On and Off are detected in your FX Controller.

Continuing will use whichever value of **Write Defaults** you set under **Advanced Options**.

</details>

<details>

  <summary> <strong> WARNING: Default Controllers/Expressions Detected </strong> </summary>
​
<blockquote>

Triggers if the FX Controller, Expression Parameters, or Expressions Menu in your Avatar Descriptor is either default or empty.

</details>

<details>

  <summary> <strong> WARNING: Previous ThrowaBall Installation Detected </strong> </summary>
​
<blockquote>

Triggers if a remnants of a previous ThrowaBall installation were detected. Continuing will attempt to install another instance of ThrowaBall.

</details>

<details>

  <summary> <strong> ERROR: Double Layer Rig Bug Detected </strong> </summary>
​
<blockquote>

Triggers if your Avatar Descriptor has two FX Playable Layers. Pressing Fix will restore the Action Playable Layer for you, but you will need to re-populate any custom layers you had previously set here.

This is a [known VRCSDK bug](https://notes.sleightly.dev/My-VRC-Avatar-Descriptor-is-not-showing-the-Playable-Layers-properly-Double-FX-Bug-e6a68eca97644ec3896d3bda410cd97e) that occurs when switching the avatar in the root animator or switching the FBX of that avatar between Generic and Humanoid rigs when it already has an Avatar Descriptor in the scene.

![TB Double FX Layer Bug Example png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Double%20FX%20Layer%20Bug%20Example.png)

</details>

</details>

<details>

  <summary> <strong> Remove From Avatar </strong> </summary>
​
<blockquote>

Removes any trace of ThrowaBall out of the avatar's hierarchy and Avatar Descriptor.

![TB Delete Button png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Delete%20Button.png)

<details>

  <summary> <strong> Technical Details </strong> </summary>
​
<blockquote>

Deletes Hierarchy: Any GameObjects with the Prefix "TB".

Deletes Controller Layers: Any Layers with the TB Identifier on the AnyState.

Deletes Controller Parameters: Any Parameters with the Prefix "TB/".

Deletes From Expressions Menu: Any SubMenu whose name contains "ThrowaBall" or leads to a SubMenu with the Prefix "TB".

Deletes From Expression Parameters: Any Parameters with the Prefix "TB".

<blockquote>

</details>

</details>

<details>

  <summary> <strong> Delete from Project </strong> </summary>
​
<blockquote>

Deletes the Generated Resources folder at path `Save File Path/GeneratedTBResources`. This may contain files for more than just the current avatar if you have generated ThrowaBall multiple times in this project.

![TB Delete Button png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Delete%20Button.png)

</details>

<details>

  <summary> <strong> Authorized user </strong> </summary>
​
<blockquote>

Dynamically displays the current Authorized User's discord name and license type. Just a little extra personal touch!

![TB Authorized User png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Authorized%20User.png)

</details>

<details>

  <summary> <strong> Check For Update </strong> </summary>
​
<blockquote>

Click the three lines next to the version number in the bottom left to check for newer versions of ThrowaBall. If a new version is detected, a pop-up window will point you to the changelog.

This will automatically check the first time it is loaded per day.

</details>

<details>

  <summary> <strong> Send Feedback </strong> </summary>
​
<blockquote>

Click the three lines next to the version number in the bottom left to send feedback for ThrowaBall straight from Unity.

</details>

<details>

  <summary> <strong> Verify </strong> </summary>
​
<blockquote>

Click the three lines next to the version number in the bottom left to select when ThrowaBall verifies authentication.

On Display initiates authentication when the window is opened.

On Project Load initiates authentication when the project is opened.

</details>

</details>

### Positioning/Scaling

<details>

  <summary> <strong> Edit Pedestal </strong> </summary>
​
<blockquote>

Adjust the labeled Pedestal target in the scene view to the desired position using the positioning handles.

The Pedestal will always maintain a flat rotation on the XZ plane, and have its button facing the player until placed.

Show/Hide the Position/Rotation handles as necessary.

![TB Edit Pedestal gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Edit%20Pedestal.gif)

</details>

<details>

  <summary> <strong> Edit Ball Target </strong> </summary>
​
<blockquote>

Adjust the Ball Target in the scene view to the desired position/rotation using the positioning handles.

This will follow the Pedestal transform if the Pedestal is included, or otherwise follow the custom target directly.

Enable **Edit Individual Target Offsets per Ball** in order to adjust the ball target on a per-ball basis. This can be helpful for aligning balls of varying sizes with the pedestal/follow target.

Show/Hide the Position/Rotation handles as necessary.

![TB Edit Ball Target gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Edit%20Ball%20Target.gif)

</details>

<details>

  <summary> <strong> Edit Ball Size </strong> </summary>
​
<blockquote>

Adjust the Ball Sizes and Collider Sizes in the scene view using the scale/radius handles or the field below.

Alternatively, you can also multi-select balls to scale multiple balls at once.

Show/Hide the Scale/Radius handles as necessary.

If you're using Unity 2019, using the center scale handle when the scale is not (1, 1, 1) will exponentially snap initially due to a [Unity 2019 bug](https://forum.unity.com/threads/case-1264038-handles-scalehandle-incorrect-when-center-scaling.933798/), but it can still be used to uniformly scale across all axes.

![TB Edit Ball Size gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Edit%20Ball%20Size.gif)

</details>

<details>

  <summary> <strong> Show/Hide Handles </strong> </summary>
​
<blockquote>

Toggle these options to help manage the clutter in the scene while editing the above steps.

This option is only visible while editing the above steps.

![TB Show Hide Handles gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20Show%20Hide%20Handles.gif)

</details>

<details>

  <summary> <strong> Complete Setup </strong> </summary>
​
<blockquote>

Once **Positioning/Scaling** is finished, click **Complete Setup** to generate all the required animations and finalize the system and 3.0.

</details>

---

# Usage

### In-Game Usage Tutorial Video

[![ThrowaBall In-Game Usage Tutorial](http://img.youtube.com/vi/TODO/0.jpg)](https://www.youtube.com/watch?v=TODO "ThrowaBall In-Game Usage Tutorial")

To start using ThrowaBall in game, use the `Toggle` menu to select a ball to make visible, then use `Enable` to initialize the system. Once initialized, the ball should be grabbable via controller grip, as it uses PhysBones to hold rather than gestures.

> [!WARNING]
> Avoid moving while pressing `Enable` in order to avoid offsetting the sync system between you and other players

| Menu Control | Function | Requirement |
| :------------- | :------------- | :------------- |
| `Toggle` | Enable visibility of the pedestal + ball of your choice |  |
| `Enable` | Enable the TB system, drop in world if enabled, and initiate syncing if included |  |
| `Respawn` | Respawn the ball to the ball target/pedestal | Menu Respawn |
| `Sync` | Toggle remote ball syncing (See **Throw Force Mode** above) | Sync Toggle + Physjoint |
| `Force` | Radial puppet to control the relative force multiplier of the ball throw | Throw Force Radial Control |
| `Custom` | Custom animator logic tied to specific custom balls | Custom TB API |

---

# Designing a Custom Ball for ThrowaBall

ThrowaBall is designed to work with the majority of GameObjects, as it generates its own physics collision system independent of the ball object you use.

With that said, below are a few notes you may want to take into account when building your own ball, whether for yourself or to distribute to others.

<details>

  <summary> <strong> Considerations of a ThrowaBall </strong> </summary>
​
<blockquote>

When designing a ball for use with ThrowaBall, below are a few elements you may want to consider:

1. Shape - It's best to use shapes that don't noticeably rely on rotation like spheres (See **Throw Force Mode** above)
2. Uniformity - Non-uniform textures/designs may be noticeable due to lack of proper rotation (See **Throw Force Mode** above)
3. Collision Detection - Optional effects/logic triggered on bounce/collision (See **Include Collision Parameter** above)

</details>

<details>

  <summary> <strong> Usable Components </strong> </summary>
​
<blockquote>

The ThrowaBall system handles the physics/movement of the ball inputs on its own, so the system is designed to work with most objects as long as they are largely static and unmoving on their own (such as the default Unity sphere).

As such, there are a few components to be careful of when creating your custom ball.

- Rigidbodies and Joints (Spring/Configurable) are automatically removed during installation
- Unity Colliders (Sphere/Box/Capsule/Mesh) are automatically removed during installation **if they are not set to IsTrigger**
- Avatar Descriptors on the ball root object are automatically removed during installation due to the [Animator Pseudo API](https://github.com/JustSleightly/ThrowaBall#animator-pseudo-api)
  - Pipeline Managers are also removed from the ball root if an Avatar Descriptor is detected
  - Animator components are also removed from the ball root if an Avatar Descriptor is detected

</details>

## Animator Pseudo API

For those who want to integrate custom animation systems on their ball without losing the functionality of ThrowaBall, this pseudo API provides additional tools to advanced Unity creators to facilitate the process!

![TB API Highlight gif](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Gifs/TB%20API%20Highlight.gif)
![TB Info API png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20Info%20API.png)

To enable this functionality on your own custom ball, **create an empty GameObject as a new parent/root** to your custom ball and add a `VRCAvatarDescriptor`. ThrowaBall will automatically detect ball inputs with Avatar Descriptors and highlight green.

<details>

  <summary> <strong> Automatic 3.0 Merging </strong> </summary>
​
<blockquote>

ThrowaBall will automatically merge in the FX Controller, Expressions Menu, and Expression Parameters from the Avatar Descriptor of the custom ball. There is no particular naming convention you need to follow, except when using **Aliased System/Dynamics Parameters** *(see below)*.

All parameters across all three files will be prefixed with `TB/` and the ball's index, such as `1`, to avoid conflicts between multiple custom balls in the same system. Native VRChat parameters and the VRLabs IsMirror parameter are ignored.

All animation clips and expressions menu (and submenus) will be duplicated so that they are modified non-destructively.

All animation clips will be repathed with their respective location in the ThrowaBall hierarchy as the new root. Your ball animations should be created with the `VRCAvatarDescriptor` as the root in order to be repathed correctly.

![TB API Path png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20API%20Path.png)

</details>

<details>

  <summary> <strong> Aliased System Parameters </strong> </summary>
​
<blockquote>

All ThrowaBall system animator parameters will not be automatically prefixed on a per-ball basis, and will maintain their names to align with the generated system. Additionally installed systems will automatically be suffixed accordingly.

ThrowaBall also offers `TB/Ball` as an aliased parameter that you can use in your custom ball's FX controller.

By using this parameter, you can detect whenever this particular ball is enabled within the ThrowaBall system.

ThrowaBall will automatically change `TB/Ball` according to the index the ball is installed to by the end user.

</details>

<details>

  <summary> <strong> Aliased Dynamics Parameters </strong> </summary>
​
<blockquote>

ThrowaBall offers `TB/AD/` as a parameter prefix that you can use in your custom ball's Avatar Dynamics components, FX controller, and Expression Parameters.

By using this prefix in your parameters, you can accommodate for PhysBones or Contact Receivers per custom ball to avoid conflicts between multiple custom balls in the same system.

This prefix can also be used to adjust Contact Collision Tags dynamically per custom ball to avoid conflicts between multiple custom balls in the same system.

ThrowaBall will automatically change `TB/AD/` according to the mode the ball is installed to by the end user, such as `TB/1/`.

*Avoid having Aliased Dynamics Parameters and regular parameters named identically with or without the prefix, as regular parameters will also be prefixed with `TB/` and their respective index. Example: `TB/AD/Test` and `Test` will both end up being `TB/1/Test`.*

</details>

<details>

  <summary> <strong> Preset Control </strong> </summary>
​
<blockquote>

ThrowaBall can automatically force specific values for the ball physics preset based on explicit values.

ThrowaBall will detect GameObjects underneath the custom ball's Avatar Descriptor for a GameObject named `TB_Preset`.

Only GameObjects that are **direct children** to the Avatar Descriptor will be scanned.

| Preset Property | Transform Field |
| :------------- | :-------------: |
| `Drag` | Scale X |
| `Bounce` | Scale Y |

The `TB_Preset` GameObject will automatically be removed after installation.

</details>

<details>

  <summary> <strong> Collision Parameter Control </strong> </summary>
​
<blockquote>

ThrowaBall can automatically enable **Include Collision Parameter** as an install option if a custom ball requires it.

ThrowaBall will detect GameObjects underneath the custom ball's Avatar Descriptor for a GameObject named `TB_CollisionParameter`.

Only GameObjects that are **direct children** to the Avatar Descriptor will be scanned.

The `TB_CollisionParameter` GameObject will automatically be removed after installation.

</details>

<details>

  <summary> <strong> Automatic Target Reparenting </strong> </summary>
​
<blockquote>

ThrowaBall will automatically reparent certain GameObjects underneath the custom ball's Avatar Descriptor to various parts of the ThrowaBall system, in case you need to use those targets for your own internal logic.

Only GameObjects that are **direct children** to the Avatar Descriptor will be scanned.

![TB API Reparent png](https://github.com/JustSleightly/ThrowaBall/raw/main/Documentation/Images/TB%20API%20Reparent.png)

GameObjects must start with one of the below naming conventions in order to be reparented:

| Target Name | Animation Repathing |
| :------------- | :-------------: |
| `TB_Spawn` | :white_square_button: |
| `TB_Head` | :white_square_button: |
| `TB_Exempt` | :white_check_mark: |
| `TB_Root` | :white_check_mark: |

The `TB_Spawn` target represents the position the ball will respawn at, and automatically accounts for individual ball offsets. It's recommended to give this target a Y-offset of `0.01` in order to account for the grabbable PhysBone offset.

The `TB_Head` target represents the position of the head bone, in case it's needed for aim/rotation constraints.

These targets are not intended to be used for animation clips themselves, but rather as component sources such as for constraints. Animation clips using these targets will not be repathed properly.

The `TB_Exempt` target will be automatically moved just outside of its respective Ball Object so that it and any children will not be automatically disabled when the Ball Object is disabled.

The `TB_Root` target will be automatically moved just under the Avatar Root outside of the ThrowaBall system.

Unlike all other above targets, animation clip properties that start with `TB_Exempt` and `TB_Root` will be repathed properly. These is typically intended to be used alongside **Aliased System Parameters** in order to handle custom logic when the ball/system is enabled/disabled.

Each reparented GameObject will have its name modified to include the index of the ball it's associated with.

</details>

*If you have any questions about this API, or would like to develop for this API but don't own ThrowaBall, feel free to reach out to me!*

---

# Frequently Asked Questions

<details>

  <summary> <strong> Is ThrowaBall compatible with VRChat Quest Avatars? </strong> </summary>
​
<blockquote>

**No**, as [VRChat Quest Avatars](https://docs.vrchat.com/docs/quest-content-limitations) do not support Physics Objects (Rigidbodies, Joints, Colliders) nor Constraints at this time.

</details>

<details>

  <summary> <strong> Is ThrowaBall compatible with Optimized Avatars? </strong> </summary>
​
<blockquote>

**Depends**. The most limiting restrictions are easily the RigidBodies, Colliders, and Audio Sources. It is possible to pull your Avatar down to at least [Medium/Poor](https://docs.vrchat.com/docs/avatar-performance-ranking-system). Below is a table describing all the stat-influencing components that are generated according to what options you enable. Any other stat reductions are dependent on what balls you choose to use alongside this system.

| Options | Components |
| --- | --- |
| `Base` | 2 Rigidbodies + 1 Collider (per unique bounce preset) + 1 PhysBone |
| `Force Particle` | 1 Collider + 1 Particle System + 100 Particles Active + Particle Collision Enabled + 1 Material (VRChat) |
| `Phys Joint` | 1 Rigidbody + 2 PhysBones |
| `Ball Syncing` | 1 Contact Sender + 3 Contact Receivers |
| `Remote Tracker` | 7 Contact Receivers |
| `Collision Parameter` | 1 Contact Sender + 1 Contact Receiver + 1 Particle System + 1 Particle Active + Particle Collision Enabled + 1 Material (VRChat) |
| `Physical Respawn Pedestal` | 1 Skinned Mesh Renderer + 2 Materials + 7219 Polygons + 1 PhysBone + 1 Animator + 1 Particle System + 50 Particles Active + 342 KB VRAM |
| `Default Ball` | 1 Mesh Renderer + 5 Materials + 768 Polygons + 2 Colliders + 43 KB VRAM |
| `Tennis Ball` | 1 Mesh Renderer + 1 Material + 768 Polygons + 2 MB VRAM |
| `Basket Ball` | 1 Mesh Renderer + 1 Material + 768 Polygons + 2 MB VRAM |

</details>

<details>

  <summary> <strong> Why can't other players see my ThrowaBall system in game / Why is it spazzing out?</strong> </summary>
​
<blockquote>

Make sure your Avatar is uploaded at world origin (0,0,0 Position and Rotation)!

</details>

<details>

  <summary> <strong> Why is ThrowaBall's position desyncing? </strong> </summary>
​
<blockquote>

Make sure you have syncing installed/enabled (automatically included for `Force Particle` throw mode), and make sure ThrowaBall is enabled from the menu while standing still.

The syncing accuracy may not be perfectly accurate, but should be within a 0.1 meter tolerance.

The ball movement is also interpolated for remote players due to parameter sync rate, so the peaks/valleys of bounces/collisions may be clipped.

</details>

<details>

  <summary> <strong> Why can't ThrowaBall rotate properly? </strong> </summary>
​
<blockquote>

While it is possible to simulate expected ball (rigidbody) rotation for the local player, it does not sync to remote players regardless of the Throw Force Mode used.

</details>

<details>

  <summary> <strong> Why does throwing ThrowaBall as an external player feel so bad? </strong> </summary>
​
<blockquote>

See the **Disclaimer** near the top of the documentation.

</details>

<details>

  <summary> <strong> Can I edit/swap the balls after I generate ThrowaBall? </strong> </summary>
​
<blockquote>

**Yes**, expand the TB_ThrowaBall hierarchy until you reach the Ball Containers. You can replace any child to the Ball objects, just remember to leave those child objects enabled, as your animations toggle the Ball objects themselves on/off. You should also remove any pre-existing spring/configurable joints, rigidbodies, or sphere/box/capsule/mesh colliders on your balls that would usually be auto-removed by the ThrowaBall installer.

</details>

<details>

  <summary> <strong> How do I export ThrowaBall with my commercial package? </strong> </summary>
​
<blockquote>

Assuming you have a **commercial license** for ThrowaBall, the script generates everything from scratch, making it easy to export without worrying about conflicting with other packages.

You can find these generated resources at `Save File Path/GeneratedTBResources/`. By default, this is `Assets/JustSleightly/ThrowaBall/GeneratedTBResources/`.

The folder with your avatar's ThrowaBall under Generated Resources is the only one you need to export, aside from the files of the actual balls you used with the tool. The only exception to this is if you did not have an FX controller, Gesture controller, Expression Parameters, or Expressions Menu by default, in which those will be generated in your `Assets/` folder.

**You may not** export or redistribute the *ThrowaBall.dll* file and other contents under `Packages/JS - ThrowaBall/`. Please refer to the full Terms and Conditions on my [store](https://store.sleightly.dev/).

</details>

<details>

  <summary> <strong> Why is my project crashing after importing ThrowaBall? </strong> </summary>
​
<blockquote>

Remove ThrowaBall via Windows File Explorer and check your project to see if it currently contains Cinemachine. You can locate this by clicking on `Window > Package Manager` from the top toolbar, and browsing the packages currently in your project. If Cinemachine is added, remove it. It is sometimes added through the VRChat Worlds SDK, so you may need to remove any remnants of the Worlds SDK from your project and this package manager window before removing Cinemachine.

</details>

<details>

  <summary> <strong> Can I change the computer my license is registered to? </strong> </summary>
​
<blockquote>

**Yes**, in the event you change hardware, you can use the **Transfer License** option when trying to verify your license key in Unity on the new hardware. There is a cooldown period to prevent abuse, and these logs will be monitored for misuse. If you need to re-transfer sooner than this transfer period, open a support ticket on [discord](https://discord.sleightly.dev/).

</details>

<details>

  <summary> <strong> Can I upgrade my personal license? </strong> </summary>
​
<blockquote>

**Yes**, open a support ticket on [discord](https://discord.sleightly.dev/) and we can get that process started for you.

</details>

<details>

  <summary> <strong> My license key isn't working! </strong> </summary>
​
<blockquote>

Open a support ticket on [discord](https://discord.sleightly.dev/) or check the ThrowaBall support channel for known issues if you are a validated customer.

</details>

<details>

  <summary> <strong> Where do I report a bug? </strong> </summary>
​
<blockquote>

You can add issues to this github repository, or post it in the support channel for ThrowaBall on [discord](https://discord.sleightly.dev/).

</details>

<details>

  <summary> <strong> Where can I request features/make suggestions? </strong> </summary>
​
<blockquote>

Feel free to leave these in the support channel on [discord](https://discord.sleightly.dev/) and we can discuss them in more detail.

</details>

<details>

  <summary> <strong> I need more help! </strong> </summary>
​
<blockquote>

If you need help with using ThrowaBall, reach out in the designated support channel on [discord](https://discord.sleightly.dev/) so me or a community member can help. If you have private issues involving purchase details, open up a support ticket instead.

</details>

---

## Special Thanks

To my early testers and friends waiting over a year for this release - Blurry/JayJay

**[gonsodany](https://gonsodany.gumroad.com/)** - For helping me speed up dev/testing on the tedious tasks when I was busy/traveling

**[Meechu](https://meechu.gumroad.com/)** - For making the Physical Respawn Pedestal used in ThrowaBall

**[Zekk](https://shop.zekk.dev/)** - Who not only tested ThrowaBall but also developed the default particle ball prefab

**[hfcRed](https://github.com/hfcRed)** - For developing the `Force Particle` throw mode utilized in ThrowaBall

**[jellejurre](https://github.com/jellejurre)** - Who helped polish the `Force Particle` method with **[JeTeeS](https://github.com/JeTeeS)** and helped considerably with troubleshooting ThrowaBall

**[Dreadrith](https://github.com/Dreadrith/DreadScripts)** - For directly implementing the licensing system on the script
