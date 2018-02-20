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

