---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451315"
---
# <span data-ttu-id="0e3d4-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0e3d4-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="0e3d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3d4-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e3d4-104">SYNTAX</span></span>

### <span data-ttu-id="0e3d4-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e3d4-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e3d4-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="0e3d4-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3d4-107">說明</span><span class="sxs-lookup"><span data-stu-id="0e3d4-107">DESCRIPTION</span></span>
<span data-ttu-id="0e3d4-108">**AzureRmAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="0e3d4-109">示例</span><span class="sxs-lookup"><span data-stu-id="0e3d4-109">EXAMPLES</span></span>

### <span data-ttu-id="0e3d4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0e3d4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="0e3d4-111">這個命令會將名為 "ResourceGroup01" 的資源群組中名為「AvSet01」的可用性集，更新為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="0e3d4-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e3d4-112">PARAMETERS</span></span>

### <span data-ttu-id="0e3d4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e3d4-113">-AsJob</span></span>
<span data-ttu-id="0e3d4-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0e3d4-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0e3d4-115">-AvailabilitySet</span></span>
<span data-ttu-id="0e3d4-116">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="0e3d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3d4-117">-DefaultProfile</span></span>
<span data-ttu-id="0e3d4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3d4-119">-管理</span><span class="sxs-lookup"><span data-stu-id="0e3d4-119">-Managed</span></span>
<span data-ttu-id="0e3d4-120">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="0e3d4-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3d4-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="0e3d4-121">-Sku</span></span>
<span data-ttu-id="0e3d4-122">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="0e3d4-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3d4-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e3d4-123">-Tag</span></span>
<span data-ttu-id="0e3d4-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="0e3d4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="0e3d4-125">-Confirm</span></span>
<span data-ttu-id="0e3d4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3d4-127">-WhatIf</span></span>
<span data-ttu-id="0e3d4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e3d4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3d4-130">CommonParameters</span></span>
<span data-ttu-id="0e3d4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3d4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e3d4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3d4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0e3d4-133">INPUTS</span></span>

### <span data-ttu-id="0e3d4-134">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0e3d4-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="0e3d4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0e3d4-135">OUTPUTS</span></span>

### <span data-ttu-id="0e3d4-136">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0e3d4-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="0e3d4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0e3d4-137">NOTES</span></span>

## <span data-ttu-id="0e3d4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e3d4-138">RELATED LINKS</span></span>
