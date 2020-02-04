<#
.SYNOPSIS
    Azure Automation RBAC workspace.
.DESCRIPTION
    A workspace is example code for performing common tasks.
    It is meant to demonstrate how to perform an operation or change.
.EXAMPLE
    
.INPUTS

.OUTPUTS

.NOTES

#>

Login-AzAccount

$grantee = '' # The user who you are applying the RBAC to.

$sId = 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX' # Azure Subscription Id
$rGn = '' # Azure Resource Group Name
$aAn = '' # Azure Automation Account Name
$rBn = '' # Azure Automation Account Runbook Name


# The Automation Runbook Operator role allows you to **view** a runbook’s name and properties.
New-AzRoleAssignment `
                    -SignInName $grantee `
                    -Scope "/subscriptions/$sId/resourcegroups/$rGn/Providers/Microsoft.Automation/automationAccounts/$aAn/runbooks/$rBn" `
                    -RoleDefinitionName 'Automation Runbook Operator'

# The Automation Job Operator role allows you to create and manage jobs for all runbooks in an Automation account.
New-AzRoleAssignment `
                    -SignInName $grantee `
                    -scope "/subscriptions/$sId/resourcegroups/$rGn/Providers/Microsoft.Automation/automationAccounts/$aAn" `
                    -RoleDefinitionName 'Automation Job Operator'

# The Contributor role allows you to manage the runbook and edit the associated script.
New-AzRoleAssignment `
                    -SignInName $grantee `
                    -Scope "/subscriptions/$sId/resourcegroups/$rGn/Providers/Microsoft.Automation/automationAccounts/$aAn/runbooks/$rBn" `
                    -RoleDefinitionName 'Contributor'
