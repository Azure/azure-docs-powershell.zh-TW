---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140595"
---
# <span data-ttu-id="74de1-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="74de1-101">New-AzSearchService</span></span>

## <span data-ttu-id="74de1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74de1-102">SYNOPSIS</span></span>
<span data-ttu-id="74de1-103">建立 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="74de1-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="74de1-104">句法</span><span class="sxs-lookup"><span data-stu-id="74de1-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74de1-105">說明</span><span class="sxs-lookup"><span data-stu-id="74de1-105">DESCRIPTION</span></span>
<span data-ttu-id="74de1-106">**新的-AzSearchService** Cmdlet 會使用指定的參數建立 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="74de1-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="74de1-107">示例</span><span class="sxs-lookup"><span data-stu-id="74de1-107">EXAMPLES</span></span>

### <span data-ttu-id="74de1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="74de1-108">Example 1</span></span>
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

<span data-ttu-id="74de1-109">命令會建立 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="74de1-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="74de1-110">參數</span><span class="sxs-lookup"><span data-stu-id="74de1-110">PARAMETERS</span></span>

### <span data-ttu-id="74de1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74de1-111">-DefaultProfile</span></span>
<span data-ttu-id="74de1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74de1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74de1-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="74de1-113">-HostingMode</span></span>
<span data-ttu-id="74de1-114">搜尋服務主機模式。</span><span class="sxs-lookup"><span data-stu-id="74de1-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="74de1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="74de1-115">-Location</span></span>
<span data-ttu-id="74de1-116">搜尋服務位置。</span><span class="sxs-lookup"><span data-stu-id="74de1-116">Search Service location.</span></span>

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

### <span data-ttu-id="74de1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="74de1-117">-Name</span></span>
<span data-ttu-id="74de1-118">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="74de1-118">Search Service name.</span></span>

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

### <span data-ttu-id="74de1-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="74de1-119">-PartitionCount</span></span>
<span data-ttu-id="74de1-120">搜尋服務分區計數。</span><span class="sxs-lookup"><span data-stu-id="74de1-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="74de1-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="74de1-121">-ReplicaCount</span></span>
<span data-ttu-id="74de1-122">搜尋服務複本計數。</span><span class="sxs-lookup"><span data-stu-id="74de1-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="74de1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74de1-123">-ResourceGroupName</span></span>
<span data-ttu-id="74de1-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="74de1-124">Resource Group name.</span></span>

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

### <span data-ttu-id="74de1-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="74de1-125">-Sku</span></span>
<span data-ttu-id="74de1-126">搜尋服務 Sku。</span><span class="sxs-lookup"><span data-stu-id="74de1-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="74de1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="74de1-127">-Confirm</span></span>
<span data-ttu-id="74de1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74de1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74de1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74de1-129">-WhatIf</span></span>
<span data-ttu-id="74de1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74de1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74de1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74de1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74de1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74de1-132">CommonParameters</span></span>
<span data-ttu-id="74de1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74de1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74de1-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74de1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74de1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="74de1-135">INPUTS</span></span>

### <span data-ttu-id="74de1-136">所有</span><span class="sxs-lookup"><span data-stu-id="74de1-136">None</span></span>

## <span data-ttu-id="74de1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="74de1-137">OUTPUTS</span></span>

### <span data-ttu-id="74de1-138">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="74de1-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="74de1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="74de1-139">NOTES</span></span>

## <span data-ttu-id="74de1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="74de1-140">RELATED LINKS</span></span>

[<span data-ttu-id="74de1-141">AzSearchService</span><span class="sxs-lookup"><span data-stu-id="74de1-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="74de1-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="74de1-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="74de1-143">移除-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="74de1-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)