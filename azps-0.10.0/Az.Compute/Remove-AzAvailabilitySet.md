---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796086"
---
# <span data-ttu-id="5521c-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5521c-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="5521c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5521c-102">SYNOPSIS</span></span>
<span data-ttu-id="5521c-103">從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="5521c-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="5521c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5521c-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5521c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5521c-105">DESCRIPTION</span></span>
<span data-ttu-id="5521c-106">**AzAvailabilitySet** Cmdlet 會從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="5521c-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="5521c-107">示例</span><span class="sxs-lookup"><span data-stu-id="5521c-107">EXAMPLES</span></span>

### <span data-ttu-id="5521c-108">範例1：移除可用性集</span><span class="sxs-lookup"><span data-stu-id="5521c-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5521c-109">這個命令會在名為 ResourceGroup11 的資源群組中移除一個名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="5521c-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="5521c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5521c-110">PARAMETERS</span></span>

### <span data-ttu-id="5521c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5521c-111">-AsJob</span></span>
<span data-ttu-id="5521c-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="5521c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5521c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5521c-113">-DefaultProfile</span></span>
<span data-ttu-id="5521c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5521c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5521c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5521c-115">-Force</span></span>
<span data-ttu-id="5521c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5521c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5521c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5521c-117">-Name</span></span>
<span data-ttu-id="5521c-118">可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="5521c-118">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5521c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5521c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5521c-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5521c-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5521c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5521c-121">-Confirm</span></span>
<span data-ttu-id="5521c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5521c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5521c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5521c-123">-WhatIf</span></span>
<span data-ttu-id="5521c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5521c-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5521c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5521c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5521c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5521c-126">CommonParameters</span></span>
<span data-ttu-id="5521c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5521c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5521c-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5521c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5521c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5521c-129">INPUTS</span></span>

### <span data-ttu-id="5521c-130">所有</span><span class="sxs-lookup"><span data-stu-id="5521c-130">None</span></span>
<span data-ttu-id="5521c-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5521c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5521c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5521c-132">OUTPUTS</span></span>

### <span data-ttu-id="5521c-133">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="5521c-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5521c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5521c-134">NOTES</span></span>

## <span data-ttu-id="5521c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5521c-135">RELATED LINKS</span></span>

[<span data-ttu-id="5521c-136">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5521c-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="5521c-137">新-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5521c-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


