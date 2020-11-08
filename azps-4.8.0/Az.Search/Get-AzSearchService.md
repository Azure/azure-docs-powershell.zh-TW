---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970208"
---
# <span data-ttu-id="f9607-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f9607-101">Get-AzSearchService</span></span>

## <span data-ttu-id="f9607-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9607-102">SYNOPSIS</span></span>
<span data-ttu-id="f9607-103">取得 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="f9607-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="f9607-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9607-104">SYNTAX</span></span>

### <span data-ttu-id="f9607-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9607-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9607-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9607-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9607-107">說明</span><span class="sxs-lookup"><span data-stu-id="f9607-107">DESCRIPTION</span></span>
<span data-ttu-id="f9607-108">**AzSearchService** Cmdlet 會取得指定的 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="f9607-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="f9607-109">示例</span><span class="sxs-lookup"><span data-stu-id="f9607-109">EXAMPLES</span></span>

### <span data-ttu-id="f9607-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f9607-110">Example 1</span></span>
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

<span data-ttu-id="f9607-111">使用指定的參數取得 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="f9607-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="f9607-112">參數</span><span class="sxs-lookup"><span data-stu-id="f9607-112">PARAMETERS</span></span>

### <span data-ttu-id="f9607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9607-113">-DefaultProfile</span></span>
<span data-ttu-id="f9607-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9607-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9607-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9607-115">-Name</span></span>
<span data-ttu-id="f9607-116">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f9607-116">Search Service name.</span></span>

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

### <span data-ttu-id="f9607-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9607-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9607-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f9607-118">Resource Group name.</span></span>

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

### <span data-ttu-id="f9607-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9607-119">-ResourceId</span></span>
<span data-ttu-id="f9607-120">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9607-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="f9607-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9607-121">CommonParameters</span></span>
<span data-ttu-id="f9607-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9607-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9607-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9607-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9607-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f9607-124">INPUTS</span></span>

### <span data-ttu-id="f9607-125">System.object</span><span class="sxs-lookup"><span data-stu-id="f9607-125">System.String</span></span>

## <span data-ttu-id="f9607-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f9607-126">OUTPUTS</span></span>

### <span data-ttu-id="f9607-127">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f9607-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="f9607-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f9607-128">NOTES</span></span>

## <span data-ttu-id="f9607-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9607-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9607-130">新-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f9607-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="f9607-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f9607-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="f9607-132">移除-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f9607-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)