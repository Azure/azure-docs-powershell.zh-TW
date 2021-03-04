---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: 4babe23fbddbc11838cad6307117884c3bb14ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911789"
---
# <span data-ttu-id="30c8a-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="30c8a-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="30c8a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="30c8a-103">刪除組組存放區。</span><span class="sxs-lookup"><span data-stu-id="30c8a-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="30c8a-104">語法</span><span class="sxs-lookup"><span data-stu-id="30c8a-104">SYNTAX</span></span>

### <span data-ttu-id="30c8a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="30c8a-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30c8a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30c8a-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30c8a-107">描述</span><span class="sxs-lookup"><span data-stu-id="30c8a-107">DESCRIPTION</span></span>
<span data-ttu-id="30c8a-108">刪除組組存放區。</span><span class="sxs-lookup"><span data-stu-id="30c8a-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="30c8a-109">例子</span><span class="sxs-lookup"><span data-stu-id="30c8a-109">EXAMPLES</span></span>

### <span data-ttu-id="30c8a-110">範例 1：移除應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="30c8a-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="30c8a-111">此命令會移除應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="30c8a-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="30c8a-112">範例 2：移除應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="30c8a-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="30c8a-113">此命令會移除應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="30c8a-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="30c8a-114">參數</span><span class="sxs-lookup"><span data-stu-id="30c8a-114">PARAMETERS</span></span>

### <span data-ttu-id="30c8a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30c8a-115">-AsJob</span></span>
<span data-ttu-id="30c8a-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="30c8a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="30c8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c8a-117">-DefaultProfile</span></span>
<span data-ttu-id="30c8a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30c8a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30c8a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30c8a-119">-InputObject</span></span>
<span data-ttu-id="30c8a-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="30c8a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c8a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="30c8a-121">-Name</span></span>
<span data-ttu-id="30c8a-122">組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="30c8a-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c8a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30c8a-123">-NoWait</span></span>
<span data-ttu-id="30c8a-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="30c8a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30c8a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30c8a-125">-PassThru</span></span>
<span data-ttu-id="30c8a-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="30c8a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30c8a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c8a-127">-ResourceGroupName</span></span>
<span data-ttu-id="30c8a-128">容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="30c8a-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c8a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30c8a-129">-SubscriptionId</span></span>
<span data-ttu-id="30c8a-130">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="30c8a-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c8a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="30c8a-131">-Confirm</span></span>
<span data-ttu-id="30c8a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30c8a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c8a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c8a-133">-WhatIf</span></span>
<span data-ttu-id="30c8a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30c8a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c8a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30c8a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c8a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c8a-136">CommonParameters</span></span>
<span data-ttu-id="30c8a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30c8a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c8a-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30c8a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c8a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="30c8a-139">INPUTS</span></span>

### <span data-ttu-id="30c8a-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="30c8a-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="30c8a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="30c8a-141">OUTPUTS</span></span>

### <span data-ttu-id="30c8a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30c8a-142">System.Boolean</span></span>

## <span data-ttu-id="30c8a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="30c8a-143">NOTES</span></span>

<span data-ttu-id="30c8a-144">別名</span><span class="sxs-lookup"><span data-stu-id="30c8a-144">ALIASES</span></span>

<span data-ttu-id="30c8a-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="30c8a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30c8a-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="30c8a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30c8a-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="30c8a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30c8a-148">INPUTOBJECT： <IAppConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="30c8a-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30c8a-149">`[ConfigStoreName <String>]`：組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="30c8a-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="30c8a-150">`[GroupName <String>]`：私人連結資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30c8a-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="30c8a-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="30c8a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30c8a-152">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="30c8a-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="30c8a-153">`[ResourceGroupName <String>]`：容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="30c8a-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="30c8a-154">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="30c8a-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="30c8a-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="30c8a-155">RELATED LINKS</span></span>

