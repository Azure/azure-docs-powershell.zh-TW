---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911294"
---
# <span data-ttu-id="dbdec-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dbdec-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="dbdec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbdec-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdec-103">從 Azure 認知 () 查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="dbdec-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dbdec-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbdec-104">SYNTAX</span></span>

### <span data-ttu-id="dbdec-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbdec-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbdec-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdec-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdec-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdec-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdec-108">描述</span><span class="sxs-lookup"><span data-stu-id="dbdec-108">DESCRIPTION</span></span>
<span data-ttu-id="dbdec-109">**Get-AzSearchQueryKey** Cmdlet 會取得 Azure 認知 () 的查詢金鑰。</span><span class="sxs-lookup"><span data-stu-id="dbdec-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dbdec-110">例子</span><span class="sxs-lookup"><span data-stu-id="dbdec-110">EXAMPLES</span></span>

### <span data-ttu-id="dbdec-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="dbdec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="dbdec-112">此範例會獲得 Azure 認知 () 的所有查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="dbdec-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="dbdec-113">參數</span><span class="sxs-lookup"><span data-stu-id="dbdec-113">PARAMETERS</span></span>

### <span data-ttu-id="dbdec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdec-114">-DefaultProfile</span></span>
<span data-ttu-id="dbdec-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbdec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdec-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbdec-116">-ParentObject</span></span>
<span data-ttu-id="dbdec-117">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="dbdec-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="dbdec-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dbdec-118">-ParentResourceId</span></span>
<span data-ttu-id="dbdec-119">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbdec-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="dbdec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdec-120">-ResourceGroupName</span></span>
<span data-ttu-id="dbdec-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="dbdec-121">Resource Group name.</span></span>

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

### <span data-ttu-id="dbdec-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dbdec-122">-ServiceName</span></span>
<span data-ttu-id="dbdec-123">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="dbdec-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="dbdec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdec-124">CommonParameters</span></span>
<span data-ttu-id="dbdec-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbdec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdec-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbdec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdec-127">輸入</span><span class="sxs-lookup"><span data-stu-id="dbdec-127">INPUTS</span></span>

### <span data-ttu-id="dbdec-128">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="dbdec-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="dbdec-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dbdec-129">System.String</span></span>

## <span data-ttu-id="dbdec-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dbdec-130">OUTPUTS</span></span>

### <span data-ttu-id="dbdec-131">Microsoft.Azure.Commands.management.Search.models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="dbdec-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="dbdec-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dbdec-132">NOTES</span></span>

## <span data-ttu-id="dbdec-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbdec-133">RELATED LINKS</span></span>

[<span data-ttu-id="dbdec-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dbdec-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="dbdec-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="dbdec-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)