

<p align="center">
<img src="https://i.imgur.com/SpP6fsr.png" alt="honeypot logo"/>
</p>

<h1>Cowrie - SSH Honeypot Threat Simulation &amp; Log Analysis </h1>
  <p>
Deployed and configured Cowrie, a medium-interaction honeypot, on a Linux environment using a Chromebook terminal. Simulated brute-force SSH attacks and analyzed attacker behavior through JSON logs. Used fake login attempts and command execution to capture realistic threat data.
  </p>

<h2>Enviroments and Technologies Used</h2>

- Linux (Crostini on Chromebook)
- Python virtual environments
- Cowrie honeypot
- SSH, Bash, sshpass
- Log analysis with shell tools (cat, tail, grep,jq)

<h2>Installing a Basic Cowrie Honeypot on Chromebook</h2>
<h3>Step 1: Simple Terminal Config</h3>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/fJjQzvI.png" alt="screenshot"/>
    </td>
    <td>
      <img src="https://i.imgur.com/ov4a8q1.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<p>
  1. Go to settings > Advanced > Developers > Linux Development Environment.
  2. Click "Turn On" and be sure to allocate at least 10GB of storage to Linux.
</p>
<br>
<h3>Step 2: Update Linux</h3>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/KUOiw3u.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<p>
  Once you have the terminal open, type in the command "sudo apt update && sudo apt upgrade -y". This command is made up of two parts, joined by && (which means "run the second command only if the first one succeeds)
</p>
  <strong>sudo apt update</strong>
  
  - sudo: Runs the command with admin privileges.
  - apt: This is the package manager.
  - update: Tells your system to refresh the list of available software packages from the internet 
  <p>This line is pretty much saying "Check for the latest avaliable versions of softeare, but don't install them yet"</p>
  <strong>sudo apt upgrade -y</strong>

  - upgrade: Installs the newest versions of all the software packages on your system that have update available
  - -y: Automatically answers "yes" to any prompts (so you don't have to manually confirm each update)
  <p>This is part of the command is saying "Now install the latest versions of everything that has updates, and don't ask me to confirm each one"</p>
  <h3>Step 3: Install Dependencies for Cowrie</h3>
  <table>
    <tr>
      <td>
        <img src="https://i.imgur.com/aqnrfa6.png" alt="screenshot"/>
      </td>
    </tr>
  </table>
<p>
  We will once again use the "sudo apt install" command because we will be installing  multiple software packages needed for Cowrie.
</p>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/8Dz5x4i.png" alt="screenshot"/>
    </td>
    <td>
      <img src="https://i.imgur.com/SjJ2kMb.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<p>To type out all the descriptions for each of the packages would be a lot of text, so here is the list of all the packages that are within the command and what they do</p>
<h3>Step 4: Clone and Set Up Crowrie</h3>
<p>This part will be a little extensive, not too much, but it has a few steps within it, so let's get to it.</p>
<strong>1. Clone the Cowrie honeypot code from GitHub</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/hnF35z7.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<strong>2. Go into the Cowrie folder</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/Hk999PO.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<strong>3. Create a Python virtual environment named "cowrie-env"</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/EeMept9.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<strong>4. Activate the virtual environment</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/f4fFQ9p.png" alt="screenshot"/>
    </td>
  </tr>
  <p>(You'll know it's active if you see something like (cowrie-env) at the beginning of your terminal prompt.)</p>
</table>
<strong>5. Upgrade pip (Python's package installer)</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/tLbfTXa.png" alt="screenshot"/>
    </td>
  </tr>
</table>
<strong>6. Install Cowrie's required Python libraries</strong>
<table>
  <tr>
    <td>
      <img src="https://i.imgur.com/M0ycOvX.png" alt="screenshot"/>
    </td>
  </tr>
</table>
