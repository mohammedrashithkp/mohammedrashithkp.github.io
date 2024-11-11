<p align="center" style="font-size: 25px; text-decoration: none">
  <a href="/index">Home</a> |
  <a href="/blogs/index">Blogs</a> 
</p>

# Setting Up Kitty and Yazi in Ubuntu

Kitty and Yazi are two powerful tools for making your terminal experience in Ubuntu more efficient and visually appealing. This guide will walk you through installing and setting them up.

## What You'll Need

Before you begin, ensure that you have the following:

- A working installation of **Ubuntu** (this guide assumes Ubuntu 20.04 or newer)
- A terminal to execute commands

## Step 1: Install Kitty

**Kitty** is a GPU-based terminal emulator that’s fast and highly customizable. To install it on Ubuntu:

1. **Update your package list**:
   Open the terminal and run:
   ```bash
   sudo apt update
   ```

2. **Install Kitty**:
   Kitty is available in the Ubuntu repositories, so you can install it easily with `apt`:
   ```bash
   sudo apt install kitty
   ```

3. **Launch Kitty**:
   Once the installation is complete, you can open Kitty by simply typing:
   ```bash
   kitty
   ```

   You should see the Kitty terminal window open up.

### Optional: Set Kitty as Default Terminal
If you want to set Kitty as your default terminal, follow these steps:

1. Open the **Settings** application in Ubuntu.
2. Go to **Details** > **Default Applications**.
3. Under **Terminal**, choose **Kitty** from the dropdown list.

Alternatively, you can set Kitty as your default terminal by running the following command:
```bash
sudo update-alternatives --config x-terminal-emulator
```
Then select **Kitty** from the list.

## Step 2: Install Yazi

**Yazi** is a dynamic, customizable prompt system for the terminal that enhances your terminal’s prompt with useful information (e.g., system status, git status, etc.). To install Yazi on Ubuntu:

1. **Install dependencies**:
   Yazi requires a few tools, including **git** and **curl**. Make sure they are installed first:
   ```bash
   sudo apt install git curl
   ```

2. **Clone the Yazi repository**:
   Run the following command to clone Yazi from GitHub:
   ```bash
   git clone https://github.com/TebbaaX/yazi.git
   ```

3. **Install Yazi**:
   Navigate to the cloned `yazi` directory:
   ```bash
   cd yazi
   ```

   Run the installation script:
   ```bash
   ./install.sh
   ```

4. **Set up Yazi**:
   Once Yazi is installed, you’ll need to add it to your shell configuration file (e.g., `.bashrc`, `.zshrc`, or `.bash_profile`):

   - For **Bash** users, add the following line to the end of your `~/.bashrc` file:
     ```bash
     source ~/yazi/.yazi_prompt
     ```

   - For **Zsh** users, add the following to your `~/.zshrc` file:
     ```bash
     source ~/yazi/.yazi_prompt
     ```

   After adding the line, reload the shell configuration by running:
   ```bash
   source ~/.bashrc  # for Bash users
   # or
   source ~/.zshrc   # for Zsh users
   ```

## Step 3: Customizing Yazi

Yazi comes with some pre-configured styles, but you can easily customize the prompt to fit your needs.

1. Open the `~/.yazi` directory (or the directory where you cloned Yazi).
2. Edit the `config` file to change how your prompt looks:
   ```bash
   nano ~/.yazi/config
   ```

   You can modify the prompt's colors, display system information (like CPU usage or disk space), and configure how Git information is shown in the prompt.

3. **Test your changes**:
   After saving the changes, open a new terminal window, and you should see the updated prompt.

## Step 4: Enjoy Your New Terminal Setup

Now, you should have:

- **Kitty** as your fast and feature-rich terminal emulator.
- **Yazi** as a dynamic prompt that enhances your terminal experience.

### Some Useful Kitty Customizations

If you want to go beyond the basics, Kitty offers plenty of customization options in its configuration file (`~/.config/kitty/kitty.conf`), such as:

- Font and theme adjustments
- Window layouts
- Color schemes

You can find a list of configuration options in the [Kitty Documentation](https://sw.kovidgoyal.net/kitty/conf/).

---

With **Kitty** and **Yazi**, you'll have a powerful and visually appealing terminal setup that is both efficient and customizable. Enjoy your enhanced Ubuntu terminal experience!
