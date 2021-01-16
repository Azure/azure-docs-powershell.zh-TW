---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279817"
---
# <span data-ttu-id="58a8d-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="58a8d-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="58a8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="58a8d-103">在共用上調用特定動作。</span><span class="sxs-lookup"><span data-stu-id="58a8d-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="58a8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="58a8d-104">SYNTAX</span></span>

### <span data-ttu-id="58a8d-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58a8d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58a8d-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a8d-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58a8d-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a8d-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="58a8d-108">DESCRIPTION</span></span>
<span data-ttu-id="58a8d-109">**AzStackEdgeShare** Cmdlet 會呼叫 action，以重新整理堆疊 Edge 裝置上共用的資料。</span><span class="sxs-lookup"><span data-stu-id="58a8d-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="58a8d-110">示例</span><span class="sxs-lookup"><span data-stu-id="58a8d-110">EXAMPLES</span></span>

### <span data-ttu-id="58a8d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="58a8d-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="58a8d-112">範例2</span><span class="sxs-lookup"><span data-stu-id="58a8d-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="58a8d-113">參數</span><span class="sxs-lookup"><span data-stu-id="58a8d-113">PARAMETERS</span></span>

### <span data-ttu-id="58a8d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58a8d-114">-AsJob</span></span>
<span data-ttu-id="58a8d-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58a8d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58a8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a8d-116">-DefaultProfile</span></span>
<span data-ttu-id="58a8d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58a8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a8d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="58a8d-118">-DeviceName</span></span>
<span data-ttu-id="58a8d-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="58a8d-119">Device Name</span></span>

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

### <span data-ttu-id="58a8d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58a8d-120">-InputObject</span></span>
<span data-ttu-id="58a8d-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="58a8d-121">Input Object</span></span>

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

### <span data-ttu-id="58a8d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="58a8d-122">-Name</span></span>
<span data-ttu-id="58a8d-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="58a8d-123">Resource Name</span></span>

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

### <span data-ttu-id="58a8d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58a8d-124">-PassThru</span></span>
<span data-ttu-id="58a8d-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="58a8d-125">returns true if successful</span></span>

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

### <span data-ttu-id="58a8d-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="58a8d-126">-RefreshData</span></span>
<span data-ttu-id="58a8d-127">使用雲端的資料重新整理共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="58a8d-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="58a8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="58a8d-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="58a8d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="58a8d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a8d-130">-ResourceId</span></span>
<span data-ttu-id="58a8d-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a8d-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="58a8d-132">-確認</span><span class="sxs-lookup"><span data-stu-id="58a8d-132">-Confirm</span></span>
<span data-ttu-id="58a8d-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58a8d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a8d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a8d-134">-WhatIf</span></span>
<span data-ttu-id="58a8d-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58a8d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58a8d-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58a8d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a8d-137">CommonParameters</span></span>
<span data-ttu-id="58a8d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58a8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a8d-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58a8d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a8d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="58a8d-140">INPUTS</span></span>

### <span data-ttu-id="58a8d-141">System.object</span><span class="sxs-lookup"><span data-stu-id="58a8d-141">System.String</span></span>

### <span data-ttu-id="58a8d-142">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="58a8d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="58a8d-143">輸出</span><span class="sxs-lookup"><span data-stu-id="58a8d-143">OUTPUTS</span></span>

### <span data-ttu-id="58a8d-144">System.object</span><span class="sxs-lookup"><span data-stu-id="58a8d-144">System.Boolean</span></span>

## <span data-ttu-id="58a8d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="58a8d-145">NOTES</span></span>

## <span data-ttu-id="58a8d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="58a8d-146">RELATED LINKS</span></span>
