## Purpose
Simplifies Boolean algebra expressions visually to create optimal logic circuits.

## Basic Rules

### Grouping
- Rectangles only (2^n cells: 1,2,4,8)
- Maximize group size
- Minimize number of groups
- Groups can wrap around edges (top-bottom, left-right)
- Overlapping groups are allowed

### Reading Groups
- Identify variables that **don't change** within the group
- Eliminate variables that change within the group

---
## 4-Variable K-Map

<img src="Pictures/kmap.png" width=500 height="auto" style="display: block; margin: auto">

**Result**: 


---
## Limitations
Beyond 6 variables becomes **impractical**. Use Quine-McCluskey algorithm instead.Retry

Tags: #k-maps