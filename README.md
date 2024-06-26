# aframe-trail-component

___

Trail component base upon code by [svartmc](https://github.com/svartmc).

### API

| Parameter  | Default | Description              |
|------------|---------|--------------------------|
| length     | 80      | The length of the trail. |
| width      | 0.8     | The width of the trail.  |
| resolution | 18      | The detail of the trail. |
| color      | white   | The color of the trail.  |
| offset     | 0 0 0   | The offset of the trail. |

## Usage

![pic](https://cdn.glitch.com/76718f34-7920-4a0e-bee1-bd0646eab927%2Ftrail_component.gif?v=1587846617145)

### Include script tag in HTML Head
```
<script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
<script src="https://cdn.jsdelivr.net/gh/EricEisaman/aframe-trail-component@latest/aframe-trail-component.min.js"></script>

```

### HTML (entity with single trail instance and default settings)
```
<a-sphere trail></a-sphere>

```
![pic](https://cdn.glitch.com/76718f34-7920-4a0e-bee1-bd0646eab927%2Fgrabbable_trails.gif?v=1587918027146)

### HTML (entity with multiple trail instances and custom settings)
```
<a-sphere 
trail__red="color:red; offset:-1 0 0"
trail__white="color:white; length:120"
trail__blue="color:blue; offset:1 0 0"
grabbable
></a-sphere>

```

### JS (single instance on an entity)
```
const s = document.createElement('a-sphere');
s.setAttribute('trail','length:50; width:0.9; resolution:10');
AFRAME.scenes[0].appendChild(s);

```

![pic](https://cdn.glitch.com/76718f34-7920-4a0e-bee1-bd0646eab927%2Ftrails_with_colors_and_offsets.gif?v=1587906365878)

### JS (multiple instances on an entity)
```
const s = document.createElement('a-sphere');
s.setAttribute('trail__red','color:red; offset:-1 0 0');
s.setAttribute('trail__white','color:white; length:120');
s.setAttribute('trail__blue','color:blue; offset:1 0 0');
s.setAttribute('color','blue');
s.setAttribute('radius', 0.5);
s.setAttribute('circle-movement','center:0 6 -20; radius: 6');
AFRAME.scenes[0].appendChild(s);

```

![pic](https://cdn.glitch.com/76718f34-7920-4a0e-bee1-bd0646eab927%2Fmultiple_entities.gif?v=1587908954568)
