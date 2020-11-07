---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802526"
---
# <span data-ttu-id="b9183-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b9183-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="b9183-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9183-102">SYNOPSIS</span></span>
<span data-ttu-id="b9183-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="b9183-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9183-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9183-104">SYNTAX</span></span>

### <span data-ttu-id="b9183-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9183-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9183-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="b9183-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9183-107">說明</span><span class="sxs-lookup"><span data-stu-id="b9183-107">DESCRIPTION</span></span>
<span data-ttu-id="b9183-108">**AzureRmAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="b9183-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="b9183-109">示例</span><span class="sxs-lookup"><span data-stu-id="b9183-109">EXAMPLES</span></span>

### <span data-ttu-id="b9183-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b9183-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="b9183-111">這個命令會將名為 "ResourceGroup01" 的資源群組中名為「AvSet01」的可用性集，更新為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="b9183-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="b9183-112">參數</span><span class="sxs-lookup"><span data-stu-id="b9183-112">PARAMETERS</span></span>

### <span data-ttu-id="b9183-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9183-113">-AsJob</span></span>
<span data-ttu-id="b9183-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b9183-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9183-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b9183-115">-AvailabilitySet</span></span>
<span data-ttu-id="b9183-116">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="b9183-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="b9183-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9183-117">-DefaultProfile</span></span>
<span data-ttu-id="b9183-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9183-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9183-119">-管理</span><span class="sxs-lookup"><span data-stu-id="b9183-119">-Managed</span></span>
<span data-ttu-id="b9183-120">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="b9183-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="b9183-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="b9183-121">-Sku</span></span>
<span data-ttu-id="b9183-122">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="b9183-122">The Name of Sku</span></span>

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

### <span data-ttu-id="b9183-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b9183-123">-Confirm</span></span>
<span data-ttu-id="b9183-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9183-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9183-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9183-125">-WhatIf</span></span>
<span data-ttu-id="b9183-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9183-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9183-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9183-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9183-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9183-128">CommonParameters</span></span>
<span data-ttu-id="b9183-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9183-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9183-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9183-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9183-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b9183-131">INPUTS</span></span>

### <span data-ttu-id="b9183-132">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b9183-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b9183-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b9183-133">OUTPUTS</span></span>

### <span data-ttu-id="b9183-134">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b9183-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b9183-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b9183-135">NOTES</span></span>

## <span data-ttu-id="b9183-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9183-136">RELATED LINKS</span></span>

