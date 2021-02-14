---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130166"
---
# <span data-ttu-id="6c1b7-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="6c1b7-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="6c1b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1b7-103">針對指定的配置存放區重新產生便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="6c1b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c1b7-104">SYNTAX</span></span>

### <span data-ttu-id="6c1b7-105">RegenerateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6c1b7-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c1b7-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6c1b7-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c1b7-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c1b7-107">DESCRIPTION</span></span>
<span data-ttu-id="6c1b7-108">針對指定的配置存放區重新產生便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="6c1b7-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c1b7-109">EXAMPLES</span></span>

### <span data-ttu-id="6c1b7-110">範例1：重新產生 app 設定存放區的金鑰</span><span class="sxs-lookup"><span data-stu-id="6c1b7-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="6c1b7-111">這個命令會重新產生 app 配置存放區的金鑰。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="6c1b7-112">範例2：依物件重新產生 app 設定存儲區的按鍵</span><span class="sxs-lookup"><span data-stu-id="6c1b7-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="6c1b7-113">這個命令會依據物件重新產生 app 設定存儲區的金鑰。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="6c1b7-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c1b7-114">PARAMETERS</span></span>

### <span data-ttu-id="6c1b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1b7-115">-DefaultProfile</span></span>
<span data-ttu-id="6c1b7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c1b7-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6c1b7-117">-Id</span></span>
<span data-ttu-id="6c1b7-118">要重新產生的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="6c1b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c1b7-119">-InputObject</span></span>
<span data-ttu-id="6c1b7-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c1b7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c1b7-121">-Name</span></span>
<span data-ttu-id="6c1b7-122">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="6c1b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c1b7-124">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="6c1b7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c1b7-125">-SubscriptionId</span></span>
<span data-ttu-id="6c1b7-126">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="6c1b7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6c1b7-127">-Confirm</span></span>
<span data-ttu-id="6c1b7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1b7-129">-WhatIf</span></span>
<span data-ttu-id="6c1b7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c1b7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1b7-132">CommonParameters</span></span>
<span data-ttu-id="6c1b7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1b7-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1b7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6c1b7-135">INPUTS</span></span>

### <span data-ttu-id="6c1b7-136">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="6c1b7-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6c1b7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6c1b7-137">OUTPUTS</span></span>

### <span data-ttu-id="6c1b7-138">IApiKey （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="6c1b7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6c1b7-139">NOTES</span></span>

<span data-ttu-id="6c1b7-140">別名</span><span class="sxs-lookup"><span data-stu-id="6c1b7-140">ALIASES</span></span>

<span data-ttu-id="6c1b7-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6c1b7-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c1b7-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c1b7-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c1b7-144">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6c1b7-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c1b7-145">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6c1b7-146">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6c1b7-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6c1b7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c1b7-148">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="6c1b7-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6c1b7-149">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6c1b7-150">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6c1b7-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6c1b7-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c1b7-151">RELATED LINKS</span></span>

