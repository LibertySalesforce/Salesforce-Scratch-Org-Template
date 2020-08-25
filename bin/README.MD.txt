Store various PC and Mac scripts to streamline the scratch org process.
These will be the commands run by the non technical teams. 

The following is an example of a PC .bat file.

call sfdx force:org:create -s -f config\project-scratch-def.json -a ScratchOrg
call sfdx toolbox:package:dependencies:install -w 60
call sfdx force:apex:execute -f scripts\PermissionSetLicenseAssignment.apex
call sfdx force:apex:execute -f scripts\PermissionSetAssignment.apex
call sfdx force:source:push
call sfdx force:apex:execute -f scripts\CreateCareProgram.apex
call sfdx force:apex:execute -f scripts\UpdateCustomMetadataTypes.apex


The same script for Mac users:

sfdx force:org:create -s -f config/project-scratch-def.json -a ScratchOrg
sfdx toolbox:package:dependencies:install -w 60
sfdx force:apex:execute -f scripts/PermissionSetLicenseAssignment.apex
sfdx force:apex:execute -f scripts/PermissionSetAssignment.apex
sfdx force:source:push
sfdx force:apex:execute -f scripts/CreateCareProgram.apex
sfdx force:apex:execute -f scripts/UpdateCustomMetadataTypes.apex
