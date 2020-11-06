---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 245cbce2516dcb26502313bcac35dd35b957f94d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620718"
---
# <span data-ttu-id="68238-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="68238-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="68238-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68238-102">SYNOPSIS</span></span>
<span data-ttu-id="68238-103">移除 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="68238-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="68238-104">句法</span><span class="sxs-lookup"><span data-stu-id="68238-104">SYNTAX</span></span>

### <span data-ttu-id="68238-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68238-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68238-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68238-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68238-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68238-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68238-108">說明</span><span class="sxs-lookup"><span data-stu-id="68238-108">DESCRIPTION</span></span>
<span data-ttu-id="68238-109">**AzSearchService** Cmdlet 會將 Azure 搜尋服務與指定的一個指令移除。</span><span class="sxs-lookup"><span data-stu-id="68238-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="68238-110">示例</span><span class="sxs-lookup"><span data-stu-id="68238-110">EXAMPLES</span></span>

### <span data-ttu-id="68238-111">範例1</span><span class="sxs-lookup"><span data-stu-id="68238-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="68238-112">此範例會移除 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="68238-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="68238-113">參數</span><span class="sxs-lookup"><span data-stu-id="68238-113">PARAMETERS</span></span>

### <span data-ttu-id="68238-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68238-114">-DefaultProfile</span></span>
<span data-ttu-id="68238-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68238-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68238-116">-Force</span><span class="sxs-lookup"><span data-stu-id="68238-116">-Force</span></span>
<span data-ttu-id="68238-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="68238-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68238-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68238-118">-InputObject</span></span>
<span data-ttu-id="68238-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="68238-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="68238-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="68238-120">-Name</span></span>
<span data-ttu-id="68238-121">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="68238-121">Search Service name.</span></span>

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

### <span data-ttu-id="68238-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68238-122">-PassThru</span></span>
<span data-ttu-id="68238-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="68238-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="68238-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="68238-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="68238-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68238-125">-ResourceGroupName</span></span>
<span data-ttu-id="68238-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="68238-126">Resource Group name.</span></span>

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

### <span data-ttu-id="68238-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68238-127">-ResourceId</span></span>
<span data-ttu-id="68238-128">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68238-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="68238-129">-確認</span><span class="sxs-lookup"><span data-stu-id="68238-129">-Confirm</span></span>
<span data-ttu-id="68238-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68238-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68238-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68238-131">-WhatIf</span></span>
<span data-ttu-id="68238-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68238-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68238-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68238-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68238-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68238-134">CommonParameters</span></span>
<span data-ttu-id="68238-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68238-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68238-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68238-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68238-137">輸入</span><span class="sxs-lookup"><span data-stu-id="68238-137">INPUTS</span></span>

### <span data-ttu-id="68238-138">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="68238-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="68238-139">System.object</span><span class="sxs-lookup"><span data-stu-id="68238-139">System.String</span></span>

## <span data-ttu-id="68238-140">輸出</span><span class="sxs-lookup"><span data-stu-id="68238-140">OUTPUTS</span></span>

### <span data-ttu-id="68238-141">System.object</span><span class="sxs-lookup"><span data-stu-id="68238-141">System.Boolean</span></span>

## <span data-ttu-id="68238-142">筆記</span><span class="sxs-lookup"><span data-stu-id="68238-142">NOTES</span></span>

## <span data-ttu-id="68238-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="68238-143">RELATED LINKS</span></span>

[<span data-ttu-id="68238-144">新-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="68238-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="68238-145">AzSearchService</span><span class="sxs-lookup"><span data-stu-id="68238-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="68238-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="68238-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

