---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452364"
---
# <span data-ttu-id="cdc37-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cdc37-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="cdc37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdc37-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc37-103">移除資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="cdc37-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc37-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdc37-104">SYNTAX</span></span>

### <span data-ttu-id="cdc37-105">已設定部署名稱參數。</span><span class="sxs-lookup"><span data-stu-id="cdc37-105">The deployment name parameter set.</span></span> <span data-ttu-id="cdc37-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="cdc37-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdc37-107">已設定部署識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="cdc37-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc37-108">說明</span><span class="sxs-lookup"><span data-stu-id="cdc37-108">DESCRIPTION</span></span>
<span data-ttu-id="cdc37-109">**AzureRmResourceGroupDeployment** Cmdlet 會移除 Azure 資源群組部署及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="cdc37-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="cdc37-110">示例</span><span class="sxs-lookup"><span data-stu-id="cdc37-110">EXAMPLES</span></span>

## <span data-ttu-id="cdc37-111">參數</span><span class="sxs-lookup"><span data-stu-id="cdc37-111">PARAMETERS</span></span>

### <span data-ttu-id="cdc37-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cdc37-112">-ApiVersion</span></span>
<span data-ttu-id="cdc37-113">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cdc37-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cdc37-114">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="cdc37-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cdc37-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="cdc37-115">-Id</span></span>
<span data-ttu-id="cdc37-116">指定要移除之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="cdc37-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc37-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdc37-117">-Name</span></span>
<span data-ttu-id="cdc37-118">指定要移除之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdc37-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc37-119">-預先</span><span class="sxs-lookup"><span data-stu-id="cdc37-119">-Pre</span></span>
<span data-ttu-id="cdc37-120">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cdc37-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cdc37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc37-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdc37-122">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdc37-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc37-123">-確認</span><span class="sxs-lookup"><span data-stu-id="cdc37-123">-Confirm</span></span>
<span data-ttu-id="cdc37-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cdc37-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc37-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc37-125">-WhatIf</span></span>
<span data-ttu-id="cdc37-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdc37-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc37-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdc37-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc37-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc37-128">-DefaultProfile</span></span>
<span data-ttu-id="cdc37-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdc37-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc37-130">CommonParameters</span></span>
<span data-ttu-id="cdc37-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdc37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc37-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdc37-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc37-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cdc37-133">INPUTS</span></span>

## <span data-ttu-id="cdc37-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cdc37-134">OUTPUTS</span></span>

### <span data-ttu-id="cdc37-135">System.object</span><span class="sxs-lookup"><span data-stu-id="cdc37-135">System.Boolean</span></span>

## <span data-ttu-id="cdc37-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cdc37-136">NOTES</span></span>

## <span data-ttu-id="cdc37-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdc37-137">RELATED LINKS</span></span>

[<span data-ttu-id="cdc37-138">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cdc37-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="cdc37-139">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cdc37-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="cdc37-140">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cdc37-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="cdc37-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cdc37-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


