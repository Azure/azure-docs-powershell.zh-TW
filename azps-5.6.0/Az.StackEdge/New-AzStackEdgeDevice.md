---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: 1ad2719ae67c96088dde968d96ca7104436083e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909421"
---
# <span data-ttu-id="db646-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="db646-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="db646-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db646-102">SYNOPSIS</span></span>
<span data-ttu-id="db646-103">設定新的 Stack Edge 裝置</span><span class="sxs-lookup"><span data-stu-id="db646-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="db646-104">語法</span><span class="sxs-lookup"><span data-stu-id="db646-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db646-105">描述</span><span class="sxs-lookup"><span data-stu-id="db646-105">DESCRIPTION</span></span>
<span data-ttu-id="db646-106">**New-AzStackEdgeDevice Cmdlet** 會設定新的 Stack Edge 裝置</span><span class="sxs-lookup"><span data-stu-id="db646-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="db646-107">例子</span><span class="sxs-lookup"><span data-stu-id="db646-107">EXAMPLES</span></span>

### <span data-ttu-id="db646-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="db646-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="db646-109">參數</span><span class="sxs-lookup"><span data-stu-id="db646-109">PARAMETERS</span></span>

### <span data-ttu-id="db646-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db646-110">-AsJob</span></span>
<span data-ttu-id="db646-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db646-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db646-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db646-112">-DefaultProfile</span></span>
<span data-ttu-id="db646-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db646-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db646-114">-位置</span><span class="sxs-lookup"><span data-stu-id="db646-114">-Location</span></span>
<span data-ttu-id="db646-115">裝置位置</span><span class="sxs-lookup"><span data-stu-id="db646-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db646-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="db646-116">-Name</span></span>
<span data-ttu-id="db646-117">資源名稱</span><span class="sxs-lookup"><span data-stu-id="db646-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db646-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db646-118">-ResourceGroupName</span></span>
<span data-ttu-id="db646-119">資源組名</span><span class="sxs-lookup"><span data-stu-id="db646-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db646-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="db646-120">-Sku</span></span>
<span data-ttu-id="db646-121">可用的 SKU 為 Edge、閘道</span><span class="sxs-lookup"><span data-stu-id="db646-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db646-122">-確認</span><span class="sxs-lookup"><span data-stu-id="db646-122">-Confirm</span></span>
<span data-ttu-id="db646-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="db646-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db646-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db646-124">-WhatIf</span></span>
<span data-ttu-id="db646-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db646-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db646-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db646-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db646-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db646-127">CommonParameters</span></span>
<span data-ttu-id="db646-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db646-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db646-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db646-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db646-130">輸入</span><span class="sxs-lookup"><span data-stu-id="db646-130">INPUTS</span></span>

### <span data-ttu-id="db646-131">沒有</span><span class="sxs-lookup"><span data-stu-id="db646-131">None</span></span>

## <span data-ttu-id="db646-132">輸出</span><span class="sxs-lookup"><span data-stu-id="db646-132">OUTPUTS</span></span>

### <span data-ttu-id="db646-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="db646-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="db646-134">筆記</span><span class="sxs-lookup"><span data-stu-id="db646-134">NOTES</span></span>

## <span data-ttu-id="db646-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="db646-135">RELATED LINKS</span></span>
