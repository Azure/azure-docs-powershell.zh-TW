---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a9f76ef0d1955076171cc157686b7ae5d7be266
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135362"
---
# <span data-ttu-id="0d69d-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0d69d-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="0d69d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d69d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d69d-103">建立 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="0d69d-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0d69d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d69d-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d69d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d69d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d69d-106">**新的-AzSearchSharedPrivateLinkResource** 會建立 Azure 認知搜尋服務的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="0d69d-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0d69d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d69d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d69d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0d69d-108">Example 1</span></span>
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

<span data-ttu-id="0d69d-109">這個範例會建立一個共用私人連結資源至 Azure 認知搜尋服務之儲存空間帳戶的 blob 服務。</span><span class="sxs-lookup"><span data-stu-id="0d69d-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0d69d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d69d-110">PARAMETERS</span></span>

### <span data-ttu-id="0d69d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d69d-111">-AsJob</span></span>
<span data-ttu-id="0d69d-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d69d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d69d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d69d-113">-DefaultProfile</span></span>
<span data-ttu-id="0d69d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d69d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d69d-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0d69d-115">-GroupId</span></span>
<span data-ttu-id="0d69d-116">共用私人連結資源群組識別碼</span><span class="sxs-lookup"><span data-stu-id="0d69d-116">Shared private link resource group id</span></span>

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

### <span data-ttu-id="0d69d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d69d-117">-Name</span></span>
<span data-ttu-id="0d69d-118">Azure 認知搜尋共用的私人連結資源</span><span class="sxs-lookup"><span data-stu-id="0d69d-118">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="0d69d-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0d69d-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0d69d-120">共用私人連結目標資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0d69d-120">Shared private link target resource id</span></span>

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

### <span data-ttu-id="0d69d-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="0d69d-121">-RequestMessage</span></span>
<span data-ttu-id="0d69d-122">共用私人連結資源要求訊息</span><span class="sxs-lookup"><span data-stu-id="0d69d-122">Shared private link resource request message</span></span>

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

### <span data-ttu-id="0d69d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d69d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d69d-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0d69d-124">Resource Group name.</span></span>

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

### <span data-ttu-id="0d69d-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="0d69d-125">-ResourceRegion</span></span>
<span data-ttu-id="0d69d-126"> (選擇性) 共用私人連結資源區域</span><span class="sxs-lookup"><span data-stu-id="0d69d-126">(Optional) Shared private link resource region</span></span>

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

### <span data-ttu-id="0d69d-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0d69d-127">-ServiceName</span></span>
<span data-ttu-id="0d69d-128">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0d69d-128">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="0d69d-129">-確認</span><span class="sxs-lookup"><span data-stu-id="0d69d-129">-Confirm</span></span>
<span data-ttu-id="0d69d-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d69d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d69d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d69d-131">-WhatIf</span></span>
<span data-ttu-id="0d69d-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d69d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d69d-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d69d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d69d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d69d-134">CommonParameters</span></span>
<span data-ttu-id="0d69d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d69d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d69d-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d69d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d69d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="0d69d-137">INPUTS</span></span>

### <span data-ttu-id="0d69d-138">所有</span><span class="sxs-lookup"><span data-stu-id="0d69d-138">None</span></span>

## <span data-ttu-id="0d69d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0d69d-139">OUTPUTS</span></span>

### <span data-ttu-id="0d69d-140">[PSSharedPrivateLinkResource]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0d69d-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="0d69d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0d69d-141">NOTES</span></span>

## <span data-ttu-id="0d69d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d69d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d69d-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0d69d-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0d69d-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0d69d-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0d69d-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0d69d-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
