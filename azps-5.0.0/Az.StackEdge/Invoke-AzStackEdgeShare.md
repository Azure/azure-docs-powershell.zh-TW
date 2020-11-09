---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287184"
---
# <span data-ttu-id="0dfe6-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0dfe6-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="0dfe6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfe6-103">在共用上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="0dfe6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dfe6-104">SYNTAX</span></span>

### <span data-ttu-id="0dfe6-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0dfe6-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dfe6-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dfe6-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dfe6-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dfe6-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dfe6-108">說明</span><span class="sxs-lookup"><span data-stu-id="0dfe6-108">DESCRIPTION</span></span>
<span data-ttu-id="0dfe6-109">**AzStackEdgeShare** Cmdlet 會呼叫 action，以重新整理堆疊 Edge 裝置上共用的資料。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="0dfe6-110">示例</span><span class="sxs-lookup"><span data-stu-id="0dfe6-110">EXAMPLES</span></span>

### <span data-ttu-id="0dfe6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0dfe6-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="0dfe6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="0dfe6-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="0dfe6-113">參數</span><span class="sxs-lookup"><span data-stu-id="0dfe6-113">PARAMETERS</span></span>

### <span data-ttu-id="0dfe6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dfe6-114">-AsJob</span></span>
<span data-ttu-id="0dfe6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0dfe6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dfe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfe6-116">-DefaultProfile</span></span>
<span data-ttu-id="0dfe6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dfe6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0dfe6-118">-DeviceName</span></span>
<span data-ttu-id="0dfe6-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe6-119">Device Name</span></span>

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

### <span data-ttu-id="0dfe6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dfe6-120">-InputObject</span></span>
<span data-ttu-id="0dfe6-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="0dfe6-121">Input Object</span></span>

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

### <span data-ttu-id="0dfe6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe6-122">-Name</span></span>
<span data-ttu-id="0dfe6-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe6-123">Resource Name</span></span>

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

### <span data-ttu-id="0dfe6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dfe6-124">-PassThru</span></span>
<span data-ttu-id="0dfe6-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="0dfe6-125">returns true if successful</span></span>

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

### <span data-ttu-id="0dfe6-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="0dfe6-126">-RefreshData</span></span>
<span data-ttu-id="0dfe6-127">使用雲端的資料重新整理共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="0dfe6-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="0dfe6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dfe6-128">-ResourceGroupName</span></span>
<span data-ttu-id="0dfe6-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0dfe6-129">Resource Group Name</span></span>

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

### <span data-ttu-id="0dfe6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dfe6-130">-ResourceId</span></span>
<span data-ttu-id="0dfe6-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dfe6-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0dfe6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0dfe6-132">-Confirm</span></span>
<span data-ttu-id="0dfe6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dfe6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfe6-134">-WhatIf</span></span>
<span data-ttu-id="0dfe6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dfe6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dfe6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfe6-137">CommonParameters</span></span>
<span data-ttu-id="0dfe6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfe6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dfe6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfe6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0dfe6-140">INPUTS</span></span>

### <span data-ttu-id="0dfe6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0dfe6-141">System.String</span></span>

### <span data-ttu-id="0dfe6-142">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="0dfe6-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="0dfe6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0dfe6-143">OUTPUTS</span></span>

### <span data-ttu-id="0dfe6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="0dfe6-144">System.Boolean</span></span>

## <span data-ttu-id="0dfe6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0dfe6-145">NOTES</span></span>

## <span data-ttu-id="0dfe6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dfe6-146">RELATED LINKS</span></span>
