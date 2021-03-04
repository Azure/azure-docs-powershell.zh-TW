---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909750"
---
# <span data-ttu-id="1b616-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1b616-101">Remove-AzHost</span></span>

## <span data-ttu-id="1b616-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b616-102">SYNOPSIS</span></span>
<span data-ttu-id="1b616-103">移除主機。</span><span class="sxs-lookup"><span data-stu-id="1b616-103">Removes a host.</span></span>

## <span data-ttu-id="1b616-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b616-104">SYNTAX</span></span>

### <span data-ttu-id="1b616-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1b616-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b616-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1b616-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b616-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1b616-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b616-108">描述</span><span class="sxs-lookup"><span data-stu-id="1b616-108">DESCRIPTION</span></span>
<span data-ttu-id="1b616-109">此 Cmdlet 會刪除主機</span><span class="sxs-lookup"><span data-stu-id="1b616-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="1b616-110">例子</span><span class="sxs-lookup"><span data-stu-id="1b616-110">EXAMPLES</span></span>

### <span data-ttu-id="1b616-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1b616-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="1b616-112">此命令會獲得並移除所給予的主機。</span><span class="sxs-lookup"><span data-stu-id="1b616-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="1b616-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="1b616-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="1b616-114">此命令會移除所給予的主機。</span><span class="sxs-lookup"><span data-stu-id="1b616-114">This command removes the given host.</span></span>

## <span data-ttu-id="1b616-115">參數</span><span class="sxs-lookup"><span data-stu-id="1b616-115">PARAMETERS</span></span>

### <span data-ttu-id="1b616-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b616-116">-AsJob</span></span>
<span data-ttu-id="1b616-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b616-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b616-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b616-118">-DefaultProfile</span></span>
<span data-ttu-id="1b616-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b616-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b616-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="1b616-120">-HostGroupName</span></span>
<span data-ttu-id="1b616-121">主機組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b616-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b616-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b616-122">-InputObject</span></span>
<span data-ttu-id="1b616-123">主機的本機物件。</span><span class="sxs-lookup"><span data-stu-id="1b616-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b616-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b616-124">-Name</span></span>
<span data-ttu-id="1b616-125">主機名稱。</span><span class="sxs-lookup"><span data-stu-id="1b616-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b616-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b616-126">-ResourceGroupName</span></span>
<span data-ttu-id="1b616-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b616-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b616-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b616-128">-ResourceId</span></span>
<span data-ttu-id="1b616-129">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b616-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="1b616-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1b616-130">-Confirm</span></span>
<span data-ttu-id="1b616-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1b616-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b616-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b616-132">-WhatIf</span></span>
<span data-ttu-id="1b616-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b616-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b616-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b616-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b616-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b616-135">CommonParameters</span></span>
<span data-ttu-id="1b616-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b616-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b616-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b616-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b616-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1b616-138">INPUTS</span></span>

### <span data-ttu-id="1b616-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1b616-139">System.String</span></span>

### <span data-ttu-id="1b616-140">Microsoft.Azure.Commands.Compute.Automation.models.PSHost</span><span class="sxs-lookup"><span data-stu-id="1b616-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="1b616-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1b616-141">OUTPUTS</span></span>

### <span data-ttu-id="1b616-142">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1b616-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1b616-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1b616-143">NOTES</span></span>

## <span data-ttu-id="1b616-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b616-144">RELATED LINKS</span></span>
