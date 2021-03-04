---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: 49da6e1efbd1bb0e6b0ac4dc693d51fe5b58bfac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917769"
---
# <span data-ttu-id="0eff6-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eff6-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="0eff6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0eff6-102">SYNOPSIS</span></span>
<span data-ttu-id="0eff6-103">移除容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="0eff6-103">Removes a container registry.</span></span>

## <span data-ttu-id="0eff6-104">語法</span><span class="sxs-lookup"><span data-stu-id="0eff6-104">SYNTAX</span></span>

### <span data-ttu-id="0eff6-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0eff6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eff6-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eff6-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eff6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eff6-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eff6-108">描述</span><span class="sxs-lookup"><span data-stu-id="0eff6-108">DESCRIPTION</span></span>
<span data-ttu-id="0eff6-109">此Remove-AzContainerRegistry Cmdlet 會移除容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="0eff6-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="0eff6-110">例子</span><span class="sxs-lookup"><span data-stu-id="0eff6-110">EXAMPLES</span></span>

### <span data-ttu-id="0eff6-111">範例 1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="0eff6-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="0eff6-112">此命令會移除指定的容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="0eff6-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="0eff6-113">參數</span><span class="sxs-lookup"><span data-stu-id="0eff6-113">PARAMETERS</span></span>

### <span data-ttu-id="0eff6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eff6-114">-DefaultProfile</span></span>
<span data-ttu-id="0eff6-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0eff6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eff6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eff6-116">-Name</span></span>
<span data-ttu-id="0eff6-117">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="0eff6-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eff6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eff6-118">-PassThru</span></span>
<span data-ttu-id="0eff6-119">表示移除成功時，此 Cmdlet 會返回 True。</span><span class="sxs-lookup"><span data-stu-id="0eff6-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="0eff6-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="0eff6-120">-Registry</span></span>
<span data-ttu-id="0eff6-121">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="0eff6-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eff6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eff6-122">-ResourceGroupName</span></span>
<span data-ttu-id="0eff6-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0eff6-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eff6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eff6-124">-ResourceId</span></span>
<span data-ttu-id="0eff6-125">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0eff6-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eff6-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0eff6-126">-Confirm</span></span>
<span data-ttu-id="0eff6-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0eff6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eff6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eff6-128">-WhatIf</span></span>
<span data-ttu-id="0eff6-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eff6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eff6-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eff6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eff6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eff6-131">CommonParameters</span></span>
<span data-ttu-id="0eff6-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0eff6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eff6-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eff6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eff6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0eff6-134">INPUTS</span></span>

### <span data-ttu-id="0eff6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0eff6-135">System.String</span></span>

## <span data-ttu-id="0eff6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0eff6-136">OUTPUTS</span></span>

### <span data-ttu-id="0eff6-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0eff6-137">System.Boolean</span></span>

## <span data-ttu-id="0eff6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0eff6-138">NOTES</span></span>

## <span data-ttu-id="0eff6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eff6-139">RELATED LINKS</span></span>

[<span data-ttu-id="0eff6-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eff6-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="0eff6-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eff6-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="0eff6-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eff6-142">Update-AzContainerRegistry</span></span>]()

