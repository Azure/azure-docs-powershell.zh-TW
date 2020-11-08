---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136504"
---
# <span data-ttu-id="09022-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="09022-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="09022-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09022-102">SYNOPSIS</span></span>
<span data-ttu-id="09022-103">刪除自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="09022-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="09022-104">句法</span><span class="sxs-lookup"><span data-stu-id="09022-104">SYNTAX</span></span>

### <span data-ttu-id="09022-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="09022-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09022-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09022-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09022-107">說明</span><span class="sxs-lookup"><span data-stu-id="09022-107">DESCRIPTION</span></span>
<span data-ttu-id="09022-108">刪除自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="09022-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="09022-109">示例</span><span class="sxs-lookup"><span data-stu-id="09022-109">EXAMPLES</span></span>

### <span data-ttu-id="09022-110">範例1：移除自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="09022-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="09022-111">移除自訂提供者</span><span class="sxs-lookup"><span data-stu-id="09022-111">Remove a custom provider</span></span>

### <span data-ttu-id="09022-112">範例2：在 PassThru 中移除自訂提供者</span><span class="sxs-lookup"><span data-stu-id="09022-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="09022-113">使用 PassThru 功能來指示成功或失敗，移除自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="09022-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="09022-114">參數</span><span class="sxs-lookup"><span data-stu-id="09022-114">PARAMETERS</span></span>

### <span data-ttu-id="09022-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09022-115">-AsJob</span></span>
<span data-ttu-id="09022-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="09022-116">Run the command as a job</span></span>

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

### <span data-ttu-id="09022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09022-117">-DefaultProfile</span></span>
<span data-ttu-id="09022-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09022-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09022-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09022-119">-InputObject</span></span>
<span data-ttu-id="09022-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="09022-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09022-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="09022-121">-Name</span></span>
<span data-ttu-id="09022-122">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="09022-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09022-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09022-123">-NoWait</span></span>
<span data-ttu-id="09022-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="09022-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="09022-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09022-125">-PassThru</span></span>
<span data-ttu-id="09022-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="09022-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="09022-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09022-127">-ResourceGroupName</span></span>
<span data-ttu-id="09022-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09022-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="09022-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09022-129">-SubscriptionId</span></span>
<span data-ttu-id="09022-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="09022-130">The Azure subscription ID.</span></span>
<span data-ttu-id="09022-131">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="09022-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="09022-132">-確認</span><span class="sxs-lookup"><span data-stu-id="09022-132">-Confirm</span></span>
<span data-ttu-id="09022-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="09022-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09022-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09022-134">-WhatIf</span></span>
<span data-ttu-id="09022-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09022-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09022-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09022-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09022-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09022-137">CommonParameters</span></span>
<span data-ttu-id="09022-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09022-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09022-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09022-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09022-140">輸入</span><span class="sxs-lookup"><span data-stu-id="09022-140">INPUTS</span></span>

### <span data-ttu-id="09022-141">ICustomProvidersIdentity （CustomProviders）的</span><span class="sxs-lookup"><span data-stu-id="09022-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="09022-142">輸出</span><span class="sxs-lookup"><span data-stu-id="09022-142">OUTPUTS</span></span>

### <span data-ttu-id="09022-143">System.object</span><span class="sxs-lookup"><span data-stu-id="09022-143">System.Boolean</span></span>

## <span data-ttu-id="09022-144">筆記</span><span class="sxs-lookup"><span data-stu-id="09022-144">NOTES</span></span>

<span data-ttu-id="09022-145">別名</span><span class="sxs-lookup"><span data-stu-id="09022-145">ALIASES</span></span>

<span data-ttu-id="09022-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="09022-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09022-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="09022-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09022-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="09022-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09022-149">INPUTOBJECT <ICustomProvidersIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="09022-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09022-150">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="09022-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="09022-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="09022-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09022-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09022-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="09022-153">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="09022-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="09022-154">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="09022-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="09022-155">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="09022-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="09022-156">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="09022-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="09022-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="09022-157">RELATED LINKS</span></span>

