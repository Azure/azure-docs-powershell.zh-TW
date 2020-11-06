---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447225"
---
# <span data-ttu-id="d35e7-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d35e7-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="d35e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d35e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d35e7-103">取得 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d35e7-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d35e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d35e7-104">SYNTAX</span></span>

### <span data-ttu-id="d35e7-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d35e7-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d35e7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d35e7-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d35e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="d35e7-107">DESCRIPTION</span></span>
<span data-ttu-id="d35e7-108">**AzureRmSearchService** Cmdlet 會取得指定的 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d35e7-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="d35e7-109">示例</span><span class="sxs-lookup"><span data-stu-id="d35e7-109">EXAMPLES</span></span>

### <span data-ttu-id="d35e7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d35e7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="d35e7-111">使用指定的參數取得 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="d35e7-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="d35e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="d35e7-112">PARAMETERS</span></span>

### <span data-ttu-id="d35e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35e7-113">-DefaultProfile</span></span>
<span data-ttu-id="d35e7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d35e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35e7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d35e7-115">-Name</span></span>
<span data-ttu-id="d35e7-116">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d35e7-116">Search Service name.</span></span>

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

### <span data-ttu-id="d35e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d35e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d35e7-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d35e7-118">Resource Group name.</span></span>

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

### <span data-ttu-id="d35e7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d35e7-119">-ResourceId</span></span>
<span data-ttu-id="d35e7-120">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d35e7-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d35e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35e7-121">CommonParameters</span></span>
<span data-ttu-id="d35e7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d35e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35e7-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d35e7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35e7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d35e7-124">INPUTS</span></span>

### <span data-ttu-id="d35e7-125">System.object</span><span class="sxs-lookup"><span data-stu-id="d35e7-125">System.String</span></span>

## <span data-ttu-id="d35e7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d35e7-126">OUTPUTS</span></span>

### <span data-ttu-id="d35e7-127">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d35e7-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d35e7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d35e7-128">NOTES</span></span>

## <span data-ttu-id="d35e7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d35e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="d35e7-130">新-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d35e7-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="d35e7-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d35e7-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="d35e7-132">移除-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="d35e7-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
