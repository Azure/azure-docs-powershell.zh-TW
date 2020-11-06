---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444675"
---
# <span data-ttu-id="7cbda-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7cbda-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="7cbda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cbda-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbda-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="7cbda-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cbda-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cbda-104">SYNTAX</span></span>

### <span data-ttu-id="7cbda-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cbda-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cbda-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="7cbda-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cbda-107">說明</span><span class="sxs-lookup"><span data-stu-id="7cbda-107">DESCRIPTION</span></span>
<span data-ttu-id="7cbda-108">**AzureRmAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="7cbda-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="7cbda-109">示例</span><span class="sxs-lookup"><span data-stu-id="7cbda-109">EXAMPLES</span></span>

### <span data-ttu-id="7cbda-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7cbda-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="7cbda-111">這個命令會將名為 "ResourceGroup01" 的資源群組中名為「AvSet01」的可用性集，更新為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="7cbda-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="7cbda-112">參數</span><span class="sxs-lookup"><span data-stu-id="7cbda-112">PARAMETERS</span></span>

### <span data-ttu-id="7cbda-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7cbda-113">-AvailabilitySet</span></span>
<span data-ttu-id="7cbda-114">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="7cbda-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbda-115">-管理</span><span class="sxs-lookup"><span data-stu-id="7cbda-115">-Managed</span></span>
<span data-ttu-id="7cbda-116">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="7cbda-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbda-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="7cbda-117">-Sku</span></span>
<span data-ttu-id="7cbda-118">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="7cbda-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbda-119">-確認</span><span class="sxs-lookup"><span data-stu-id="7cbda-119">-Confirm</span></span>
<span data-ttu-id="7cbda-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cbda-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbda-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbda-121">-WhatIf</span></span>
<span data-ttu-id="7cbda-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cbda-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cbda-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cbda-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbda-124">CommonParameters</span></span>
<span data-ttu-id="7cbda-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cbda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbda-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7cbda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbda-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7cbda-127">INPUTS</span></span>

### <span data-ttu-id="7cbda-128">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7cbda-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7cbda-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7cbda-129">OUTPUTS</span></span>

### <span data-ttu-id="7cbda-130">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7cbda-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7cbda-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7cbda-131">NOTES</span></span>

## <span data-ttu-id="7cbda-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cbda-132">RELATED LINKS</span></span>
