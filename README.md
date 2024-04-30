## Stamps for Nuke with alternative GUI

Here is a quick summary of the changes made to the original code:

- new GUI to set up new Node Connections
- search and create like Nuke Nodes (Character-based matching, hit Tab/Enter to create)
- Support for colored Anchors and Backdrops
- disable/hide Anchors (e.g. you import another nukescript as reference)
- **CTRL+SHIFT+Drop Node** to swap nodes preserves connections
- performance improvements

### new Shortcuts

within the new GUI:

- **RIGHT CLICK** to preview with Viewer (resets Viewer on close)
- **SHIFT+CLICK:** select and create multiple Stamps
- **ALT+CLICK:** open color quick menu to colorize Anchor
- **CTRL+CLICK:** jumps to Anchor or Category (also works on top row of UI)
- **CTRL+ALT+CLICK:** jump/cycle through Stamps

and outside the GUI:

- **CTRL+STAMPS_SHORTCUT:** with one or multiple Anchors selected, set a new color
- **CTRL+STAMPS_SHORTCUT:** with Stamp selected, will jump to it's anchor
- **SHIFT+STAMPS_SHORTCUT:** with one or multiple Anchors or Stamps selected, will select all stamps of their/that anchor
- **D:** disable (hide) Anchors. They won't show up in the new UI.

#### new GUI 

![Stamps Example 1](https://lukasschwabe.com/wp-content/uploads/2024/04/stamps_example1.png)
(Tag Categories left, Backdrop Categories right)

#### Create multiple Stamps

![Stamps Example 5](https://lukasschwabe.com/wp-content/uploads/2024/04/stamps_example5.png)

#### Show all Connections

![Stamps Example 2](https://lukasschwabe.com/wp-content/uploads/2024/04/stamps_example2.png)

#### Set color (works with multiple Anchors selected)

![Stamps Example 3](https://lukasschwabe.com/wp-content/uploads/2024/04/stamps_example3.png)

#### Jump to Anchor/Category

![Stamps Example 4](https://lukasschwabe.com/wp-content/uploads/2024/04/stamps_example4.png)

### Known issues

To properly support colored Anchors and Stamps (red font for broken connections, nicer formatting), we had to utilize HTML for the autolabel. Unfortunately, Nuke behaves a bit funky with those. If you zoom in/out in the DAG, you'll notice that the last character sometimes flips into a new line. We haven't found a way to work around this, I opened a bug report, let's hope for the best :) -> [Bug Report (Foundry Account required)](https://support.foundry.com/hc/en-us/articles/18657215784978-ID-575964-The-formatting-on-a-nodes-autolabel-breaks-at-certain-zoom-levels-in-the-Node-Graph)