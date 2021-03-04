---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915486"
---
# <span data-ttu-id="3bb14-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3bb14-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="3bb14-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3bb14-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb14-103">更新 IoT 中樞中的郵件擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3bb14-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="3bb14-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bb14-104">SYNTAX</span></span>

### <span data-ttu-id="3bb14-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3bb14-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb14-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3bb14-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb14-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3bb14-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb14-108">描述</span><span class="sxs-lookup"><span data-stu-id="3bb14-108">DESCRIPTION</span></span>
<span data-ttu-id="3bb14-109">有關 Azure IoT Hub 中郵件擴充的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3bb14-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3bb14-110">例子</span><span class="sxs-lookup"><span data-stu-id="3bb14-110">EXAMPLES</span></span>

### <span data-ttu-id="3bb14-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3bb14-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="3bb14-112">將金鑰 "newKey" 的擴充值更新為 "updatedValue"。</span><span class="sxs-lookup"><span data-stu-id="3bb14-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="3bb14-113">有關 Azure IoT Hub 中郵件擴充的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3bb14-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="3bb14-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="3bb14-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="3bb14-115">將擴充的端點更新為金鑰"newKey"的"端點1、端點2、端點3"。</span><span class="sxs-lookup"><span data-stu-id="3bb14-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="3bb14-116">有關 Azure IoT Hub 中郵件擴充的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3bb14-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3bb14-117">參數</span><span class="sxs-lookup"><span data-stu-id="3bb14-117">PARAMETERS</span></span>

### <span data-ttu-id="3bb14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb14-118">-DefaultProfile</span></span>
<span data-ttu-id="3bb14-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bb14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb14-120">-端點</span><span class="sxs-lookup"><span data-stu-id="3bb14-120">-Endpoint</span></span>
<span data-ttu-id="3bb14-121">端點 () 的端點。</span><span class="sxs-lookup"><span data-stu-id="3bb14-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="3bb14-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb14-122">-InputObject</span></span>
<span data-ttu-id="3bb14-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="3bb14-123">IotHub Object</span></span>

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

### <span data-ttu-id="3bb14-124">-Key</span><span class="sxs-lookup"><span data-stu-id="3bb14-124">-Key</span></span>
<span data-ttu-id="3bb14-125">這是擴充的關鍵。</span><span class="sxs-lookup"><span data-stu-id="3bb14-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="3bb14-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bb14-126">-Name</span></span>
<span data-ttu-id="3bb14-127">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="3bb14-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3bb14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb14-128">-ResourceGroupName</span></span>
<span data-ttu-id="3bb14-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="3bb14-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3bb14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb14-130">-ResourceId</span></span>
<span data-ttu-id="3bb14-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3bb14-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3bb14-132">-值</span><span class="sxs-lookup"><span data-stu-id="3bb14-132">-Value</span></span>
<span data-ttu-id="3bb14-133">這是擴充值。</span><span class="sxs-lookup"><span data-stu-id="3bb14-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="3bb14-134">-確認</span><span class="sxs-lookup"><span data-stu-id="3bb14-134">-Confirm</span></span>
<span data-ttu-id="3bb14-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3bb14-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb14-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb14-136">-WhatIf</span></span>
<span data-ttu-id="3bb14-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bb14-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb14-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bb14-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb14-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb14-139">CommonParameters</span></span>
<span data-ttu-id="3bb14-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3bb14-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb14-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3bb14-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb14-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3bb14-142">INPUTS</span></span>

### <span data-ttu-id="3bb14-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3bb14-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3bb14-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3bb14-144">System.String</span></span>

## <span data-ttu-id="3bb14-145">輸出</span><span class="sxs-lookup"><span data-stu-id="3bb14-145">OUTPUTS</span></span>

### <span data-ttu-id="3bb14-146">Microsoft.Azure.Commands.management.IotHub.models.PSEn用mentMetadata</span><span class="sxs-lookup"><span data-stu-id="3bb14-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="3bb14-147">筆記</span><span class="sxs-lookup"><span data-stu-id="3bb14-147">NOTES</span></span>

## <span data-ttu-id="3bb14-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bb14-148">RELATED LINKS</span></span>
