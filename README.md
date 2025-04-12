# UnitySimpleIK
First i cannot guarantee that this will work for your workflow. I tested it with mine and i seemed to work consistently, but i am neither a unity programmer nor a 3d artist, so this still might not work for you. This is basically an alpha version.

Installing the IK:
Copy the contents of the plugin folder to game/bepinex/plugins/.
Copy the UnityProject folder contents into your unity project.

Creating Models using this IK chain:
For both scripts, only check the IK rotation once your ik is setup correctly, or it might mess up the foot rotation.

For both scripts, i suggest getting the IK to work in blender first. Once that is done, export the FBX and import it into your Unity scene. You should then be able to setup the IK chain in unity.

You need to add an ik component for each limb (or other use of ik chains) you want to setup. There are two different kinds of IK scripts:

Two bone IK:
Blender style 2 bone IK chain.
Requires the two bone chain, an IK target and an IK pole. Use Pole Angle for the correct adjustment (try 45° steps if in doubt).

Three bone advanced IK:
This is intended for 3 bone back legs of quadrupeds. It is a bit more tricky to build. It consists of two IK chains for one leg.

Use shin and foot bones, as well as the IK heel bone and a pole placed behind the leg for the first IK chain.
For the second IK Chain, create a dummy bone placed at your thigh, and a dummy shin bone that leads to your foot. Create an IK pole in front of the leg. Set the "Dummythigh" to dummy thigh, the "DummyShin" to your dummy shin, the Thigh to your models actual thigh, and the Thigh Pole to your created one. Adjust both pole angles accordingly (try 45° steps if in doubt).

If you are unsure about how the three bone ik works, or how to build the prerequisites in blender, i would recommend watching this video for reference (~5 Minutes):
https://youtu.be/2p_o6XmmTN0?feature=shared&t=401
