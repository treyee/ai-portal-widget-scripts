# ai-portal-widget-scripts

Widget Scripts to embed [Treyee AI Portal](https://treyee.ai/ecosystem/components/ai-portal) Assistants in Web Sites

## Getting Started

The `AI Assistant ID` and `Region` are required to embed the AI Assistant in your website. Check with your Account or Business Development Manager for the correct values.

## Chatbox (iFrame like)

Use this if want to render the chatbot itself in a div, style the div with `id="VG_OVERLAY_CONTAINER"`, so if you have 500px as width & height for example it will render the chatbot within these dimensions.

```html
<div style="width: 500px; height: 500px;" id="VG_OVERLAY_CONTAINER">
<!-- Here is where AI Portal renders the widget. -->
<!-- Set width, height for 500px as an example after changing render to 'full-width' -->
</div>

<!-- Remove 'defer' if you want widget to load faster (Will affect website loading) -->
<script defer>
    (function() {
        window.VG_CONFIG = {
            ID: "m38bw8umb0rujkzz", // Treyee AI Assistant ID (from Treyee AI Portal)
            region: 'na', // 'eu' or 'na'corresponding to Europe and North America
            render: 'full-width', // popup or full-width
            stylesheets: [
                // Default Treyee AI Portal CSS
                "https://vg-bunny-cdn.b-cdn.net/vg_live_build/styles.css",
                // Add your custom css stylesheets, Can also add relative URL ('/public/your-file.css)
            ],
        }
        var VG_SCRIPT = document.createElement("script");
        VG_SCRIPT.src = "https://vg-bunny-cdn.b-cdn.net/vg_live_build/vg_bundle.js";
        VG_SCRIPT.defer = true; // Remove 'defer' if you want widget to load faster (Will affect website loading)
        document.body.appendChild(VG_SCRIPT);
    })()
</script>
```

### Demonstration

Check out the demo for the chatbox mode: [https://treyee.ai/ecosystem/components/ai-portal/widget/chatbox](https://treyee.ai/ecosystem/components/ai-portal/widget/chatbox)

## Popup

Use this if want to render a popup that is shown at the bottom right of your website, when a user clicks on it the chatbot appears in a little chatbox.

```html
<div style="width: 0; height: 0;" id="VG_OVERLAY_CONTAINER">
<!-- Here is where Treyee AI Portal renders the widget. -->
<!-- Set render to 'full-width' then adjust the width and height to 500px (for example) to render the chatbot itself without the popup. -->
</div>

<!-- Remove 'defer' if you want widget to load faster (Will affect website loading) -->
<script defer>
    (function() {
        window.VG_CONFIG = {
            ID: "m38bw8umb0rujkzz", // Treyee AI Assistant ID (from Treyee AI Portal)
            region: 'na', // 'eu' or 'na'corresponding to Europe and North America
            render: 'bottom-right', // can be 'full-width' or 'bottom-left' or 'bottom-right'
            stylesheets: [
                // Default Treyee AI Portal CSS
                "https://vg-bunny-cdn.b-cdn.net/vg_live_build/styles.css",
                // Add your custom css stylesheets, Can also add relative URL ('/public/your-file.css)
            ],
        }
        var VG_SCRIPT = document.createElement("script");
        VG_SCRIPT.src = "https://vg-bunny-cdn.b-cdn.net/vg_live_build/vg_bundle.js";
        VG_SCRIPT.defer = true; // Remove 'defer' if you want widget to load faster (Will affect website loading)
        document.body.appendChild(VG_SCRIPT);
    })()
</script>
```

### Demonstration

Check out the demo for the popup mode: [https://treyee.ai/ecosystem/components/ai-portal/widget/popup](https://treyee.ai/ecosystem/components/ai-portal/widget/popup)

## iFrame

Similar to the "Chatbox" script and will render the chatbot itself in the iframe tag, you can also style that iframe with a custom width and height, Note: you cannot add custom CSS directly using this method.

```html
<iframe
    src="https://www.tixaeagents.ai/app/na/render/m38bw8umb0rujkzz/iframe"
    style="width: 100%; height: 100vh;"
    frameborder="0">
</iframe>
```

### Demonstration

Check out the demo for the iFrame mode: [https://treyee.ai/ecosystem/components/ai-portal/widget/iframe](https://treyee.ai/ecosystem/components/ai-portal/widget/iframe)

## Modal

Use this if you want to render a modal popup in the center of the screen. The chatbot will appear in a larger chat window that overlays the website when a user clicks on the trigger button.

```html

<div style="width: 0; height: 0;" id="VG_OVERLAY_CONTAINER">
    <!-- Here is where Treyee AI Portal renders the widget. -->
</div>

<!-- Remove 'defer' if you want widget to load faster (Will affect website loading) -->
<script defer>
    (function() {
        window.VG_CONFIG = {
            ID: "m38bw8umb0rujkzz", // Treyee AI Assistant ID (from Treyee AI Portal)
            region: 'na', // YOUR ACCOUNT REGION 
            render: 'bottom-right', // can be 'bottom-left' or 'bottom-right'
            modalMode: true, // Set this to 'true' to open the widget in modal mode
            stylesheets: [
                // Base Treyee AI Portal CSS
                "https://vg-bunny-cdn.b-cdn.net/vg_live_build/styles.css",
                // Add your custom css stylesheets, Can also add relative URL ('/public/your-file.css)
            ],
        }
        var VG_SCRIPT = document.createElement("script");
        VG_SCRIPT.src = "https://vg-bunny-cdn.b-cdn.net/vg_live_build/vg_bundle.js";
        VG_SCRIPT.defer = true; // Remove 'defer' if you want widget to load faster (Will affect website loading)
        document.body.appendChild(VG_SCRIPT);
    })()
</script>
```

### Demonstration

Check out the demo for the modal mode: [https://treyee.ai/ecosystem/components/ai-portal/widget/modal](https://treyee.ai/ecosystem/components/ai-portal/widget/modal)
