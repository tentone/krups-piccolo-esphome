# krups-piccolo-esphome
ESPHome based controller for dolce gusto (krups) piccolo coffer machine

# State Machine
```mermaid
  graph TD;
      HEATING_UP--WAITING;
      WAITING-->COFFE;
      COFFE-->HEATING_UP;
      HEATING_UP-->MAITENANCE
```