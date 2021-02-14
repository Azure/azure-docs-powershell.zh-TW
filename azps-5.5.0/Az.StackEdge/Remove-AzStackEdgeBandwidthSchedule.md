---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142926"
---
# <span data-ttu-id="c4beb-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="c4beb-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="c4beb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c4beb-103">移除頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="c4beb-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="c4beb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4beb-104">SYNTAX</span></span>

### <span data-ttu-id="c4beb-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c4beb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4beb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4beb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4beb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4beb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4beb-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4beb-108">DESCRIPTION</span></span>
<span data-ttu-id="c4beb-109">**AzStackEdgeBandwidthSchedule** Cmdlet 會移除堆疊邊緣裝置的頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="c4beb-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="c4beb-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4beb-110">EXAMPLES</span></span>

### <span data-ttu-id="c4beb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c4beb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="c4beb-112">參數</span><span class="sxs-lookup"><span data-stu-id="c4beb-112">PARAMETERS</span></span>

### <span data-ttu-id="c4beb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4beb-113">-AsJob</span></span>
<span data-ttu-id="c4beb-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4beb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4beb-115">-DefaultProfile</span></span>
<span data-ttu-id="c4beb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4beb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4beb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c4beb-117">-DeviceName</span></span>
<span data-ttu-id="c4beb-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="c4beb-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4beb-119">-InputObject</span></span>
<span data-ttu-id="c4beb-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="c4beb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4beb-121">-Name</span></span>
<span data-ttu-id="c4beb-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="c4beb-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4beb-123">-PassThru</span></span>
<span data-ttu-id="c4beb-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="c4beb-124">returns true if successful</span></span>

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

### <span data-ttu-id="c4beb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4beb-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4beb-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c4beb-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4beb-127">-ResourceId</span></span>
<span data-ttu-id="c4beb-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4beb-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c4beb-129">-Confirm</span></span>
<span data-ttu-id="c4beb-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4beb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4beb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4beb-131">-WhatIf</span></span>
<span data-ttu-id="c4beb-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4beb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4beb-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4beb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4beb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4beb-134">CommonParameters</span></span>
<span data-ttu-id="c4beb-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4beb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4beb-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4beb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4beb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c4beb-137">INPUTS</span></span>

### <span data-ttu-id="c4beb-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c4beb-138">System.String</span></span>

### <span data-ttu-id="c4beb-139">PSStackEdgeBandWidthSchedule （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="c4beb-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="c4beb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c4beb-140">OUTPUTS</span></span>

### <span data-ttu-id="c4beb-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c4beb-141">System.Boolean</span></span>

## <span data-ttu-id="c4beb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c4beb-142">NOTES</span></span>

## <span data-ttu-id="c4beb-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4beb-143">RELATED LINKS</span></span>
