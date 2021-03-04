---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 9373a154e6bc717c22705961fb5232814ac3d2c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910798"
---
# <span data-ttu-id="84c3e-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="84c3e-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="84c3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="84c3e-103">使用指定的參數建立設定存放區。</span><span class="sxs-lookup"><span data-stu-id="84c3e-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="84c3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="84c3e-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="84c3e-105">描述</span><span class="sxs-lookup"><span data-stu-id="84c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="84c3e-106">使用指定的參數建立設定存放區。</span><span class="sxs-lookup"><span data-stu-id="84c3e-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="84c3e-107">例子</span><span class="sxs-lookup"><span data-stu-id="84c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="84c3e-108">範例 1：建立應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="84c3e-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="84c3e-109">此命令會建立應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="84c3e-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="84c3e-110">範例 2：建立將 IdentityType 設為 "UserAssigned" 的應用程式設定</span><span class="sxs-lookup"><span data-stu-id="84c3e-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="84c3e-111">此命令會建立應用程式組式，並指派使用者指派的受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="84c3e-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="84c3e-112">請參閱下列步驟的範例，以啟用 CMK (`Update-AzAppConfigurationStore` cusomer 受管理金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="84c3e-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="84c3e-113">範例 3：建立將 IdentityType 設為 "SystemAssigned" 的應用程式設定</span><span class="sxs-lookup"><span data-stu-id="84c3e-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="84c3e-114">此命令會建立應用程式組式，並啟用與資源相關聯的系統指派受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="84c3e-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="84c3e-115">請參閱下列步驟的範例，以啟用 CMK (`Update-AzAppConfigurationStore` cusomer 受管理金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="84c3e-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="84c3e-116">範例 4：使用 IdentityType 設為 "SystemAssigned， UserAssigned" 建立應用程式設定</span><span class="sxs-lookup"><span data-stu-id="84c3e-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="84c3e-117">您可以啟用系統指派的受管理身分識別，並同時提供使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="84c3e-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="84c3e-118">請參閱下列步驟的範例，以啟用 CMK (`Update-AzAppConfigurationStore` cusomer 受管理金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="84c3e-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="84c3e-119">參數</span><span class="sxs-lookup"><span data-stu-id="84c3e-119">PARAMETERS</span></span>

### <span data-ttu-id="84c3e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84c3e-120">-AsJob</span></span>
<span data-ttu-id="84c3e-121">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="84c3e-121">Run the command as a job</span></span>

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

### <span data-ttu-id="84c3e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c3e-122">-DefaultProfile</span></span>
<span data-ttu-id="84c3e-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84c3e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c3e-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="84c3e-124">-IdentityType</span></span>
<span data-ttu-id="84c3e-125">使用的受管理身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="84c3e-125">The type of managed identity used.</span></span>
<span data-ttu-id="84c3e-126">"SystemAssignedAndUserAssigned" 類型包括隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="84c3e-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="84c3e-127">類型為 "None" 會移除任何身分。</span><span class="sxs-lookup"><span data-stu-id="84c3e-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="84c3e-128">-位置</span><span class="sxs-lookup"><span data-stu-id="84c3e-128">-Location</span></span>
<span data-ttu-id="84c3e-129">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="84c3e-129">The location of the resource.</span></span>
<span data-ttu-id="84c3e-130">建立資源之後，就無法變更這項功能。</span><span class="sxs-lookup"><span data-stu-id="84c3e-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3e-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="84c3e-131">-Name</span></span>
<span data-ttu-id="84c3e-132">組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="84c3e-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3e-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84c3e-133">-NoWait</span></span>
<span data-ttu-id="84c3e-134">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="84c3e-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84c3e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c3e-135">-ResourceGroupName</span></span>
<span data-ttu-id="84c3e-136">容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="84c3e-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3e-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="84c3e-137">-Sku</span></span>
<span data-ttu-id="84c3e-138">組組儲存的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="84c3e-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84c3e-139">-SubscriptionId</span></span>
<span data-ttu-id="84c3e-140">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="84c3e-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3e-141">-標記</span><span class="sxs-lookup"><span data-stu-id="84c3e-141">-Tag</span></span>
<span data-ttu-id="84c3e-142">資源的標記。</span><span class="sxs-lookup"><span data-stu-id="84c3e-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="84c3e-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="84c3e-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="84c3e-144">與資源相關聯的使用者指派身分驗證清單。</span><span class="sxs-lookup"><span data-stu-id="84c3e-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="84c3e-145">使用者指派的身分識別字典金鑰為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentity/{identityName}'。</span><span class="sxs-lookup"><span data-stu-id="84c3e-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="84c3e-146">-確認</span><span class="sxs-lookup"><span data-stu-id="84c3e-146">-Confirm</span></span>
<span data-ttu-id="84c3e-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84c3e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c3e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c3e-148">-WhatIf</span></span>
<span data-ttu-id="84c3e-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84c3e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c3e-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84c3e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c3e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c3e-151">CommonParameters</span></span>
<span data-ttu-id="84c3e-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84c3e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c3e-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84c3e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c3e-154">輸入</span><span class="sxs-lookup"><span data-stu-id="84c3e-154">INPUTS</span></span>

## <span data-ttu-id="84c3e-155">輸出</span><span class="sxs-lookup"><span data-stu-id="84c3e-155">OUTPUTS</span></span>

### <span data-ttu-id="84c3e-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="84c3e-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="84c3e-157">筆記</span><span class="sxs-lookup"><span data-stu-id="84c3e-157">NOTES</span></span>

<span data-ttu-id="84c3e-158">別名</span><span class="sxs-lookup"><span data-stu-id="84c3e-158">ALIASES</span></span>

## <span data-ttu-id="84c3e-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="84c3e-159">RELATED LINKS</span></span>



[<span data-ttu-id="84c3e-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="84c3e-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

