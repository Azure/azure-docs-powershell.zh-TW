---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: a4b4e5048e4d11a5b376650b94520232f10b29bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911162"
---
# <span data-ttu-id="a5f48-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a5f48-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="a5f48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5f48-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f48-103">從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="a5f48-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="a5f48-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5f48-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5f48-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5f48-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f48-106">**Remove-AzAvailabilitySet** Cmdlet 會從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="a5f48-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="a5f48-107">例子</span><span class="sxs-lookup"><span data-stu-id="a5f48-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f48-108">範例 1：移除可用性集</span><span class="sxs-lookup"><span data-stu-id="a5f48-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a5f48-109">此命令會移除名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="a5f48-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a5f48-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5f48-110">PARAMETERS</span></span>

### <span data-ttu-id="a5f48-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5f48-111">-AsJob</span></span>
<span data-ttu-id="a5f48-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a5f48-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a5f48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f48-113">-DefaultProfile</span></span>
<span data-ttu-id="a5f48-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5f48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f48-115">-強制</span><span class="sxs-lookup"><span data-stu-id="a5f48-115">-Force</span></span>
<span data-ttu-id="a5f48-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a5f48-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5f48-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5f48-117">-Name</span></span>
<span data-ttu-id="a5f48-118">可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f48-118">The availability set name.</span></span>

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

### <span data-ttu-id="a5f48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f48-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5f48-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f48-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a5f48-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a5f48-121">-Confirm</span></span>
<span data-ttu-id="a5f48-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5f48-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f48-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f48-123">-WhatIf</span></span>
<span data-ttu-id="a5f48-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5f48-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f48-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5f48-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f48-126">CommonParameters</span></span>
<span data-ttu-id="a5f48-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5f48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f48-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5f48-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f48-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a5f48-129">INPUTS</span></span>

### <span data-ttu-id="a5f48-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a5f48-130">System.String</span></span>

## <span data-ttu-id="a5f48-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a5f48-131">OUTPUTS</span></span>

### <span data-ttu-id="a5f48-132">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a5f48-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a5f48-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a5f48-133">NOTES</span></span>

## <span data-ttu-id="a5f48-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5f48-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5f48-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a5f48-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a5f48-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a5f48-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


