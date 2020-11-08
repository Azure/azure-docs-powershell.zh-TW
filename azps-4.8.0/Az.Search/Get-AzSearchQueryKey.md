---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128101"
---
# <span data-ttu-id="e178b-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e178b-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="e178b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e178b-102">SYNOPSIS</span></span>
<span data-ttu-id="e178b-103">取得 Azure 搜尋服務 (s) 的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="e178b-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="e178b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e178b-104">SYNTAX</span></span>

### <span data-ttu-id="e178b-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e178b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e178b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e178b-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e178b-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e178b-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e178b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e178b-108">DESCRIPTION</span></span>
<span data-ttu-id="e178b-109">**AzSearchQueryKey** Cmdlet 會取得 Azure 搜尋服務 (s) 的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="e178b-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="e178b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e178b-110">EXAMPLES</span></span>

### <span data-ttu-id="e178b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e178b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="e178b-112">此範例會取得 Azure 搜尋服務 (s) 的所有查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="e178b-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="e178b-113">參數</span><span class="sxs-lookup"><span data-stu-id="e178b-113">PARAMETERS</span></span>

### <span data-ttu-id="e178b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e178b-114">-DefaultProfile</span></span>
<span data-ttu-id="e178b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e178b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e178b-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e178b-116">-ParentObject</span></span>
<span data-ttu-id="e178b-117">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e178b-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="e178b-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e178b-118">-ParentResourceId</span></span>
<span data-ttu-id="e178b-119">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e178b-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e178b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e178b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e178b-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e178b-121">Resource Group name.</span></span>

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

### <span data-ttu-id="e178b-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e178b-122">-ServiceName</span></span>
<span data-ttu-id="e178b-123">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e178b-123">Search Service name.</span></span>

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

### <span data-ttu-id="e178b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e178b-124">CommonParameters</span></span>
<span data-ttu-id="e178b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e178b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e178b-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e178b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e178b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e178b-127">INPUTS</span></span>

### <span data-ttu-id="e178b-128">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="e178b-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e178b-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e178b-129">System.String</span></span>

## <span data-ttu-id="e178b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e178b-130">OUTPUTS</span></span>

### <span data-ttu-id="e178b-131">[PSSearchQueryKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="e178b-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="e178b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e178b-132">NOTES</span></span>

## <span data-ttu-id="e178b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e178b-133">RELATED LINKS</span></span>

[<span data-ttu-id="e178b-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e178b-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="e178b-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e178b-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)