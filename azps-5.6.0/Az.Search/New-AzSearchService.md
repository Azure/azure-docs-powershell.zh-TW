---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903422"
---
# <span data-ttu-id="0a4d5-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0a4d5-101">New-AzSearchService</span></span>

## <span data-ttu-id="0a4d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4d5-103">建立 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0a4d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a4d5-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a4d5-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a4d5-106">**New-AzSearchService** Cmdlet 會建立具有指定參數的 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="0a4d5-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a4d5-107">EXAMPLES</span></span>

### <span data-ttu-id="0a4d5-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0a4d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="0a4d5-109">該命令會建立 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0a4d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a4d5-110">PARAMETERS</span></span>

### <span data-ttu-id="0a4d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4d5-111">-DefaultProfile</span></span>
<span data-ttu-id="0a4d5-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a4d5-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="0a4d5-113">-HostingMode</span></span>
<span data-ttu-id="0a4d5-114">Azure 認知搜尋服務主機模式。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4d5-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0a4d5-115">-IdentityType</span></span>
<span data-ttu-id="0a4d5-116"> (Azure 認知) 搜尋服務身分識別的 (/SystemAssigned) </span><span class="sxs-lookup"><span data-stu-id="0a4d5-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="0a4d5-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="0a4d5-117">-IPRuleList</span></span>
<span data-ttu-id="0a4d5-118"> (Azure 認知) 服務 IP 規則中的選擇性選項</span><span class="sxs-lookup"><span data-stu-id="0a4d5-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="0a4d5-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0a4d5-119">-Location</span></span>
<span data-ttu-id="0a4d5-120">Azure 認知搜尋服務位置。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-120">Azure Cognitive Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4d5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a4d5-121">-Name</span></span>
<span data-ttu-id="0a4d5-122">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-122">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="0a4d5-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="0a4d5-123">-PartitionCount</span></span>
<span data-ttu-id="0a4d5-124">Azure 認知搜尋服務分割計數。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="0a4d5-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0a4d5-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="0a4d5-126"> (Azure 認知) 服務公用網路存取的選擇性 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="0a4d5-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="0a4d5-127">-複本計數</span><span class="sxs-lookup"><span data-stu-id="0a4d5-127">-ReplicaCount</span></span>
<span data-ttu-id="0a4d5-128">Azure 認知搜尋服務複本計數。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="0a4d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a4d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="0a4d5-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-130">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4d5-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="0a4d5-131">-Sku</span></span>
<span data-ttu-id="0a4d5-132">Azure 認知搜尋服務 SKU。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4d5-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0a4d5-133">-Confirm</span></span>
<span data-ttu-id="0a4d5-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a4d5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a4d5-135">-WhatIf</span></span>
<span data-ttu-id="0a4d5-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a4d5-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a4d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4d5-138">CommonParameters</span></span>
<span data-ttu-id="0a4d5-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a4d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4d5-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a4d5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4d5-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0a4d5-141">INPUTS</span></span>

### <span data-ttu-id="0a4d5-142">沒有</span><span class="sxs-lookup"><span data-stu-id="0a4d5-142">None</span></span>

## <span data-ttu-id="0a4d5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0a4d5-143">OUTPUTS</span></span>

### <span data-ttu-id="0a4d5-144">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0a4d5-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0a4d5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0a4d5-145">NOTES</span></span>

## <span data-ttu-id="0a4d5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a4d5-146">RELATED LINKS</span></span>

[<span data-ttu-id="0a4d5-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0a4d5-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0a4d5-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0a4d5-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="0a4d5-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0a4d5-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)