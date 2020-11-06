---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446363"
---
# <span data-ttu-id="4c7d0-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c7d0-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="4c7d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7d0-103">從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c7d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c7d0-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c7d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="4c7d0-106">**AzureRmAvailabilitySet** Cmdlet 會從 Azure 移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="4c7d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="4c7d0-108">範例1：移除可用性集</span><span class="sxs-lookup"><span data-stu-id="4c7d0-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4c7d0-109">這個命令會在名為 ResourceGroup11 的資源群組中移除一個名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4c7d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c7d0-110">PARAMETERS</span></span>

### <span data-ttu-id="4c7d0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4c7d0-111">-Force</span></span>
<span data-ttu-id="4c7d0-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c7d0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c7d0-113">-Name</span></span>
<span data-ttu-id="4c7d0-114">可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-114">The availability set name.</span></span>

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

### <span data-ttu-id="4c7d0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c7d0-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c7d0-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4c7d0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="4c7d0-117">-Confirm</span></span>
<span data-ttu-id="4c7d0-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c7d0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c7d0-119">-WhatIf</span></span>
<span data-ttu-id="4c7d0-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4c7d0-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c7d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7d0-122">CommonParameters</span></span>
<span data-ttu-id="4c7d0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7d0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7d0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4c7d0-125">INPUTS</span></span>

### <span data-ttu-id="4c7d0-126">所有</span><span class="sxs-lookup"><span data-stu-id="4c7d0-126">None</span></span>
<span data-ttu-id="4c7d0-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4c7d0-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c7d0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4c7d0-128">OUTPUTS</span></span>

## <span data-ttu-id="4c7d0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4c7d0-129">NOTES</span></span>

## <span data-ttu-id="4c7d0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c7d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="4c7d0-131">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c7d0-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4c7d0-132">新-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c7d0-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


