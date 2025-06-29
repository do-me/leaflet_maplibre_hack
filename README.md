# Leaflet-Maplibre-Hack

**This repo is only for you if you are bound to some legacy Leaflet version below v1.0 where vector tiles could not yet be displayed.**

The example here uses maplibre as base layer displaying vector-tile-based basemaps. This layer is not supposed to be interactive, so it can stay in the background. The markers, lines and geometries are drawn on top of this basemap with Leaflet so you do not need to rewrite your application but can still use:

- super performant and cheap protomaps-based basemaps. See https://maps.protomaps.com/#flavorName=light&lang=en&map=1.22/0/0 for reference. This repo includes a style.json but you need to enter a valid URL for your own protomaps instance like `"url": "pmtiles://https://fsn1.your-objectstorage.com/your-bucket/world.pmtiles"`
- official OSM vector tiles
- BKG basemaps for Germany with: style: `https://gdz.bkg.bund.de/index.php/default/gdz-basemapde-vektor-gdz-basemapde-vektor.html`
- OpenFreeMaps with: style: `https://tiles.openfreemap.org/styles/liberty`

## Issues 

Everything works, however, note that animations (for a "smooth" zooming experience) are currently turned off. I did not manage yet to get smooth zooming for both leaflet & maplibre at the same time without delay. 

For Leaflet, you can turn it on again with: `zoomAnimation: false,`, then the markers etc. will be animated. However, it creates an annoying offset for the animation duration between the actual coordinates of the markers vs. the basemap (that is not animated). 


