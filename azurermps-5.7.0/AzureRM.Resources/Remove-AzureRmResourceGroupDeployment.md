---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450500"
---
# <span data-ttu-id="b3102-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3102-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b3102-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3102-102">SYNOPSIS</span></span>
<span data-ttu-id="b3102-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="b3102-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3102-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3102-104">SYNTAX</span></span>

### <span data-ttu-id="b3102-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="b3102-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3102-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b3102-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3102-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3102-107">DESCRIPTION</span></span>
<span data-ttu-id="b3102-108">**AzureRmResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="b3102-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="b3102-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3102-109">EXAMPLES</span></span>

## <span data-ttu-id="b3102-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3102-110">PARAMETERS</span></span>

### <span data-ttu-id="b3102-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3102-111">-ApiVersion</span></span>
<span data-ttu-id="b3102-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b3102-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b3102-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="b3102-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3102-114">-DefaultProfile</span></span>
<span data-ttu-id="b3102-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b3102-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b3102-116">-Id</span></span>
<span data-ttu-id="b3102-117">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="b3102-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3102-118">-Name</span></span>
<span data-ttu-id="b3102-119">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3102-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-120">-預先</span><span class="sxs-lookup"><span data-stu-id="b3102-120">-Pre</span></span>
<span data-ttu-id="b3102-121">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b3102-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3102-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3102-123">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3102-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b3102-124">-Confirm</span></span>
<span data-ttu-id="b3102-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3102-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3102-126">-WhatIf</span></span>
<span data-ttu-id="b3102-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3102-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3102-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3102-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3102-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3102-129">CommonParameters</span></span>
<span data-ttu-id="b3102-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3102-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3102-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3102-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3102-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b3102-132">INPUTS</span></span>

### <span data-ttu-id="b3102-133">所有</span><span class="sxs-lookup"><span data-stu-id="b3102-133">None</span></span>
<span data-ttu-id="b3102-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b3102-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3102-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b3102-135">OUTPUTS</span></span>

### <span data-ttu-id="b3102-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b3102-136">System.Boolean</span></span>

## <span data-ttu-id="b3102-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b3102-137">NOTES</span></span>

## <span data-ttu-id="b3102-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3102-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3102-139">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3102-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3102-140">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3102-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3102-141">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3102-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3102-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3102-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


