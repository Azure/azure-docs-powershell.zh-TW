---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 2e024d3b82b6e553aa40bd6e570a848645538e11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913865"
---
# <span data-ttu-id="61d30-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="61d30-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="61d30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61d30-102">SYNOPSIS</span></span>
<span data-ttu-id="61d30-103">為 IoT 中心中所選端點建立郵件擴充功能。</span><span class="sxs-lookup"><span data-stu-id="61d30-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="61d30-104">語法</span><span class="sxs-lookup"><span data-stu-id="61d30-104">SYNTAX</span></span>

### <span data-ttu-id="61d30-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61d30-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d30-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="61d30-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61d30-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61d30-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d30-108">描述</span><span class="sxs-lookup"><span data-stu-id="61d30-108">DESCRIPTION</span></span>
<span data-ttu-id="61d30-109">每個 IoT 中心最多新增 10 封郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="61d30-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="61d30-110">這些會新增為應用程式屬性至郵件，以 (所選端點) 。</span><span class="sxs-lookup"><span data-stu-id="61d30-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="61d30-111">若要進一瞭解更多資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="61d30-111">To know more, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="61d30-112">例子</span><span class="sxs-lookup"><span data-stu-id="61d30-112">EXAMPLES</span></span>

### <span data-ttu-id="61d30-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="61d30-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="61d30-114">使用 Key "newKey" 和 value "newValue" 來新增擴充功能。</span><span class="sxs-lookup"><span data-stu-id="61d30-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="61d30-115">這項新的擴充功能會適用于「端點1」和「端點2」端點。</span><span class="sxs-lookup"><span data-stu-id="61d30-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="61d30-116">參數</span><span class="sxs-lookup"><span data-stu-id="61d30-116">PARAMETERS</span></span>

### <span data-ttu-id="61d30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d30-117">-DefaultProfile</span></span>
<span data-ttu-id="61d30-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61d30-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61d30-119">-端點</span><span class="sxs-lookup"><span data-stu-id="61d30-119">-Endpoint</span></span>
<span data-ttu-id="61d30-120">端點 () 的端點。</span><span class="sxs-lookup"><span data-stu-id="61d30-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="61d30-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61d30-121">-InputObject</span></span>
<span data-ttu-id="61d30-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="61d30-122">IotHub object</span></span>

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

### <span data-ttu-id="61d30-123">-Key</span><span class="sxs-lookup"><span data-stu-id="61d30-123">-Key</span></span>
<span data-ttu-id="61d30-124">這是擴充的關鍵。</span><span class="sxs-lookup"><span data-stu-id="61d30-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="61d30-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="61d30-125">-Name</span></span>
<span data-ttu-id="61d30-126">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="61d30-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="61d30-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d30-127">-ResourceGroupName</span></span>
<span data-ttu-id="61d30-128">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="61d30-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="61d30-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61d30-129">-ResourceId</span></span>
<span data-ttu-id="61d30-130">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="61d30-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="61d30-131">-值</span><span class="sxs-lookup"><span data-stu-id="61d30-131">-Value</span></span>
<span data-ttu-id="61d30-132">這是擴充值。</span><span class="sxs-lookup"><span data-stu-id="61d30-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="61d30-133">-確認</span><span class="sxs-lookup"><span data-stu-id="61d30-133">-Confirm</span></span>
<span data-ttu-id="61d30-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61d30-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d30-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d30-135">-WhatIf</span></span>
<span data-ttu-id="61d30-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61d30-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d30-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61d30-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d30-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d30-138">CommonParameters</span></span>
<span data-ttu-id="61d30-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61d30-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d30-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="61d30-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d30-141">輸入</span><span class="sxs-lookup"><span data-stu-id="61d30-141">INPUTS</span></span>

### <span data-ttu-id="61d30-142">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="61d30-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="61d30-143">System.String</span><span class="sxs-lookup"><span data-stu-id="61d30-143">System.String</span></span>

## <span data-ttu-id="61d30-144">輸出</span><span class="sxs-lookup"><span data-stu-id="61d30-144">OUTPUTS</span></span>

### <span data-ttu-id="61d30-145">Microsoft.Azure.Commands.management.IotHub.models.PSEn用mentMetadata</span><span class="sxs-lookup"><span data-stu-id="61d30-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="61d30-146">筆記</span><span class="sxs-lookup"><span data-stu-id="61d30-146">NOTES</span></span>

## <span data-ttu-id="61d30-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="61d30-147">RELATED LINKS</span></span>
