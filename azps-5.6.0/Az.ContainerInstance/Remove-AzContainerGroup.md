---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: f4774ea7dec4ddd8df29c0a131fbaf080cbbba94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915577"
---
# <span data-ttu-id="abdeb-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="abdeb-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="abdeb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="abdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="abdeb-103">移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-103">Removes a container group.</span></span>

## <span data-ttu-id="abdeb-104">語法</span><span class="sxs-lookup"><span data-stu-id="abdeb-104">SYNTAX</span></span>

### <span data-ttu-id="abdeb-105">RemoveContainerGroupByResourceGroupAndNameParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="abdeb-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abdeb-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="abdeb-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abdeb-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="abdeb-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abdeb-108">描述</span><span class="sxs-lookup"><span data-stu-id="abdeb-108">DESCRIPTION</span></span>
<span data-ttu-id="abdeb-109">**Remove-AzContainerGroup** Cmdlet 會移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="abdeb-110">例子</span><span class="sxs-lookup"><span data-stu-id="abdeb-110">EXAMPLES</span></span>

### <span data-ttu-id="abdeb-111">範例 1：移除容器群組</span><span class="sxs-lookup"><span data-stu-id="abdeb-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="abdeb-112">此命令會移除指定的容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="abdeb-113">範例 2：使用管道移除容器群組</span><span class="sxs-lookup"><span data-stu-id="abdeb-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="abdeb-114">此命令會以管線移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="abdeb-115">範例 3：根據資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="abdeb-116">此命令會按資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="abdeb-117">參數</span><span class="sxs-lookup"><span data-stu-id="abdeb-117">PARAMETERS</span></span>

### <span data-ttu-id="abdeb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdeb-118">-DefaultProfile</span></span>
<span data-ttu-id="abdeb-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="abdeb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abdeb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abdeb-120">-InputObject</span></span>
<span data-ttu-id="abdeb-121">要移除的容器群組。</span><span class="sxs-lookup"><span data-stu-id="abdeb-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abdeb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="abdeb-122">-Name</span></span>
<span data-ttu-id="abdeb-123">容器組名。</span><span class="sxs-lookup"><span data-stu-id="abdeb-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdeb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abdeb-124">-PassThru</span></span>
<span data-ttu-id="abdeb-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="abdeb-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="abdeb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abdeb-126">-ResourceGroupName</span></span>
<span data-ttu-id="abdeb-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="abdeb-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdeb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abdeb-128">-ResourceId</span></span>
<span data-ttu-id="abdeb-129">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="abdeb-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abdeb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="abdeb-130">-Confirm</span></span>
<span data-ttu-id="abdeb-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="abdeb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdeb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdeb-132">-WhatIf</span></span>
<span data-ttu-id="abdeb-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abdeb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abdeb-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abdeb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdeb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdeb-135">CommonParameters</span></span>
<span data-ttu-id="abdeb-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="abdeb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdeb-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="abdeb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdeb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="abdeb-138">INPUTS</span></span>

### <span data-ttu-id="abdeb-139">Microsoft.Azure.Commands.ContainerInstance.models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="abdeb-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="abdeb-140">System.String</span><span class="sxs-lookup"><span data-stu-id="abdeb-140">System.String</span></span>

## <span data-ttu-id="abdeb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="abdeb-141">OUTPUTS</span></span>

### <span data-ttu-id="abdeb-142">Microsoft.Azure.Commands.ContainerInstance.models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="abdeb-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="abdeb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="abdeb-143">NOTES</span></span>

## <span data-ttu-id="abdeb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="abdeb-144">RELATED LINKS</span></span>
