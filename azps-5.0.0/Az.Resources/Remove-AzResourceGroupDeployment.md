---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141275"
---
# <span data-ttu-id="10ae3-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10ae3-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="10ae3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="10ae3-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="10ae3-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="10ae3-104">句法</span><span class="sxs-lookup"><span data-stu-id="10ae3-104">SYNTAX</span></span>

### <span data-ttu-id="10ae3-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="10ae3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ae3-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="10ae3-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ae3-107">說明</span><span class="sxs-lookup"><span data-stu-id="10ae3-107">DESCRIPTION</span></span>

<span data-ttu-id="10ae3-108">**AzResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="10ae3-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="10ae3-109">示例</span><span class="sxs-lookup"><span data-stu-id="10ae3-109">EXAMPLES</span></span>

### <span data-ttu-id="10ae3-110">範例1：移除與 ResourceId 的資源群組部署</span><span class="sxs-lookup"><span data-stu-id="10ae3-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="10ae3-111">這個命令會移除具有部署之完全限定資源識別碼的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="10ae3-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="10ae3-112">成功的移除會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="10ae3-112">Successful removal returns true.</span></span>

### <span data-ttu-id="10ae3-113">範例2：移除含 ResourceGroupName 和資源組的資源群組部署</span><span class="sxs-lookup"><span data-stu-id="10ae3-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="10ae3-114">這個命令會移除具有提供的 ResourceGroupName 和資源組的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="10ae3-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="10ae3-115">成功的移除會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="10ae3-115">Successful removal returns true.</span></span>

## <span data-ttu-id="10ae3-116">參數</span><span class="sxs-lookup"><span data-stu-id="10ae3-116">PARAMETERS</span></span>

### <span data-ttu-id="10ae3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ae3-117">-DefaultProfile</span></span>
<span data-ttu-id="10ae3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="10ae3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10ae3-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="10ae3-119">-Id</span></span>
<span data-ttu-id="10ae3-120">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="10ae3-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="10ae3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="10ae3-121">-Name</span></span>
<span data-ttu-id="10ae3-122">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="10ae3-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="10ae3-123">-預先</span><span class="sxs-lookup"><span data-stu-id="10ae3-123">-Pre</span></span>
<span data-ttu-id="10ae3-124">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="10ae3-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="10ae3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ae3-125">-ResourceGroupName</span></span>
<span data-ttu-id="10ae3-126">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10ae3-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="10ae3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="10ae3-127">-Confirm</span></span>
<span data-ttu-id="10ae3-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10ae3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ae3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ae3-129">-WhatIf</span></span>
<span data-ttu-id="10ae3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10ae3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ae3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10ae3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ae3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ae3-132">CommonParameters</span></span>
<span data-ttu-id="10ae3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10ae3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ae3-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10ae3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ae3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="10ae3-135">INPUTS</span></span>

### <span data-ttu-id="10ae3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="10ae3-136">System.String</span></span>

## <span data-ttu-id="10ae3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="10ae3-137">OUTPUTS</span></span>

### <span data-ttu-id="10ae3-138">System.object</span><span class="sxs-lookup"><span data-stu-id="10ae3-138">System.Boolean</span></span>

## <span data-ttu-id="10ae3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="10ae3-139">NOTES</span></span>

## <span data-ttu-id="10ae3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="10ae3-140">RELATED LINKS</span></span>

[<span data-ttu-id="10ae3-141">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10ae3-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="10ae3-142">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10ae3-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="10ae3-143">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10ae3-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="10ae3-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10ae3-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

