---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: a135a9bf994e2837351347a4cc741ed20b406a28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914861"
---
# <span data-ttu-id="88a95-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="88a95-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="88a95-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88a95-102">SYNOPSIS</span></span>
<span data-ttu-id="88a95-103">在共用上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="88a95-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="88a95-104">語法</span><span class="sxs-lookup"><span data-stu-id="88a95-104">SYNTAX</span></span>

### <span data-ttu-id="88a95-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88a95-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88a95-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88a95-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a95-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88a95-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a95-108">描述</span><span class="sxs-lookup"><span data-stu-id="88a95-108">DESCRIPTION</span></span>
<span data-ttu-id="88a95-109">**Invoke-AzDataBoxEdgeShare** Cmdlet 會以動作來重新更新 Data Box Edge 裝置上共用的資料。</span><span class="sxs-lookup"><span data-stu-id="88a95-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="88a95-110">例子</span><span class="sxs-lookup"><span data-stu-id="88a95-110">EXAMPLES</span></span>

### <span data-ttu-id="88a95-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="88a95-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="88a95-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="88a95-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="88a95-113">參數</span><span class="sxs-lookup"><span data-stu-id="88a95-113">PARAMETERS</span></span>

### <span data-ttu-id="88a95-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88a95-114">-AsJob</span></span>
<span data-ttu-id="88a95-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88a95-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88a95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a95-116">-DefaultProfile</span></span>
<span data-ttu-id="88a95-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88a95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="88a95-118">-DeviceName</span></span>
<span data-ttu-id="88a95-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="88a95-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88a95-120">-InputObject</span></span>
<span data-ttu-id="88a95-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="88a95-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="88a95-122">-Name</span></span>
<span data-ttu-id="88a95-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="88a95-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88a95-124">-PassThru</span></span>
<span data-ttu-id="88a95-125">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="88a95-125">returns true if successful</span></span>

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

### <span data-ttu-id="88a95-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="88a95-126">-RefreshData</span></span>
<span data-ttu-id="88a95-127">重新使用雲端資料重新更新共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="88a95-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="88a95-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a95-128">-ResourceGroupName</span></span>
<span data-ttu-id="88a95-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="88a95-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a95-130">-ResourceId</span></span>
<span data-ttu-id="88a95-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a95-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a95-132">-確認</span><span class="sxs-lookup"><span data-stu-id="88a95-132">-Confirm</span></span>
<span data-ttu-id="88a95-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="88a95-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a95-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a95-134">-WhatIf</span></span>
<span data-ttu-id="88a95-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88a95-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88a95-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88a95-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a95-137">CommonParameters</span></span>
<span data-ttu-id="88a95-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88a95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a95-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88a95-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a95-140">輸入</span><span class="sxs-lookup"><span data-stu-id="88a95-140">INPUTS</span></span>

### <span data-ttu-id="88a95-141">System.String</span><span class="sxs-lookup"><span data-stu-id="88a95-141">System.String</span></span>

### <span data-ttu-id="88a95-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="88a95-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="88a95-143">輸出</span><span class="sxs-lookup"><span data-stu-id="88a95-143">OUTPUTS</span></span>

### <span data-ttu-id="88a95-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88a95-144">System.Boolean</span></span>

## <span data-ttu-id="88a95-145">筆記</span><span class="sxs-lookup"><span data-stu-id="88a95-145">NOTES</span></span>

## <span data-ttu-id="88a95-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="88a95-146">RELATED LINKS</span></span>
