---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625322"
---
# <span data-ttu-id="b0954-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b0954-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="b0954-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0954-102">SYNOPSIS</span></span>
<span data-ttu-id="b0954-103">移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="b0954-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0954-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0954-104">SYNTAX</span></span>

### <span data-ttu-id="b0954-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0954-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0954-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0954-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0954-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0954-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0954-108">說明</span><span class="sxs-lookup"><span data-stu-id="b0954-108">DESCRIPTION</span></span>
<span data-ttu-id="b0954-109">Remove-AzureRmContainerRegistry Cmdlet 會移除容器註冊。</span><span class="sxs-lookup"><span data-stu-id="b0954-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="b0954-110">示例</span><span class="sxs-lookup"><span data-stu-id="b0954-110">EXAMPLES</span></span>

### <span data-ttu-id="b0954-111">範例1：移除指定的容器註冊表</span><span class="sxs-lookup"><span data-stu-id="b0954-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="b0954-112">這個命令會移除指定的容器註冊。</span><span class="sxs-lookup"><span data-stu-id="b0954-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="b0954-113">參數</span><span class="sxs-lookup"><span data-stu-id="b0954-113">PARAMETERS</span></span>

### <span data-ttu-id="b0954-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0954-114">-DefaultProfile</span></span>
<span data-ttu-id="b0954-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0954-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0954-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0954-116">-Name</span></span>
<span data-ttu-id="b0954-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="b0954-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="b0954-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0954-118">-PassThru</span></span>
<span data-ttu-id="b0954-119">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="b0954-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b0954-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="b0954-120">-Registry</span></span>
<span data-ttu-id="b0954-121">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="b0954-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="b0954-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0954-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0954-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b0954-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0954-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0954-124">-ResourceId</span></span>
<span data-ttu-id="b0954-125">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b0954-125">The container registry resource id</span></span>

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

### <span data-ttu-id="b0954-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b0954-126">-Confirm</span></span>
<span data-ttu-id="b0954-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0954-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0954-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0954-128">-WhatIf</span></span>
<span data-ttu-id="b0954-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0954-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0954-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0954-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0954-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0954-131">CommonParameters</span></span>
<span data-ttu-id="b0954-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0954-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0954-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0954-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0954-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b0954-134">INPUTS</span></span>

### <span data-ttu-id="b0954-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b0954-135">System.String</span></span>

## <span data-ttu-id="b0954-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b0954-136">OUTPUTS</span></span>

### <span data-ttu-id="b0954-137">System.object</span><span class="sxs-lookup"><span data-stu-id="b0954-137">System.Boolean</span></span>

## <span data-ttu-id="b0954-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b0954-138">NOTES</span></span>

## <span data-ttu-id="b0954-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0954-139">RELATED LINKS</span></span>

[<span data-ttu-id="b0954-140">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b0954-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="b0954-141">AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b0954-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="b0954-142">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b0954-142">Update-AzureRmContainerRegistry</span></span>]()

