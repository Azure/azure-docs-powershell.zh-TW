---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791173"
---
# <span data-ttu-id="4f922-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f922-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4f922-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f922-102">SYNOPSIS</span></span>
<span data-ttu-id="4f922-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="4f922-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4f922-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f922-104">SYNTAX</span></span>

### <span data-ttu-id="4f922-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="4f922-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f922-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4f922-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f922-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f922-107">DESCRIPTION</span></span>
<span data-ttu-id="4f922-108">**AzResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="4f922-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4f922-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f922-109">EXAMPLES</span></span>

## <span data-ttu-id="4f922-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f922-110">PARAMETERS</span></span>

### <span data-ttu-id="4f922-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4f922-111">-ApiVersion</span></span>
<span data-ttu-id="4f922-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4f922-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4f922-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="4f922-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4f922-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f922-114">-DefaultProfile</span></span>
<span data-ttu-id="4f922-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4f922-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f922-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4f922-116">-Id</span></span>
<span data-ttu-id="4f922-117">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="4f922-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4f922-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f922-118">-Name</span></span>
<span data-ttu-id="4f922-119">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f922-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4f922-120">-預先</span><span class="sxs-lookup"><span data-stu-id="4f922-120">-Pre</span></span>
<span data-ttu-id="4f922-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4f922-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4f922-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f922-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f922-123">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f922-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="4f922-124">-確認</span><span class="sxs-lookup"><span data-stu-id="4f922-124">-Confirm</span></span>
<span data-ttu-id="4f922-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f922-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f922-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f922-126">-WhatIf</span></span>
<span data-ttu-id="4f922-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f922-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f922-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f922-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f922-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f922-129">CommonParameters</span></span>
<span data-ttu-id="4f922-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f922-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f922-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f922-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f922-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4f922-132">INPUTS</span></span>

### <span data-ttu-id="4f922-133">System.object</span><span class="sxs-lookup"><span data-stu-id="4f922-133">System.String</span></span>

## <span data-ttu-id="4f922-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4f922-134">OUTPUTS</span></span>

### <span data-ttu-id="4f922-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4f922-135">System.Boolean</span></span>

## <span data-ttu-id="4f922-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4f922-136">NOTES</span></span>

## <span data-ttu-id="4f922-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f922-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f922-138">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f922-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4f922-139">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f922-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4f922-140">停止 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f922-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4f922-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f922-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


