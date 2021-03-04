---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b71be7ed7475f89df52c22f69b38234ba8cee132
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910793"
---
# <span data-ttu-id="adc1c-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="adc1c-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="adc1c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="adc1c-103">重新產生指定組組存放區的存取權限鍵。</span><span class="sxs-lookup"><span data-stu-id="adc1c-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="adc1c-104">語法</span><span class="sxs-lookup"><span data-stu-id="adc1c-104">SYNTAX</span></span>

### <span data-ttu-id="adc1c-105">重新產生Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="adc1c-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="adc1c-106">重新產生ViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="adc1c-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="adc1c-107">描述</span><span class="sxs-lookup"><span data-stu-id="adc1c-107">DESCRIPTION</span></span>
<span data-ttu-id="adc1c-108">重新產生指定組組存放區的存取權限鍵。</span><span class="sxs-lookup"><span data-stu-id="adc1c-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="adc1c-109">例子</span><span class="sxs-lookup"><span data-stu-id="adc1c-109">EXAMPLES</span></span>

### <span data-ttu-id="adc1c-110">範例 1：重新產生應用程式組配置存放區金鑰</span><span class="sxs-lookup"><span data-stu-id="adc1c-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="adc1c-111">此命令會重新產生應用程式組配置存放區金鑰。</span><span class="sxs-lookup"><span data-stu-id="adc1c-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="adc1c-112">範例 2：根據物件重新產生應用程式組配置存放區金鑰</span><span class="sxs-lookup"><span data-stu-id="adc1c-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="adc1c-113">此命令會根據物件重新產生應用程式組配置存放區金鑰。</span><span class="sxs-lookup"><span data-stu-id="adc1c-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="adc1c-114">參數</span><span class="sxs-lookup"><span data-stu-id="adc1c-114">PARAMETERS</span></span>

### <span data-ttu-id="adc1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc1c-115">-DefaultProfile</span></span>
<span data-ttu-id="adc1c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc1c-117">-Id</span><span class="sxs-lookup"><span data-stu-id="adc1c-117">-Id</span></span>
<span data-ttu-id="adc1c-118">要重新產生之金鑰的識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc1c-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="adc1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adc1c-119">-InputObject</span></span>
<span data-ttu-id="adc1c-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="adc1c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adc1c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="adc1c-121">-Name</span></span>
<span data-ttu-id="adc1c-122">組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="adc1c-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="adc1c-124">容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="adc1c-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc1c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adc1c-125">-SubscriptionId</span></span>
<span data-ttu-id="adc1c-126">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc1c-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc1c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="adc1c-127">-Confirm</span></span>
<span data-ttu-id="adc1c-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="adc1c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc1c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc1c-129">-WhatIf</span></span>
<span data-ttu-id="adc1c-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adc1c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc1c-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adc1c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc1c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc1c-132">CommonParameters</span></span>
<span data-ttu-id="adc1c-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adc1c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc1c-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adc1c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc1c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="adc1c-135">INPUTS</span></span>

### <span data-ttu-id="adc1c-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="adc1c-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="adc1c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="adc1c-137">OUTPUTS</span></span>

### <span data-ttu-id="adc1c-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="adc1c-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="adc1c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="adc1c-139">NOTES</span></span>

<span data-ttu-id="adc1c-140">別名</span><span class="sxs-lookup"><span data-stu-id="adc1c-140">ALIASES</span></span>

<span data-ttu-id="adc1c-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="adc1c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="adc1c-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="adc1c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="adc1c-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="adc1c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="adc1c-144">INPUTOBJECT： <IAppConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="adc1c-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="adc1c-145">`[ConfigStoreName <String>]`：組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="adc1c-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="adc1c-146">`[GroupName <String>]`：私人連結資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="adc1c-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="adc1c-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="adc1c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="adc1c-148">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="adc1c-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="adc1c-149">`[ResourceGroupName <String>]`：容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="adc1c-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="adc1c-150">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc1c-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="adc1c-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc1c-151">RELATED LINKS</span></span>

