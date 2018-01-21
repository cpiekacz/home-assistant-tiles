# Tiles custom state card for [Home Assistant](https://home-assistant.io)

![preview](https://raw.githubusercontent.com/c727/home-assistant-tiles/master/docs/preview.png)

## Installation
* Download `/www/custom_ui/state-card-tiles.html` and `/www/custom_ui/state-card-tiles_es5.html` to `<config-dir>/www/custom_ui/`
* Add it to your `configuration.yaml`:
```yaml
frontend:
  extra_html_url:
    - /local/custom_ui/state-card-tiles.html
  extra_html_url_es5:
    - /local/custom_ui/state-card-tiles_es5.html
```

## Configuration
```yaml
homeassistant:
  customize:
    input_text.dummy_tiles:
      custom_ui_state_card: state-card-tiles
      config:
        columns: 3            # optional
        column_width: 75px    # optional
        row_height: 75px      # optional
        gap: 4px              # optional
        color: blue           # optional
        color_on: green       # optional
        color_off: red        # optional
        text_color: #FFF      # optional
        text_color_on: #FFF   # optional
        text_color_off: #FFF  # optional
        entities:
          - entity: script.test
            label: S1              # optional
            label_state: input_boolean.switch2  # optional
            icon: mdi:power        # optional
            image: /local/test.png # optional
            data: {value: right}   # optional
            column: 2              # optional
            column_span: 2         # optional
            row: 2                 # optional
            row_span: 2            # optional
            color: blue            # optional
            color_on: green        # optional
            color_off: red         # optional
            text_color: #FFF       # optional
            text_color_on: #FFF    # optional
            text_color_off: #FFF   # optional
 ```
 
 Also check the sample configuration.

## Run as panel
```
panel_custom:
  - name: tiles
    sidebar_title: Tiles
    sidebar_icon: mdi:view-dashboard
    url_path: tiles
    config:
      entities:
        - entity: input_boolean.switch1
          label: Switch 1
```

## Changelog
Version 20180120:
```
-added ES5 and ES6 version
-changed default column width to 1fr
-changed background image to no-repeat and center
-added color, color_on, color_off (global + per entity)
-added text_color, text_color_on, text_color_off (global + per entity)
-added label_state: state from any entity_id as label text
```