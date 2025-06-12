⚡ Lightning Node Project Summary
✅ Goal:
Run a Bitcoin + Lightning Network node on SBC hardware (currently LeefBox with Armbian) to potentially earn routing fees and learn the Lightning ecosystem.

🖥️ Current Setup:
Component	Status
Hardware	LeefBox (RK322x-based), Armbian
Bitcoin Core	✅ Compiled (v26.0), syncing blockchain (pruned mode, last ~30 days)
Core Lightning (CLN)	✅ Compiled (v25.02.2), running, connected to Bitcoin Core
Configurations	Matching rpcuser / rpcpassword ✔
Logs	Bitcoin: ~/.bitcoin/debug.log
CLN: Custom log file via --log-file
Backup Plan	NAND backup planned before hardware transfer to M9S Pro

⚙️ Next Planned Steps:
Finish Bitcoin Core sync

Generate Bitcoin address for funding Lightning wallet

Connect to peers

Open Lightning channels

Begin routing transactions → potential to earn fees over time

Monitor node performance and possibly advertise node for routing traffic

📝 Optional Future Enhancements:
Migrate setup to M9S Pro (with NAND backup/fallback plan)

Automate with systemd services for autostart

Set up external backups for wallet data

Add Tor for privacy

Use Amboss or 1ML to list node publicly if desired

