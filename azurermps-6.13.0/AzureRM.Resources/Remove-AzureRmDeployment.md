---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
ms.openlocfilehash: a008ecf8b8c6681941e19b4db63f79c85fab8ba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448250"
---
# <span data-ttu-id="2eb46-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2eb46-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="2eb46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2eb46-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb46-103">移除部署及任何相關聯的作業</span><span class="sxs-lookup"><span data-stu-id="2eb46-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb46-104">句法</span><span class="sxs-lookup"><span data-stu-id="2eb46-104">SYNTAX</span></span>

### <span data-ttu-id="2eb46-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="2eb46-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb46-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2eb46-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb46-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2eb46-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb46-108">說明</span><span class="sxs-lookup"><span data-stu-id="2eb46-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb46-109">**AzureRmDeployment** Cmdlet 會移除訂閱作用中的 Azure 部署以及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="2eb46-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="2eb46-110">示例</span><span class="sxs-lookup"><span data-stu-id="2eb46-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb46-111">範例1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="2eb46-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="2eb46-112">這個命令會在目前的訂閱範圍中移除部署 "RolesDeployment"。</span><span class="sxs-lookup"><span data-stu-id="2eb46-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="2eb46-113">範例2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="2eb46-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="2eb46-114">這個命令會在目前的訂閱範圍中取得部署 "RolesDeployment"，並將它移除。</span><span class="sxs-lookup"><span data-stu-id="2eb46-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="2eb46-115">參數</span><span class="sxs-lookup"><span data-stu-id="2eb46-115">PARAMETERS</span></span>

### <span data-ttu-id="2eb46-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2eb46-116">-ApiVersion</span></span>
<span data-ttu-id="2eb46-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2eb46-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2eb46-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="2eb46-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2eb46-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb46-119">-AsJob</span></span>
<span data-ttu-id="2eb46-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2eb46-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2eb46-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb46-121">-DefaultProfile</span></span>
<span data-ttu-id="2eb46-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2eb46-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb46-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2eb46-123">-Id</span></span>
<span data-ttu-id="2eb46-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eb46-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2eb46-125">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2eb46-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb46-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb46-126">-InputObject</span></span>
<span data-ttu-id="2eb46-127">部署物件。</span><span class="sxs-lookup"><span data-stu-id="2eb46-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb46-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2eb46-128">-Name</span></span>
<span data-ttu-id="2eb46-129">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="2eb46-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb46-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eb46-130">-PassThru</span></span>
<span data-ttu-id="2eb46-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="2eb46-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2eb46-132">-預先</span><span class="sxs-lookup"><span data-stu-id="2eb46-132">-Pre</span></span>
<span data-ttu-id="2eb46-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="2eb46-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2eb46-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2eb46-134">-Confirm</span></span>
<span data-ttu-id="2eb46-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2eb46-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb46-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb46-136">-WhatIf</span></span>
<span data-ttu-id="2eb46-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2eb46-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb46-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2eb46-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb46-139">CommonParameters</span></span>
<span data-ttu-id="2eb46-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2eb46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb46-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2eb46-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb46-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2eb46-142">INPUTS</span></span>

### <span data-ttu-id="2eb46-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2eb46-143">System.String</span></span>

## <span data-ttu-id="2eb46-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2eb46-144">OUTPUTS</span></span>

### <span data-ttu-id="2eb46-145">System.object</span><span class="sxs-lookup"><span data-stu-id="2eb46-145">System.Boolean</span></span>

## <span data-ttu-id="2eb46-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2eb46-146">NOTES</span></span>

## <span data-ttu-id="2eb46-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2eb46-147">RELATED LINKS</span></span>
