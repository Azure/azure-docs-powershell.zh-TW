---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907058"
---
# <span data-ttu-id="0d4b2-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-101">Set-AzSearchService</span></span>

## <span data-ttu-id="0d4b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4b2-103">更新 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0d4b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d4b2-104">SYNTAX</span></span>

### <span data-ttu-id="0d4b2-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0d4b2-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4b2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4b2-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4b2-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d4b2-108">描述</span><span class="sxs-lookup"><span data-stu-id="0d4b2-108">DESCRIPTION</span></span>
<span data-ttu-id="0d4b2-109">**Set-AzSearchService** Cmdlet 會修改 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0d4b2-110">例子</span><span class="sxs-lookup"><span data-stu-id="0d4b2-110">EXAMPLES</span></span>

### <span data-ttu-id="0d4b2-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0d4b2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="0d4b2-112">此範例將 Azure 認知搜尋服務的磁片分割計數和複本計數變更為 2。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="0d4b2-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d4b2-113">PARAMETERS</span></span>

### <span data-ttu-id="0d4b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4b2-114">-DefaultProfile</span></span>
<span data-ttu-id="0d4b2-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d4b2-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0d4b2-116">-IdentityType</span></span>
<span data-ttu-id="0d4b2-117"> (Azure 認知) 搜尋服務身分識別的 (/SystemAssigned) </span><span class="sxs-lookup"><span data-stu-id="0d4b2-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d4b2-118">-InputObject</span></span>
<span data-ttu-id="0d4b2-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="0d4b2-120">-IPRuleList</span></span>
<span data-ttu-id="0d4b2-121"> (Azure 認知) 服務 IP 規則中的選擇性選項</span><span class="sxs-lookup"><span data-stu-id="0d4b2-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d4b2-122">-Name</span></span>
<span data-ttu-id="0d4b2-123">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-123">Search Service name.</span></span>

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

### <span data-ttu-id="0d4b2-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="0d4b2-124">-PartitionCount</span></span>
<span data-ttu-id="0d4b2-125">搜尋服務磁碟分割計數。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-125">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0d4b2-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="0d4b2-127"> (Azure 認知) 服務公用網路存取的選擇性 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="0d4b2-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-128">-複本計數</span><span class="sxs-lookup"><span data-stu-id="0d4b2-128">-ReplicaCount</span></span>
<span data-ttu-id="0d4b2-129">搜尋服務複本計數。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-129">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4b2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4b2-130">-ResourceGroupName</span></span>
<span data-ttu-id="0d4b2-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-131">Resource Group name.</span></span>

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

### <span data-ttu-id="0d4b2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4b2-132">-ResourceId</span></span>
<span data-ttu-id="0d4b2-133">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-133">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="0d4b2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="0d4b2-134">-Confirm</span></span>
<span data-ttu-id="0d4b2-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d4b2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4b2-136">-WhatIf</span></span>
<span data-ttu-id="0d4b2-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d4b2-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d4b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4b2-139">CommonParameters</span></span>
<span data-ttu-id="0d4b2-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d4b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4b2-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d4b2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4b2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0d4b2-142">INPUTS</span></span>

### <span data-ttu-id="0d4b2-143">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0d4b2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0d4b2-144">System.String</span></span>

## <span data-ttu-id="0d4b2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="0d4b2-145">OUTPUTS</span></span>

### <span data-ttu-id="0d4b2-146">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0d4b2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0d4b2-147">NOTES</span></span>

## <span data-ttu-id="0d4b2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d4b2-148">RELATED LINKS</span></span>

[<span data-ttu-id="0d4b2-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0d4b2-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0d4b2-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0d4b2-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)