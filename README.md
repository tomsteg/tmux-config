# tmux Konfiguration

Prefix: `Ctrl+s`

## Setup auf neuem Rechner

### 1. Repository klonen

```bash
git clone git@github.com:tomsteg/tmux-config.git ~/.config/tmux
```

### 2. tmux.conf verlinken

tmux liest standardmäßig `~/.tmux.conf`. Diese Datei muss auf die Config in `~/.config/tmux/` verweisen:

```bash
cat > ~/.tmux.conf << 'EOF'
unbind r
bind r source-file ~/.config/tmux/tmux.conf

source-file ~/.config/tmux/tmux.conf
EOF
```

### 3. TPM (Plugin Manager) installieren

```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

### 4. Plugins installieren

tmux starten, dann:

```
Ctrl+s I
```

(großes I) – installiert alle Plugins aus der `tmux.conf`.

### Verwendete Plugins

- **[tmux-power](https://github.com/wfxr/tmux-power)** – Statusleiste, Theme: `everforest`

---

## Pane-Navigation

| Taste | Aktion |
|-------|--------|
| `Ctrl+s h` | Pane links |
| `Ctrl+s j` | Pane unten |
| `Ctrl+s k` | Pane oben |
| `Ctrl+s l` | Pane rechts |

## Copy-Mode

| Taste | Aktion |
|-------|--------|
| `Ctrl+s [` | Copy-Mode aktivieren |
| `j / k` | Zeile runter / hoch |
| `Ctrl+d / Ctrl+u` | Halbe Seite runter / hoch |
| `g / G` | Anfang / Ende des Scrollbacks |
| `v` | Selektion starten |
| `w / b` | Wort vor / zurück |
| `y` | Kopieren ins macOS-Clipboard |
| `q` | Copy-Mode beenden |

Einfügen: `Cmd+V` (macOS-Clipboard)

## Sonstiges

| Taste | Aktion |
|-------|--------|
| `Ctrl+s r` | Konfiguration neu laden |
| `Ctrl+s I` | Plugins installieren (TPM) |
| `Ctrl+s U` | Plugins updaten (TPM) |
