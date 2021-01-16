---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437563"
---
# <span data-ttu-id="cf046-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="cf046-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="cf046-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf046-102">SYNOPSIS</span></span>
<span data-ttu-id="cf046-103">刪除 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="cf046-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="cf046-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf046-104">SYNTAX</span></span>

### <span data-ttu-id="cf046-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf046-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf046-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf046-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf046-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf046-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf046-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf046-108">DESCRIPTION</span></span>
<span data-ttu-id="cf046-109">**AzIpAllocation** Cmdlet 會刪除 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="cf046-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="cf046-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf046-110">EXAMPLES</span></span>

### <span data-ttu-id="cf046-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cf046-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="cf046-112">參數</span><span class="sxs-lookup"><span data-stu-id="cf046-112">PARAMETERS</span></span>

### <span data-ttu-id="cf046-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf046-113">-AsJob</span></span>
<span data-ttu-id="cf046-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf046-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf046-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf046-115">-DefaultProfile</span></span>
<span data-ttu-id="cf046-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf046-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf046-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf046-117">-Force</span></span>
<span data-ttu-id="cf046-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cf046-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf046-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf046-119">-InputObject</span></span>
<span data-ttu-id="cf046-120">{{Fill InputObject 描述}}</span><span class="sxs-lookup"><span data-stu-id="cf046-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="cf046-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf046-121">-Name</span></span>
<span data-ttu-id="cf046-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cf046-122">The resource name.</span></span>

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

### <span data-ttu-id="cf046-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf046-123">-PassThru</span></span>
<span data-ttu-id="cf046-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cf046-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf046-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cf046-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf046-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf046-126">-ResourceGroupName</span></span>
<span data-ttu-id="cf046-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf046-127">The resource group name.</span></span>

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

### <span data-ttu-id="cf046-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf046-128">-ResourceId</span></span>
<span data-ttu-id="cf046-129">IpAllocation 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf046-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="cf046-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cf046-130">-Confirm</span></span>
<span data-ttu-id="cf046-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf046-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf046-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf046-132">-WhatIf</span></span>
<span data-ttu-id="cf046-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf046-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf046-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf046-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf046-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf046-135">CommonParameters</span></span>
<span data-ttu-id="cf046-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf046-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf046-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf046-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf046-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cf046-138">INPUTS</span></span>

### <span data-ttu-id="cf046-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cf046-139">System.String</span></span>

## <span data-ttu-id="cf046-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cf046-140">OUTPUTS</span></span>

### <span data-ttu-id="cf046-141">System.object</span><span class="sxs-lookup"><span data-stu-id="cf046-141">System.Boolean</span></span>

## <span data-ttu-id="cf046-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cf046-142">NOTES</span></span>

## <span data-ttu-id="cf046-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf046-143">RELATED LINKS</span></span>
