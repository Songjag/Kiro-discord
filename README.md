# Discord Presence for Kiro

> Update your Discord status with a rich presence — customized for **Kiro IDE**.

<div align="center">
	<p>
		<a href="https://github.com/Songjag/Kiro-discord">
			<img alt="GitHub Stars" src="https://img.shields.io/github/stars/Songjag/Kiro-discord?style=social">
		</a>
		<a href="https://github.com/Songjag/Kiro-discord/releases">
			<img alt="GitHub Release" src="https://img.shields.io/github/v/release/Songjag/Kiro-discord">
		</a>
	</p>
</div>

## What's Different?

This is a **Edited version for Kiro IDE** of the original [Discord Presence by iCrawl](https://github.com/iCrawl/discord-vscode), with the following modifications:

- ✅ **Kiro IDE branding** — Shows "Kiro" instead of "Visual Studio Code" on Discord
- ✅ **Custom Discord Application** — Uses dedicated Discord App with Kiro icon
- ✅ **No command conflicts** — Commands prefixed with `discord-kiro.*` to avoid conflicts with original extension
- ✅ **Optimized for Kiro** — Tested and working on Kiro IDE environment

## Features

- Shows what you are editing in Kiro IDE
- Support for over 200+ of the most popular languages
- Enable/Disable Rich Presence for individual workspaces (enabled by default)
- Custom string support
- Debug mode detection
- Easily manually reconnect to Discord
- Git repository detection and "View Repository" button

## Installation

### From .vsix file (recommended)

1. Download the latest `.vsix` file from [Releases](https://github.com/Songjag/Kiro-discord/releases)
2. Open Kiro IDE
3. Go to Extensions (`Ctrl+Shift+X`)
4. Click `...` → `Install from VSIX...`
5. Select the downloaded `.vsix` file
6. Reload window

### Build from source

**Requirements:**

- Node.js v20+ (tested on v26.2.0)
- pnpm v10+ (tested on v10.8.0)

```bash
# Clone the repository
git clone https://github.com/Songjag/Kiro-discord.git
cd Kiro-discord

# Install dependencies
pnpm install

# Build
node esbuild.mjs --production

# Package
pnpm exec vsce package --no-dependencies

# Install the generated .vsix file in Kiro
```

## Troubleshooting

**Windows:** Do not run your Kiro IDE or Discord as admin, there is no reason to and it just further complicates everything down the line.

**Linux:** Discord versions installed using `flatpak` or `snap` need modifications in order to support IPC. In order to avoid this (and as Discord itself suggests) you should download it from [discord.com](https://discord.com/download)

**Extension not working?**

1. Make sure Discord is running before starting Kiro
2. Check **Output → Discord Presence** for error messages
3. Try the reconnect command: `Ctrl+Shift+P` → "Reconnect Discord Presence to Discord"
4. If you have the original `discord-vscode` extension installed, uninstall it to avoid conflicts

**Node.js v26 compatibility:**  
This version includes patches for Node.js v26 compatibility (fixed `SlowBuffer` deprecation issues in dependencies). If you encounter build errors on older Node versions, consider upgrading to Node.js v20 LTS or later.

References:  
https://github.com/flathub/com.discordapp.Discord/issues/29  
https://github.com/iCrawl/discord-vscode/issues/77#issuecomment-435622205  
https://github.com/iCrawl/discord-vscode/issues/85#issuecomment-417895483

## Contributing

1. [Fork the repository](https://github.com/Songjag/Kiro-discord/fork)!
2. Clone your fork: `git clone https://github.com/Songjag/Kiro-discord.git`
3. Create your feature branch: `git checkout -b my-new-feature`
4. Commit your changes: `git commit -am 'Add some feature'`
5. Push to the branch: `git push origin my-new-feature`
6. Submit a pull request :D

## Credits

**Discord Presence for Kiro** © [songjag](https://github.com/songjag)  
Forked and maintained by songjag for Kiro IDE.

**Original Discord Presence** © [iCrawl](https://github.com/iCrawl)  
Created and maintained by iCrawl.

> **Kiro version:** GitHub [@songjag](https://github.com/songjag)  
> **Original:** GitHub [@iCrawl](https://github.com/iCrawl)

## License

MIT License - see [LICENSE](LICENSE) for details.

---

_Based on [discord-vscode](https://github.com/iCrawl/discord-vscode) by iCrawl_
