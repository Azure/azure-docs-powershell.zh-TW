---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136370"
---
# <span data-ttu-id="0eef7-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0eef7-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="0eef7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eef7-102">SYNOPSIS</span></span>
<span data-ttu-id="0eef7-103">為您的 IoT 中樞中所選的端點建立郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="0eef7-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="0eef7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eef7-104">SYNTAX</span></span>

### <span data-ttu-id="0eef7-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0eef7-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eef7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0eef7-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eef7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0eef7-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eef7-108">說明</span><span class="sxs-lookup"><span data-stu-id="0eef7-108">DESCRIPTION</span></span>
<span data-ttu-id="0eef7-109">在每個 IoT 中樞中新增最多10個郵件 enrichments。</span><span class="sxs-lookup"><span data-stu-id="0eef7-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="0eef7-110">這些會新增為應用程式屬性，以將郵件傳送到所選的端點 (s) 。</span><span class="sxs-lookup"><span data-stu-id="0eef7-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="0eef7-111">若要深入瞭解，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="0eef7-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="0eef7-112">示例</span><span class="sxs-lookup"><span data-stu-id="0eef7-112">EXAMPLES</span></span>

### <span data-ttu-id="0eef7-113">範例1</span><span class="sxs-lookup"><span data-stu-id="0eef7-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="0eef7-114">新增具有索引鍵 "newKey" 和值 "newValue" 的新擴充。</span><span class="sxs-lookup"><span data-stu-id="0eef7-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="0eef7-115">這個新的擴充會套用至「endpoint1」和「endpoint2」端點。</span><span class="sxs-lookup"><span data-stu-id="0eef7-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="0eef7-116">參數</span><span class="sxs-lookup"><span data-stu-id="0eef7-116">PARAMETERS</span></span>

### <span data-ttu-id="0eef7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eef7-117">-DefaultProfile</span></span>
<span data-ttu-id="0eef7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0eef7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eef7-119">-端點</span><span class="sxs-lookup"><span data-stu-id="0eef7-119">-Endpoint</span></span>
<span data-ttu-id="0eef7-120">要將 enrichments 套用至的端點 (s) 。</span><span class="sxs-lookup"><span data-stu-id="0eef7-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eef7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eef7-121">-InputObject</span></span>
<span data-ttu-id="0eef7-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="0eef7-122">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eef7-123">-鍵</span><span class="sxs-lookup"><span data-stu-id="0eef7-123">-Key</span></span>
<span data-ttu-id="0eef7-124">擴充的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0eef7-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="0eef7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eef7-125">-Name</span></span>
<span data-ttu-id="0eef7-126">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="0eef7-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eef7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eef7-127">-ResourceGroupName</span></span>
<span data-ttu-id="0eef7-128">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="0eef7-128">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eef7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eef7-129">-ResourceId</span></span>
<span data-ttu-id="0eef7-130">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0eef7-130">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eef7-131">-值</span><span class="sxs-lookup"><span data-stu-id="0eef7-131">-Value</span></span>
<span data-ttu-id="0eef7-132">擴充的值。</span><span class="sxs-lookup"><span data-stu-id="0eef7-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="0eef7-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0eef7-133">-Confirm</span></span>
<span data-ttu-id="0eef7-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0eef7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eef7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eef7-135">-WhatIf</span></span>
<span data-ttu-id="0eef7-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eef7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eef7-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eef7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eef7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eef7-138">CommonParameters</span></span>
<span data-ttu-id="0eef7-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eef7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eef7-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0eef7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eef7-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0eef7-141">INPUTS</span></span>

### <span data-ttu-id="0eef7-142">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0eef7-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0eef7-143">System.object</span><span class="sxs-lookup"><span data-stu-id="0eef7-143">System.String</span></span>

## <span data-ttu-id="0eef7-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0eef7-144">OUTPUTS</span></span>

### <span data-ttu-id="0eef7-145">PSEnrichmentMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0eef7-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="0eef7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0eef7-146">NOTES</span></span>

## <span data-ttu-id="0eef7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eef7-147">RELATED LINKS</span></span>
