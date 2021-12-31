---
weight: 1
title: "Welcome"
type: blog
bookFlatSection: false
---

# Welcome to my website!


This website is empty for now. Feel free to visit the links in the sidebar while I finish setting things up.

In the meantime, here is some code I wrote:

```python
def cloneGraph(self, node: 'Node') -> 'Node':
    if not node:
        return
    
    deq = deque([node])
    clone_map = {node : Node(node.val)}
    
    while deq:
        cur = deq.popleft()
        
        for n in cur.neighbors:
            if n not in clone_map:
                deq.append(n)
                clone_map[n] = Node(n.val)
            
            clone_map[cur].neighbors.append(clone_map[n])
                
    return clone_map[node]
```