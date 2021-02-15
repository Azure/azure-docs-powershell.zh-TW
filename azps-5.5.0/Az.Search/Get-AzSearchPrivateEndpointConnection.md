---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142571"
---
# <span data-ttu-id="ddefa-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ddefa-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="ddefa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddefa-102">SYNOPSIS</span></span>
<span data-ttu-id="ddefa-103">取得) 至 Azure 認知搜尋服務的私人端點連線 (s。</span><span class="sxs-lookup"><span data-stu-id="ddefa-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ddefa-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddefa-104">SYNTAX</span></span>

### <span data-ttu-id="ddefa-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ddefa-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddefa-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddefa-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddefa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddefa-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddefa-108">說明</span><span class="sxs-lookup"><span data-stu-id="ddefa-108">DESCRIPTION</span></span>
<span data-ttu-id="ddefa-109">**AzSearchPrivateEndpointConnection** Cmdlet 會取得私人端點連線， (s) 至 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="ddefa-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ddefa-110">示例</span><span class="sxs-lookup"><span data-stu-id="ddefa-110">EXAMPLES</span></span>

### <span data-ttu-id="ddefa-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ddefa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="ddefa-112">此範例會取得 Azure 認知搜尋服務的所有私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="ddefa-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="ddefa-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ddefa-113">Example 2</span></span>
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

<span data-ttu-id="ddefa-114">這個範例會透過名稱 (轉換為 JSON 的特定私人端點連線，輕鬆閱讀) 至 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="ddefa-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ddefa-115">參數</span><span class="sxs-lookup"><span data-stu-id="ddefa-115">PARAMETERS</span></span>

### <span data-ttu-id="ddefa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddefa-116">-DefaultProfile</span></span>
<span data-ttu-id="ddefa-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddefa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddefa-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddefa-118">-Name</span></span>
<span data-ttu-id="ddefa-119">Azure 認知搜尋服務私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="ddefa-119">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="ddefa-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddefa-120">-ParentObject</span></span>
<span data-ttu-id="ddefa-121">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="ddefa-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="ddefa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddefa-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddefa-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ddefa-123">Resource Group name.</span></span>

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

### <span data-ttu-id="ddefa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddefa-124">-ResourceId</span></span>
<span data-ttu-id="ddefa-125">私人連結服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ddefa-125">Private link service resource id</span></span>

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

### <span data-ttu-id="ddefa-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ddefa-126">-ServiceName</span></span>
<span data-ttu-id="ddefa-127">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ddefa-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="ddefa-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ddefa-128">-Confirm</span></span>
<span data-ttu-id="ddefa-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddefa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddefa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddefa-130">-WhatIf</span></span>
<span data-ttu-id="ddefa-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddefa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddefa-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddefa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddefa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddefa-133">CommonParameters</span></span>
<span data-ttu-id="ddefa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddefa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddefa-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ddefa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddefa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ddefa-136">INPUTS</span></span>

### <span data-ttu-id="ddefa-137">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ddefa-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ddefa-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ddefa-138">System.String</span></span>

## <span data-ttu-id="ddefa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ddefa-139">OUTPUTS</span></span>

### <span data-ttu-id="ddefa-140">[PSPrivateEndpointConnection]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ddefa-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="ddefa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ddefa-141">NOTES</span></span>

## <span data-ttu-id="ddefa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddefa-142">RELATED LINKS</span></span>

[<span data-ttu-id="ddefa-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="ddefa-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="ddefa-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="ddefa-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
