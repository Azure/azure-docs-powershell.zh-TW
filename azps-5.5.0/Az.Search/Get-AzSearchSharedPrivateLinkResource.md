---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135370"
---
# <span data-ttu-id="ab357-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="ab357-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="ab357-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab357-102">SYNOPSIS</span></span>
<span data-ttu-id="ab357-103">取得 Azure 認知搜尋服務 (s) 的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="ab357-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ab357-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab357-104">SYNTAX</span></span>

### <span data-ttu-id="ab357-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ab357-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab357-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab357-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab357-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab357-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab357-108">說明</span><span class="sxs-lookup"><span data-stu-id="ab357-108">DESCRIPTION</span></span>
<span data-ttu-id="ab357-109">**AzSearchSharedPrivateLinkResource** Cmdlet 會取得 Azure 認知搜尋服務 (s) 的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="ab357-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ab357-110">示例</span><span class="sxs-lookup"><span data-stu-id="ab357-110">EXAMPLES</span></span>

### <span data-ttu-id="ab357-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ab357-111">Example 1</span></span>
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

<span data-ttu-id="ab357-112">這個範例會列出 Azure 認知搜尋服務的所有共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="ab357-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="ab357-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ab357-113">Example 2</span></span>
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

<span data-ttu-id="ab357-114">這個範例會依 Azure 認知搜尋服務的名稱列出特定的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="ab357-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="ab357-115">參數</span><span class="sxs-lookup"><span data-stu-id="ab357-115">PARAMETERS</span></span>

### <span data-ttu-id="ab357-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab357-116">-DefaultProfile</span></span>
<span data-ttu-id="ab357-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab357-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab357-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab357-118">-Name</span></span>
<span data-ttu-id="ab357-119">Azure 認知搜尋共用的私人連結資源</span><span class="sxs-lookup"><span data-stu-id="ab357-119">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="ab357-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ab357-120">-ParentObject</span></span>
<span data-ttu-id="ab357-121">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="ab357-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="ab357-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab357-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab357-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ab357-123">Resource Group name.</span></span>

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

### <span data-ttu-id="ab357-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab357-124">-ResourceId</span></span>
<span data-ttu-id="ab357-125">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ab357-125">Shared private link resource id</span></span>

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

### <span data-ttu-id="ab357-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ab357-126">-ServiceName</span></span>
<span data-ttu-id="ab357-127">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ab357-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="ab357-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ab357-128">-Confirm</span></span>
<span data-ttu-id="ab357-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab357-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab357-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab357-130">-WhatIf</span></span>
<span data-ttu-id="ab357-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab357-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab357-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab357-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab357-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab357-133">CommonParameters</span></span>
<span data-ttu-id="ab357-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab357-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab357-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab357-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab357-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ab357-136">INPUTS</span></span>

### <span data-ttu-id="ab357-137">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ab357-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ab357-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ab357-138">System.String</span></span>

## <span data-ttu-id="ab357-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ab357-139">OUTPUTS</span></span>

### <span data-ttu-id="ab357-140">[PSSharedPrivateLinkResource]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ab357-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="ab357-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ab357-141">NOTES</span></span>

## <span data-ttu-id="ab357-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab357-142">RELATED LINKS</span></span>

[<span data-ttu-id="ab357-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ab357-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ab357-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ab357-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="ab357-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="ab357-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
