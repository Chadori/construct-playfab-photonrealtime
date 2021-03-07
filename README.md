# construct-playfab-photonrealtime
The Script Interface documentation for the [Photon Realtime](https://www.constructcollection.com/construct-playfab-photonrealtime) addon of the [Construct Master Collection](https://www.constructcollection.com/), for [Construct 3](https://www.construct.net/).

## IPhotonRealtime documentation
This is the documentation to use Construct 3's new JavaScript [Scripting feature](https://www.construct.net/en/make-games/manuals/construct-3/scripting/overview) with Photon Realtime.

### Easy usage
You can easily access the PhotonRealtime object's interface using the `runtime`, from both the event sheet and script.
```JS
runtime.objects.Photon.getFirstInstance().createRoom("roomName", "lobbyName", 0);
```
For more information, please see the [scripting documentation of the Sprite object](https://www.construct.net/en/make-games/manuals/construct-3/scripting/scripting-reference/plugin-interfaces/sprite).

### Advanced usage
You can also subclass instances in a script, please see the [subclassing instances documentation](https://www.construct.net/en/make-games/manuals/construct-3/scripting/guides/subclassing-instances) for more information.
```JS
class Photon extends IPhotonRealtime
{
	constructor()
	{
		super();
	}
}
```

### API
The supported methods and properties to use in Construct 3's scripting feature with Photon Realtime.

#### Globals
- Context - retrieve the current instance of the Photon Realtime object.
- Client - retrieve the current instance's load balancing client.
- Photon - retrieve the global Photon object.

#### Actions
- setUserId (userId)
- setCustomAuthentication (authParameters, authType)
- setHostingType (hostType)
- setSelfHostedAddress (address)
- setRegion (region)
- setAppId (appId)
- setAppVersion (version)
- connect (lobby)
- createRoom (name, lobbyName, lobbyType)
- joinRoom (name, rejoin, createIfNotExists, lobbyName, lobbyType)
- joinRandomRoom (matchMyRoom, matchmakingMode, lobbyName, lobbyType, sqlLobbyFilter)
- disconnect ()
- suspendRoom ()
- leaveRoom ()
- raiseEvent (eventCode, data, interestGroup, cache, receivers, targetActors, webForward)
- changeGroups (action, group)
- webRpc (uriPath, parameters, parametersType)
- findFriends (friends)
- requestLobbyStats ()
- setMyActorName (name)
- setPropertyOfActorByNr (nr, propName, propValue, webForward, checkAndSet, expectedValue)
- setPropertyOfMyRoom (propName, propValue, webForward, checkAndSet, expectedValue)
- setPropsListedInLobby (propNames)
- setMyRoomIsVisible (isVisisble)
- setMyRoomIsOpen (isOpen)
- setMyRoomMaxPlayers (maxPlayers)
- setEmptyRoomLiveTime (emptyRoomLiveTime)
- setSuspendedPlayerLiveTime (suspendedPlayerLiveTime)
- setUniqueUserId (unique)
- reset ()
- PlayFabAuthenticate (PlayFabID, PhotonToken)
- GetPhotonAuthToken ()

#### Conditions
- isConnectedToNameServer  ()
- isConnectedToMaster  ()
- isInLobby  ()
- isJoinedToRoom  ()

#### Expressions
- ErrorCode ()
- ErrorMessage ()
- State ()
- StateString ()
- UserId ()
- MyActorNr ()
- MyRoomName ()
- EventCode ()
- EventData ()
- ActorNr ()
- RoomCount ()
- RoomNameAt (i)
- RoomMaxPlayers (name)
- RoomIsOpen (name)
- RoomPlayerCount (name)
- RoomProperty (name, propName)
- PropertyOfMyRoom (propName)
- ActorCount ()
- ActorNrAt (i)
- ActorNameByNr (nr)
- PropertyOfActorByNr (nr, propName)
- ChangedPropertiesCount ()
- ChangedPropertyNameAt (i)
- MasterActorNr ()
- WebRpcUriPath ()
- WebRpcResultCode ()
- WebRpcData ()
- FriendOnline (name)
- FriendRoom (name)
- LobbyStatsCount ()
- LobbyStatsNameAt (i)
- LobbyStatsTypeAt (i)
- LobbyStatsPeerCountAt (i)
- LobbyStatsGameCountAt (i)
- AppStatsPeerCount ()
- AppStatsMasterPeerCount ()
- AppStatsGameCount ()
- PhotonToken ()

### Guide
The API documentation only shows the **methods** with its **parameters**, sometimes this is not enough to fully understand each use of the references.
To solve that, use the **Photon Realtime** addon as reference.

![image](https://user-images.githubusercontent.com/31282960/110241633-c14b0400-7f8c-11eb-8508-eb39a741997a.png)

**Instructions**
- For **text** parameters, use `string` values.
- For **number** parameters, use `int` or `float` values.
- For **combo** parameters, use the placement of the drop-down selection, starting from `0`.
- For **toggle** parameters, use `boolean` values.
