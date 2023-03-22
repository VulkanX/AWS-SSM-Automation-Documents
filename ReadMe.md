Deploying Automation Documents via CLI

aws ssm create-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-type "Automation" --document-format JSON

Updating Via CLI

PS > aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version "`$LATEST"
CMD >  aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version "$LATEST"
MACOS >  aws ssm update-document --content file://AWS-UpgradeWindows-RootVol-Backup.json --name "WindowsOSUpgrade" --document-version '$LATEST'

The update command will return some json with a property of "LatestVersion"
to Update the default version of your document run the following

aws ssm update-document-default-version --name "WindowsOSUpgrade" --document-version "3"