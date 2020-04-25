# aframe-trail-component

___

Trail component base upon code by [svartmc](https://github.com/svartmc).

![pic](https://cdn.glitch.com/76718f34-7920-4a0e-bee1-bd0646eab927%2Ftrail_component.gif?v=1587846617145)


### API

| Parameter  | Default | Description              |
|------------|---------|--------------------------|
| length     | 80      | The length of the trail. |
| width      | 0.8     | The width of the trail.  |
| resolution | 18      | The detail of the trail. |


## Usage

### HTML
```
<a-sphere trail></a-sphere>

```

### JS
```
const s = document.createElement('a-sphere');
s.setAttribute('trail','length:50; width:0.9; resolution:10');
AFRAME.scenes[0].appendChild(s);

```
