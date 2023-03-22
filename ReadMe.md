Deploying Automation Documents via CLI

aws ssm create-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-type "Automation" --document-format JSON

Updating Via CLI

PS > aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version "`$LATEST"
CMD >  aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version "$LATEST"
MACOS >  aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version '$LATEST'