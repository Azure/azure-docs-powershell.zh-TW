---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 71f5e9805467bc285b991a9aa4ee289b3d807729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911006"
---
# <span data-ttu-id="dd433-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="dd433-101">New-AzIotHub</span></span>

## <span data-ttu-id="dd433-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd433-102">SYNOPSIS</span></span>
<span data-ttu-id="dd433-103">建立新 IotHub。</span><span class="sxs-lookup"><span data-stu-id="dd433-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="dd433-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd433-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd433-105">描述</span><span class="sxs-lookup"><span data-stu-id="dd433-105">DESCRIPTION</span></span>
<span data-ttu-id="dd433-106">建立新 IotHub。</span><span class="sxs-lookup"><span data-stu-id="dd433-106">Creates a new IotHub.</span></span>
<span data-ttu-id="dd433-107">您可以使用預設屬性或指定輸入屬性來建立 IotHub。</span><span class="sxs-lookup"><span data-stu-id="dd433-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="dd433-108">例子</span><span class="sxs-lookup"><span data-stu-id="dd433-108">EXAMPLES</span></span>

### <span data-ttu-id="dd433-109">範例 1 使用預設屬性建立新 IotHub</span><span class="sxs-lookup"><span data-stu-id="dd433-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="dd433-110">建立新 IotHub，名稱為 sKU "S1" 的 "myiothub"，容量 1 且位置 "northeurope" 包含在 Tags 中。</span><span class="sxs-lookup"><span data-stu-id="dd433-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="dd433-111">範例 2 使用 CloudToDevice 佇列設為 20 的 MaxDeliveryCount 建立新 IotHub</span><span class="sxs-lookup"><span data-stu-id="dd433-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="dd433-112">建立 SKU "S1" 的名為 "myiothub" 的新 IotHub，容量 1 和位置 "northeurope" 由 $properties。</span><span class="sxs-lookup"><span data-stu-id="dd433-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="dd433-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.management.IotHub.models.PSCloudToDeviceProperties -property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.management.IotHub.models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="dd433-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="dd433-114">參數</span><span class="sxs-lookup"><span data-stu-id="dd433-114">PARAMETERS</span></span>

### <span data-ttu-id="dd433-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd433-115">-DefaultProfile</span></span>
<span data-ttu-id="dd433-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dd433-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd433-117">-位置</span><span class="sxs-lookup"><span data-stu-id="dd433-117">-Location</span></span>
<span data-ttu-id="dd433-118">需要建立 IoT 中樞的位置。</span><span class="sxs-lookup"><span data-stu-id="dd433-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="dd433-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd433-119">-Name</span></span>
<span data-ttu-id="dd433-120">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="dd433-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="dd433-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="dd433-121">-Properties</span></span>
<span data-ttu-id="dd433-122">IoT 中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd433-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="dd433-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd433-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd433-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="dd433-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dd433-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="dd433-125">-SkuName</span></span>
<span data-ttu-id="dd433-126">SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="dd433-126">Name of the sku</span></span>

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

### <span data-ttu-id="dd433-127">-標記</span><span class="sxs-lookup"><span data-stu-id="dd433-127">-Tag</span></span>
<span data-ttu-id="dd433-128">IoT 中樞實例標記。</span><span class="sxs-lookup"><span data-stu-id="dd433-128">IoT hub instance tags.</span></span> <span data-ttu-id="dd433-129">以雜湊表格形式，以索引鍵值組表示的屬性包。</span><span class="sxs-lookup"><span data-stu-id="dd433-129">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd433-130">-單位</span><span class="sxs-lookup"><span data-stu-id="dd433-130">-Units</span></span>
<span data-ttu-id="dd433-131">單位數</span><span class="sxs-lookup"><span data-stu-id="dd433-131">Number of units</span></span>

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

### <span data-ttu-id="dd433-132">-確認</span><span class="sxs-lookup"><span data-stu-id="dd433-132">-Confirm</span></span>
<span data-ttu-id="dd433-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd433-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd433-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd433-134">-WhatIf</span></span>
<span data-ttu-id="dd433-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd433-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd433-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd433-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd433-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd433-137">CommonParameters</span></span>
<span data-ttu-id="dd433-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd433-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd433-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dd433-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd433-140">輸入</span><span class="sxs-lookup"><span data-stu-id="dd433-140">INPUTS</span></span>

### <span data-ttu-id="dd433-141">System.String</span><span class="sxs-lookup"><span data-stu-id="dd433-141">System.String</span></span>

## <span data-ttu-id="dd433-142">輸出</span><span class="sxs-lookup"><span data-stu-id="dd433-142">OUTPUTS</span></span>

### <span data-ttu-id="dd433-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd433-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="dd433-144">筆記</span><span class="sxs-lookup"><span data-stu-id="dd433-144">NOTES</span></span>

## <span data-ttu-id="dd433-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd433-145">RELATED LINKS</span></span>
