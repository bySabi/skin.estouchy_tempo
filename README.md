# skin.estouchy_tempo

> Fork of the original Kodi skin to change some things in my own interest

## Fork of `skin.estouchy` version `2.0.23`. Only for Kodi `18.1` upto `18.1`

## Changes

### Use the Forward and Rewind buttons to speed up the video playback speed. Maximum 2X
It will only work if the Player Tempo setting is enabled.

## Maintenance instructions
1- Check that the version of the addon matches the latest one in the Kodi repository.

   Latest Kodi [skin.estouchy](https://github.com/xbmc/xbmc/blob/master/addons/skin.estouchy/addon.xml)
   
2- Clone the entire Kodi repository

   `git clone https://github.com/xbmc/xbmc.git`
   
3- Copy content of folder `/addons/skin.estouchy` to `skin.estouchy_tempo` repo. (Replace all files)

4- Edit `skin.estouchy_tempo/xml/IncludesPlayerControls.xml`

####   Replace#1:
   
```
     <control type="group">
         ...
            <control type="button">
               ...
               <onclick>PlayerControl(Rewind)</onclick>
```
    
     with (only "<onclick" line) ...
     
```
      <onclick condition="!Player.TempoEnabled">PlayerControl(Rewind)</onclick>
      <onclick condition="Player.TempoEnabled">PlayerControl(tempodown)</onclick>
```

     
####    Replace#2:
    
```
     <control type="group">
         ...
            <control type="button">
               ...
               <onclick>PlayerControl(Forward)</onclick>
```
    
     with (only "<onclick" line) ...
     
```
      <onclick condition="!Player.TempoEnabled">PlayerControl(Forward)</onclick>
      <onclick condition="Player.TempoEnabled">PlayerControl(tempoup)</onclick>
```

5- Edit `skin.estouchy_tempo/addon.xml`

####   Replace#1:

```
     <addon id="skin.estouchy" ... name="Estouchy" ...
```

     with ...

```
      <<addon id="skin.estouchy_tempo" ... name="Estouchy Tempo" ...
```


## Usage
Download this repo like a ZIP file. install it as is in Kodi


## CAUTION!!

This is a project created for my own use. I have shared it in case anyone has to be useful. **Use it at your own risk**

## Credits

### author

- bySabi Files <> [@bySabi](https://github.com/bySabi)

## Contributing

- Documentation improvement
- Feel free to send any PR
# New Document