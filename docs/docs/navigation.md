# Navigation

## Base Nav

<Preview>
  <RfNav :children="menu"></RfNav>
</Preview>

```html
  <RfNav :children="menu"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

## Available styles

### Horizontal alignment

<Preview>
  <RfNav :children="menu" class="justify-content-center"></RfNav>
</Preview>

```html
  <RfNav :children="menu" class="justify-content-center"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Vertical

<Preview>
  <RfNav :children="menu" direction="vertical"></RfNav>
</Preview>

```html
  <RfNav :children="menu" direction="vertical"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Tabs

<Preview>
  <RfNav :children="menu" type="tabs"></RfNav>
</Preview>

```html
  <RfNav :children="menu" type="tabs"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Pills

<Preview>
  <RfNav :children="menu" type="pills"></RfNav>
</Preview>

```html
  <RfNav :children="menu" type="pills"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Extend fill

<Preview>
  <RfNav :children="menu_extend" type="pills" extend="fill"></RfNav>
</Preview>

```html
  <RfNav :children="menu" type="pills" extend="fill"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Much longer nav link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Extend justified

<Preview>
  <RfNav :children="menu_extend" type="pills" extend="justified"></RfNav>
</Preview>

```html
  <RfNav :children="menu" type="pills" extend="justified"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Much longer nav link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

### Working with flex
If you need responsive nav variations, consider using a series of [flexbox utilities](https://getbootstrap.com/docs/4.3/utilities/flex/). While more verbose, these utilities offer greater customization across responsive breakpoints. In the example below, our nav will be stacked on the lowest breakpoint, then adapt to a horizontal layout that fills the available width starting from the small breakpoint. [More info](https://getbootstrap.com/docs/4.3/components/navs/#working-with-flex-utilities)


## Using Dropdowns

<Preview>
  <RfNav :children="menu_dropdown" type="tabs"></RfNav>
</Preview>

```html
  <RfNav :children="menu" type="tabs"></RfNav>
```
```js
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Dropdown',
            link: '#',
            active: false,
            disabled: false,
            showDropdown: false,
            children: [
              {
                name: 'Action',
                link: '/action',
              },
              {
                name: 'Another Action',
                link: '#',
                onClick: function(item, $event) { alert('another action') },
              },
              {
                name: 'Disabled Action',
                link: '#',
              },
              {
                name: 'divider',
              },
              {
                name: 'Separated link',
                link: '#',
              },
            ]
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ]
      }
    }
  }
```

## Navbar

<Preview>
  <RfNavBar
    brand="Refactory"
    logo="/logo-sm.png"
    text="UI Kit"
  ><template v-slot:collapse><RfNav :children="menu_dropdown" class="mr-auto"></RfNav></template>
  </RfNavBar>
</Preview>

<script>
  export default {
    data() {
      return {
        menu: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ],
        menu_extend: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Much longer nav link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Action',
            link: '/action',
            active: false,
            disabled: false,
            onClick: function(item, $event) { alert('action called') },
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ],
        menu_dropdown: [
          {
            name: 'Active',
            link: '/active',
            active: true,
            disabled: false
          },
          {
            name: 'Link',
            link: '/link',
            active: false,
            disabled: false
          },
          {
            name: 'Dropdown',
            link: '#',
            active: false,
            disabled: false,
            showDropdown: false,
            children: [
              {
                name: 'Action',
                link: '/action',
              },
              {
                name: 'Another Action',
                link: '#',
                onClick: function(item, $event) { alert('another action') },
              },
              {
                name: 'Disabled Action',
                link: '#',
              },
              {
                name: 'divider',
              },
              {
                name: 'Separated link',
                link: '#',
              },
            ]
          },
          {
            name: 'Disabled',
            link: '/disabled',
            active: false,
            disabled: true
          },
        ],
      }
    }
  }
</script>