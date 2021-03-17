# Sample Project with Multiple Package Directories

This is a simple Salesforce project that illustrates multiple package development on a Salesforce Standard Object and Custom Object. You can read more information about multiple package development [here](https://github.com/forcedotcom/cli/issues/379).

To try it out, clone this repository and run a source:push. You will notice it does two deployments and the results are successful.

```
-> sfdx force:org:create -f config/project-scratch-def.json -a mpd -s
Successfully created scratch org: 00D9A00000055KKUAY, username: test-1tnl3nobqwrn@example.com

-> sfdx force:source:push
Job ID | 0Af9A00000K31TWSAZ
SOURCE PROGRESS | ████████████████████████████████████████ | 3/3 Files
Job ID | 0Af9A00000K31TgSAJ
SOURCE PROGRESS | ████████████████████████████████████████ | 2/2 Files
=== Pushed Source
STATE  FULL NAME        TYPE          PROJECT PATH
─────  ───────────────  ────────────  ────────────────────────────────────────────────────────────────────
Add    force            ApexClass     force-app/main/default/apex/force.cls
Add    force            ApexClass     force-app/main/default/apex/force.cls-meta.xml
Add    MyObj__c         CustomObject  force-app/main/default/objects/MyObj__c/MyObj__c.object-meta.xml
Add    Account.asdf__c  CustomField   force-app/main/default/objects/Account/fields/asdf__c.field-meta.xml
Add    my               ApexClass     my-app/apex/my.cls
Add    my               ApexClass     my-app/apex/my.cls-meta.xml
Add    Case.myfield__c  CustomField   my-app/objects/Case/fields/myfield__c.field-meta.xml
```
