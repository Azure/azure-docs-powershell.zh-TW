---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281034"
---
# <span data-ttu-id="ece85-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ece85-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ece85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ece85-102">SYNOPSIS</span></span>
<span data-ttu-id="ece85-103">移除頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="ece85-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="ece85-104">句法</span><span class="sxs-lookup"><span data-stu-id="ece85-104">SYNTAX</span></span>

### <span data-ttu-id="ece85-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ece85-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece85-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece85-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece85-108">說明</span><span class="sxs-lookup"><span data-stu-id="ece85-108">DESCRIPTION</span></span>
<span data-ttu-id="ece85-109">**AzDataBoxEdgeBandwidthSchedule** Cmdlet 會移除資料編輯方塊邊緣裝置的頻寬排程。</span><span class="sxs-lookup"><span data-stu-id="ece85-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="ece85-110">示例</span><span class="sxs-lookup"><span data-stu-id="ece85-110">EXAMPLES</span></span>

### <span data-ttu-id="ece85-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ece85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="ece85-112">參數</span><span class="sxs-lookup"><span data-stu-id="ece85-112">PARAMETERS</span></span>

### <span data-ttu-id="ece85-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ece85-113">-AsJob</span></span>
<span data-ttu-id="ece85-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ece85-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ece85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece85-115">-DefaultProfile</span></span>
<span data-ttu-id="ece85-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ece85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece85-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ece85-117">-DeviceName</span></span>
<span data-ttu-id="ece85-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="ece85-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ece85-119">-InputObject</span></span>
<span data-ttu-id="ece85-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="ece85-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ece85-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ece85-121">-Name</span></span>
<span data-ttu-id="ece85-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ece85-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece85-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece85-123">-PassThru</span></span>
<span data-ttu-id="ece85-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="ece85-124">returns true if successful</span></span>

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

### <span data-ttu-id="ece85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece85-125">-ResourceGroupName</span></span>
<span data-ttu-id="ece85-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ece85-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece85-127">-ResourceId</span></span>
<span data-ttu-id="ece85-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece85-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ece85-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ece85-129">-Confirm</span></span>
<span data-ttu-id="ece85-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ece85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece85-131">-WhatIf</span></span>
<span data-ttu-id="ece85-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ece85-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece85-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece85-134">CommonParameters</span></span>
<span data-ttu-id="ece85-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ece85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece85-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ece85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece85-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ece85-137">INPUTS</span></span>

### <span data-ttu-id="ece85-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ece85-138">System.String</span></span>

### <span data-ttu-id="ece85-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ece85-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ece85-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ece85-140">OUTPUTS</span></span>

### <span data-ttu-id="ece85-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ece85-141">System.Boolean</span></span>

## <span data-ttu-id="ece85-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ece85-142">NOTES</span></span>

## <span data-ttu-id="ece85-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ece85-143">RELATED LINKS</span></span>
