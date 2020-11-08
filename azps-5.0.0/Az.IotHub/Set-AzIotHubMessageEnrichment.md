---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141693"
---
# <span data-ttu-id="851ce-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="851ce-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="851ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="851ce-102">SYNOPSIS</span></span>
<span data-ttu-id="851ce-103">在您的 IoT hub 中更新郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="851ce-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="851ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="851ce-104">SYNTAX</span></span>

### <span data-ttu-id="851ce-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="851ce-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="851ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="851ce-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="851ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="851ce-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="851ce-108">說明</span><span class="sxs-lookup"><span data-stu-id="851ce-108">DESCRIPTION</span></span>
<span data-ttu-id="851ce-109">如需 Azure IoT 中樞中郵件 enrichments 的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="851ce-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="851ce-110">示例</span><span class="sxs-lookup"><span data-stu-id="851ce-110">EXAMPLES</span></span>

### <span data-ttu-id="851ce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="851ce-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="851ce-112">針對鍵 "newKey"，將擴充的值更新為 "updatedValue"。</span><span class="sxs-lookup"><span data-stu-id="851ce-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="851ce-113">如需 Azure IoT 中樞中郵件 enrichments 的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="851ce-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="851ce-114">範例2</span><span class="sxs-lookup"><span data-stu-id="851ce-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="851ce-115">將擴充的端點更新為 [endpoint1，endpoint2，endpoint3 "（主要為" newKey "）。</span><span class="sxs-lookup"><span data-stu-id="851ce-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="851ce-116">如需 Azure IoT 中樞中郵件 enrichments 的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="851ce-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="851ce-117">參數</span><span class="sxs-lookup"><span data-stu-id="851ce-117">PARAMETERS</span></span>

### <span data-ttu-id="851ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851ce-118">-DefaultProfile</span></span>
<span data-ttu-id="851ce-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="851ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851ce-120">-端點</span><span class="sxs-lookup"><span data-stu-id="851ce-120">-Endpoint</span></span>
<span data-ttu-id="851ce-121">要將 enrichments 套用至的端點 (s) 。</span><span class="sxs-lookup"><span data-stu-id="851ce-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ce-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="851ce-122">-InputObject</span></span>
<span data-ttu-id="851ce-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="851ce-123">IotHub Object</span></span>

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

### <span data-ttu-id="851ce-124">-鍵</span><span class="sxs-lookup"><span data-stu-id="851ce-124">-Key</span></span>
<span data-ttu-id="851ce-125">擴充的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="851ce-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="851ce-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="851ce-126">-Name</span></span>
<span data-ttu-id="851ce-127">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="851ce-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="851ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="851ce-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="851ce-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="851ce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="851ce-130">-ResourceId</span></span>
<span data-ttu-id="851ce-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="851ce-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="851ce-132">-值</span><span class="sxs-lookup"><span data-stu-id="851ce-132">-Value</span></span>
<span data-ttu-id="851ce-133">擴充的值。</span><span class="sxs-lookup"><span data-stu-id="851ce-133">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ce-134">-確認</span><span class="sxs-lookup"><span data-stu-id="851ce-134">-Confirm</span></span>
<span data-ttu-id="851ce-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="851ce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="851ce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="851ce-136">-WhatIf</span></span>
<span data-ttu-id="851ce-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="851ce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="851ce-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="851ce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="851ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851ce-139">CommonParameters</span></span>
<span data-ttu-id="851ce-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="851ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851ce-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="851ce-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851ce-142">輸入</span><span class="sxs-lookup"><span data-stu-id="851ce-142">INPUTS</span></span>

### <span data-ttu-id="851ce-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="851ce-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="851ce-144">System.object</span><span class="sxs-lookup"><span data-stu-id="851ce-144">System.String</span></span>

## <span data-ttu-id="851ce-145">輸出</span><span class="sxs-lookup"><span data-stu-id="851ce-145">OUTPUTS</span></span>

### <span data-ttu-id="851ce-146">PSEnrichmentMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="851ce-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="851ce-147">筆記</span><span class="sxs-lookup"><span data-stu-id="851ce-147">NOTES</span></span>

## <span data-ttu-id="851ce-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="851ce-148">RELATED LINKS</span></span>
