---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 7139831accd920858e7b97f775146d01b91cef3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907057"
---
# <span data-ttu-id="5a6df-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5a6df-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="5a6df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a6df-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6df-103">更新 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="5a6df-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5a6df-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a6df-104">SYNTAX</span></span>

### <span data-ttu-id="5a6df-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a6df-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a6df-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a6df-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6df-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a6df-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6df-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a6df-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6df-109">描述</span><span class="sxs-lookup"><span data-stu-id="5a6df-109">DESCRIPTION</span></span>
<span data-ttu-id="5a6df-110">此 **Set-AzSearchSharedPrivateLinkResource** 會更新 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="5a6df-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5a6df-111">例子</span><span class="sxs-lookup"><span data-stu-id="5a6df-111">EXAMPLES</span></span>

### <span data-ttu-id="5a6df-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a6df-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="5a6df-113">此範例會更新 Azure 認知搜尋服務擱置中共用私人連結資源的要求訊息。</span><span class="sxs-lookup"><span data-stu-id="5a6df-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5a6df-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a6df-114">PARAMETERS</span></span>

### <span data-ttu-id="5a6df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a6df-115">-AsJob</span></span>
<span data-ttu-id="5a6df-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a6df-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a6df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6df-117">-DefaultProfile</span></span>
<span data-ttu-id="5a6df-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a6df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a6df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a6df-119">-InputObject</span></span>
<span data-ttu-id="5a6df-120">共用私人連結資源輸入物件</span><span class="sxs-lookup"><span data-stu-id="5a6df-120">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6df-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a6df-121">-Name</span></span>
<span data-ttu-id="5a6df-122">Azure 認知搜尋共用私人連結資源</span><span class="sxs-lookup"><span data-stu-id="5a6df-122">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6df-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a6df-123">-ParentObject</span></span>
<span data-ttu-id="5a6df-124">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="5a6df-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6df-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="5a6df-125">-RequestMessage</span></span>
<span data-ttu-id="5a6df-126">共用私人連結資源要求訊息</span><span class="sxs-lookup"><span data-stu-id="5a6df-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6df-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a6df-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5a6df-128">Resource Group name.</span></span>

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

### <span data-ttu-id="5a6df-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6df-129">-ResourceId</span></span>
<span data-ttu-id="5a6df-130">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5a6df-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="5a6df-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5a6df-131">-ServiceName</span></span>
<span data-ttu-id="5a6df-132">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5a6df-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="5a6df-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5a6df-133">-Confirm</span></span>
<span data-ttu-id="5a6df-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a6df-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6df-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6df-135">-WhatIf</span></span>
<span data-ttu-id="5a6df-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a6df-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6df-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a6df-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6df-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6df-138">CommonParameters</span></span>
<span data-ttu-id="5a6df-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a6df-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6df-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a6df-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6df-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5a6df-141">INPUTS</span></span>

### <span data-ttu-id="5a6df-142">沒有</span><span class="sxs-lookup"><span data-stu-id="5a6df-142">None</span></span>

## <span data-ttu-id="5a6df-143">輸出</span><span class="sxs-lookup"><span data-stu-id="5a6df-143">OUTPUTS</span></span>

### <span data-ttu-id="5a6df-144">Microsoft.Azure.Commands.management.Search.models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5a6df-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="5a6df-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5a6df-145">NOTES</span></span>

## <span data-ttu-id="5a6df-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a6df-146">RELATED LINKS</span></span>

[<span data-ttu-id="5a6df-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="5a6df-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="5a6df-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="5a6df-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="5a6df-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="5a6df-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)