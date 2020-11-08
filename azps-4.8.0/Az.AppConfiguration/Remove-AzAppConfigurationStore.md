---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129671"
---
# <span data-ttu-id="f8aeb-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="f8aeb-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="f8aeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="f8aeb-103">刪除配置存放區。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="f8aeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8aeb-104">SYNTAX</span></span>

### <span data-ttu-id="f8aeb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f8aeb-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8aeb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f8aeb-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8aeb-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8aeb-107">DESCRIPTION</span></span>
<span data-ttu-id="f8aeb-108">刪除配置存放區。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="f8aeb-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8aeb-109">EXAMPLES</span></span>

### <span data-ttu-id="f8aeb-110">範例1：移除 app 配置存放區</span><span class="sxs-lookup"><span data-stu-id="f8aeb-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="f8aeb-111">這個命令會移除 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="f8aeb-112">範例2：移除 app 配置存放區</span><span class="sxs-lookup"><span data-stu-id="f8aeb-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="f8aeb-113">這個命令會移除 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="f8aeb-114">參數</span><span class="sxs-lookup"><span data-stu-id="f8aeb-114">PARAMETERS</span></span>

### <span data-ttu-id="f8aeb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8aeb-115">-AsJob</span></span>
<span data-ttu-id="f8aeb-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f8aeb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f8aeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8aeb-117">-DefaultProfile</span></span>
<span data-ttu-id="f8aeb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8aeb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8aeb-119">-InputObject</span></span>
<span data-ttu-id="f8aeb-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f8aeb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8aeb-121">-Name</span></span>
<span data-ttu-id="f8aeb-122">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="f8aeb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8aeb-123">-NoWait</span></span>
<span data-ttu-id="f8aeb-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f8aeb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8aeb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8aeb-125">-PassThru</span></span>
<span data-ttu-id="f8aeb-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="f8aeb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8aeb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8aeb-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8aeb-128">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="f8aeb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8aeb-129">-SubscriptionId</span></span>
<span data-ttu-id="f8aeb-130">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="f8aeb-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f8aeb-131">-Confirm</span></span>
<span data-ttu-id="f8aeb-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8aeb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8aeb-133">-WhatIf</span></span>
<span data-ttu-id="f8aeb-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8aeb-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8aeb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8aeb-136">CommonParameters</span></span>
<span data-ttu-id="f8aeb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8aeb-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8aeb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f8aeb-139">INPUTS</span></span>

### <span data-ttu-id="f8aeb-140">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="f8aeb-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="f8aeb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f8aeb-141">OUTPUTS</span></span>

### <span data-ttu-id="f8aeb-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f8aeb-142">System.Boolean</span></span>

## <span data-ttu-id="f8aeb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f8aeb-143">NOTES</span></span>

<span data-ttu-id="f8aeb-144">別名</span><span class="sxs-lookup"><span data-stu-id="f8aeb-144">ALIASES</span></span>

<span data-ttu-id="f8aeb-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f8aeb-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8aeb-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8aeb-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8aeb-148">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f8aeb-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8aeb-149">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="f8aeb-150">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="f8aeb-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f8aeb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8aeb-152">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="f8aeb-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="f8aeb-153">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="f8aeb-154">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f8aeb-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="f8aeb-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8aeb-155">RELATED LINKS</span></span>

