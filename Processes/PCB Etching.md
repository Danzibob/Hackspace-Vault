## 1. Board Prep
- Find a suitable piece of [[Copper Clad Board]]
- Chop the board to a suitable size using the [[Guillotine]]
- Clean & rough up the board using high grit (e.g. 800) sandpaper / wet & dry
	- This is important for adhesion, even if the board looks clean!
- Clean off the debris using [[IPA]]
- Apply an even layer of [[Dykem Blue]] & allow to dry

## 2. Design Prep
- Design tips
	- Use copper fill to minimise required etching
	- Bigger traces (1mm+) will come out better; the final results will be thinner!
	- Pads should be 2mm+
- Export from [[KiCAD]] as an SVG Negative (via the fabrication outputs > gerbers menu)
	- Set the "Holes" setting to "Small" to ensure there's enough pad left
- Load the SVG into [[Inkscape]]
	- Check it over
	- Crop the page area down
	- Add any custom graphics, such as a signature
### 2.5. Export Enhancement
- If parts of the design are looking a bit slim, you can:
	- import the SVG into [[GIMP]] (Make sure to choose a sensible resolution)
	- Select all the traces by colour
	- "Grow" the selection slightly
	- Export this to a PNG then re-load into [[Inkscape]]
	- Export that again as an SVG for [[k40whisperer]]

## 3. Ablating the Etch Resist
- Use the [[Laser]] to Raster Engrave the design onto the board
	- 1 pass, 100mm/s, 5mA, default scan-line step (0.002in)
- You can also etch any Vector art you may have added in [[Inkscape]]
- Gently rub with [[White Spirit]] to clean the lasered crud off the board
- Wipe off the oils left behind with a paper towel

## 4. Etching
### [[Ferric Chloride]]
- Prepare the work surface - Ferric stains like hell
- Find a suitably sized _plastic_ container
- Place the board into the container, and cover with a small amount of Ferric
- Every 2-3 minutes, rise the board in water and rub off the crud with a gloved thumb
- When the board is nearly done, dilute the ferric a little with water so you can see
- If the solution turns perfectly clear when water is added, you need more ferric!
- The board should be translucent when etched, so hold it up to the light to check
- Use [[Acetone]] to remove the [[Dykem Blue]] covering the remaining traces