---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: f4f360cc7fd9151735f131878565a09933f1be54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904842"
---
# <span data-ttu-id="d2786-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d2786-101">Get-AzSearchService</span></span>

## <span data-ttu-id="d2786-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2786-102">SYNOPSIS</span></span>
<span data-ttu-id="d2786-103">獲得 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d2786-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d2786-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2786-104">SYNTAX</span></span>

### <span data-ttu-id="d2786-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d2786-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2786-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2786-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2786-107">描述</span><span class="sxs-lookup"><span data-stu-id="d2786-107">DESCRIPTION</span></span>
<span data-ttu-id="d2786-108">**Get-AzSearchService** Cmdlet 會取得指定的 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d2786-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d2786-109">例子</span><span class="sxs-lookup"><span data-stu-id="d2786-109">EXAMPLES</span></span>

### <span data-ttu-id="d2786-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d2786-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="d2786-111">取得具有指定參數的 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d2786-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="d2786-112">參數</span><span class="sxs-lookup"><span data-stu-id="d2786-112">PARAMETERS</span></span>

### <span data-ttu-id="d2786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2786-113">-DefaultProfile</span></span>
<span data-ttu-id="d2786-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2786-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2786-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2786-115">-Name</span></span>
<span data-ttu-id="d2786-116">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d2786-116">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2786-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2786-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2786-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d2786-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2786-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2786-119">-ResourceId</span></span>
<span data-ttu-id="d2786-120">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2786-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d2786-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2786-121">CommonParameters</span></span>
<span data-ttu-id="d2786-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2786-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2786-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2786-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2786-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d2786-124">INPUTS</span></span>

### <span data-ttu-id="d2786-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d2786-125">System.String</span></span>

## <span data-ttu-id="d2786-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d2786-126">OUTPUTS</span></span>

### <span data-ttu-id="d2786-127">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d2786-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d2786-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d2786-128">NOTES</span></span>

## <span data-ttu-id="d2786-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2786-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2786-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d2786-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="d2786-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d2786-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="d2786-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d2786-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)