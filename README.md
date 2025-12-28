# Poker Tournament Timer

A full-featured, single-file HTML poker tournament timer with a dark casino theme. No installation required - just open in any browser.

## Features

### Timer Display
- Large countdown timer with color-coded warnings (yellow at 60s, red at 10s)
- Current blind level with small blind / big blind / ante display
- Next level preview
- Presentation mode for TV/projector display
- Fullscreen support

### Sound Alerts
- Level change chime
- Break announcement
- Warning beeps at 60s and 30s
- Countdown beeps for last 5 seconds
- Mute/unmute toggle

### Tournament Management
- **Player Tracking**: Track players remaining with +/- buttons
- **Table Calculation**: Automatic table count based on players per table setting
- **Rebuy Tracking**: Track rebuys with automatic prize pool updates
- **Hand-for-Hand Mode**: Toggle for bubble play situations
- **Bubble Mode**: Visual indicator when on the bubble
- **Random Seat Assignment**: Generate random table/seat assignments

### Blind Structure
- Fully editable blind levels (Small Blind, Big Blind, Ante)
- Individual duration per level
- Add/remove levels and breaks
- Click any level to jump to it

### Built-in Presets
| Preset | Level Duration | Description |
|--------|---------------|-------------|
| Turbo | 10 min | Fast-paced tournament |
| Standard | 20 min | Traditional home game |
| Deep Stack | 30 min | More play, slower blinds |
| Super Turbo | 5 min | Very fast action |
| Shootout | 15 min | No antes structure |
| Bounty | 15 min | Knockout format |

### Import/Export
- Export structure as JSON file
- Import custom structures
- Save tournaments locally for reuse

### Statistics Display
- Total elapsed time
- Average stack in big blinds
- M-Ratio calculation
- Levels remaining
- Chip values legend
- Prize pool with customizable payouts

### Settings
| Setting | Description |
|---------|-------------|
| Tournament Name | Custom name for your event |
| Level Duration | Default time per level |
| Starting Chips | Initial stack size |
| Starting Players | Number of entrants |
| Buy-in Amount | Entry fee for prize pool |
| Rebuy Amount | Cost per rebuy |
| Players Per Table | Seats per table (2-10) |
| Rebuy End Level | When rebuy period closes |
| Warning Time | When timer turns yellow |
| Danger Time | When timer turns red |
| Payout Structure | 1st/2nd/3rd place percentages |

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play/Pause timer |
| `←` | Previous level |
| `→` | Next level |
| `R` | Reset current level |
| `F` | Toggle fullscreen |
| `P` | Toggle presentation mode |
| `M` | Mute/unmute sounds |
| `H` | Toggle hand-for-hand |
| `B` | Toggle bubble mode |
| `+` | Add 1 minute |
| `-` | Remove 1 minute |
| `1-9` | Jump to level 1-9 |
| `Esc` | Exit presentation/close modals |

## Usage

1. Open `poker_timer.html` in any modern browser
2. Select a preset or customize the blind structure
3. Set your tournament parameters (players, buy-in, etc.)
4. Press START or hit Space to begin

## Data Persistence

- Timer state is automatically saved to browser localStorage
- Resumes from where you left off if you close/reopen
- Save custom tournaments for future use

## Browser Compatibility

Works in all modern browsers:
- Chrome
- Firefox
- Safari
- Edge

## License

Free to use for personal and commercial purposes.
