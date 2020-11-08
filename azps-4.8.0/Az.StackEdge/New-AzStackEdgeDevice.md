---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129768"
---
# <span data-ttu-id="687f4-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="687f4-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="687f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="687f4-102">SYNOPSIS</span></span>
<span data-ttu-id="687f4-103">配置新的堆疊邊緣裝置</span><span class="sxs-lookup"><span data-stu-id="687f4-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="687f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="687f4-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="687f4-105">DESCRIPTION</span></span>
<span data-ttu-id="687f4-106">**新的 AzStackEdgeDevice** Cmdlet 會配置新的堆疊邊緣裝置</span><span class="sxs-lookup"><span data-stu-id="687f4-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="687f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="687f4-107">EXAMPLES</span></span>

### <span data-ttu-id="687f4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="687f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="687f4-109">參數</span><span class="sxs-lookup"><span data-stu-id="687f4-109">PARAMETERS</span></span>

### <span data-ttu-id="687f4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="687f4-110">-AsJob</span></span>
<span data-ttu-id="687f4-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="687f4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="687f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687f4-112">-DefaultProfile</span></span>
<span data-ttu-id="687f4-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="687f4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687f4-114">-位置</span><span class="sxs-lookup"><span data-stu-id="687f4-114">-Location</span></span>
<span data-ttu-id="687f4-115">裝置的位置</span><span class="sxs-lookup"><span data-stu-id="687f4-115">Location of the device</span></span>

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

### <span data-ttu-id="687f4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="687f4-116">-Name</span></span>
<span data-ttu-id="687f4-117">資源名稱</span><span class="sxs-lookup"><span data-stu-id="687f4-117">Resource Name</span></span>

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

### <span data-ttu-id="687f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="687f4-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="687f4-119">Resource Group Name</span></span>

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

### <span data-ttu-id="687f4-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="687f4-120">-Sku</span></span>
<span data-ttu-id="687f4-121">可用的 Sku 是 Edge、閘道</span><span class="sxs-lookup"><span data-stu-id="687f4-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="687f4-122">-確認</span><span class="sxs-lookup"><span data-stu-id="687f4-122">-Confirm</span></span>
<span data-ttu-id="687f4-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="687f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687f4-124">-WhatIf</span></span>
<span data-ttu-id="687f4-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="687f4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="687f4-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="687f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687f4-127">CommonParameters</span></span>
<span data-ttu-id="687f4-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="687f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687f4-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="687f4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687f4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="687f4-130">INPUTS</span></span>

### <span data-ttu-id="687f4-131">所有</span><span class="sxs-lookup"><span data-stu-id="687f4-131">None</span></span>

## <span data-ttu-id="687f4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="687f4-132">OUTPUTS</span></span>

### <span data-ttu-id="687f4-133">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="687f4-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="687f4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="687f4-134">NOTES</span></span>

## <span data-ttu-id="687f4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="687f4-135">RELATED LINKS</span></span>
