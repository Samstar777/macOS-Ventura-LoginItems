# macOS-Ventura-LoginItems

Sample Configuration Profile XML
Note: all items are evaluated against all RuleTypes and when matched it will be locked in the UI and automatically approved. Rule types to consider:
• BundleIdentifier
• The bundle identifier of the app to match, which must be an exact match.
• BundleIdentifierPrefix
• The prefix of the bundle identifier of the app to match.
• Label
• The value of the launchd plist Label parameter to match, which must be an exact match.
• LabelPrefix
• The prefix of the launchd plist Label parameter to match.
• TeamIdentifier
• The team identifier from the code signing attributes, which must be an exact match. Edit the XML below to identify Background and Login Items you plan to manage:
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/
DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
     <key>PayloadContent</key>
     <array>
           <dict>
                <key>PayloadDescription</key>
                <string>Test Payload for Background Item Management</string>
                <key>PayloadDisplayName</key>
                <string>Background Item Management Test</string>
                <key>PayloadIdentifier</key>
                <string>com.example.56EE8C1E-9C20-483B-
                AD0E-9558E6091035.privacy.04102481-C1F1-44F2-B548-
                E0B554890493</string>
                <key>PayloadUUID</key>
                <string>A9BF8FA9-CEA3-42A2-B8C1-E1998B84CBB0</string>
                <key>PayloadType</key>
Login and Background Item Management September 2022
 <string>com.apple.servicemanagement</string>
<key>PayloadOrganization</key>
<string>Example Org</string>
<key>Rules</key>
<array>
     <dict>
           <key>RuleType</key>
           <string>BundleIdentifier</string>
           <key>RuleValue</key>
           <string>com.example.bundle.identifier</string>
           <key>Comment</key>
           <string>Example bundle identifier</string>
     </dict>
     <dict>
           <key>RuleType</key>
           <string>BundleIdentifierPrefix</string>
           <key>RuleValue</key>
           <string>com.example</string>
           <key>Comment</key>
           <string>Example bundle identifier prefix</string>
     </dict>
     <dict>
           <key>RuleType</key>
           <string>Label</string>
           <key>RuleValue</key>
           <string>com.example.label</string>
           <key>Comment</key>
           <string>Example label</string>
     </dict>
     <dict>
           <key>RuleType</key>
           <string>LabelPrefix</string>
           <key>RuleValue</key>
           <string>com.example</string>
           <key>Comment</key>
           <string>Example label prefix</string>
     </dict>
     <dict>
Login and Background Item Management September 2022

<key>RuleType</key>
                           <string>TeamIdentifier</string>
                           <key>RuleValue</key>
                           <string>TeamID</string>
                           <key>Comment</key>
                           <string>Example Team ID</string>
                      </dict>
                </array>
           </dict>
     </array>
     <key>PayloadDisplayName</key>
     <string>Background Service Configuration Profile</string>
     <key>PayloadIdentifier</key>
     <string>com.apple.servicemanagement.4DB96276-2310-44C2-AE11-
     C6E761FB0304.privacy</string>
     <key>PayloadUUID</key>
     <string>79E2E390-641B-41FC-B11D-9DF6CAC71EE8</string>
     <key>PayloadType</key>
     <string>Configuration</string>
     <key>PayloadScope</key>
     <string>System</string>
</dict>
</plist>
