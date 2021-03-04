---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4f268ae4278712e16e8efc126702d0130dc225cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905161"
---
# <span data-ttu-id="90192-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90192-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="90192-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90192-102">SYNOPSIS</span></span>
<span data-ttu-id="90192-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="90192-103">Updates an availability set.</span></span>

## <span data-ttu-id="90192-104">語法</span><span class="sxs-lookup"><span data-stu-id="90192-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90192-105">描述</span><span class="sxs-lookup"><span data-stu-id="90192-105">DESCRIPTION</span></span>
<span data-ttu-id="90192-106">**Update-AzAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="90192-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="90192-107">例子</span><span class="sxs-lookup"><span data-stu-id="90192-107">EXAMPLES</span></span>

### <span data-ttu-id="90192-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="90192-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="90192-109">此命令會更新資源群組中名為 "ResourceGroup01" 的可用性集 "AvSet01" 為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="90192-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="90192-110">參數</span><span class="sxs-lookup"><span data-stu-id="90192-110">PARAMETERS</span></span>

### <span data-ttu-id="90192-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90192-111">-AsJob</span></span>
<span data-ttu-id="90192-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="90192-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="90192-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90192-113">-AvailabilitySet</span></span>
<span data-ttu-id="90192-114">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="90192-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90192-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90192-115">-DefaultProfile</span></span>
<span data-ttu-id="90192-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90192-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90192-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="90192-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="90192-118">要用於此可用性集的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="90192-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90192-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="90192-119">-Sku</span></span>
<span data-ttu-id="90192-120">SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="90192-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90192-121">-標記</span><span class="sxs-lookup"><span data-stu-id="90192-121">-Tag</span></span>
<span data-ttu-id="90192-122">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="90192-122">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90192-123">-確認</span><span class="sxs-lookup"><span data-stu-id="90192-123">-Confirm</span></span>
<span data-ttu-id="90192-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90192-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90192-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90192-125">-WhatIf</span></span>
<span data-ttu-id="90192-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90192-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90192-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90192-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90192-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90192-128">CommonParameters</span></span>
<span data-ttu-id="90192-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90192-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90192-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90192-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90192-131">輸入</span><span class="sxs-lookup"><span data-stu-id="90192-131">INPUTS</span></span>

### <span data-ttu-id="90192-132">Microsoft.Azure.Commands.Compute.models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90192-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="90192-133">輸出</span><span class="sxs-lookup"><span data-stu-id="90192-133">OUTPUTS</span></span>

### <span data-ttu-id="90192-134">Microsoft.Azure.Commands.Compute.models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90192-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="90192-135">筆記</span><span class="sxs-lookup"><span data-stu-id="90192-135">NOTES</span></span>

## <span data-ttu-id="90192-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="90192-136">RELATED LINKS</span></span>
