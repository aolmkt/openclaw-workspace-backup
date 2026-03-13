# OpenClaw Workspace Backup

Backup diário de `/root/.openclaw/workspace` versionado no GitHub.

## Restore em outra máquina/VPS

```bash
git clone git@github.com:aolmkt/openclaw-workspace-backup.git /tmp/openclaw-workspace-backup
sudo mkdir -p /root/.openclaw/workspace
sudo rsync -av --delete /tmp/openclaw-workspace-backup/ /root/.openclaw/workspace/ --exclude ".git"
openclaw status
