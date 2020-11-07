---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802189"
---
# <span data-ttu-id="b33f0-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b33f0-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b33f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b33f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b33f0-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="b33f0-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b33f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b33f0-104">SYNTAX</span></span>

### <span data-ttu-id="b33f0-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="b33f0-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b33f0-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b33f0-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b33f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="b33f0-107">DESCRIPTION</span></span>
<span data-ttu-id="b33f0-108">**AzureRmResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="b33f0-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="b33f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="b33f0-109">EXAMPLES</span></span>

## <span data-ttu-id="b33f0-110">參數</span><span class="sxs-lookup"><span data-stu-id="b33f0-110">PARAMETERS</span></span>

### <span data-ttu-id="b33f0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b33f0-111">-ApiVersion</span></span>
<span data-ttu-id="b33f0-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b33f0-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b33f0-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="b33f0-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b33f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33f0-114">-DefaultProfile</span></span>
<span data-ttu-id="b33f0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b33f0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b33f0-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b33f0-116">-Id</span></span>
<span data-ttu-id="b33f0-117">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="b33f0-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="b33f0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b33f0-118">-Name</span></span>
<span data-ttu-id="b33f0-119">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b33f0-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="b33f0-120">-預先</span><span class="sxs-lookup"><span data-stu-id="b33f0-120">-Pre</span></span>
<span data-ttu-id="b33f0-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b33f0-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b33f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="b33f0-123">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b33f0-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="b33f0-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b33f0-124">-Confirm</span></span>
<span data-ttu-id="b33f0-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b33f0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33f0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33f0-126">-WhatIf</span></span>
<span data-ttu-id="b33f0-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b33f0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33f0-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b33f0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33f0-129">CommonParameters</span></span>
<span data-ttu-id="b33f0-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b33f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33f0-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b33f0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33f0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b33f0-132">INPUTS</span></span>

### <span data-ttu-id="b33f0-133">所有</span><span class="sxs-lookup"><span data-stu-id="b33f0-133">None</span></span>

## <span data-ttu-id="b33f0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b33f0-134">OUTPUTS</span></span>

## <span data-ttu-id="b33f0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b33f0-135">NOTES</span></span>

## <span data-ttu-id="b33f0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b33f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="b33f0-137">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b33f0-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b33f0-138">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b33f0-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b33f0-139">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b33f0-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b33f0-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b33f0-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


