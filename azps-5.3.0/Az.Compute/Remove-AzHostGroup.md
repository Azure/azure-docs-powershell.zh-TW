---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449779"
---
# <span data-ttu-id="0e6d8-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="0e6d8-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="0e6d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6d8-103">移除主機群組。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-103">Removes a host group.</span></span>

## <span data-ttu-id="0e6d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e6d8-104">SYNTAX</span></span>

### <span data-ttu-id="0e6d8-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0e6d8-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6d8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0e6d8-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6d8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0e6d8-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="0e6d8-108">DESCRIPTION</span></span>
<span data-ttu-id="0e6d8-109">這個 Cmdlet 會刪除主機群組</span><span class="sxs-lookup"><span data-stu-id="0e6d8-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="0e6d8-110">示例</span><span class="sxs-lookup"><span data-stu-id="0e6d8-110">EXAMPLES</span></span>

### <span data-ttu-id="0e6d8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0e6d8-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="0e6d8-112">這個命令會取得並移除指定的主機群組。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="0e6d8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0e6d8-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="0e6d8-114">這個命令會移除指定的主機群組。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-114">This command removes the given host group.</span></span>

## <span data-ttu-id="0e6d8-115">參數</span><span class="sxs-lookup"><span data-stu-id="0e6d8-115">PARAMETERS</span></span>

### <span data-ttu-id="0e6d8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e6d8-116">-AsJob</span></span>
<span data-ttu-id="0e6d8-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e6d8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e6d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6d8-118">-DefaultProfile</span></span>
<span data-ttu-id="0e6d8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6d8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e6d8-120">-InputObject</span></span>
<span data-ttu-id="0e6d8-121">主機群組的本機物件。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="0e6d8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e6d8-122">-Name</span></span>
<span data-ttu-id="0e6d8-123">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-123">The name of the host group.</span></span>

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

### <span data-ttu-id="0e6d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e6d8-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e6d8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e6d8-126">-ResourceId</span></span>
<span data-ttu-id="0e6d8-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="0e6d8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="0e6d8-128">-Confirm</span></span>
<span data-ttu-id="0e6d8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6d8-130">-WhatIf</span></span>
<span data-ttu-id="0e6d8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6d8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6d8-133">CommonParameters</span></span>
<span data-ttu-id="0e6d8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6d8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6d8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0e6d8-136">INPUTS</span></span>

### <span data-ttu-id="0e6d8-137">System.object</span><span class="sxs-lookup"><span data-stu-id="0e6d8-137">System.String</span></span>

### <span data-ttu-id="0e6d8-138">PSHostGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="0e6d8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0e6d8-139">OUTPUTS</span></span>

### <span data-ttu-id="0e6d8-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="0e6d8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0e6d8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0e6d8-141">NOTES</span></span>

## <span data-ttu-id="0e6d8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e6d8-142">RELATED LINKS</span></span>
