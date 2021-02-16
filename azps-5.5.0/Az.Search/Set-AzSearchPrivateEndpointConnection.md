---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141810"
---
# <span data-ttu-id="814ba-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="814ba-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="814ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="814ba-102">SYNOPSIS</span></span>
<span data-ttu-id="814ba-103">更新連線至 Azure 認知搜尋服務的專用端點連線。</span><span class="sxs-lookup"><span data-stu-id="814ba-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="814ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="814ba-104">SYNTAX</span></span>

### <span data-ttu-id="814ba-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="814ba-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814ba-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="814ba-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="814ba-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814ba-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="814ba-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="814ba-109">說明</span><span class="sxs-lookup"><span data-stu-id="814ba-109">DESCRIPTION</span></span>
<span data-ttu-id="814ba-110">**AzSearchPrivateEndpointConnection** 會將私人端點連線更新為 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="814ba-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="814ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="814ba-111">EXAMPLES</span></span>

### <span data-ttu-id="814ba-112">範例1</span><span class="sxs-lookup"><span data-stu-id="814ba-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="814ba-113">這個範例會將 Azure 認知搜尋服務的私人端點線上狀態更新為「已拒絕」。</span><span class="sxs-lookup"><span data-stu-id="814ba-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="814ba-114">參數</span><span class="sxs-lookup"><span data-stu-id="814ba-114">PARAMETERS</span></span>

### <span data-ttu-id="814ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814ba-115">-DefaultProfile</span></span>
<span data-ttu-id="814ba-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="814ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="814ba-117">-描述</span><span class="sxs-lookup"><span data-stu-id="814ba-117">-Description</span></span>
<span data-ttu-id="814ba-118">私人端點連接描述</span><span class="sxs-lookup"><span data-stu-id="814ba-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="814ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="814ba-119">-InputObject</span></span>
<span data-ttu-id="814ba-120">私人端點連接輸入物件</span><span class="sxs-lookup"><span data-stu-id="814ba-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="814ba-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="814ba-121">-Name</span></span>
<span data-ttu-id="814ba-122">Azure 認知搜尋服務私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="814ba-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814ba-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="814ba-123">-ParentObject</span></span>
<span data-ttu-id="814ba-124">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="814ba-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="814ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="814ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="814ba-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="814ba-126">Resource Group name.</span></span>

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

### <span data-ttu-id="814ba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="814ba-127">-ResourceId</span></span>
<span data-ttu-id="814ba-128">私人連結服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="814ba-128">Private link service resource id</span></span>

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

### <span data-ttu-id="814ba-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="814ba-129">-ServiceName</span></span>
<span data-ttu-id="814ba-130">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="814ba-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="814ba-131">-狀態</span><span class="sxs-lookup"><span data-stu-id="814ba-131">-Status</span></span>
<span data-ttu-id="814ba-132">私人連結服務線上狀態</span><span class="sxs-lookup"><span data-stu-id="814ba-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814ba-133">-確認</span><span class="sxs-lookup"><span data-stu-id="814ba-133">-Confirm</span></span>
<span data-ttu-id="814ba-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="814ba-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814ba-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814ba-135">-WhatIf</span></span>
<span data-ttu-id="814ba-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="814ba-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="814ba-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="814ba-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814ba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814ba-138">CommonParameters</span></span>
<span data-ttu-id="814ba-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="814ba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814ba-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="814ba-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814ba-141">輸入</span><span class="sxs-lookup"><span data-stu-id="814ba-141">INPUTS</span></span>

### <span data-ttu-id="814ba-142">System.object</span><span class="sxs-lookup"><span data-stu-id="814ba-142">System.String</span></span>

## <span data-ttu-id="814ba-143">輸出</span><span class="sxs-lookup"><span data-stu-id="814ba-143">OUTPUTS</span></span>

### <span data-ttu-id="814ba-144">[PSPrivateEndpointConnection]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="814ba-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="814ba-145">筆記</span><span class="sxs-lookup"><span data-stu-id="814ba-145">NOTES</span></span>

## <span data-ttu-id="814ba-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="814ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="814ba-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="814ba-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="814ba-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="814ba-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
