# Tiles custom state card for [Home Assistant](https://home-assistant.io)

![preview](https://raw.githubusercontent.com/c727/home-assistant-tiles/master/docs/preview.png)

## Installation
* Download `/www/custom_ui/state-card-tiles.html` to `<config-dir>/www/custom_ui/state-card-tiles.html`
* Add it to your `configuration.yaml`:
```yaml
frontend:
  extra_html_url:
    - /local/custom_ui/state-card-tiles.html
  extra_html_url_es5:
    - /local/custom_ui/state-card-tiles.html
```

## Configuration
```yaml
homeassistant:
  customize:
    input_text.dummy_tiles:
      custom_ui_state_card: state-card-tiles
      config:
        columns: 3          # optional
        column_width: 75px  # optional
        row_height: 75px    # optional
        gap: 4px            # optional
        color: blue         # optional
        color_on: green     # optional
        color_off: red      # optional
        entities:
          - entity: script.test
            label: S1       # optional
            icon: mdi:power # optional
            image: /local/test.png # optional
            data: {value: right}   # optional
            column: 2       # optional
            column_span: 2  # optional
            row: 2          # optional
            row_span: 2     # optional
 ```
 
 Also check the sample configuration.
