---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: b8297580f088678f1fdd61b8bff670adb03d2bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905249"
---
# <span data-ttu-id="60f60-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="60f60-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="60f60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60f60-102">SYNOPSIS</span></span>
<span data-ttu-id="60f60-103">使用指定的參數更新設定存放區。</span><span class="sxs-lookup"><span data-stu-id="60f60-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="60f60-104">語法</span><span class="sxs-lookup"><span data-stu-id="60f60-104">SYNTAX</span></span>

### <span data-ttu-id="60f60-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="60f60-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60f60-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="60f60-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="60f60-107">描述</span><span class="sxs-lookup"><span data-stu-id="60f60-107">DESCRIPTION</span></span>
<span data-ttu-id="60f60-108">使用指定的參數更新設定存放區。</span><span class="sxs-lookup"><span data-stu-id="60f60-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="60f60-109">例子</span><span class="sxs-lookup"><span data-stu-id="60f60-109">EXAMPLES</span></span>

### <span data-ttu-id="60f60-110">範例 1：根據系統指派的受管理身分識別啟用應用程式組配置存放區的資料加密</span><span class="sxs-lookup"><span data-stu-id="60f60-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="60f60-111">此命令可讓儲存在 Azure 金鑰保存庫中的金鑰使用系統指派的受管理身分識別進行資料加密。</span><span class="sxs-lookup"><span data-stu-id="60f60-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="60f60-112">該儲存庫必須啟用柔刪除和清除保護，而受管理的身分識別必須擁有以下重要許可權：get、wrapKey、unwrapKey。</span><span class="sxs-lookup"><span data-stu-id="60f60-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="60f60-113">範例 2：根據使用者指派的受管理身分識別啟用應用程式組配置存放區的資料加密</span><span class="sxs-lookup"><span data-stu-id="60f60-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="60f60-114">此命令可讓儲存在 Azure 金鑰保存庫中的金鑰使用使用者指派的受管理身分識別進行資料加密。</span><span class="sxs-lookup"><span data-stu-id="60f60-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="60f60-115">使用者指派的身分識別必須設定為 `-UserAssignedIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="60f60-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="60f60-116">該儲存庫必須啟用柔刪除和清除保護，而受管理的身分識別必須擁有以下重要許可權：get、wrapKey、unwrapKey。</span><span class="sxs-lookup"><span data-stu-id="60f60-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="60f60-117">範例 3：停用應用程式組配置存放區加密。</span><span class="sxs-lookup"><span data-stu-id="60f60-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="60f60-118">此命令會停用應用程式組配置存放區加密。</span><span class="sxs-lookup"><span data-stu-id="60f60-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="60f60-119">範例 3：根據管道更新 App 組配置存放區 SKU 和標記。</span><span class="sxs-lookup"><span data-stu-id="60f60-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="60f60-120">此命令會根據管線更新應用程式組配置存放區 SKU 和標記。</span><span class="sxs-lookup"><span data-stu-id="60f60-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="60f60-121">參數</span><span class="sxs-lookup"><span data-stu-id="60f60-121">PARAMETERS</span></span>

### <span data-ttu-id="60f60-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60f60-122">-AsJob</span></span>
<span data-ttu-id="60f60-123">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="60f60-123">Run the command as a job</span></span>

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

### <span data-ttu-id="60f60-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f60-124">-DefaultProfile</span></span>
<span data-ttu-id="60f60-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60f60-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f60-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="60f60-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="60f60-127">用來加密資料的金鑰保存庫金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="60f60-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="60f60-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="60f60-128">-IdentityType</span></span>
<span data-ttu-id="60f60-129">使用的受管理身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="60f60-129">The type of managed identity used.</span></span>
<span data-ttu-id="60f60-130">"SystemAssignedAndUserAssigned" 類型包括隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="60f60-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="60f60-131">類型為 "None" 會移除任何身分。</span><span class="sxs-lookup"><span data-stu-id="60f60-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="60f60-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f60-132">-InputObject</span></span>
<span data-ttu-id="60f60-133">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="60f60-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60f60-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="60f60-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="60f60-135">用來存取金鑰庫之身分識別的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="60f60-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="60f60-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="60f60-136">-Name</span></span>
<span data-ttu-id="60f60-137">組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="60f60-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="60f60-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="60f60-138">-NoWait</span></span>
<span data-ttu-id="60f60-139">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="60f60-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60f60-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f60-140">-ResourceGroupName</span></span>
<span data-ttu-id="60f60-141">容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="60f60-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="60f60-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="60f60-142">-Sku</span></span>
<span data-ttu-id="60f60-143">組組儲存的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="60f60-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="60f60-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60f60-144">-SubscriptionId</span></span>
<span data-ttu-id="60f60-145">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="60f60-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="60f60-146">-標記</span><span class="sxs-lookup"><span data-stu-id="60f60-146">-Tag</span></span>
<span data-ttu-id="60f60-147">ARM 資源標記。</span><span class="sxs-lookup"><span data-stu-id="60f60-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="60f60-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="60f60-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="60f60-149">與資源相關聯的使用者指派身分驗證清單。</span><span class="sxs-lookup"><span data-stu-id="60f60-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="60f60-150">使用者指派的身分識別字典金鑰為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentity/{identityName}'。</span><span class="sxs-lookup"><span data-stu-id="60f60-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="60f60-151">-確認</span><span class="sxs-lookup"><span data-stu-id="60f60-151">-Confirm</span></span>
<span data-ttu-id="60f60-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="60f60-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f60-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f60-153">-WhatIf</span></span>
<span data-ttu-id="60f60-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60f60-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f60-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60f60-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f60-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f60-156">CommonParameters</span></span>
<span data-ttu-id="60f60-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60f60-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f60-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60f60-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f60-159">輸入</span><span class="sxs-lookup"><span data-stu-id="60f60-159">INPUTS</span></span>

### <span data-ttu-id="60f60-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="60f60-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="60f60-161">輸出</span><span class="sxs-lookup"><span data-stu-id="60f60-161">OUTPUTS</span></span>

### <span data-ttu-id="60f60-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="60f60-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="60f60-163">筆記</span><span class="sxs-lookup"><span data-stu-id="60f60-163">NOTES</span></span>

<span data-ttu-id="60f60-164">別名</span><span class="sxs-lookup"><span data-stu-id="60f60-164">ALIASES</span></span>

<span data-ttu-id="60f60-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="60f60-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60f60-166">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="60f60-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60f60-167">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="60f60-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60f60-168">INPUTOBJECT： <IAppConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="60f60-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60f60-169">`[ConfigStoreName <String>]`：組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="60f60-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="60f60-170">`[GroupName <String>]`：私人連結資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60f60-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="60f60-171">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="60f60-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60f60-172">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="60f60-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="60f60-173">`[ResourceGroupName <String>]`：容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="60f60-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="60f60-174">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="60f60-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="60f60-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="60f60-175">RELATED LINKS</span></span>



<span data-ttu-id="60f60-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="60f60-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

