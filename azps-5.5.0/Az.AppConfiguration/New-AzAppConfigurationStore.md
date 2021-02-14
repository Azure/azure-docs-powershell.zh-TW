---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130167"
---
# <span data-ttu-id="61b8c-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="61b8c-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="61b8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="61b8c-103">使用指定的參數建立配置存放區。</span><span class="sxs-lookup"><span data-stu-id="61b8c-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="61b8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="61b8c-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="61b8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="61b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="61b8c-106">使用指定的參數建立配置存放區。</span><span class="sxs-lookup"><span data-stu-id="61b8c-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="61b8c-107">示例</span><span class="sxs-lookup"><span data-stu-id="61b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="61b8c-108">範例1：建立應用程式佈建存放區</span><span class="sxs-lookup"><span data-stu-id="61b8c-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="61b8c-109">這個命令會建立應用程式佈建存放區。</span><span class="sxs-lookup"><span data-stu-id="61b8c-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="61b8c-110">範例2：建立 IdentityType 設定為 "UserAssigned" 的 app 設定</span><span class="sxs-lookup"><span data-stu-id="61b8c-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="61b8c-111">這個命令會建立 app 設定並指派使用者指派的管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="61b8c-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="61b8c-112">請參閱下列步驟的範例， `Update-AzAppConfigurationStore` 以啟用 CMK (cusomer 受管理的金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="61b8c-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="61b8c-113">範例3：建立 IdentityType 設定為 "SystemAssigned" 的 app 設定</span><span class="sxs-lookup"><span data-stu-id="61b8c-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="61b8c-114">這個命令會建立應用程式設定，並啟用系統指派的與資源相關聯的管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="61b8c-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="61b8c-115">請參閱下列步驟的範例， `Update-AzAppConfigurationStore` 以啟用 CMK (cusomer 受管理的金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="61b8c-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="61b8c-116">範例4：建立 IdentityType 設定為 "SystemAssigned，UserAssigned" 的 app 設定</span><span class="sxs-lookup"><span data-stu-id="61b8c-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="61b8c-117">您可以啟用系統指派的管理身分識別，並同時提供使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="61b8c-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="61b8c-118">請參閱下列步驟的範例， `Update-AzAppConfigurationStore` 以啟用 CMK (cusomer 受管理的金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="61b8c-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="61b8c-119">參數</span><span class="sxs-lookup"><span data-stu-id="61b8c-119">PARAMETERS</span></span>

### <span data-ttu-id="61b8c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61b8c-120">-AsJob</span></span>
<span data-ttu-id="61b8c-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="61b8c-121">Run the command as a job</span></span>

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

### <span data-ttu-id="61b8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b8c-122">-DefaultProfile</span></span>
<span data-ttu-id="61b8c-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61b8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61b8c-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="61b8c-124">-IdentityType</span></span>
<span data-ttu-id="61b8c-125">所使用的 managed 身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="61b8c-125">The type of managed identity used.</span></span>
<span data-ttu-id="61b8c-126">"SystemAssignedAndUserAssigned" 類型包含隱式建立的身分識別和一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="61b8c-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="61b8c-127">類型 "None" 將移除任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="61b8c-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="61b8c-128">-位置</span><span class="sxs-lookup"><span data-stu-id="61b8c-128">-Location</span></span>
<span data-ttu-id="61b8c-129">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="61b8c-129">The location of the resource.</span></span>
<span data-ttu-id="61b8c-130">在建立資源之後，就無法變更此功能。</span><span class="sxs-lookup"><span data-stu-id="61b8c-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="61b8c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="61b8c-131">-Name</span></span>
<span data-ttu-id="61b8c-132">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="61b8c-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="61b8c-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61b8c-133">-NoWait</span></span>
<span data-ttu-id="61b8c-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="61b8c-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="61b8c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b8c-135">-ResourceGroupName</span></span>
<span data-ttu-id="61b8c-136">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61b8c-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="61b8c-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="61b8c-137">-Sku</span></span>
<span data-ttu-id="61b8c-138">[配置] 存放區的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="61b8c-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="61b8c-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61b8c-139">-SubscriptionId</span></span>
<span data-ttu-id="61b8c-140">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="61b8c-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="61b8c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="61b8c-141">-Tag</span></span>
<span data-ttu-id="61b8c-142">資源的標籤。</span><span class="sxs-lookup"><span data-stu-id="61b8c-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="61b8c-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="61b8c-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="61b8c-144">與資源相關聯的使用者指派身分識別的清單。</span><span class="sxs-lookup"><span data-stu-id="61b8c-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="61b8c-145">使用者指派的身分識別字典金鑰會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}」。</span><span class="sxs-lookup"><span data-stu-id="61b8c-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="61b8c-146">-確認</span><span class="sxs-lookup"><span data-stu-id="61b8c-146">-Confirm</span></span>
<span data-ttu-id="61b8c-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61b8c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61b8c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b8c-148">-WhatIf</span></span>
<span data-ttu-id="61b8c-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61b8c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61b8c-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61b8c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61b8c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b8c-151">CommonParameters</span></span>
<span data-ttu-id="61b8c-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61b8c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b8c-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61b8c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b8c-154">輸入</span><span class="sxs-lookup"><span data-stu-id="61b8c-154">INPUTS</span></span>

## <span data-ttu-id="61b8c-155">輸出</span><span class="sxs-lookup"><span data-stu-id="61b8c-155">OUTPUTS</span></span>

### <span data-ttu-id="61b8c-156">IConfigurationStore （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="61b8c-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="61b8c-157">筆記</span><span class="sxs-lookup"><span data-stu-id="61b8c-157">NOTES</span></span>

<span data-ttu-id="61b8c-158">別名</span><span class="sxs-lookup"><span data-stu-id="61b8c-158">ALIASES</span></span>

## <span data-ttu-id="61b8c-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="61b8c-159">RELATED LINKS</span></span>



[<span data-ttu-id="61b8c-160">新-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="61b8c-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

