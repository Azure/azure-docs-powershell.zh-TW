---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613063"
---
# <span data-ttu-id="78d17-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78d17-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="78d17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78d17-102">SYNOPSIS</span></span>
<span data-ttu-id="78d17-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="78d17-103">Removes a container registry.</span></span>

## <span data-ttu-id="78d17-104">句法</span><span class="sxs-lookup"><span data-stu-id="78d17-104">SYNTAX</span></span>

### <span data-ttu-id="78d17-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78d17-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d17-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d17-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d17-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d17-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d17-108">說明</span><span class="sxs-lookup"><span data-stu-id="78d17-108">DESCRIPTION</span></span>
<span data-ttu-id="78d17-109">Remove-AzContainerRegistry Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="78d17-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="78d17-110">示例</span><span class="sxs-lookup"><span data-stu-id="78d17-110">EXAMPLES</span></span>

### <span data-ttu-id="78d17-111">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="78d17-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="78d17-112">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="78d17-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="78d17-113">參數</span><span class="sxs-lookup"><span data-stu-id="78d17-113">PARAMETERS</span></span>

### <span data-ttu-id="78d17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d17-114">-DefaultProfile</span></span>
<span data-ttu-id="78d17-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78d17-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d17-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="78d17-116">-Name</span></span>
<span data-ttu-id="78d17-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="78d17-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="78d17-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78d17-118">-PassThru</span></span>
<span data-ttu-id="78d17-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="78d17-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="78d17-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="78d17-120">-Registry</span></span>
<span data-ttu-id="78d17-121">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="78d17-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="78d17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d17-122">-ResourceGroupName</span></span>
<span data-ttu-id="78d17-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="78d17-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="78d17-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d17-124">-ResourceId</span></span>
<span data-ttu-id="78d17-125">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="78d17-125">The container registry resource id</span></span>

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

### <span data-ttu-id="78d17-126">-確認</span><span class="sxs-lookup"><span data-stu-id="78d17-126">-Confirm</span></span>
<span data-ttu-id="78d17-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78d17-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d17-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d17-128">-WhatIf</span></span>
<span data-ttu-id="78d17-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78d17-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d17-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78d17-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d17-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d17-131">CommonParameters</span></span>
<span data-ttu-id="78d17-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78d17-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d17-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78d17-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d17-134">輸入</span><span class="sxs-lookup"><span data-stu-id="78d17-134">INPUTS</span></span>

### <span data-ttu-id="78d17-135">System.object</span><span class="sxs-lookup"><span data-stu-id="78d17-135">System.String</span></span>

## <span data-ttu-id="78d17-136">輸出</span><span class="sxs-lookup"><span data-stu-id="78d17-136">OUTPUTS</span></span>

### <span data-ttu-id="78d17-137">System.object</span><span class="sxs-lookup"><span data-stu-id="78d17-137">System.Boolean</span></span>

## <span data-ttu-id="78d17-138">筆記</span><span class="sxs-lookup"><span data-stu-id="78d17-138">NOTES</span></span>

## <span data-ttu-id="78d17-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="78d17-139">RELATED LINKS</span></span>

[<span data-ttu-id="78d17-140">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78d17-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="78d17-141">AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78d17-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="78d17-142">更新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78d17-142">Update-AzContainerRegistry</span></span>]()

