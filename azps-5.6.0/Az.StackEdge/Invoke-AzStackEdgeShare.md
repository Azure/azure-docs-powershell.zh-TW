---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: fc920e04ce3e031e25b0c27ec0998266f077840c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915190"
---
# <span data-ttu-id="196cc-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="196cc-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="196cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="196cc-102">SYNOPSIS</span></span>
<span data-ttu-id="196cc-103">在共用上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="196cc-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="196cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="196cc-104">SYNTAX</span></span>

### <span data-ttu-id="196cc-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="196cc-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="196cc-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="196cc-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196cc-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="196cc-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196cc-108">描述</span><span class="sxs-lookup"><span data-stu-id="196cc-108">DESCRIPTION</span></span>
<span data-ttu-id="196cc-109">**Invoke-AzStackEdgeShare** Cmdlet 會以動作來重新更新 Stack Edge 裝置上共用的資料。</span><span class="sxs-lookup"><span data-stu-id="196cc-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="196cc-110">例子</span><span class="sxs-lookup"><span data-stu-id="196cc-110">EXAMPLES</span></span>

### <span data-ttu-id="196cc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="196cc-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="196cc-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="196cc-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="196cc-113">參數</span><span class="sxs-lookup"><span data-stu-id="196cc-113">PARAMETERS</span></span>

### <span data-ttu-id="196cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="196cc-114">-AsJob</span></span>
<span data-ttu-id="196cc-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="196cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="196cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196cc-116">-DefaultProfile</span></span>
<span data-ttu-id="196cc-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="196cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196cc-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="196cc-118">-DeviceName</span></span>
<span data-ttu-id="196cc-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="196cc-119">Device Name</span></span>

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

### <span data-ttu-id="196cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="196cc-120">-InputObject</span></span>
<span data-ttu-id="196cc-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="196cc-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="196cc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="196cc-122">-Name</span></span>
<span data-ttu-id="196cc-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="196cc-123">Resource Name</span></span>

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

### <span data-ttu-id="196cc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196cc-124">-PassThru</span></span>
<span data-ttu-id="196cc-125">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="196cc-125">returns true if successful</span></span>

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

### <span data-ttu-id="196cc-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="196cc-126">-RefreshData</span></span>
<span data-ttu-id="196cc-127">重新使用雲端資料重新更新共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="196cc-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="196cc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196cc-128">-ResourceGroupName</span></span>
<span data-ttu-id="196cc-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="196cc-129">Resource Group Name</span></span>

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

### <span data-ttu-id="196cc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="196cc-130">-ResourceId</span></span>
<span data-ttu-id="196cc-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="196cc-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="196cc-132">-確認</span><span class="sxs-lookup"><span data-stu-id="196cc-132">-Confirm</span></span>
<span data-ttu-id="196cc-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="196cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196cc-134">-WhatIf</span></span>
<span data-ttu-id="196cc-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="196cc-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="196cc-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="196cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196cc-137">CommonParameters</span></span>
<span data-ttu-id="196cc-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="196cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196cc-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="196cc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196cc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="196cc-140">INPUTS</span></span>

### <span data-ttu-id="196cc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="196cc-141">System.String</span></span>

### <span data-ttu-id="196cc-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="196cc-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="196cc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="196cc-143">OUTPUTS</span></span>

### <span data-ttu-id="196cc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="196cc-144">System.Boolean</span></span>

## <span data-ttu-id="196cc-145">筆記</span><span class="sxs-lookup"><span data-stu-id="196cc-145">NOTES</span></span>

## <span data-ttu-id="196cc-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="196cc-146">RELATED LINKS</span></span>
