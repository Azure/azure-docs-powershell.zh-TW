---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797473"
---
# <span data-ttu-id="a849a-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a849a-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="a849a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a849a-102">SYNOPSIS</span></span>
<span data-ttu-id="a849a-103">取得 Azure 搜尋服務的管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="a849a-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="a849a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a849a-104">SYNTAX</span></span>

### <span data-ttu-id="a849a-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a849a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a849a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a849a-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a849a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a849a-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a849a-108">說明</span><span class="sxs-lookup"><span data-stu-id="a849a-108">DESCRIPTION</span></span>
<span data-ttu-id="a849a-109">**AzSearchAdminKeyPair** Cmdlet 會取得 Azure 搜尋服務的管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="a849a-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="a849a-110">示例</span><span class="sxs-lookup"><span data-stu-id="a849a-110">EXAMPLES</span></span>

### <span data-ttu-id="a849a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a849a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="a849a-112">此範例會取得 Azure 搜尋服務的管理金鑰組。</span><span class="sxs-lookup"><span data-stu-id="a849a-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="a849a-113">參數</span><span class="sxs-lookup"><span data-stu-id="a849a-113">PARAMETERS</span></span>

### <span data-ttu-id="a849a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a849a-114">-DefaultProfile</span></span>
<span data-ttu-id="a849a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a849a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a849a-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a849a-116">-ParentObject</span></span>
<span data-ttu-id="a849a-117">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a849a-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a849a-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a849a-118">-ParentResourceId</span></span>
<span data-ttu-id="a849a-119">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a849a-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a849a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a849a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a849a-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a849a-121">Resource Group name.</span></span>

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

### <span data-ttu-id="a849a-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a849a-122">-ServiceName</span></span>
<span data-ttu-id="a849a-123">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a849a-123">Search Service name.</span></span>

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

### <span data-ttu-id="a849a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a849a-124">CommonParameters</span></span>
<span data-ttu-id="a849a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a849a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a849a-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a849a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a849a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a849a-127">INPUTS</span></span>

### <span data-ttu-id="a849a-128">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a849a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a849a-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a849a-129">System.String</span></span>

## <span data-ttu-id="a849a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a849a-130">OUTPUTS</span></span>

### <span data-ttu-id="a849a-131">[PSSearchAdminKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a849a-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a849a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a849a-132">NOTES</span></span>

## <span data-ttu-id="a849a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a849a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a849a-134">新-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a849a-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
