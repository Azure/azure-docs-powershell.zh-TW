---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957696"
---
# <span data-ttu-id="ce75d-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce75d-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ce75d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce75d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce75d-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="ce75d-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ce75d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce75d-104">SYNTAX</span></span>

### <span data-ttu-id="ce75d-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="ce75d-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce75d-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ce75d-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce75d-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce75d-107">DESCRIPTION</span></span>

<span data-ttu-id="ce75d-108">**AzResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="ce75d-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ce75d-109">示例</span><span class="sxs-lookup"><span data-stu-id="ce75d-109">EXAMPLES</span></span>

### <span data-ttu-id="ce75d-110">範例1：移除與 ResourceId 的資源群組部署</span><span class="sxs-lookup"><span data-stu-id="ce75d-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="ce75d-111">這個命令會移除具有部署之完全限定資源識別碼的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="ce75d-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ce75d-112">成功的移除會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ce75d-112">Successful removal returns true.</span></span>

### <span data-ttu-id="ce75d-113">範例2：移除含 ResourceGroupName 和資源組的資源群組部署</span><span class="sxs-lookup"><span data-stu-id="ce75d-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="ce75d-114">這個命令會移除具有提供的 ResourceGroupName 和資源組的資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="ce75d-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="ce75d-115">成功的移除會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ce75d-115">Successful removal returns true.</span></span>

## <span data-ttu-id="ce75d-116">參數</span><span class="sxs-lookup"><span data-stu-id="ce75d-116">PARAMETERS</span></span>

### <span data-ttu-id="ce75d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ce75d-117">-ApiVersion</span></span>
<span data-ttu-id="ce75d-118">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ce75d-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ce75d-119">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="ce75d-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce75d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce75d-120">-DefaultProfile</span></span>
<span data-ttu-id="ce75d-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce75d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce75d-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ce75d-122">-Id</span></span>
<span data-ttu-id="ce75d-123">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="ce75d-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="ce75d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce75d-124">-Name</span></span>
<span data-ttu-id="ce75d-125">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce75d-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="ce75d-126">-預先</span><span class="sxs-lookup"><span data-stu-id="ce75d-126">-Pre</span></span>
<span data-ttu-id="ce75d-127">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ce75d-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ce75d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce75d-128">-ResourceGroupName</span></span>
<span data-ttu-id="ce75d-129">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce75d-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="ce75d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ce75d-130">-Confirm</span></span>
<span data-ttu-id="ce75d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce75d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce75d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce75d-132">-WhatIf</span></span>
<span data-ttu-id="ce75d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce75d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce75d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce75d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce75d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce75d-135">CommonParameters</span></span>
<span data-ttu-id="ce75d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce75d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce75d-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce75d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce75d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ce75d-138">INPUTS</span></span>

### <span data-ttu-id="ce75d-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ce75d-139">System.String</span></span>

## <span data-ttu-id="ce75d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ce75d-140">OUTPUTS</span></span>

### <span data-ttu-id="ce75d-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ce75d-141">System.Boolean</span></span>

## <span data-ttu-id="ce75d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ce75d-142">NOTES</span></span>

## <span data-ttu-id="ce75d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce75d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ce75d-144">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce75d-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce75d-145">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce75d-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce75d-146">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce75d-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ce75d-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce75d-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


