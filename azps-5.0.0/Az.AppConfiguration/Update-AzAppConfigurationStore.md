---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137887"
---
# <span data-ttu-id="e8e93-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="e8e93-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="e8e93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8e93-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e93-103">使用指定的參數更新配置存儲區。</span><span class="sxs-lookup"><span data-stu-id="e8e93-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="e8e93-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8e93-104">SYNTAX</span></span>

### <span data-ttu-id="e8e93-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="e8e93-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8e93-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e8e93-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e8e93-107">說明</span><span class="sxs-lookup"><span data-stu-id="e8e93-107">DESCRIPTION</span></span>
<span data-ttu-id="e8e93-108">使用指定的參數更新配置存儲區。</span><span class="sxs-lookup"><span data-stu-id="e8e93-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="e8e93-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8e93-109">EXAMPLES</span></span>

### <span data-ttu-id="e8e93-110">範例1：使用系統指派的管理身分識別來啟用 app conifguration store 的資料加密</span><span class="sxs-lookup"><span data-stu-id="e8e93-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="e8e93-111">這個命令透過使用系統指派的受管理身分識別身分儲存在 Azure 金鑰保存庫中的金鑰來啟用資料加密。</span><span class="sxs-lookup"><span data-stu-id="e8e93-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="e8e93-112">Vault 必須已啟用虛刪除和清除保護，而且受管理的身分識別必須具備下列主要許可權：取得、wrapKey、unwrapKey。</span><span class="sxs-lookup"><span data-stu-id="e8e93-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="e8e93-113">範例2：依使用者指派的管理身分識別，啟用 app conifguration store 的資料加密</span><span class="sxs-lookup"><span data-stu-id="e8e93-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="e8e93-114">這個命令利用使用者指派的 managed 身分識別，透過 Azure 金鑰保存庫中儲存的金鑰來啟用資料加密。</span><span class="sxs-lookup"><span data-stu-id="e8e93-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="e8e93-115">使用者指派的身分識別必須已設定為 `-UserAssignedIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="e8e93-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="e8e93-116">Vault 必須已啟用虛刪除和清除保護，而且受管理的身分識別必須具備下列主要許可權：取得、wrapKey、unwrapKey。</span><span class="sxs-lookup"><span data-stu-id="e8e93-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="e8e93-117">範例3：停用應用程式 conifguration 存放區的加密。</span><span class="sxs-lookup"><span data-stu-id="e8e93-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="e8e93-118">這個命令會停用應用程式 conifguration 存放區的加密。</span><span class="sxs-lookup"><span data-stu-id="e8e93-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="e8e93-119">範例3：透過管線更新 app conifguration store 的 sku 和標記。</span><span class="sxs-lookup"><span data-stu-id="e8e93-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="e8e93-120">這個命令會透過管線更新 app conifguration store 的 sku 和標記。</span><span class="sxs-lookup"><span data-stu-id="e8e93-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="e8e93-121">參數</span><span class="sxs-lookup"><span data-stu-id="e8e93-121">PARAMETERS</span></span>

### <span data-ttu-id="e8e93-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8e93-122">-AsJob</span></span>
<span data-ttu-id="e8e93-123">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e8e93-123">Run the command as a job</span></span>

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

### <span data-ttu-id="e8e93-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e93-124">-DefaultProfile</span></span>
<span data-ttu-id="e8e93-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e93-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="e8e93-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="e8e93-127">用來加密資料之主要保存庫金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="e8e93-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="e8e93-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e8e93-128">-IdentityType</span></span>
<span data-ttu-id="e8e93-129">所使用的 managed 身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="e8e93-129">The type of managed identity used.</span></span>
<span data-ttu-id="e8e93-130">"SystemAssignedAndUserAssigned" 類型包含隱式建立的身分識別和一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e8e93-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="e8e93-131">類型 "None" 將移除任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="e8e93-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e93-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e93-132">-InputObject</span></span>
<span data-ttu-id="e8e93-133">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e8e93-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e93-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="e8e93-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="e8e93-135">將用來存取金鑰保存庫之身分識別的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8e93-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="e8e93-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8e93-136">-Name</span></span>
<span data-ttu-id="e8e93-137">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="e8e93-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e8e93-138">-NoWait</span></span>
<span data-ttu-id="e8e93-139">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e8e93-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e8e93-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e93-140">-ResourceGroupName</span></span>
<span data-ttu-id="e8e93-141">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="e8e93-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8e93-142">-Sku</span></span>
<span data-ttu-id="e8e93-143">[配置] 存放區的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="e8e93-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8e93-144">-SubscriptionId</span></span>
<span data-ttu-id="e8e93-145">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e8e93-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="e8e93-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8e93-146">-Tag</span></span>
<span data-ttu-id="e8e93-147">ARM 資源標記。</span><span class="sxs-lookup"><span data-stu-id="e8e93-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="e8e93-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e8e93-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="e8e93-149">與資源相關聯的使用者指派身分識別的清單。</span><span class="sxs-lookup"><span data-stu-id="e8e93-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="e8e93-150">使用者指派的身分識別字典金鑰會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="e8e93-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e93-151">-確認</span><span class="sxs-lookup"><span data-stu-id="e8e93-151">-Confirm</span></span>
<span data-ttu-id="e8e93-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8e93-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e93-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e93-153">-WhatIf</span></span>
<span data-ttu-id="e8e93-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8e93-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e93-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8e93-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e93-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e93-156">CommonParameters</span></span>
<span data-ttu-id="e8e93-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8e93-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e93-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8e93-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e93-159">輸入</span><span class="sxs-lookup"><span data-stu-id="e8e93-159">INPUTS</span></span>

### <span data-ttu-id="e8e93-160">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="e8e93-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="e8e93-161">輸出</span><span class="sxs-lookup"><span data-stu-id="e8e93-161">OUTPUTS</span></span>

### <span data-ttu-id="e8e93-162">IConfigurationStore （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="e8e93-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="e8e93-163">筆記</span><span class="sxs-lookup"><span data-stu-id="e8e93-163">NOTES</span></span>

<span data-ttu-id="e8e93-164">別名</span><span class="sxs-lookup"><span data-stu-id="e8e93-164">ALIASES</span></span>

<span data-ttu-id="e8e93-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e8e93-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8e93-166">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e8e93-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8e93-167">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e8e93-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8e93-168">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e8e93-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8e93-169">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="e8e93-170">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="e8e93-171">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e8e93-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8e93-172">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="e8e93-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="e8e93-173">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e93-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="e8e93-174">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e8e93-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="e8e93-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8e93-175">RELATED LINKS</span></span>



<span data-ttu-id="e8e93-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
[新-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="e8e93-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>
