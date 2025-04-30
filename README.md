# Revolution-Macro-DEMO
The Future Site Of Revolution Macro!

# Revolution Macro Website - Alert System Customization

This document explains how to customize the alert system in the Revolution Macro Website. The alert system displays a modal popup on the homepage (`index.html`) when the page loads, and it can be configured to show a message, change its color, and include up to two buttons with custom actions.

## Alert System Configuration

The alert system is controlled by the `alertConfig` object in `index.html`. Follow these steps to customize it:

1. **Open `index.html`**: Locate the file in the root directory of the project.
2. **Find the `alertConfig` Object**: At the top of the `<script>` section in `index.html`, you’ll find the `alertConfig` object:
   ```javascript
   const alertConfig = {
       // -- INFO CONFIGURE --
       alertEnabled: true, // Enable or disable the alert (true or false)
       alertColour: 'Green', // Options: Red, Blue, Green, Purple, Pink, Yellow, Orange, Grey

       // -- TEXT --
       alertHeaderText: 'ALERRT!!!', // The header text for the alert
       alertText: 'This is a test alert do not be alerted! Join our discord too!', // The body text for the alert

       // -- BUTTONS --
       button1: {
           enabled: true, // Enable or disable Button 1 (true or false)
           text: 'Close', // Text for Button 1
           function: '[closesite]' // Options: '[closesite]' or a URL (e.g., 'https://example.com')
       },
       button2: {
           enabled: true, // Enable or disable Button 2 (true or false)
           text: 'Discord', // Text for Button 2
           function: 'https://discord.com/invite/bm2bcwZWkj' // Options: '[closesite]' or a URL
       }
   };
   ```
3. **Edit the Configuration**:
   - **Enable/Disable the Alert**:
     - Set `alertEnabled` to `true` to show the alert on page load, or `false` to disable it.
     - Example: `alertEnabled: false`
   - **Change the Color**:
     - Set `alertColour` to one of the following options: `Red`, `Blue`, `Green`, `Purple`, `Pink`, `Yellow`, `Orange`, `Grey`.
     - This changes the border, header, and button color of the alert.
     - Example: `alertColour: 'Red'`
   - **Change the Text**:
     - Update `alertHeaderText` to change the alert’s header.
     - Update `alertText` to change the alert’s body text.
     - Example:
       ```javascript
       alertHeaderText: 'New Alert!',
       alertText: 'Check out our latest update!',
       ```
   - **Configure Buttons**:
     - **Button 1**:
       - `enabled`: Set to `true` to show the button, `false` to hide it.
       - `text`: The button’s label.
       - `function`: Set to `'[closesite]'` to close the alert, or a URL (e.g., `'https://example.com'`) to open a link in a new tab.
       - Example:
         ```javascript
         button1: {
             enabled: true,
             text: 'Learn More',
             function: 'https://example.com'
         }
         ```
     - **Button 2**:
       - Same options as Button 1.
       - Example:
         ```javascript
         button2: {
             enabled: false,
             text: 'Discord',
             function: 'https://discord.com/invite/bm2bcwZWkj'
         }
         ```
4. **Save and Test**:
   - Save `index.html` and open it in a browser to see the updated alert.

## Available Colors
The alert system supports the following colors, each with a matching border, header, and button gradient:
- `Red`: Bright red theme.
- `Blue`: Vibrant blue theme.
- `Green`: Fresh green theme.
- `Purple`: Deep purple theme.
- `Pink`: Soft pink theme.
- `Yellow`: Sunny yellow theme.
- `Orange`: Warm orange theme.
- `Grey`: Neutral grey theme.

If an invalid color is specified, the alert defaults to `Green`.
