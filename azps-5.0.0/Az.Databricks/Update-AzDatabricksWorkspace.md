---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284838"
---
# <span data-ttu-id="b85c7-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="b85c7-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="b85c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b85c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b85c7-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="b85c7-103">Updates a workspace.</span></span>

## <span data-ttu-id="b85c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b85c7-104">SYNTAX</span></span>

### <span data-ttu-id="b85c7-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b85c7-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b85c7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b85c7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b85c7-107">說明</span><span class="sxs-lookup"><span data-stu-id="b85c7-107">DESCRIPTION</span></span>
<span data-ttu-id="b85c7-108">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="b85c7-108">Updates a workspace.</span></span>

## <span data-ttu-id="b85c7-109">示例</span><span class="sxs-lookup"><span data-stu-id="b85c7-109">EXAMPLES</span></span>

### <span data-ttu-id="b85c7-110">範例1：更新 Databricks 工作區的標籤</span><span class="sxs-lookup"><span data-stu-id="b85c7-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="b85c7-111">這個命令會更新 Databricks 工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="b85c7-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="b85c7-112">範例2：在 Databricks 工作區上啟用加密</span><span class="sxs-lookup"><span data-stu-id="b85c7-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="b85c7-113">在 Databricks 工作區上啟用加密，需要三個步驟：</span><span class="sxs-lookup"><span data-stu-id="b85c7-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="b85c7-114">使用 (來更新工作區（ `-PrepareEncryption` 如果尚未建立的話）) 。</span><span class="sxs-lookup"><span data-stu-id="b85c7-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="b85c7-115">`StorageAccountIdentityPrincipalId`在最後一個步驟的輸出中尋找。</span><span class="sxs-lookup"><span data-stu-id="b85c7-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="b85c7-116">授與原則的金鑰許可權。</span><span class="sxs-lookup"><span data-stu-id="b85c7-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="b85c7-117">再次更新工作區，以填入有關加密金鑰的資訊：</span><span class="sxs-lookup"><span data-stu-id="b85c7-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="b85c7-118">範例3：停用 Databricks 工作區上的加密</span><span class="sxs-lookup"><span data-stu-id="b85c7-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="b85c7-119">若要停用加密，只要設定 `-EncryptionKeySource` 為 `'Default'` 。</span><span class="sxs-lookup"><span data-stu-id="b85c7-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="b85c7-120">參數</span><span class="sxs-lookup"><span data-stu-id="b85c7-120">PARAMETERS</span></span>

### <span data-ttu-id="b85c7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b85c7-121">-AsJob</span></span>
<span data-ttu-id="b85c7-122">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b85c7-122">Run the command as a job</span></span>

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

### <span data-ttu-id="b85c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85c7-123">-DefaultProfile</span></span>
<span data-ttu-id="b85c7-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85c7-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="b85c7-125">-EncryptionKeyName</span></span>
<span data-ttu-id="b85c7-126">主要保存庫金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="b85c7-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="b85c7-127">-EncryptionKeySource</span></span>
<span data-ttu-id="b85c7-128">加密 keySource (提供者) 。</span><span class="sxs-lookup"><span data-stu-id="b85c7-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="b85c7-129">可能的值 (不區分大小寫) ： Default、Keyvault</span><span class="sxs-lookup"><span data-stu-id="b85c7-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="b85c7-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="b85c7-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="b85c7-131">金鑰保存庫的 URI (DNS 名稱) 。</span><span class="sxs-lookup"><span data-stu-id="b85c7-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="b85c7-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b85c7-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="b85c7-133">KeyVault 金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="b85c7-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="b85c7-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b85c7-134">-InputObject</span></span>
<span data-ttu-id="b85c7-135">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="b85c7-135">Identity parameter.</span></span>
<span data-ttu-id="b85c7-136">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b85c7-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b85c7-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="b85c7-137">-Name</span></span>
<span data-ttu-id="b85c7-138">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="b85c7-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b85c7-139">-NoWait</span></span>
<span data-ttu-id="b85c7-140">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b85c7-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b85c7-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="b85c7-141">-PrepareEncryption</span></span>
<span data-ttu-id="b85c7-142">準備工作區以進行加密。</span><span class="sxs-lookup"><span data-stu-id="b85c7-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="b85c7-143">啟用受管理的儲存空間帳戶的 Managed 身分識別。</span><span class="sxs-lookup"><span data-stu-id="b85c7-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="b85c7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85c7-144">-ResourceGroupName</span></span>
<span data-ttu-id="b85c7-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-145">The name of the resource group.</span></span>
<span data-ttu-id="b85c7-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b85c7-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b85c7-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b85c7-147">-SubscriptionId</span></span>
<span data-ttu-id="b85c7-148">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="b85c7-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b85c7-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="b85c7-149">-Tag</span></span>
<span data-ttu-id="b85c7-150">資源標記。</span><span class="sxs-lookup"><span data-stu-id="b85c7-150">Resource tags.</span></span>

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

### <span data-ttu-id="b85c7-151">-確認</span><span class="sxs-lookup"><span data-stu-id="b85c7-151">-Confirm</span></span>
<span data-ttu-id="b85c7-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b85c7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85c7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85c7-153">-WhatIf</span></span>
<span data-ttu-id="b85c7-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b85c7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85c7-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b85c7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85c7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85c7-156">CommonParameters</span></span>
<span data-ttu-id="b85c7-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b85c7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85c7-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b85c7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85c7-159">輸入</span><span class="sxs-lookup"><span data-stu-id="b85c7-159">INPUTS</span></span>

### <span data-ttu-id="b85c7-160">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="b85c7-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b85c7-161">輸出</span><span class="sxs-lookup"><span data-stu-id="b85c7-161">OUTPUTS</span></span>

### <span data-ttu-id="b85c7-162">IWorkspace （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="b85c7-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="b85c7-163">筆記</span><span class="sxs-lookup"><span data-stu-id="b85c7-163">NOTES</span></span>

<span data-ttu-id="b85c7-164">別名</span><span class="sxs-lookup"><span data-stu-id="b85c7-164">ALIASES</span></span>

<span data-ttu-id="b85c7-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b85c7-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b85c7-166">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b85c7-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b85c7-167">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b85c7-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b85c7-168">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="b85c7-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="b85c7-169">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b85c7-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b85c7-170">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b85c7-171">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b85c7-172">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b85c7-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="b85c7-173">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b85c7-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b85c7-174">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85c7-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b85c7-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="b85c7-175">RELATED LINKS</span></span>

