# GAME_PROGRAM-EX--4
## ATTACT RIFLE WITH CHARACTER MESH AND IMPLEMENTATION BULLET SPAWN FROM RIFLE:
## NAME : A.NABITHRA
## REGISTER NO : 212224230172
## AIM :
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.

## PROCEDURE :
## 1.Attach the Rifle to the Character
Import the Rifle Skeletal Mesh into Unreal Engine. Open your Character Blueprint (e.g., BP_ThirdPersonCharacter). In the Components tab: Add a Skeletal Mesh or Static Mesh component (name it Rifle). Set its Skeletal Mesh to your rifle asset.

## 2.Attach the Rifle to a socket on the character’s skeleton
In the Rifle component, set the Parent Socket to something like hand_r (right hand socket).

manually attach in Event Graph:
```
Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");
```
## 3. Add Aiming Mechanism
Create a Boolean variable called IsAiming. Set up Input in Project Settings: Go to Edit > Project Settings > Input. Add an Action Mapping named Aim (e.g., Right Mouse Button).

## 4. Adjust Camera When Aiming
Add a Camera Boom and Follow Camera.

In Event Graph:
```
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.
```
## OUTPUT :
<img width="929" height="743" alt="image" src="https://github.com/user-attachments/assets/e00e2942-0885-474f-b3ee-fcaa83fd119c" />
<img width="933" height="498" alt="Screenshot 2025-11-19 142922" src="https://github.com/user-attachments/assets/22eff454-2efe-4523-bda1-816e0fd2ebaf" />

## RESULT :
Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.
