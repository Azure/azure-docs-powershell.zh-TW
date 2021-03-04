---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f345b5f03fead63a1f041e364955e68d44dd9f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907513"
---
# <span data-ttu-id="4b033-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b033-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4b033-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b033-102">SYNOPSIS</span></span>
<span data-ttu-id="4b033-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="4b033-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4b033-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b033-104">SYNTAX</span></span>

### <span data-ttu-id="4b033-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="4b033-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b033-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4b033-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b033-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b033-107">DESCRIPTION</span></span>

<span data-ttu-id="4b033-108">**Remove-AzResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="4b033-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4b033-109">例子</span><span class="sxs-lookup"><span data-stu-id="4b033-109">EXAMPLES</span></span>

### <span data-ttu-id="4b033-110">範例 1：使用 ResourceId 移除資源群組部署</span><span class="sxs-lookup"><span data-stu-id="4b033-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="4b033-111">此命令會移除具有部署完整資源識別碼的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="4b033-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4b033-112">成功移除會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4b033-112">Successful removal returns true.</span></span>

### <span data-ttu-id="4b033-113">範例 2：使用 ResourceGroupName 和 ResourceName 移除資源群組部署</span><span class="sxs-lookup"><span data-stu-id="4b033-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="4b033-114">此命令會移除提供 ResourceGroupName 和 ResourceName 的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="4b033-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="4b033-115">成功移除會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4b033-115">Successful removal returns true.</span></span>

## <span data-ttu-id="4b033-116">參數</span><span class="sxs-lookup"><span data-stu-id="4b033-116">PARAMETERS</span></span>

### <span data-ttu-id="4b033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b033-117">-DefaultProfile</span></span>
<span data-ttu-id="4b033-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4b033-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b033-119">-Id</span><span class="sxs-lookup"><span data-stu-id="4b033-119">-Id</span></span>
<span data-ttu-id="4b033-120">指定要移除的資源群組部署識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b033-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b033-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b033-121">-Name</span></span>
<span data-ttu-id="4b033-122">指定要移除的資源組部署名稱。</span><span class="sxs-lookup"><span data-stu-id="4b033-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b033-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b033-123">-Pre</span></span>
<span data-ttu-id="4b033-124">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4b033-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4b033-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b033-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b033-126">指定要移除的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4b033-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b033-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4b033-127">-Confirm</span></span>
<span data-ttu-id="4b033-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b033-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b033-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b033-129">-WhatIf</span></span>
<span data-ttu-id="4b033-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b033-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b033-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b033-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b033-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b033-132">CommonParameters</span></span>
<span data-ttu-id="4b033-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b033-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b033-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b033-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b033-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4b033-135">INPUTS</span></span>

### <span data-ttu-id="4b033-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4b033-136">System.String</span></span>

## <span data-ttu-id="4b033-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4b033-137">OUTPUTS</span></span>

### <span data-ttu-id="4b033-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b033-138">System.Boolean</span></span>

## <span data-ttu-id="4b033-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4b033-139">NOTES</span></span>

## <span data-ttu-id="4b033-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b033-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b033-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b033-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4b033-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b033-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4b033-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b033-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4b033-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b033-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


