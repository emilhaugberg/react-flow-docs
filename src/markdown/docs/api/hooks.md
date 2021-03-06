---
title: Hooks
---

<InfoBox title="Note" text="The following hooks are available from version 8.0.0 upwards. You have to use the ReactFlowProvider if you want to use these hooks."/>

For modifying or reading the state of the graph, you can use the following hooks:

### useZoomPanHelper

This hook can only be used when your application is wrapped with a [`ReactFlowProvider`](/docs/api/components/provider/).
It can be used to modify the viewport of the react flow graph. Example:

```javascript
import { useZoomPanHelper } from 'react-flow';

export default () => {
  const { fitView } = useZoomPanHelper();

  return <button onClick={() => fitView()}></button>;
};
```

The `useZoomPanHelper` hook returns an object containing the following functions:

- `fitView = ({ padding }): void`
- `zoomIn = (): void`
- `zoomOut = (): void`
- `zoomTo = (zoomLevel: number): void`
- `transform: (_: FlowTransform): void`
- `initialized: boolean`
