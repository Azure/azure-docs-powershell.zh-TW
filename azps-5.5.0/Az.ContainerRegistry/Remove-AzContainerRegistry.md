---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138578"
---
# <span data-ttu-id="2fbbf-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fbbf-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="2fbbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbbf-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-103">Removes a container registry.</span></span>

## <span data-ttu-id="2fbbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fbbf-104">SYNTAX</span></span>

### <span data-ttu-id="2fbbf-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2fbbf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fbbf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fbbf-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fbbf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fbbf-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbbf-108">說明</span><span class="sxs-lookup"><span data-stu-id="2fbbf-108">DESCRIPTION</span></span>
<span data-ttu-id="2fbbf-109">Remove-AzContainerRegistry Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="2fbbf-110">示例</span><span class="sxs-lookup"><span data-stu-id="2fbbf-110">EXAMPLES</span></span>

### <span data-ttu-id="2fbbf-111">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="2fbbf-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="2fbbf-112">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="2fbbf-113">參數</span><span class="sxs-lookup"><span data-stu-id="2fbbf-113">PARAMETERS</span></span>

### <span data-ttu-id="2fbbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbbf-114">-DefaultProfile</span></span>
<span data-ttu-id="2fbbf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2fbbf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fbbf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fbbf-116">-Name</span></span>
<span data-ttu-id="2fbbf-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="2fbbf-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fbbf-118">-PassThru</span></span>
<span data-ttu-id="2fbbf-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="2fbbf-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="2fbbf-120">-Registry</span></span>
<span data-ttu-id="2fbbf-121">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="2fbbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fbbf-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="2fbbf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fbbf-124">-ResourceId</span></span>
<span data-ttu-id="2fbbf-125">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2fbbf-125">The container registry resource id</span></span>

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

### <span data-ttu-id="2fbbf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="2fbbf-126">-Confirm</span></span>
<span data-ttu-id="2fbbf-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fbbf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fbbf-128">-WhatIf</span></span>
<span data-ttu-id="2fbbf-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fbbf-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fbbf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbbf-131">CommonParameters</span></span>
<span data-ttu-id="2fbbf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbbf-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2fbbf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbbf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2fbbf-134">INPUTS</span></span>

### <span data-ttu-id="2fbbf-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2fbbf-135">System.String</span></span>

## <span data-ttu-id="2fbbf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2fbbf-136">OUTPUTS</span></span>

### <span data-ttu-id="2fbbf-137">System.object</span><span class="sxs-lookup"><span data-stu-id="2fbbf-137">System.Boolean</span></span>

## <span data-ttu-id="2fbbf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2fbbf-138">NOTES</span></span>

## <span data-ttu-id="2fbbf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fbbf-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fbbf-140">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fbbf-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="2fbbf-141">AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fbbf-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="2fbbf-142">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fbbf-142">Update-AzContainerRegistry</span></span>]()

