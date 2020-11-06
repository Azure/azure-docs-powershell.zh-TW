---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 7dccf9410ff4d03503763354aabbe6b02d0c0c6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613278"
---
# <span data-ttu-id="d8d9b-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d9b-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="d8d9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d9b-103">從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="d8d9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8d9b-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d9b-106">**AzAvailabilitySet** Cmdlet 會從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="d8d9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8d9b-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d9b-108">範例1：移除可用性集</span><span class="sxs-lookup"><span data-stu-id="d8d9b-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d8d9b-109">這個命令會在名為 ResourceGroup11 的資源群組中移除一個名為 AvailabilitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d8d9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8d9b-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d9b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8d9b-111">-AsJob</span></span>
<span data-ttu-id="d8d9b-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d8d9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d9b-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d9b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8d9b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d8d9b-115">-Force</span></span>
<span data-ttu-id="d8d9b-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d9b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8d9b-117">-Name</span></span>
<span data-ttu-id="d8d9b-118">可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d9b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d9b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8d9b-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d9b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d8d9b-121">-Confirm</span></span>
<span data-ttu-id="d8d9b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d9b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d9b-123">-WhatIf</span></span>
<span data-ttu-id="d8d9b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d9b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d9b-126">CommonParameters</span></span>
<span data-ttu-id="d8d9b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d9b-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d9b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d8d9b-129">INPUTS</span></span>

### <span data-ttu-id="d8d9b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d8d9b-130">System.String</span></span>

## <span data-ttu-id="d8d9b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d8d9b-131">OUTPUTS</span></span>

### <span data-ttu-id="d8d9b-132">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d8d9b-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d8d9b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d8d9b-133">NOTES</span></span>

## <span data-ttu-id="d8d9b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8d9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d8d9b-135">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d9b-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d8d9b-136">新-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d9b-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

