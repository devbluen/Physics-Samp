# 🎢 Physics-Samp
Include updated physics for SAMP with support for [Streamer plugin](https://github.com/samp-incognito/samp-streamer-plugin)
This include supports up to 1024 objects from the Streamer plugin. If you need more than that, you have to configure the 'PHY_MAX_OBJECTS' define and adjust it according to your needs.

# Description:
The project currently does not support native objects, but soon I will update it and add this functionality to support both.

# 📃 Functions
```pawn
- PHY_InitObject(objectid, modelid = 0, Float:mass = 1.0, Float:size = FLOAT_NAN, mode = PHY_MODE_3D)
- PHY_DeleteObject(objectid)
- PHY_SetObjectVelocity(objectid, Float:vx, Float:vy, Float:vz = 0.0)
- PHY_GetObjectVelocity(objectid, &Float:vx, &Float:vy, &Float:vz)
- PHY_SetObjectAcceleration(objectid, Float:ax, Float:ay, Float:az = 0.0)
- PHY_GetObjectAcceleration(objectid, &Float:ax, &Float:ay, &Float:az)
- PHY_GetObjectSpeed(objectid, &Float:speed, _3D = 0)
- PHY_GetObjectMoveAngle(objectid, &Float:moveangle)
- PHY_UseColAndreas(objectid, mode = 1)
- PHY_RollObject(objectid, toggle = 1, rollingmode = PHY_ROLLING_MODE_DEFAULT)
- PHY_SetObjectFriction(objectid, Float:friction)
- PHY_SetObjectAirResistance(objectid, Float:resistance)
- PHY_SetObjectZBound(objectid, Float:low = FLOAT_NAN, Float:high = FLOAT_NAN, Float:constant = 0.0)
- PHY_SetObjectGravity(objectid, Float:gravity)
- PHY_SetObjectWorld(objectid, world)
- PHY_ToggleObjectPlayerColls(objectid, toggle = 1, Float:constant = 1.0, Float:distoffset = 0.8, Float:zoffsetlow = 1.0, Float:zoffsethigh = 1.0)
- PHY_ApplyRotation(objectid, Float:speed, Float:moveangle)
- PHY_ApplyQuaternionsRotation(objectid, Float:speed, Float:moveangle)
- PHY_CreateWall(Float:x1, Float:y1, Float:x2, Float:y2, Float:constant = 1.0, Float:low = FLOAT_NEG_INFINITY, Float:high = FLOAT_INFINITY)
- PHY_CreateArea(Float:minX, Float:minY, Float:maxX, Float:maxY, Float:constant = 1.0, Float:low = FLOAT_NEG_INFINITY, Float:high = FLOAT_INFINITY)
- PHY_DestroyWall(wallid)
- PHY_SetWallWorld(wallid, world)
- PHY_CreateCylinder(Float:x, Float:y, Float:size, Float:constant = 1.0, Float:low = FLOAT_NEG_INFINITY, Float:high = FLOAT_INFINITY)
- PHY_DestroyCylinder(cylinderid)
- PHY_SetCylinderWorld(cylinderid, world)
- PHY_SetPlayerWorld(playerid, world)
```

# 📃 Callbacks
```pawn
public PHY_OnObjectUpdate(objectid);
public PHY_OnObjectCOLWithObj(object1, object2);		// This used to be called "PHY_OnObjectCollideWithObject" and was changed to "PHY_OnObjectCOLWithObj" due to YSI support, you can change it.
public PHY_OnObjectCollideWithZBound(objectid, lowhigh); // low bound = 0, high bound = 1
public PHY_OnObjectCollideWithSAWorld(objectid, Float:cx, Float:cy, Float:cz);
public PHY_OnObjectCollideWithWall(objectid, wallid);
public PHY_OnObjectCollideWithCylinder(objectid, cylinderid);
public PHY_OnObjectCollideWithPlayer(objectid, playerid);
```

### 📁 Credits

[uPeppe](https://github.com/uPeppe/physics.inc) original project.<br>
[zeelorenc](https://github.com/zeelorenc/Object-Physics) for editing the original project (But it's outdated).
