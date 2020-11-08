---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137025"
---
# <span data-ttu-id="af5e0-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af5e0-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="af5e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="af5e0-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="af5e0-103">Removes a container registry.</span></span>

## <span data-ttu-id="af5e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="af5e0-104">SYNTAX</span></span>

### <span data-ttu-id="af5e0-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af5e0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5e0-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af5e0-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af5e0-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5e0-108">說明</span><span class="sxs-lookup"><span data-stu-id="af5e0-108">DESCRIPTION</span></span>
<span data-ttu-id="af5e0-109">Remove-AzContainerRegistry Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="af5e0-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="af5e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="af5e0-110">EXAMPLES</span></span>

### <span data-ttu-id="af5e0-111">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="af5e0-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="af5e0-112">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="af5e0-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="af5e0-113">參數</span><span class="sxs-lookup"><span data-stu-id="af5e0-113">PARAMETERS</span></span>

### <span data-ttu-id="af5e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5e0-114">-DefaultProfile</span></span>
<span data-ttu-id="af5e0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af5e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af5e0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="af5e0-116">-Name</span></span>
<span data-ttu-id="af5e0-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="af5e0-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="af5e0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af5e0-118">-PassThru</span></span>
<span data-ttu-id="af5e0-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="af5e0-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="af5e0-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="af5e0-120">-Registry</span></span>
<span data-ttu-id="af5e0-121">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="af5e0-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="af5e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="af5e0-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="af5e0-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="af5e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af5e0-124">-ResourceId</span></span>
<span data-ttu-id="af5e0-125">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="af5e0-125">The container registry resource id</span></span>

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

### <span data-ttu-id="af5e0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="af5e0-126">-Confirm</span></span>
<span data-ttu-id="af5e0-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af5e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5e0-128">-WhatIf</span></span>
<span data-ttu-id="af5e0-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af5e0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af5e0-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af5e0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5e0-131">CommonParameters</span></span>
<span data-ttu-id="af5e0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af5e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5e0-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af5e0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5e0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="af5e0-134">INPUTS</span></span>

### <span data-ttu-id="af5e0-135">System.object</span><span class="sxs-lookup"><span data-stu-id="af5e0-135">System.String</span></span>

## <span data-ttu-id="af5e0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="af5e0-136">OUTPUTS</span></span>

### <span data-ttu-id="af5e0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="af5e0-137">System.Boolean</span></span>

## <span data-ttu-id="af5e0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="af5e0-138">NOTES</span></span>

## <span data-ttu-id="af5e0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="af5e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="af5e0-140">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af5e0-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="af5e0-141">AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af5e0-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="af5e0-142">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af5e0-142">Update-AzContainerRegistry</span></span>]()

