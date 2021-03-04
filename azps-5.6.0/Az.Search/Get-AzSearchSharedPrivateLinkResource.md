---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ac27d706afcce4b8b431e0253b0a4e5146883640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909469"
---
# <span data-ttu-id="a8f7f-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a8f7f-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="a8f7f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f7f-103">在 Azure 認知搜尋 (中) 共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a8f7f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8f7f-104">SYNTAX</span></span>

### <span data-ttu-id="a8f7f-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a8f7f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f7f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f7f-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f7f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f7f-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f7f-108">描述</span><span class="sxs-lookup"><span data-stu-id="a8f7f-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f7f-109">**Get-AzSearchSharedPrivateLinkResource** Cmdlet 會取得共用私人連結資源 (Azure 認知) 服務之最愛。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a8f7f-110">例子</span><span class="sxs-lookup"><span data-stu-id="a8f7f-110">EXAMPLES</span></span>

### <span data-ttu-id="a8f7f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a8f7f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="a8f7f-112">此範例列出 Azure 認知搜尋服務的所有共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="a8f7f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a8f7f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="a8f7f-114">此範例會以 Azure 認知搜尋服務的名稱列出特定的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a8f7f-115">參數</span><span class="sxs-lookup"><span data-stu-id="a8f7f-115">PARAMETERS</span></span>

### <span data-ttu-id="a8f7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f7f-116">-DefaultProfile</span></span>
<span data-ttu-id="a8f7f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f7f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8f7f-118">-Name</span></span>
<span data-ttu-id="a8f7f-119">Azure 認知搜尋共用私人連結資源</span><span class="sxs-lookup"><span data-stu-id="a8f7f-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f7f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a8f7f-120">-ParentObject</span></span>
<span data-ttu-id="a8f7f-121">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="a8f7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8f7f-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-123">Resource Group name.</span></span>

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

### <span data-ttu-id="a8f7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f7f-124">-ResourceId</span></span>
<span data-ttu-id="a8f7f-125">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a8f7f-125">Shared private link resource id</span></span>

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

### <span data-ttu-id="a8f7f-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8f7f-126">-ServiceName</span></span>
<span data-ttu-id="a8f7f-127">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a8f7f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a8f7f-128">-Confirm</span></span>
<span data-ttu-id="a8f7f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f7f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f7f-130">-WhatIf</span></span>
<span data-ttu-id="a8f7f-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8f7f-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f7f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f7f-133">CommonParameters</span></span>
<span data-ttu-id="a8f7f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8f7f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f7f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8f7f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f7f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a8f7f-136">INPUTS</span></span>

### <span data-ttu-id="a8f7f-137">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a8f7f-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a8f7f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a8f7f-138">System.String</span></span>

## <span data-ttu-id="a8f7f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a8f7f-139">OUTPUTS</span></span>

### <span data-ttu-id="a8f7f-140">Microsoft.Azure.Commands.management.Search.models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a8f7f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="a8f7f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a8f7f-141">NOTES</span></span>

## <span data-ttu-id="a8f7f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8f7f-142">RELATED LINKS</span></span>

[<span data-ttu-id="a8f7f-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a8f7f-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="a8f7f-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a8f7f-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="a8f7f-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a8f7f-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
