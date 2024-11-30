# Cheat Script

An executable script that integrates with [cheat.sh](https://cheat.sh) to fetch command-line cheat sheets and open them in `nvim` for easy browsing, editing, and copying.

## Features

- Fetches cheat sheet data for any command from [cheat.sh](https://cheat.sh).
- Removes unnecessary ANSI escape codes for a clean output.
- Opens the cheat sheet in `nvim`, allowing seamless editing, searching, and copying.
- Temporary files are automatically cleaned up after use.

## Prerequisites

- `curl`: For fetching data from cheat.sh.
- `nvim`: The script uses `nvim` to open the fetched cheat sheets. Ensure it is installed and available in your PATH.

## Installation

### Clone the Repository

```bash
git clone https://github.com/leonti98/cheat $HOME/cheat
```

### Install the Script

#### Global Installation

```bash
sudo mv $HOME/cheat/cheat /usr/local/bin/
```

### OR

#### Local Installation

```bash
mv $HOME/cheat/cheat $HOME/.local/bin
```

Ensure `$HOME/.local/bin` is in your `PATH` by adding this to your shell configuration file (`~/.bashrc`, `~/.zshrc`, etc.):

```bash
export PATH=$HOME/.local/bin:$PATH
```

## Usage

```bash
cheat <command>
```

- Replace `<command>` with the name of the command you want to look up.
- Example:

```bash
  cheat ls
```

## How It Works

1.  The script checks if a command is provided. If not, it displays usage instructions.
2.  It fetches the cheat sheet for the given command from [cheat.sh](https://cheat.sh).
3.  Strips out any ANSI escape codes for better readability.
4.  Opens the cheat sheet in `nvim`.
5.  Deletes the temporary file after closing `nvim`.

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

---

Let me know if you'd like further tweaks or additions!
