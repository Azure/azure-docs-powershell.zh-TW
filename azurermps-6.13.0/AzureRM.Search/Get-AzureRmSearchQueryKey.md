---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447229"
---
# <span data-ttu-id="d1841-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d1841-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="d1841-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1841-102">SYNOPSIS</span></span>
<span data-ttu-id="d1841-103">取得 Azure 搜尋服務 (s) 的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="d1841-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1841-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1841-104">SYNTAX</span></span>

### <span data-ttu-id="d1841-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d1841-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1841-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1841-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1841-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1841-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1841-108">說明</span><span class="sxs-lookup"><span data-stu-id="d1841-108">DESCRIPTION</span></span>
<span data-ttu-id="d1841-109">**AzureRmSearchQueryKey** Cmdlet 會取得 Azure 搜尋服務 (s) 的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="d1841-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="d1841-110">示例</span><span class="sxs-lookup"><span data-stu-id="d1841-110">EXAMPLES</span></span>

### <span data-ttu-id="d1841-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d1841-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="d1841-112">此範例會取得 Azure 搜尋服務 (s) 的所有查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="d1841-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="d1841-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1841-113">PARAMETERS</span></span>

### <span data-ttu-id="d1841-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1841-114">-DefaultProfile</span></span>
<span data-ttu-id="d1841-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1841-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1841-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1841-116">-ParentObject</span></span>
<span data-ttu-id="d1841-117">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d1841-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="d1841-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1841-118">-ParentResourceId</span></span>
<span data-ttu-id="d1841-119">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1841-119">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1841-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1841-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1841-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d1841-121">Resource Group name.</span></span>

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

### <span data-ttu-id="d1841-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d1841-122">-ServiceName</span></span>
<span data-ttu-id="d1841-123">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d1841-123">Search Service name.</span></span>

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

### <span data-ttu-id="d1841-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1841-124">CommonParameters</span></span>
<span data-ttu-id="d1841-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1841-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1841-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1841-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1841-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d1841-127">INPUTS</span></span>

### <span data-ttu-id="d1841-128">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d1841-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="d1841-129">參數： ParentObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d1841-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="d1841-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d1841-130">System.String</span></span>

## <span data-ttu-id="d1841-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d1841-131">OUTPUTS</span></span>

### <span data-ttu-id="d1841-132">[PSSearchQueryKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d1841-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="d1841-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d1841-133">NOTES</span></span>

## <span data-ttu-id="d1841-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1841-134">RELATED LINKS</span></span>

[<span data-ttu-id="d1841-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d1841-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="d1841-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d1841-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
