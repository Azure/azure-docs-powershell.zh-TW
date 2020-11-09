---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287536"
---
# <span data-ttu-id="0f6d7-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="0f6d7-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="0f6d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6d7-103">移除主機群組。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-103">Removes a host group.</span></span>

## <span data-ttu-id="0f6d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f6d7-104">SYNTAX</span></span>

### <span data-ttu-id="0f6d7-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0f6d7-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6d7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0f6d7-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6d7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0f6d7-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6d7-108">說明</span><span class="sxs-lookup"><span data-stu-id="0f6d7-108">DESCRIPTION</span></span>
<span data-ttu-id="0f6d7-109">這個 Cmdlet 會刪除主機群組</span><span class="sxs-lookup"><span data-stu-id="0f6d7-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="0f6d7-110">示例</span><span class="sxs-lookup"><span data-stu-id="0f6d7-110">EXAMPLES</span></span>

### <span data-ttu-id="0f6d7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0f6d7-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="0f6d7-112">這個命令會取得並移除指定的主機群組。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="0f6d7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0f6d7-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="0f6d7-114">這個命令會移除指定的主機群組。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-114">This command removes the given host group.</span></span>

## <span data-ttu-id="0f6d7-115">參數</span><span class="sxs-lookup"><span data-stu-id="0f6d7-115">PARAMETERS</span></span>

### <span data-ttu-id="0f6d7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f6d7-116">-AsJob</span></span>
<span data-ttu-id="0f6d7-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0f6d7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f6d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6d7-118">-DefaultProfile</span></span>
<span data-ttu-id="0f6d7-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f6d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f6d7-120">-InputObject</span></span>
<span data-ttu-id="0f6d7-121">主機群組的本機物件。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f6d7-122">-Name</span></span>
<span data-ttu-id="0f6d7-123">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f6d7-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6d7-126">-ResourceId</span></span>
<span data-ttu-id="0f6d7-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d7-128">-確認</span><span class="sxs-lookup"><span data-stu-id="0f6d7-128">-Confirm</span></span>
<span data-ttu-id="0f6d7-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6d7-130">-WhatIf</span></span>
<span data-ttu-id="0f6d7-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6d7-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6d7-133">CommonParameters</span></span>
<span data-ttu-id="0f6d7-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6d7-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6d7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0f6d7-136">INPUTS</span></span>

### <span data-ttu-id="0f6d7-137">System.object</span><span class="sxs-lookup"><span data-stu-id="0f6d7-137">System.String</span></span>

### <span data-ttu-id="0f6d7-138">PSHostGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="0f6d7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0f6d7-139">OUTPUTS</span></span>

### <span data-ttu-id="0f6d7-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="0f6d7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0f6d7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0f6d7-141">NOTES</span></span>

## <span data-ttu-id="0f6d7-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f6d7-142">RELATED LINKS</span></span>
