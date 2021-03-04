---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908022"
---
# <span data-ttu-id="4ba6e-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4ba6e-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="4ba6e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ba6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba6e-103">建立 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4ba6e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ba6e-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba6e-105">描述</span><span class="sxs-lookup"><span data-stu-id="4ba6e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba6e-106">**New-AzSearchSharedPrivateLinkResource** 會為 Azure 認知搜尋服務建立共用的私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4ba6e-107">例子</span><span class="sxs-lookup"><span data-stu-id="4ba6e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba6e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4ba6e-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="4ba6e-109">此範例會針對 Azure 認知搜尋服務建立儲存帳戶 Blob 服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4ba6e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ba6e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ba6e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ba6e-111">-AsJob</span></span>
<span data-ttu-id="4ba6e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4ba6e-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba6e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ba6e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba6e-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4ba6e-115">-GroupId</span></span>
<span data-ttu-id="4ba6e-116">共用私人連結資源群組識別碼</span><span class="sxs-lookup"><span data-stu-id="4ba6e-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ba6e-117">-Name</span></span>
<span data-ttu-id="4ba6e-118">Azure 認知搜尋共用私人連結資源</span><span class="sxs-lookup"><span data-stu-id="4ba6e-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="4ba6e-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="4ba6e-120">共用私人連結目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4ba6e-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="4ba6e-121">-RequestMessage</span></span>
<span data-ttu-id="4ba6e-122">共用私人連結資源要求訊息</span><span class="sxs-lookup"><span data-stu-id="4ba6e-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba6e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ba6e-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="4ba6e-125">-ResourceRegion</span></span>
<span data-ttu-id="4ba6e-126"> (共用) 連結資源區域選擇</span><span class="sxs-lookup"><span data-stu-id="4ba6e-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4ba6e-127">-ServiceName</span></span>
<span data-ttu-id="4ba6e-128">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4ba6e-129">-Confirm</span></span>
<span data-ttu-id="4ba6e-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba6e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba6e-131">-WhatIf</span></span>
<span data-ttu-id="4ba6e-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba6e-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba6e-134">CommonParameters</span></span>
<span data-ttu-id="4ba6e-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ba6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba6e-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ba6e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba6e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4ba6e-137">INPUTS</span></span>

### <span data-ttu-id="4ba6e-138">沒有</span><span class="sxs-lookup"><span data-stu-id="4ba6e-138">None</span></span>

## <span data-ttu-id="4ba6e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4ba6e-139">OUTPUTS</span></span>

### <span data-ttu-id="4ba6e-140">Microsoft.Azure.Commands.management.Search.models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4ba6e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="4ba6e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4ba6e-141">NOTES</span></span>

## <span data-ttu-id="4ba6e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ba6e-142">RELATED LINKS</span></span>

[<span data-ttu-id="4ba6e-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4ba6e-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="4ba6e-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4ba6e-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="4ba6e-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4ba6e-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
