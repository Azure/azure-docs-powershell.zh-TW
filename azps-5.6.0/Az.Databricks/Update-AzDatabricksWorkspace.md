---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 10a3a4d77cd6156bc2d6abe64a60773582ec50b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904469"
---
# <span data-ttu-id="76a57-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="76a57-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="76a57-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76a57-102">SYNOPSIS</span></span>
<span data-ttu-id="76a57-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="76a57-103">Updates a workspace.</span></span>

## <span data-ttu-id="76a57-104">語法</span><span class="sxs-lookup"><span data-stu-id="76a57-104">SYNTAX</span></span>

### <span data-ttu-id="76a57-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="76a57-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76a57-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76a57-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="76a57-107">描述</span><span class="sxs-lookup"><span data-stu-id="76a57-107">DESCRIPTION</span></span>
<span data-ttu-id="76a57-108">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="76a57-108">Updates a workspace.</span></span>

## <span data-ttu-id="76a57-109">例子</span><span class="sxs-lookup"><span data-stu-id="76a57-109">EXAMPLES</span></span>

### <span data-ttu-id="76a57-110">範例 1：更新 Datab位工作區的標記</span><span class="sxs-lookup"><span data-stu-id="76a57-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="76a57-111">此命令會更新 Datab一s 工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="76a57-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="76a57-112">範例 2：在 Datab一s 工作區上啟用加密</span><span class="sxs-lookup"><span data-stu-id="76a57-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="76a57-113">在 Datab一s 工作區上啟用加密需要三個步驟：</span><span class="sxs-lookup"><span data-stu-id="76a57-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="76a57-114">如果工作區尚未 `-PrepareEncryption` (，請更新) 。</span><span class="sxs-lookup"><span data-stu-id="76a57-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="76a57-115">尋找 `StorageAccountIdentityPrincipalId` 最後一個步驟的輸出。</span><span class="sxs-lookup"><span data-stu-id="76a57-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="76a57-116">將金鑰許可權授予主體。</span><span class="sxs-lookup"><span data-stu-id="76a57-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="76a57-117">再次更新工作區以填入有關加密金鑰的資訊：</span><span class="sxs-lookup"><span data-stu-id="76a57-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="76a57-118">範例 3：停用 Datab一s 工作區上的加密</span><span class="sxs-lookup"><span data-stu-id="76a57-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="76a57-119">若要停用加密，只要設定 `-EncryptionKeySource` 為 `'Default'` 。</span><span class="sxs-lookup"><span data-stu-id="76a57-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="76a57-120">參數</span><span class="sxs-lookup"><span data-stu-id="76a57-120">PARAMETERS</span></span>

### <span data-ttu-id="76a57-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76a57-121">-AsJob</span></span>
<span data-ttu-id="76a57-122">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="76a57-122">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a57-123">-DefaultProfile</span></span>
<span data-ttu-id="76a57-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76a57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="76a57-125">-EncryptionKeyName</span></span>
<span data-ttu-id="76a57-126">Key Vault 鍵的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="76a57-127">-EncryptionKeySource</span></span>
<span data-ttu-id="76a57-128">加密金鑰Source (提供者) 。</span><span class="sxs-lookup"><span data-stu-id="76a57-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="76a57-129">區分大小寫 (值) ：預設、Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="76a57-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="76a57-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="76a57-131">金鑰庫 (URI) DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="76a57-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="76a57-133">KeyVault 金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="76a57-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a57-134">-InputObject</span></span>
<span data-ttu-id="76a57-135">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="76a57-135">Identity parameter.</span></span>
<span data-ttu-id="76a57-136">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="76a57-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="76a57-137">-Name</span></span>
<span data-ttu-id="76a57-138">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="76a57-139">-NoWait</span></span>
<span data-ttu-id="76a57-140">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="76a57-140">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="76a57-141">-PrepareEncryption</span></span>
<span data-ttu-id="76a57-142">準備工作區進行加密。</span><span class="sxs-lookup"><span data-stu-id="76a57-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="76a57-143">啟用受管理儲存帳戶的受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="76a57-143">Enables the Managed Identity for managed storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a57-144">-ResourceGroupName</span></span>
<span data-ttu-id="76a57-145">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-145">The name of the resource group.</span></span>
<span data-ttu-id="76a57-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="76a57-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76a57-147">-SubscriptionId</span></span>
<span data-ttu-id="76a57-148">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76a57-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-149">-標記</span><span class="sxs-lookup"><span data-stu-id="76a57-149">-Tag</span></span>
<span data-ttu-id="76a57-150">資源標記。</span><span class="sxs-lookup"><span data-stu-id="76a57-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-151">-確認</span><span class="sxs-lookup"><span data-stu-id="76a57-151">-Confirm</span></span>
<span data-ttu-id="76a57-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76a57-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a57-153">-WhatIf</span></span>
<span data-ttu-id="76a57-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76a57-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a57-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76a57-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a57-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a57-156">CommonParameters</span></span>
<span data-ttu-id="76a57-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76a57-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a57-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76a57-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a57-159">輸入</span><span class="sxs-lookup"><span data-stu-id="76a57-159">INPUTS</span></span>

### <span data-ttu-id="76a57-160">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="76a57-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="76a57-161">輸出</span><span class="sxs-lookup"><span data-stu-id="76a57-161">OUTPUTS</span></span>

### <span data-ttu-id="76a57-162">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="76a57-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="76a57-163">筆記</span><span class="sxs-lookup"><span data-stu-id="76a57-163">NOTES</span></span>

<span data-ttu-id="76a57-164">別名</span><span class="sxs-lookup"><span data-stu-id="76a57-164">ALIASES</span></span>

<span data-ttu-id="76a57-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="76a57-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76a57-166">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="76a57-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76a57-167">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="76a57-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76a57-168">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="76a57-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="76a57-169">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="76a57-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76a57-170">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="76a57-171">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76a57-172">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="76a57-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="76a57-173">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76a57-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76a57-174">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a57-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="76a57-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="76a57-175">RELATED LINKS</span></span>

