# Discourse Flow Renderer

A Discourse Theme component to render Node-RED Flow json using the FlowFuse Flow Renderer

Any code block with the `flows` type will be rendered as a Node-RED flow:

````
```flows
[{"id":"45b09c2541029b05","type":"inject","z":"9f9e32404549681c","name":"test","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":180,"y":80,"wires":[["c983a304e0ac7655"]]},{"id":"c983a304e0ac7655","type":"debug","z":"9f9e32404549681c","name":"debug 7","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":370,"y":80,"wires":[]}]
```
````


### Notes

This uses a slightly modified version of the FlowFuse Flow Renderer module: https://github.com/FlowFuse/flow-renderer

The current module is provided as a JavaScript module with an `export` statement at the end. I couldn't find a way to get the Discourse component api to load that module; it complains about the `export` statement. The copy of the flow renderer library (under `assets/`) has that one line removed.

