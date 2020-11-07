---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: ad9c032a4384a82e03704529796a209e8c88f4c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959757"
---
# <span data-ttu-id="b2894-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b2894-101">New-AzIotHub</span></span>

## <span data-ttu-id="b2894-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2894-102">SYNOPSIS</span></span>
<span data-ttu-id="b2894-103">建立新的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="b2894-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="b2894-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2894-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2894-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2894-105">DESCRIPTION</span></span>
<span data-ttu-id="b2894-106">建立新的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="b2894-106">Creates a new IotHub.</span></span>
<span data-ttu-id="b2894-107">您可以使用預設屬性建立 IotHub，或指定輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="b2894-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="b2894-108">示例</span><span class="sxs-lookup"><span data-stu-id="b2894-108">EXAMPLES</span></span>

### <span data-ttu-id="b2894-109">範例1使用預設屬性建立新的 IotHub</span><span class="sxs-lookup"><span data-stu-id="b2894-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="b2894-110">在 sku "S1" （容量1和位置 "northeurope"）中，建立名為 "myiothub" 的新 IotHub。</span><span class="sxs-lookup"><span data-stu-id="b2894-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="b2894-111">範例2使用 CloudToDevice 佇列的 MaxDeliveryCount 設定為20來建立新的 IotHub</span><span class="sxs-lookup"><span data-stu-id="b2894-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="b2894-112">使用 $properties 所代表的高級輸入屬性，建立 sku "S1" （容量1和位置 "northeurope"）的新 IotHub （名為 "myiothub"）。</span><span class="sxs-lookup"><span data-stu-id="b2894-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="b2894-113">$psCloudToDeviceProperties = New-Object MaxDeliveryCount PSCloudToDeviceProperties 屬性 @ {= 20} $properties = New-Object IotHub "PSIotHubInputProperties" CloudToDevice "ResourceGroupName"-myresourcegroup "myiothub"-單位 1-Location "SkuName"-屬性 $psCloudToDeviceProperties 的內容 New-AzIotHub 的內容 $properties 的名稱 "northeurope"-"S1"-單位 1-位置 ""</span><span class="sxs-lookup"><span data-stu-id="b2894-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="b2894-114">參數</span><span class="sxs-lookup"><span data-stu-id="b2894-114">PARAMETERS</span></span>

### <span data-ttu-id="b2894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2894-115">-DefaultProfile</span></span>
<span data-ttu-id="b2894-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b2894-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2894-117">-位置</span><span class="sxs-lookup"><span data-stu-id="b2894-117">-Location</span></span>
<span data-ttu-id="b2894-118">需要建立 IoT 中樞的位置。</span><span class="sxs-lookup"><span data-stu-id="b2894-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="b2894-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2894-119">-Name</span></span>
<span data-ttu-id="b2894-120">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b2894-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-121">-屬性</span><span class="sxs-lookup"><span data-stu-id="b2894-121">-Properties</span></span>
<span data-ttu-id="b2894-122">IoT 中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="b2894-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2894-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2894-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b2894-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b2894-125">-SkuName</span></span>
<span data-ttu-id="b2894-126">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="b2894-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-127">單位</span><span class="sxs-lookup"><span data-stu-id="b2894-127">-Units</span></span>
<span data-ttu-id="b2894-128">單位數量</span><span class="sxs-lookup"><span data-stu-id="b2894-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b2894-129">-Confirm</span></span>
<span data-ttu-id="b2894-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2894-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2894-131">-WhatIf</span></span>
<span data-ttu-id="b2894-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2894-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2894-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2894-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2894-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2894-134">CommonParameters</span></span>
<span data-ttu-id="b2894-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2894-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2894-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2894-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2894-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b2894-137">INPUTS</span></span>

### <span data-ttu-id="b2894-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b2894-138">System.String</span></span>

## <span data-ttu-id="b2894-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b2894-139">OUTPUTS</span></span>

### <span data-ttu-id="b2894-140">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b2894-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="b2894-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b2894-141">NOTES</span></span>

## <span data-ttu-id="b2894-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2894-142">RELATED LINKS</span></span>
