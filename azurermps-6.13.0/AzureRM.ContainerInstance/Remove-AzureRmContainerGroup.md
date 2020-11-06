---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445639"
---
# <span data-ttu-id="357d5-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="357d5-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="357d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="357d5-102">SYNOPSIS</span></span>
<span data-ttu-id="357d5-103">移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="357d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="357d5-104">SYNTAX</span></span>

### <span data-ttu-id="357d5-105">RemoveContainerGroupByResourceGroupAndNameParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="357d5-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357d5-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="357d5-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357d5-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="357d5-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357d5-108">說明</span><span class="sxs-lookup"><span data-stu-id="357d5-108">DESCRIPTION</span></span>
<span data-ttu-id="357d5-109">**AzureRmContainerGroup** Cmdlet 會移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="357d5-110">示例</span><span class="sxs-lookup"><span data-stu-id="357d5-110">EXAMPLES</span></span>

### <span data-ttu-id="357d5-111">範例1：移除容器群組</span><span class="sxs-lookup"><span data-stu-id="357d5-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="357d5-112">這個命令會移除指定的容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="357d5-113">範例2：依管道移除容器群組</span><span class="sxs-lookup"><span data-stu-id="357d5-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="357d5-114">這個命令會透過 [管道] 移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="357d5-115">範例3：依資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="357d5-116">這個命令會依資源識別碼移除容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="357d5-117">參數</span><span class="sxs-lookup"><span data-stu-id="357d5-117">PARAMETERS</span></span>

### <span data-ttu-id="357d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357d5-118">-DefaultProfile</span></span>
<span data-ttu-id="357d5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="357d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="357d5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="357d5-120">-InputObject</span></span>
<span data-ttu-id="357d5-121">要移除的容器群組。</span><span class="sxs-lookup"><span data-stu-id="357d5-121">The container group to remove.</span></span>

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

### <span data-ttu-id="357d5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="357d5-122">-Name</span></span>
<span data-ttu-id="357d5-123">容器組名。</span><span class="sxs-lookup"><span data-stu-id="357d5-123">The container group name.</span></span>

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

### <span data-ttu-id="357d5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="357d5-124">-PassThru</span></span>
<span data-ttu-id="357d5-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="357d5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="357d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="357d5-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="357d5-127">The resource group name.</span></span>

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

### <span data-ttu-id="357d5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="357d5-128">-ResourceId</span></span>
<span data-ttu-id="357d5-129">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="357d5-129">The resource id.</span></span>

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

### <span data-ttu-id="357d5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="357d5-130">-Confirm</span></span>
<span data-ttu-id="357d5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="357d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357d5-132">-WhatIf</span></span>
<span data-ttu-id="357d5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="357d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="357d5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="357d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357d5-135">CommonParameters</span></span>
<span data-ttu-id="357d5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="357d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357d5-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="357d5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357d5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="357d5-138">INPUTS</span></span>

### <span data-ttu-id="357d5-139">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="357d5-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="357d5-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="357d5-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="357d5-141">System.object</span><span class="sxs-lookup"><span data-stu-id="357d5-141">System.String</span></span>

## <span data-ttu-id="357d5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="357d5-142">OUTPUTS</span></span>

### <span data-ttu-id="357d5-143">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="357d5-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="357d5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="357d5-144">NOTES</span></span>

## <span data-ttu-id="357d5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="357d5-145">RELATED LINKS</span></span>
