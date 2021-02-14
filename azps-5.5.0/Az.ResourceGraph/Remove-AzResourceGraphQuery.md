---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127231"
---
# <span data-ttu-id="f4e8a-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="f4e8a-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="f4e8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e8a-103">刪除圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-103">Delete a graph query.</span></span>

## <span data-ttu-id="f4e8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4e8a-104">SYNTAX</span></span>

### <span data-ttu-id="f4e8a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f4e8a-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4e8a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4e8a-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4e8a-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e8a-108">刪除圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-108">Delete a graph query.</span></span>

## <span data-ttu-id="f4e8a-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="f4e8a-110">範例1：依名稱移除資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="f4e8a-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="f4e8a-111">這個命令會依名稱移除資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="f4e8a-112">範例2：移除依物件的資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="f4e8a-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="f4e8a-113">這個命令會移除依物件的資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="f4e8a-114">參數</span><span class="sxs-lookup"><span data-stu-id="f4e8a-114">PARAMETERS</span></span>

### <span data-ttu-id="f4e8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e8a-115">-DefaultProfile</span></span>
<span data-ttu-id="f4e8a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e8a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4e8a-117">-InputObject</span></span>
<span data-ttu-id="f4e8a-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e8a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4e8a-119">-Name</span></span>
<span data-ttu-id="f4e8a-120">圖形查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="f4e8a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4e8a-121">-PassThru</span></span>
<span data-ttu-id="f4e8a-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="f4e8a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f4e8a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e8a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4e8a-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4e8a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4e8a-125">-SubscriptionId</span></span>
<span data-ttu-id="f4e8a-126">Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="f4e8a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f4e8a-127">-Confirm</span></span>
<span data-ttu-id="f4e8a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e8a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e8a-129">-WhatIf</span></span>
<span data-ttu-id="f4e8a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e8a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e8a-132">CommonParameters</span></span>
<span data-ttu-id="f4e8a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e8a-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e8a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f4e8a-135">INPUTS</span></span>

### <span data-ttu-id="f4e8a-136">IResourceGraphIdentity （ResourceGraph）的</span><span class="sxs-lookup"><span data-stu-id="f4e8a-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="f4e8a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f4e8a-137">OUTPUTS</span></span>

### <span data-ttu-id="f4e8a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f4e8a-138">System.Boolean</span></span>

## <span data-ttu-id="f4e8a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f4e8a-139">NOTES</span></span>

<span data-ttu-id="f4e8a-140">別名</span><span class="sxs-lookup"><span data-stu-id="f4e8a-140">ALIASES</span></span>

<span data-ttu-id="f4e8a-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f4e8a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4e8a-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4e8a-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4e8a-144">INPUTOBJECT <IResourceGraphIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f4e8a-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4e8a-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f4e8a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4e8a-146">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f4e8a-147">`[ResourceName <String>]`：圖表查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="f4e8a-148">`[SubscriptionId <String>]`： Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="f4e8a-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="f4e8a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4e8a-149">RELATED LINKS</span></span>

