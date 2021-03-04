---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 0ed07bed894d31be68b8fd4b71605e94b19171ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914401"
---
# <span data-ttu-id="b27f9-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b27f9-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="b27f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b27f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b27f9-103">將私人端點 (Azure) Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="b27f9-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b27f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="b27f9-104">SYNTAX</span></span>

### <span data-ttu-id="b27f9-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b27f9-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27f9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b27f9-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27f9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b27f9-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27f9-108">描述</span><span class="sxs-lookup"><span data-stu-id="b27f9-108">DESCRIPTION</span></span>
<span data-ttu-id="b27f9-109">**Get-AzSearchPrivateEndpointConnection** Cmdlet 會取得私人端點 () Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="b27f9-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b27f9-110">例子</span><span class="sxs-lookup"><span data-stu-id="b27f9-110">EXAMPLES</span></span>

### <span data-ttu-id="b27f9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b27f9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="b27f9-112">此範例會獲得 Azure 認知搜尋服務的所有私人端點連結。</span><span class="sxs-lookup"><span data-stu-id="b27f9-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="b27f9-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b27f9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="b27f9-114">此範例會依名稱將特定私人端點 (轉換為 JSON，方便您) Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="b27f9-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b27f9-115">參數</span><span class="sxs-lookup"><span data-stu-id="b27f9-115">PARAMETERS</span></span>

### <span data-ttu-id="b27f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27f9-116">-DefaultProfile</span></span>
<span data-ttu-id="b27f9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b27f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27f9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b27f9-118">-Name</span></span>
<span data-ttu-id="b27f9-119">Azure 認知搜尋服務私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="b27f9-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27f9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b27f9-120">-ParentObject</span></span>
<span data-ttu-id="b27f9-121">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b27f9-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b27f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b27f9-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b27f9-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b27f9-124">-ResourceId</span></span>
<span data-ttu-id="b27f9-125">私人連結服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b27f9-125">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27f9-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b27f9-126">-ServiceName</span></span>
<span data-ttu-id="b27f9-127">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b27f9-127">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27f9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b27f9-128">-Confirm</span></span>
<span data-ttu-id="b27f9-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b27f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27f9-130">-WhatIf</span></span>
<span data-ttu-id="b27f9-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b27f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b27f9-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b27f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27f9-133">CommonParameters</span></span>
<span data-ttu-id="b27f9-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b27f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27f9-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b27f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27f9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b27f9-136">INPUTS</span></span>

### <span data-ttu-id="b27f9-137">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b27f9-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b27f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b27f9-138">System.String</span></span>

## <span data-ttu-id="b27f9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b27f9-139">OUTPUTS</span></span>

### <span data-ttu-id="b27f9-140">Microsoft.Azure.Commands.management.Search.models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b27f9-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="b27f9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b27f9-141">NOTES</span></span>

## <span data-ttu-id="b27f9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b27f9-142">RELATED LINKS</span></span>

[<span data-ttu-id="b27f9-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="b27f9-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="b27f9-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="b27f9-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
