---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959341"
---
# <span data-ttu-id="442ac-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="442ac-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="442ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="442ac-102">SYNOPSIS</span></span>
<span data-ttu-id="442ac-103">配置新的資料編輯方塊邊緣裝置</span><span class="sxs-lookup"><span data-stu-id="442ac-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="442ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="442ac-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="442ac-105">DESCRIPTION</span></span>
<span data-ttu-id="442ac-106">**新的 AzDataBoxEdgeDevice** Cmdlet 會設定新的資料盒 Edge 裝置</span><span class="sxs-lookup"><span data-stu-id="442ac-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="442ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="442ac-107">EXAMPLES</span></span>

### <span data-ttu-id="442ac-108">範例1</span><span class="sxs-lookup"><span data-stu-id="442ac-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="442ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="442ac-109">PARAMETERS</span></span>

### <span data-ttu-id="442ac-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="442ac-110">-AsJob</span></span>
<span data-ttu-id="442ac-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="442ac-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="442ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442ac-112">-DefaultProfile</span></span>
<span data-ttu-id="442ac-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="442ac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442ac-114">-位置</span><span class="sxs-lookup"><span data-stu-id="442ac-114">-Location</span></span>
<span data-ttu-id="442ac-115">裝置的位置</span><span class="sxs-lookup"><span data-stu-id="442ac-115">Location of the device</span></span>

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

### <span data-ttu-id="442ac-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="442ac-116">-Name</span></span>
<span data-ttu-id="442ac-117">資源名稱</span><span class="sxs-lookup"><span data-stu-id="442ac-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="442ac-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="442ac-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442ac-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="442ac-120">-Sku</span></span>
<span data-ttu-id="442ac-121">可用的 Sku 是 Edge、閘道</span><span class="sxs-lookup"><span data-stu-id="442ac-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="442ac-122">-確認</span><span class="sxs-lookup"><span data-stu-id="442ac-122">-Confirm</span></span>
<span data-ttu-id="442ac-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="442ac-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442ac-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442ac-124">-WhatIf</span></span>
<span data-ttu-id="442ac-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="442ac-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="442ac-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="442ac-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442ac-127">CommonParameters</span></span>
<span data-ttu-id="442ac-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="442ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442ac-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="442ac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442ac-130">輸入</span><span class="sxs-lookup"><span data-stu-id="442ac-130">INPUTS</span></span>

### <span data-ttu-id="442ac-131">所有</span><span class="sxs-lookup"><span data-stu-id="442ac-131">None</span></span>

## <span data-ttu-id="442ac-132">輸出</span><span class="sxs-lookup"><span data-stu-id="442ac-132">OUTPUTS</span></span>

### <span data-ttu-id="442ac-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="442ac-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="442ac-134">筆記</span><span class="sxs-lookup"><span data-stu-id="442ac-134">NOTES</span></span>

## <span data-ttu-id="442ac-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="442ac-135">RELATED LINKS</span></span>
