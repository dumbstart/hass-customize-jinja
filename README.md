## hass-customize

Customize your Home Assistant install with this Jinja script.

You can view the customization of your components as well as create your customization.yaml file using the output.

It allows you to view all components, select components and entities as well has just viewing your HomeBridge and Emulated Hue items.

Changing these settings is done by adding information to the top of the Jinja script. Setting show_only_emulated_hue and show_only_homebrdige to True will only output entities that are respective to their group.

>{%- set show_only_emulated_hue=False -%}
>{%- set show_only_homebridge=False -%}

Adding domains to these lists will only show entities from that domain or will hide those entities when viewing everything.

>{%- set ignored_domains=[] -%}
>{%- set visible_domains=[] -%}

### Known Issues:

If you use Home Assistant Custom UI there are some things to know about how your customizations will be handled.

- state_card_mode: badges will NOT be added
- state_card_custom_ui_secondary will NOT be added
- blacklist_states will NOT be added
- unit will NOT be added
- confirm_controls_show_lock will NOT be added
- confirm_controls will NOT be added
- state_card_mode will NOT be added
- stretch_slider will NOT be added
- slider_theme will NOT be added
- report_when_not_changed will NOT be added
- Template attributes will be included
- show_last_changed will be included
- Per entity themes will be included

Since custom_ui allows you to make changes to all entities of a domain it is expecting you to make changes to them in your configuration file. If it is added to every entity customization then you would have to manually remove them if you wanted to revert any customized domains through custom_ui.