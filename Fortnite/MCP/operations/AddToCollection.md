# AddToCollection

**Description**: `Adds an item to the collection` \
**Profiles**: `collections` \
**Note**: `DedicatedServer ONLY`

## Body

```js
{
    "category": "", // Category Template Id, e.g. CollectableCharacter:tandem, CollectableCharacter:boss, CollectablePlayerAugment:collection
    "variant": "", // The Variant Gameplaytag, e.g. AISpawnerData.Type.Tandem.SpaceChimp, PlayerAugment.Collection.PartyTime, Fish.Angler.PurpleOrange
    "contextTags": [], // Context Gameplaytags if existing, e.g. Athena.Location.UnNamedPOI.Tandem.SpaceChimp
    "properties": {}, // see below
    "seenState": "", // Enum: EFortCollectedState
    "count": 1 // catch count (fish) or talk count (npc)
}
```

### Properties

> **Fish** (FFortMcpCollectedFishProperties)
>
> - weight: float
> - length: float

> **NPC / Character (Tandem)** (FFortMcpCollectedCharacterProperties)
>
> - questsGiven: int
> - questsCompleted: int
> - encounterTypeFlags: int

<br/>

### Enum: EFortCollectedState

- Unknown
- New
- Known
- NewlyCollected
- Collected
- NewBest
- NewRecord
- NewLocation
- NewlyCompleted
- Complete
