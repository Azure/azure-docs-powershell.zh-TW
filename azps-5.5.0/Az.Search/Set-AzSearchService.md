---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 60969665c2989e026af3334e38e1d3035467b25b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128351"
---
# <span data-ttu-id="d76d8-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d76d8-101">Set-AzSearchService</span></span>

## <span data-ttu-id="d76d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d76d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d76d8-103">更新 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d76d8-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d76d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="d76d8-104">SYNTAX</span></span>

### <span data-ttu-id="d76d8-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d76d8-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76d8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76d8-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76d8-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="d76d8-108">DESCRIPTION</span></span>
<span data-ttu-id="d76d8-109">**AzSearchService** Cmdlet 會修改 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d76d8-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d76d8-110">示例</span><span class="sxs-lookup"><span data-stu-id="d76d8-110">EXAMPLES</span></span>

### <span data-ttu-id="d76d8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d76d8-111">Example 1</span></span>
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

<span data-ttu-id="d76d8-112">這個範例會將 Azure 認知搜尋服務的 [分區計數] 和 [複本計數] 變更為 [2]。</span><span class="sxs-lookup"><span data-stu-id="d76d8-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="d76d8-113">參數</span><span class="sxs-lookup"><span data-stu-id="d76d8-113">PARAMETERS</span></span>

### <span data-ttu-id="d76d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76d8-114">-DefaultProfile</span></span>
<span data-ttu-id="d76d8-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d76d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76d8-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d76d8-116">-IdentityType</span></span>
<span data-ttu-id="d76d8-117"> (選用) Azure 認知搜尋服務身分識別 (無/SystemAssigned) </span><span class="sxs-lookup"><span data-stu-id="d76d8-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="d76d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d76d8-118">-InputObject</span></span>
<span data-ttu-id="d76d8-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d76d8-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="d76d8-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="d76d8-120">-IPRuleList</span></span>
<span data-ttu-id="d76d8-121"> (選用) Azure 認知搜尋服務 IP 規則</span><span class="sxs-lookup"><span data-stu-id="d76d8-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="d76d8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d76d8-122">-Name</span></span>
<span data-ttu-id="d76d8-123">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d76d8-123">Search Service name.</span></span>

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

### <span data-ttu-id="d76d8-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="d76d8-124">-PartitionCount</span></span>
<span data-ttu-id="d76d8-125">搜尋服務分區計數。</span><span class="sxs-lookup"><span data-stu-id="d76d8-125">Search Service partition count.</span></span>

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

### <span data-ttu-id="d76d8-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d76d8-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="d76d8-127"> (選用) Azure 認知搜尋服務公用網路存取 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="d76d8-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="d76d8-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d76d8-128">-ReplicaCount</span></span>
<span data-ttu-id="d76d8-129">搜尋服務複本計數。</span><span class="sxs-lookup"><span data-stu-id="d76d8-129">Search Service replica count.</span></span>

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

### <span data-ttu-id="d76d8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76d8-130">-ResourceGroupName</span></span>
<span data-ttu-id="d76d8-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d76d8-131">Resource Group name.</span></span>

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

### <span data-ttu-id="d76d8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d76d8-132">-ResourceId</span></span>
<span data-ttu-id="d76d8-133">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d76d8-133">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d76d8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d76d8-134">-Confirm</span></span>
<span data-ttu-id="d76d8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d76d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76d8-136">-WhatIf</span></span>
<span data-ttu-id="d76d8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d76d8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d76d8-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d76d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76d8-139">CommonParameters</span></span>
<span data-ttu-id="d76d8-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d76d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76d8-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d76d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76d8-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d76d8-142">INPUTS</span></span>

### <span data-ttu-id="d76d8-143">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d76d8-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d76d8-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d76d8-144">System.String</span></span>

## <span data-ttu-id="d76d8-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d76d8-145">OUTPUTS</span></span>

### <span data-ttu-id="d76d8-146">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d76d8-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d76d8-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d76d8-147">NOTES</span></span>

## <span data-ttu-id="d76d8-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="d76d8-148">RELATED LINKS</span></span>

[<span data-ttu-id="d76d8-149">新-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d76d8-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="d76d8-150">AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d76d8-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="d76d8-151">移除-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d76d8-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)