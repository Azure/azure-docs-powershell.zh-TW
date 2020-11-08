---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138214"
---
# <span data-ttu-id="88d3b-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="88d3b-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="88d3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="88d3b-103">更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="88d3b-103">Updates an availability set.</span></span>

## <span data-ttu-id="88d3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="88d3b-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="88d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="88d3b-106">**AzAvailabilitySet** Cmdlet 會更新可用性集。</span><span class="sxs-lookup"><span data-stu-id="88d3b-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="88d3b-107">示例</span><span class="sxs-lookup"><span data-stu-id="88d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="88d3b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="88d3b-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="88d3b-109">這個命令會將名為 "ResourceGroup01" 的資源群組中名為「AvSet01」的可用性集，更新為受管理的可用性集。</span><span class="sxs-lookup"><span data-stu-id="88d3b-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="88d3b-110">參數</span><span class="sxs-lookup"><span data-stu-id="88d3b-110">PARAMETERS</span></span>

### <span data-ttu-id="88d3b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88d3b-111">-AsJob</span></span>
<span data-ttu-id="88d3b-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="88d3b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="88d3b-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="88d3b-113">-AvailabilitySet</span></span>
<span data-ttu-id="88d3b-114">指定要更新的可用性集物件。</span><span class="sxs-lookup"><span data-stu-id="88d3b-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="88d3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d3b-115">-DefaultProfile</span></span>
<span data-ttu-id="88d3b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88d3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88d3b-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="88d3b-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="88d3b-118">要與此可用性集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88d3b-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="88d3b-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="88d3b-119">-Sku</span></span>
<span data-ttu-id="88d3b-120">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="88d3b-120">The Name of Sku</span></span>

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

### <span data-ttu-id="88d3b-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="88d3b-121">-Tag</span></span>
<span data-ttu-id="88d3b-122">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="88d3b-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="88d3b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="88d3b-123">-Confirm</span></span>
<span data-ttu-id="88d3b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88d3b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d3b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d3b-125">-WhatIf</span></span>
<span data-ttu-id="88d3b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88d3b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88d3b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88d3b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d3b-128">CommonParameters</span></span>
<span data-ttu-id="88d3b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88d3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d3b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88d3b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d3b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="88d3b-131">INPUTS</span></span>

### <span data-ttu-id="88d3b-132">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="88d3b-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="88d3b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="88d3b-133">OUTPUTS</span></span>

### <span data-ttu-id="88d3b-134">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="88d3b-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="88d3b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="88d3b-135">NOTES</span></span>

## <span data-ttu-id="88d3b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="88d3b-136">RELATED LINKS</span></span>