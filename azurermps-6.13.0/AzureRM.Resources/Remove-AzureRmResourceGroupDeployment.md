---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 19662972e115acb0e3a194e14abf3f956d39035e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448244"
---
# <span data-ttu-id="99a02-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99a02-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="99a02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99a02-102">SYNOPSIS</span></span>
<span data-ttu-id="99a02-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="99a02-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99a02-104">句法</span><span class="sxs-lookup"><span data-stu-id="99a02-104">SYNTAX</span></span>

### <span data-ttu-id="99a02-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="99a02-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99a02-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="99a02-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99a02-107">說明</span><span class="sxs-lookup"><span data-stu-id="99a02-107">DESCRIPTION</span></span>
<span data-ttu-id="99a02-108">**AzureRmResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="99a02-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="99a02-109">示例</span><span class="sxs-lookup"><span data-stu-id="99a02-109">EXAMPLES</span></span>

## <span data-ttu-id="99a02-110">參數</span><span class="sxs-lookup"><span data-stu-id="99a02-110">PARAMETERS</span></span>

### <span data-ttu-id="99a02-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99a02-111">-ApiVersion</span></span>
<span data-ttu-id="99a02-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="99a02-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="99a02-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="99a02-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="99a02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a02-114">-DefaultProfile</span></span>
<span data-ttu-id="99a02-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="99a02-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99a02-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="99a02-116">-Id</span></span>
<span data-ttu-id="99a02-117">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="99a02-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="99a02-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="99a02-118">-Name</span></span>
<span data-ttu-id="99a02-119">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a02-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a02-120">-預先</span><span class="sxs-lookup"><span data-stu-id="99a02-120">-Pre</span></span>
<span data-ttu-id="99a02-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="99a02-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="99a02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a02-122">-ResourceGroupName</span></span>
<span data-ttu-id="99a02-123">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a02-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a02-124">-確認</span><span class="sxs-lookup"><span data-stu-id="99a02-124">-Confirm</span></span>
<span data-ttu-id="99a02-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99a02-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a02-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a02-126">-WhatIf</span></span>
<span data-ttu-id="99a02-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99a02-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a02-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99a02-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a02-129">CommonParameters</span></span>
<span data-ttu-id="99a02-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99a02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a02-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99a02-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a02-132">輸入</span><span class="sxs-lookup"><span data-stu-id="99a02-132">INPUTS</span></span>

### <span data-ttu-id="99a02-133">所有</span><span class="sxs-lookup"><span data-stu-id="99a02-133">None</span></span>

## <span data-ttu-id="99a02-134">輸出</span><span class="sxs-lookup"><span data-stu-id="99a02-134">OUTPUTS</span></span>

## <span data-ttu-id="99a02-135">筆記</span><span class="sxs-lookup"><span data-stu-id="99a02-135">NOTES</span></span>

## <span data-ttu-id="99a02-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="99a02-136">RELATED LINKS</span></span>

[<span data-ttu-id="99a02-137">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99a02-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="99a02-138">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99a02-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="99a02-139">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99a02-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="99a02-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="99a02-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


