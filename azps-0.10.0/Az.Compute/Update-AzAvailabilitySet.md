---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794824"
---
# <span data-ttu-id="edc1d-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="edc1d-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="edc1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="edc1d-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="edc1d-103">Updates an availability set.</span></span>

## <span data-ttu-id="edc1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="edc1d-104">SYNTAX</span></span>

### <span data-ttu-id="edc1d-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="edc1d-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc1d-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="edc1d-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edc1d-107">說明</span><span class="sxs-lookup"><span data-stu-id="edc1d-107">DESCRIPTION</span></span>
<span data-ttu-id="edc1d-108">**AzAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="edc1d-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="edc1d-109">示例</span><span class="sxs-lookup"><span data-stu-id="edc1d-109">EXAMPLES</span></span>

### <span data-ttu-id="edc1d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="edc1d-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="edc1d-111">這個命令會將名為 "ResourceGroup01" 的資源群組中名為「AvSet01」的可用性集，更新為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="edc1d-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="edc1d-112">參數</span><span class="sxs-lookup"><span data-stu-id="edc1d-112">PARAMETERS</span></span>

### <span data-ttu-id="edc1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edc1d-113">-AsJob</span></span>
<span data-ttu-id="edc1d-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="edc1d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="edc1d-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="edc1d-115">-AvailabilitySet</span></span>
<span data-ttu-id="edc1d-116">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="edc1d-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="edc1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc1d-117">-DefaultProfile</span></span>
<span data-ttu-id="edc1d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edc1d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edc1d-119">-管理</span><span class="sxs-lookup"><span data-stu-id="edc1d-119">-Managed</span></span>
<span data-ttu-id="edc1d-120">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="edc1d-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="edc1d-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="edc1d-121">-Sku</span></span>
<span data-ttu-id="edc1d-122">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="edc1d-122">The Name of Sku</span></span>

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

### <span data-ttu-id="edc1d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="edc1d-123">-Confirm</span></span>
<span data-ttu-id="edc1d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edc1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc1d-125">-WhatIf</span></span>
<span data-ttu-id="edc1d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edc1d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edc1d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edc1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc1d-128">CommonParameters</span></span>
<span data-ttu-id="edc1d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edc1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc1d-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edc1d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc1d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="edc1d-131">INPUTS</span></span>

### <span data-ttu-id="edc1d-132">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="edc1d-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="edc1d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="edc1d-133">OUTPUTS</span></span>

### <span data-ttu-id="edc1d-134">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="edc1d-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="edc1d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="edc1d-135">NOTES</span></span>

## <span data-ttu-id="edc1d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="edc1d-136">RELATED LINKS</span></span>

