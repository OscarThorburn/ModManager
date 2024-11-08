# ModManager
Got tired of moving around mod files for different games and handling load orders etc. Building my own mod manaqger for the games I play and mod. 



MVP Features

    Basic Multi-Game Mod Management
        Add Game Profiles: Allow users to add supported games (Total War, Darktide, etc.), specifying a directory path where mods are located.
        Mod Detection: Automatically scan the specified mod directory for each game to detect installed mods. Store basic metadata (mod name, file path).
        Enable/Disable Mods: Let users toggle mods on or off for each game profile. Changes should be reflected in the local mod directory (e.g., renaming mod files or moving them to an "inactive" folder).

    Load Order Management
        Manual Load Order Adjustment: Allow users to manually adjust the order of mods for each game and save their configuration.
        Automatic Load Order Optimization: Add an algorithm that automatically suggests an optimal load order based on dependencies and past user settings.
        Dependency Mapping: Implement a basic dependency system where users can specify that certain mods should load before others. This can be simple text-based input for MVP.
        Conflict Detection: Basic detection of conflicts, where two mods may modify the same files or be mutually exclusive. For MVP, this can be limited to flagging duplicate filenames.

    Local Data Storage
        Save Configurations Locally: Use LiteDB or SQLite to save user configurations, mod load orders, and dependencies. This enables persistence across sessions.

    Simple User Interface
        Basic Frontend with Blazor or WPF: Provide a minimal UI to add games, manage mods, adjust load orders, and display detected conflicts.
        Settings Screen: A basic screen for adjusting paths and saving preferences per game.


Nice To have / Future PLans

    Integrate with Steam’s API to pull information about mods directly from the Steam Workshop for each game and enable updates.
    Track versions of each mod and allow users to roll back to previous configurations if needed.
    Implement a graph-based visualization of dependencies, using a graph library to display mod relationships visually.
    Allow users to create custom rules or scripts to control load order adjustments.
