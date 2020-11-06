---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451771"
---
# <span data-ttu-id="00a0c-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="00a0c-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="00a0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="00a0c-103">移除 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="00a0c-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00a0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="00a0c-104">SYNTAX</span></span>

### <span data-ttu-id="00a0c-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00a0c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00a0c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00a0c-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00a0c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00a0c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="00a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="00a0c-109">**AzureRmSearchService** Cmdlet 會將 Azure 搜尋服務與指定的一個指令移除。</span><span class="sxs-lookup"><span data-stu-id="00a0c-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="00a0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="00a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="00a0c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="00a0c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="00a0c-112">此範例會移除 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="00a0c-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="00a0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="00a0c-113">PARAMETERS</span></span>

### <span data-ttu-id="00a0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a0c-114">-DefaultProfile</span></span>
<span data-ttu-id="00a0c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00a0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a0c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="00a0c-116">-Force</span></span>
<span data-ttu-id="00a0c-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="00a0c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="00a0c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00a0c-118">-InputObject</span></span>
<span data-ttu-id="00a0c-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="00a0c-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="00a0c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="00a0c-120">-Name</span></span>
<span data-ttu-id="00a0c-121">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="00a0c-121">Search Service name.</span></span>

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

### <span data-ttu-id="00a0c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00a0c-122">-PassThru</span></span>
<span data-ttu-id="00a0c-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="00a0c-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="00a0c-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="00a0c-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="00a0c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a0c-125">-ResourceGroupName</span></span>
<span data-ttu-id="00a0c-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="00a0c-126">Resource Group name.</span></span>

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

### <span data-ttu-id="00a0c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00a0c-127">-ResourceId</span></span>
<span data-ttu-id="00a0c-128">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00a0c-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="00a0c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="00a0c-129">-Confirm</span></span>
<span data-ttu-id="00a0c-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00a0c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a0c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a0c-131">-WhatIf</span></span>
<span data-ttu-id="00a0c-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00a0c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00a0c-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00a0c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a0c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a0c-134">CommonParameters</span></span>
<span data-ttu-id="00a0c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00a0c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a0c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00a0c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a0c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="00a0c-137">INPUTS</span></span>

### <span data-ttu-id="00a0c-138">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="00a0c-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="00a0c-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="00a0c-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="00a0c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="00a0c-140">System.String</span></span>

## <span data-ttu-id="00a0c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="00a0c-141">OUTPUTS</span></span>

### <span data-ttu-id="00a0c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="00a0c-142">System.Boolean</span></span>

## <span data-ttu-id="00a0c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="00a0c-143">NOTES</span></span>

## <span data-ttu-id="00a0c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="00a0c-144">RELATED LINKS</span></span>

[<span data-ttu-id="00a0c-145">新-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="00a0c-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="00a0c-146">AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="00a0c-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="00a0c-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="00a0c-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

