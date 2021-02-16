---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128350"
---
# <span data-ttu-id="18a7e-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="18a7e-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="18a7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="18a7e-103">更新 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="18a7e-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="18a7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="18a7e-104">SYNTAX</span></span>

### <span data-ttu-id="18a7e-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="18a7e-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18a7e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a7e-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a7e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a7e-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a7e-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a7e-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a7e-109">說明</span><span class="sxs-lookup"><span data-stu-id="18a7e-109">DESCRIPTION</span></span>
<span data-ttu-id="18a7e-110">這個 **設定 AzSearchSharedPrivateLinkResource** 會更新 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="18a7e-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="18a7e-111">示例</span><span class="sxs-lookup"><span data-stu-id="18a7e-111">EXAMPLES</span></span>

### <span data-ttu-id="18a7e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="18a7e-112">Example 1</span></span>
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

<span data-ttu-id="18a7e-113">這個範例會針對 Azure 認知搜尋服務的未決共用私人連結資源更新要求訊息。</span><span class="sxs-lookup"><span data-stu-id="18a7e-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="18a7e-114">參數</span><span class="sxs-lookup"><span data-stu-id="18a7e-114">PARAMETERS</span></span>

### <span data-ttu-id="18a7e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18a7e-115">-AsJob</span></span>
<span data-ttu-id="18a7e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="18a7e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18a7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a7e-117">-DefaultProfile</span></span>
<span data-ttu-id="18a7e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18a7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a7e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18a7e-119">-InputObject</span></span>
<span data-ttu-id="18a7e-120">共用私人連結資源輸入物件</span><span class="sxs-lookup"><span data-stu-id="18a7e-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="18a7e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="18a7e-121">-Name</span></span>
<span data-ttu-id="18a7e-122">Azure 認知搜尋共用的私人連結資源</span><span class="sxs-lookup"><span data-stu-id="18a7e-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="18a7e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="18a7e-123">-ParentObject</span></span>
<span data-ttu-id="18a7e-124">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="18a7e-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="18a7e-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="18a7e-125">-RequestMessage</span></span>
<span data-ttu-id="18a7e-126">共用私人連結資源要求訊息</span><span class="sxs-lookup"><span data-stu-id="18a7e-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="18a7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="18a7e-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="18a7e-128">Resource Group name.</span></span>

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

### <span data-ttu-id="18a7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18a7e-129">-ResourceId</span></span>
<span data-ttu-id="18a7e-130">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="18a7e-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="18a7e-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="18a7e-131">-ServiceName</span></span>
<span data-ttu-id="18a7e-132">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="18a7e-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="18a7e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="18a7e-133">-Confirm</span></span>
<span data-ttu-id="18a7e-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18a7e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a7e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a7e-135">-WhatIf</span></span>
<span data-ttu-id="18a7e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18a7e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a7e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18a7e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a7e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a7e-138">CommonParameters</span></span>
<span data-ttu-id="18a7e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18a7e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a7e-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18a7e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a7e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="18a7e-141">INPUTS</span></span>

### <span data-ttu-id="18a7e-142">所有</span><span class="sxs-lookup"><span data-stu-id="18a7e-142">None</span></span>

## <span data-ttu-id="18a7e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="18a7e-143">OUTPUTS</span></span>

### <span data-ttu-id="18a7e-144">[PSSharedPrivateLinkResource]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="18a7e-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="18a7e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="18a7e-145">NOTES</span></span>

## <span data-ttu-id="18a7e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="18a7e-146">RELATED LINKS</span></span>

[<span data-ttu-id="18a7e-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="18a7e-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="18a7e-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="18a7e-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="18a7e-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="18a7e-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)