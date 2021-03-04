---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: e8a9c1f65c536abb3c7b3e7aa983292ccde925a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913429"
---
# <span data-ttu-id="d74bc-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d74bc-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="d74bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d74bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d74bc-103">刪除 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="d74bc-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="d74bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="d74bc-104">SYNTAX</span></span>

### <span data-ttu-id="d74bc-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d74bc-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74bc-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d74bc-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74bc-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d74bc-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74bc-108">描述</span><span class="sxs-lookup"><span data-stu-id="d74bc-108">DESCRIPTION</span></span>
<span data-ttu-id="d74bc-109">**Remove-AzIpAllocation** Cmdlet 會刪除 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="d74bc-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="d74bc-110">例子</span><span class="sxs-lookup"><span data-stu-id="d74bc-110">EXAMPLES</span></span>

### <span data-ttu-id="d74bc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d74bc-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="d74bc-112">參數</span><span class="sxs-lookup"><span data-stu-id="d74bc-112">PARAMETERS</span></span>

### <span data-ttu-id="d74bc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74bc-113">-AsJob</span></span>
<span data-ttu-id="d74bc-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d74bc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74bc-115">-DefaultProfile</span></span>
<span data-ttu-id="d74bc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d74bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74bc-117">-強制</span><span class="sxs-lookup"><span data-stu-id="d74bc-117">-Force</span></span>
<span data-ttu-id="d74bc-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="d74bc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d74bc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74bc-119">-InputObject</span></span>
<span data-ttu-id="d74bc-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="d74bc-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74bc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d74bc-121">-Name</span></span>
<span data-ttu-id="d74bc-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d74bc-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d74bc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d74bc-123">-PassThru</span></span>
<span data-ttu-id="d74bc-124">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d74bc-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d74bc-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d74bc-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d74bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d74bc-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d74bc-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d74bc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74bc-128">-ResourceId</span></span>
<span data-ttu-id="d74bc-129">IpAllocation 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d74bc-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d74bc-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d74bc-130">-Confirm</span></span>
<span data-ttu-id="d74bc-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d74bc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74bc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74bc-132">-WhatIf</span></span>
<span data-ttu-id="d74bc-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d74bc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74bc-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d74bc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74bc-135">CommonParameters</span></span>
<span data-ttu-id="d74bc-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d74bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74bc-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d74bc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74bc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d74bc-138">INPUTS</span></span>

### <span data-ttu-id="d74bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d74bc-139">System.String</span></span>

## <span data-ttu-id="d74bc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d74bc-140">OUTPUTS</span></span>

### <span data-ttu-id="d74bc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d74bc-141">System.Boolean</span></span>

## <span data-ttu-id="d74bc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d74bc-142">NOTES</span></span>

## <span data-ttu-id="d74bc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d74bc-143">RELATED LINKS</span></span>
