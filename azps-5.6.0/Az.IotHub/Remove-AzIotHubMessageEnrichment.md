---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: f7f163326c0ade9b2837bd732eded2ea67731fea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916133"
---
# <span data-ttu-id="938e4-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="938e4-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="938e4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="938e4-102">SYNOPSIS</span></span>
<span data-ttu-id="938e4-103">刪除 IoT 中樞中的郵件擴充功能。</span><span class="sxs-lookup"><span data-stu-id="938e4-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="938e4-104">語法</span><span class="sxs-lookup"><span data-stu-id="938e4-104">SYNTAX</span></span>

### <span data-ttu-id="938e4-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="938e4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="938e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="938e4-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="938e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="938e4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="938e4-108">描述</span><span class="sxs-lookup"><span data-stu-id="938e4-108">DESCRIPTION</span></span>
<span data-ttu-id="938e4-109">有關 Azure IoT Hub 中郵件擴充的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="938e4-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="938e4-110">例子</span><span class="sxs-lookup"><span data-stu-id="938e4-110">EXAMPLES</span></span>

### <span data-ttu-id="938e4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="938e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="938e4-112">刪除「newKey」郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="938e4-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="938e4-113">參數</span><span class="sxs-lookup"><span data-stu-id="938e4-113">PARAMETERS</span></span>

### <span data-ttu-id="938e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="938e4-114">-DefaultProfile</span></span>
<span data-ttu-id="938e4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="938e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="938e4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="938e4-116">-InputObject</span></span>
<span data-ttu-id="938e4-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="938e4-117">IotHub object</span></span>

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

### <span data-ttu-id="938e4-118">-Key</span><span class="sxs-lookup"><span data-stu-id="938e4-118">-Key</span></span>
<span data-ttu-id="938e4-119">這是擴充的關鍵。</span><span class="sxs-lookup"><span data-stu-id="938e4-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="938e4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="938e4-120">-Name</span></span>
<span data-ttu-id="938e4-121">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="938e4-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="938e4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="938e4-122">-PassThru</span></span>
<span data-ttu-id="938e4-123">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="938e4-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="938e4-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="938e4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="938e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="938e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="938e4-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="938e4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="938e4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="938e4-127">-ResourceId</span></span>
<span data-ttu-id="938e4-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="938e4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="938e4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="938e4-129">-Confirm</span></span>
<span data-ttu-id="938e4-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="938e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="938e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="938e4-131">-WhatIf</span></span>
<span data-ttu-id="938e4-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="938e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="938e4-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="938e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="938e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="938e4-134">CommonParameters</span></span>
<span data-ttu-id="938e4-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="938e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="938e4-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="938e4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="938e4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="938e4-137">INPUTS</span></span>

### <span data-ttu-id="938e4-138">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="938e4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="938e4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="938e4-139">System.String</span></span>

## <span data-ttu-id="938e4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="938e4-140">OUTPUTS</span></span>

### <span data-ttu-id="938e4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="938e4-141">System.Boolean</span></span>

## <span data-ttu-id="938e4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="938e4-142">NOTES</span></span>

## <span data-ttu-id="938e4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="938e4-143">RELATED LINKS</span></span>
