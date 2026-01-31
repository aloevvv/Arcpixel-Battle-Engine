# Arcpixel-Battle-Engine
I built my own engine for my fangame, 8-Bit's Adventure, but I decided, why not show it off? Free to use NOT DONE YET, STILL NEEDS TO REMOVE SOME ELEMENTS OF MY GAME. It is for JRPGs that use an ATB system, not turns.
<br>
<br>Battle Functions: initiateBattle(), handleEnemyDeath(), endBattle(),
<br>Enemy Handling: performEnemyAction(), spawnRound(),
<br>Player & Party: x
<br>Inventory: inventory.set, drawEquipsUI(),
<br>Special Items: x
<br>Overworld: x
<br>Dialogue: showDialog(), showBattleDialog(), showDialogWithOptions

<br> How to use the levels?
<br>{
<br>bgSrc: "arcade.png",
    <br>walls: [
      <br>{ x: 0, y: 0, width: 20, height: 20 },
    <br>],
    <br>doors: [
    <br>{ x: 0, y: 0, width: 20, height: 20, destLevel: '1', destX: 0, destY: 0 }
   <br> ],
   <br>battleZones: [],
    <br>dialogZones: [],
    <br>interactables: []
  <br>},

  <br> This is the typical format. waterZones, darkZones, iceZones, and poisonZones may also be inserted.
  
  <br> To add enemies, add { x: 0, y: 0, width: 100, height: 100, encounter: [{ type: "Dummy" }, {type: "Dummy"}], sprite: 'enemy'} to the array. Enemy sprites are added via zoneSprites.

  <br>Dialogue is added as:
  <br>{
    <br>id: 'uniqueid',
    <br>x: 0, y: 0, width: 640, height: 480,
    <br>text: [
      <br>{ speaker: 'NPC', text: "placeholder text.", style: 'npc' },
      <br>{ speaker: 'Hero',  text: "placeholder text.", style: 'dialog' }
    <br>],
    <br>autoShow: true,
    <br>style: 'dialog'
  <br>}

  <br>There are a few built in effects, added by including effect: 'example'. They are: shaky, sine/wave, and glitch. speakerConfig controls the sound that plays depending on the speaker, and style changes the background color.
