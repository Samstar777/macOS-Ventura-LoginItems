# macOS-Ventura-LoginItems

Sample Code.plist
Note: all items are evaluated against all RuleTypes and when matched it will be locked in the UI and automatically approved. Rule types to consider:
- BundleIdentifier
     - The bundle identifier of the app to match, which must be an exact match.
- BundleIdentifierPrefix
     - The prefix of the bundle identifier of the app to match.
- Label
     - The value of the launchd plist Label parameter to match, which must be an exact match.
- LabelPrefix
     - The prefix of the launchd plist Label parameter to match.
- TeamIdentifier
     - The team identifier from the code signing attributes, which must be an exact match.

**Attachment**
- sample code.plist
- Sample System Managed Login Items mobileconfig for reference
