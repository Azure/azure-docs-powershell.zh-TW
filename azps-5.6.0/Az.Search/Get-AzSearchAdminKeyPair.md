---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: bef03e951982854e00412d08c609146b55e54ef3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902182"
---
# <span data-ttu-id="b9eb5-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="b9eb5-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="b9eb5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b9eb5-103">獲得 Azure 認知搜尋服務的系統管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b9eb5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9eb5-104">SYNTAX</span></span>

### <span data-ttu-id="b9eb5-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b9eb5-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9eb5-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9eb5-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9eb5-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9eb5-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9eb5-108">描述</span><span class="sxs-lookup"><span data-stu-id="b9eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="b9eb5-109">**Get-AzSearchAdminKeyPair** Cmdlet 會取得 Azure 認知搜尋服務的系統管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b9eb5-110">例子</span><span class="sxs-lookup"><span data-stu-id="b9eb5-110">EXAMPLES</span></span>

### <span data-ttu-id="b9eb5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b9eb5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="b9eb5-112">此範例會獲得 Azure 認知搜尋服務的系統管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b9eb5-113">參數</span><span class="sxs-lookup"><span data-stu-id="b9eb5-113">PARAMETERS</span></span>

### <span data-ttu-id="b9eb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9eb5-114">-DefaultProfile</span></span>
<span data-ttu-id="b9eb5-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9eb5-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9eb5-116">-ParentObject</span></span>
<span data-ttu-id="b9eb5-117">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="b9eb5-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9eb5-118">-ParentResourceId</span></span>
<span data-ttu-id="b9eb5-119">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b9eb5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9eb5-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9eb5-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-121">Resource Group name.</span></span>

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

### <span data-ttu-id="b9eb5-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b9eb5-122">-ServiceName</span></span>
<span data-ttu-id="b9eb5-123">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="b9eb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9eb5-124">CommonParameters</span></span>
<span data-ttu-id="b9eb5-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9eb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9eb5-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9eb5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9eb5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b9eb5-127">INPUTS</span></span>

### <span data-ttu-id="b9eb5-128">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b9eb5-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b9eb5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b9eb5-129">System.String</span></span>

## <span data-ttu-id="b9eb5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b9eb5-130">OUTPUTS</span></span>

### <span data-ttu-id="b9eb5-131">Microsoft.Azure.Commands.management.Search.models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b9eb5-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="b9eb5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b9eb5-132">NOTES</span></span>

## <span data-ttu-id="b9eb5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9eb5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9eb5-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b9eb5-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
