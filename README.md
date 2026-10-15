# GW2 WvW Squad Builder

A lightweight, browser-based squad composition tool for **World vs. World (WvW)** in [Guild Wars 2](https://www.guildwars2.com/).

WvW Squad Builder helps commanders organize squad compositions, assign professions and elite specializations to players, track group roles, and share the final composition on Discord.

Built with HTML, CSS, and vanilla JavaScript, it runs directly in your browser without requiring a backend or installation.

## Features

### Squad Composition Management

- **Drag-and-drop interface** to assign professions and elite specializations to squad slots.
- **Preconfigured groups:** four groups are created automatically when the application starts.
- **Add or remove groups** to adjust the squad size.
- **Reset compositions** to clear all assigned players while keeping the group structure.
- **Player names:** optionally associate an in-game name with each assigned profession.
- **Customizable group roles:** configure the number of Support, Healer, Boon, and DPS slots per group.
- **Role-based slot layout:** automatically rebuild the group structure when applying a custom role distribution.

### Profession and Role Filtering

Browse available professions and elite specializations, and filter them by role:

- **Support**
- **Healer**
- **Boon**
- **DPS**
- **All professions**

The profession list includes the supported core professions and elite specializations defined in the application, with their corresponding icons and role assignments.

### Squad Statistics

Get an overview of the current composition with automatically updated statistics:

- Total number of assigned players.
- Number of Support players.
- Number of Healer players.
- Combined DPS and Boon player count.
- Player distribution by profession or elite specialization.

Statistics update when professions are assigned, groups are modified, or player names and compositions are changed.

### JSON Import and Export

Save your squad composition locally and restore it later.

**Export**
- Download the current composition as a JSON file.
- Preserve group compositions and assigned professions.
- Include player names when at least one name has been entered.
- Save the custom role configuration.

**Import**
- Load a previously exported JSON composition.
- Restore assigned professions, player names, and custom role configuration.
- Maintain compatibility with older JSON files that do not contain player names.
- Validate the basic file structure and report invalid imports.

No server-side storage is required: composition files are handled locally in the browser.

### Discord Export

Share your squad composition with your community using the built-in Discord export.

- Generate a formatted text representation of the squad.
- Organize the output by group.
- Display profession-specific Discord emoji codes.
- Include player names in bold when provided.
- Skip empty slots.
- Copy the generated message directly to the clipboard.

The generated text can then be pasted into a Discord channel to share the squad lineup.

> **Note:** Profession emoji codes must correspond to custom emoji available on your Discord server for the icons to render as intended.

### Light and Dark Themes

- Toggle between light and dark mode.
- Automatically apply the previously selected theme on subsequent visits.
- Store the theme preference locally in the browser.

## Getting Started

### Requirements

- A modern web browser.
- An internet connection to load profession icons from the Guild Wars 2 Wiki.
- Clipboard access for the Discord export feature.

No build tools, package manager, server, or additional dependencies are required.

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/Talos51/GW2-SquadBuilder.git
   ```

2. Navigate to the project directory:

   ```bash
   cd GW2-SquadBuilder
   ```

3. Open the HTML entry point in your browser.

Alternatively, use my GitHub Pages hosting the application as a static website : https://talos51.github.io/GW2-SquadBuilder/

## How to Use

1. Open the application. Four groups are created by default.
2. Select a role filter to narrow down the available professions.
3. Drag a profession or elite specialization into an available slot.
4. Enter the player's in-game name if needed.
5. Add or remove groups to adjust the squad structure.
6. Customize the number of slots for each role and apply the configuration when necessary.
7. Review the squad statistics to verify the composition.
8. Export the composition to JSON for later use, or copy the formatted output for Discord.

## Technology Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Application structure |
| CSS3 | Layout, styling, and themes |
| Vanilla JavaScript | Composition management and application logic |
| Browser APIs | Drag and drop, file import/export, local storage, and clipboard access |
| Guild Wars 2 Wiki | Profession and specialization icons |

The application is designed to remain lightweight and easy to deploy, with no framework or external JavaScript library required.

## Project Structure

The application is currently implemented as a self-contained HTML file.

```text
.
└── index.html    # Application markup, styles, and JavaScript
```

## Limitations

- Profession availability and role assignments are defined directly in the source code.
- Role assignments are intended as composition-planning categories; they do not validate actual in-game builds or skill configurations.
- JSON compositions are stored locally through file downloads and imports rather than a shared online database.
- Profession icons require access to the Guild Wars 2 Wiki.
- Discord export copies formatted text and emoji codes; it does not publish messages directly to Discord.
- The application does not synchronize compositions between users.

## Contributing

Contributions, bug reports, and feature suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a pull request describing the proposed changes.

For significant changes, consider opening an issue first to discuss the implementation.

## License

This project is licensed under the **MIT License**.

You are free to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to the conditions of the MIT License.

See the [LICENSE](LICENSE) file for the full license text.

## Acknowledgements

- [Guild Wars 2](https://www.guildwars2.com/) for the game and profession system.
- [Guild Wars 2 Wiki](https://wiki.guildwars2.com/wiki/Guild_Wars_2_Wiki:Profession_icons) for profession and specialization icons.
- The Guild Wars 2 WvW community for the inspiration behind squad composition planning.

---

**Developed by Talos (Talos.1875)**

WvW Squad Builder is an unofficial community project and is not affiliated with or endorsed by ArenaNet or NCSOFT. Guild Wars 2 and its associated assets are the property of their respective owners.
