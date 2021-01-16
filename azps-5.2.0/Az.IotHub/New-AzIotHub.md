---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275851"
---
# <span data-ttu-id="de6b8-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="de6b8-101">New-AzIotHub</span></span>

## <span data-ttu-id="de6b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="de6b8-103">建立新的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="de6b8-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="de6b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="de6b8-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de6b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="de6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="de6b8-106">建立新的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="de6b8-106">Creates a new IotHub.</span></span>
<span data-ttu-id="de6b8-107">您可以使用預設屬性建立 IotHub，或指定輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="de6b8-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="de6b8-108">示例</span><span class="sxs-lookup"><span data-stu-id="de6b8-108">EXAMPLES</span></span>

### <span data-ttu-id="de6b8-109">範例1使用預設屬性建立新的 IotHub</span><span class="sxs-lookup"><span data-stu-id="de6b8-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="de6b8-110">建立一個名為 "myiothub" 的新 IotHub，該名稱為 "S1"，容量1和位置 "northeurope" 包含在標記中。</span><span class="sxs-lookup"><span data-stu-id="de6b8-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="de6b8-111">範例2使用 CloudToDevice 佇列的 MaxDeliveryCount 設定為20來建立新的 IotHub</span><span class="sxs-lookup"><span data-stu-id="de6b8-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="de6b8-112">使用 $properties 所代表的高級輸入屬性，建立 sku "S1" （容量1和位置 "northeurope"）的新 IotHub （名為 "myiothub"）。</span><span class="sxs-lookup"><span data-stu-id="de6b8-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="de6b8-113">$psCloudToDeviceProperties = New-Object MaxDeliveryCount PSCloudToDeviceProperties 屬性 @ {= 20} $properties = New-Object IotHub "PSIotHubInputProperties" CloudToDevice "ResourceGroupName"-myresourcegroup "myiothub"-單位 1-Location "SkuName"-屬性 $psCloudToDeviceProperties 的內容 New-AzIotHub 的內容 $properties 的名稱 "northeurope"-"S1"-單位 1-位置 ""</span><span class="sxs-lookup"><span data-stu-id="de6b8-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="de6b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="de6b8-114">PARAMETERS</span></span>

### <span data-ttu-id="de6b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6b8-115">-DefaultProfile</span></span>
<span data-ttu-id="de6b8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="de6b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de6b8-117">-位置</span><span class="sxs-lookup"><span data-stu-id="de6b8-117">-Location</span></span>
<span data-ttu-id="de6b8-118">需要建立 IoT 中樞的位置。</span><span class="sxs-lookup"><span data-stu-id="de6b8-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="de6b8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="de6b8-119">-Name</span></span>
<span data-ttu-id="de6b8-120">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="de6b8-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="de6b8-121">-屬性</span><span class="sxs-lookup"><span data-stu-id="de6b8-121">-Properties</span></span>
<span data-ttu-id="de6b8-122">IoT 中樞的屬性。</span><span class="sxs-lookup"><span data-stu-id="de6b8-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="de6b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="de6b8-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="de6b8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="de6b8-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="de6b8-125">-SkuName</span></span>
<span data-ttu-id="de6b8-126">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="de6b8-126">Name of the sku</span></span>

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

### <span data-ttu-id="de6b8-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="de6b8-127">-Tag</span></span>
<span data-ttu-id="de6b8-128">IoT 中心實例標記。</span><span class="sxs-lookup"><span data-stu-id="de6b8-128">IoT hub instance tags.</span></span> <span data-ttu-id="de6b8-129">雜湊資料表形式的索引鍵值對中的屬性包。</span><span class="sxs-lookup"><span data-stu-id="de6b8-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="de6b8-130">單位</span><span class="sxs-lookup"><span data-stu-id="de6b8-130">-Units</span></span>
<span data-ttu-id="de6b8-131">單位數量</span><span class="sxs-lookup"><span data-stu-id="de6b8-131">Number of units</span></span>

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

### <span data-ttu-id="de6b8-132">-確認</span><span class="sxs-lookup"><span data-stu-id="de6b8-132">-Confirm</span></span>
<span data-ttu-id="de6b8-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de6b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de6b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6b8-134">-WhatIf</span></span>
<span data-ttu-id="de6b8-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de6b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6b8-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de6b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de6b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6b8-137">CommonParameters</span></span>
<span data-ttu-id="de6b8-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de6b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6b8-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de6b8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6b8-140">輸入</span><span class="sxs-lookup"><span data-stu-id="de6b8-140">INPUTS</span></span>

### <span data-ttu-id="de6b8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="de6b8-141">System.String</span></span>

## <span data-ttu-id="de6b8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="de6b8-142">OUTPUTS</span></span>

### <span data-ttu-id="de6b8-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="de6b8-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="de6b8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="de6b8-144">NOTES</span></span>

## <span data-ttu-id="de6b8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="de6b8-145">RELATED LINKS</span></span>
