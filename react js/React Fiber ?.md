In older versions of react (≤ v15) the reconcilliation was done using recursive stack calls (synchronous, blocking).
In newer versions (v16+) the reconcilliation was done using fiber architecture uses linked list.
## Reconcilliation
Reconciliation is the process where React creates a new Virtual DOM, compares it with the previous Virtual DOM using the diffing algorithm, and updates only the specific parts of the real DOM where changes occurred after a state or prop update.

## React fiber 
The react fiber architecture works in two phases:
### Phase 1 : Render (Reconciliation Phase)
Builds a new Fiber tree.
Compares it with the old Fiber tree (diffing).
Decides what needs to be updated.
Can be paused, resumed, or aborted based on priority.
### Phase 2 : Commit Phase
Applies the necessary updates to the actual DOM.
This phase is always synchronous and fast.

### Linked List 
In old React (≤ v15), reconciliation used recursion + call stack → no way to pause/resume.
Fiber replaces recursion with an iterative structure:
Each component in the tree is represented as a Fiber node (a JavaScript object).
These Fiber nodes are connected like a linked list so React can walk the tree manually instead of relying on recursion.
