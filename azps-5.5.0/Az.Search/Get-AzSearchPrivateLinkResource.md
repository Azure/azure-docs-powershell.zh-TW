---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: 24941a301d0ffcc4e7219dc923fefcf1e007de99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127186"
---
# <span data-ttu-id="14401-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="14401-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="14401-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14401-102">SYNOPSIS</span></span>
<span data-ttu-id="14401-103">取得 Azure 認知搜尋服務的私人連結資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="14401-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14401-104">句法</span><span class="sxs-lookup"><span data-stu-id="14401-104">SYNTAX</span></span>

### <span data-ttu-id="14401-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14401-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14401-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14401-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14401-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14401-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14401-108">說明</span><span class="sxs-lookup"><span data-stu-id="14401-108">DESCRIPTION</span></span>
<span data-ttu-id="14401-109">**AzSearchPrivateLinkResource** Cmdlet 會取得 Azure 認知搜尋服務的私人連結資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="14401-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14401-110">示例</span><span class="sxs-lookup"><span data-stu-id="14401-110">EXAMPLES</span></span>

### <span data-ttu-id="14401-111">範例1</span><span class="sxs-lookup"><span data-stu-id="14401-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="14401-112">這個範例示範如何取得 JSON 格式的私人連結資源詳細 (資料，以供 Azure 認知搜尋服務的便利性) 用。</span><span class="sxs-lookup"><span data-stu-id="14401-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14401-113">參數</span><span class="sxs-lookup"><span data-stu-id="14401-113">PARAMETERS</span></span>

### <span data-ttu-id="14401-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14401-114">-DefaultProfile</span></span>
<span data-ttu-id="14401-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14401-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14401-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14401-116">-InputObject</span></span>
<span data-ttu-id="14401-117">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="14401-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14401-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="14401-118">-Name</span></span>
<span data-ttu-id="14401-119">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="14401-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="14401-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14401-120">-ResourceGroupName</span></span>
<span data-ttu-id="14401-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="14401-121">Resource Group name.</span></span>

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

### <span data-ttu-id="14401-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14401-122">-ResourceId</span></span>
<span data-ttu-id="14401-123">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14401-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14401-124">-確認</span><span class="sxs-lookup"><span data-stu-id="14401-124">-Confirm</span></span>
<span data-ttu-id="14401-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14401-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14401-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14401-126">-WhatIf</span></span>
<span data-ttu-id="14401-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14401-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14401-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14401-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14401-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14401-129">CommonParameters</span></span>
<span data-ttu-id="14401-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14401-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14401-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14401-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14401-132">輸入</span><span class="sxs-lookup"><span data-stu-id="14401-132">INPUTS</span></span>

### <span data-ttu-id="14401-133">所有</span><span class="sxs-lookup"><span data-stu-id="14401-133">None</span></span>

## <span data-ttu-id="14401-134">輸出</span><span class="sxs-lookup"><span data-stu-id="14401-134">OUTPUTS</span></span>

### <span data-ttu-id="14401-135">[PSSharedPrivateLinkResource]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="14401-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="14401-136">筆記</span><span class="sxs-lookup"><span data-stu-id="14401-136">NOTES</span></span>

## <span data-ttu-id="14401-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="14401-137">RELATED LINKS</span></span>

[<span data-ttu-id="14401-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="14401-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="14401-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="14401-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="14401-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="14401-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="14401-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="14401-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)