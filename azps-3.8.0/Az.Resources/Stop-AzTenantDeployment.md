---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957651"
---
# <span data-ttu-id="71d9a-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="71d9a-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="71d9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="71d9a-103">在租使用者範圍取消正在執行的部署</span><span class="sxs-lookup"><span data-stu-id="71d9a-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="71d9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="71d9a-104">SYNTAX</span></span>

### <span data-ttu-id="71d9a-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="71d9a-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d9a-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="71d9a-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d9a-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="71d9a-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d9a-108">說明</span><span class="sxs-lookup"><span data-stu-id="71d9a-108">DESCRIPTION</span></span>
<span data-ttu-id="71d9a-109">**AzTenantDeployment** Cmdlet 會取消已啟動但未在目前租使用者範圍內完成的部署。</span><span class="sxs-lookup"><span data-stu-id="71d9a-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="71d9a-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="71d9a-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="71d9a-111">若要在租使用者範圍中建立部署，請使用 New-AzTenantDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71d9a-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="71d9a-112">示例</span><span class="sxs-lookup"><span data-stu-id="71d9a-112">EXAMPLES</span></span>

### <span data-ttu-id="71d9a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="71d9a-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="71d9a-114">這個命令會在目前的租使用者範圍中取消正在執行的部署 "deployment01"。</span><span class="sxs-lookup"><span data-stu-id="71d9a-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="71d9a-115">範例2</span><span class="sxs-lookup"><span data-stu-id="71d9a-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="71d9a-116">這個命令會在目前的租使用者範圍中取得部署 "deployment01"，並將它取消。</span><span class="sxs-lookup"><span data-stu-id="71d9a-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="71d9a-117">參數</span><span class="sxs-lookup"><span data-stu-id="71d9a-117">PARAMETERS</span></span>

### <span data-ttu-id="71d9a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71d9a-118">-ApiVersion</span></span>
<span data-ttu-id="71d9a-119">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="71d9a-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="71d9a-120">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="71d9a-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="71d9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d9a-121">-DefaultProfile</span></span>
<span data-ttu-id="71d9a-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71d9a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9a-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="71d9a-123">-Id</span></span>
<span data-ttu-id="71d9a-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="71d9a-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="71d9a-125">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="71d9a-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71d9a-126">-InputObject</span></span>
<span data-ttu-id="71d9a-127">部署物件。</span><span class="sxs-lookup"><span data-stu-id="71d9a-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71d9a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="71d9a-128">-Name</span></span>
<span data-ttu-id="71d9a-129">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="71d9a-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71d9a-130">-PassThru</span></span>
<span data-ttu-id="71d9a-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="71d9a-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="71d9a-132">-預先</span><span class="sxs-lookup"><span data-stu-id="71d9a-132">-Pre</span></span>
<span data-ttu-id="71d9a-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="71d9a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="71d9a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="71d9a-134">-Confirm</span></span>
<span data-ttu-id="71d9a-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71d9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d9a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d9a-136">-WhatIf</span></span>
<span data-ttu-id="71d9a-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71d9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d9a-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71d9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d9a-139">CommonParameters</span></span>
<span data-ttu-id="71d9a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71d9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d9a-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71d9a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d9a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="71d9a-142">INPUTS</span></span>

### <span data-ttu-id="71d9a-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="71d9a-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="71d9a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="71d9a-144">OUTPUTS</span></span>

### <span data-ttu-id="71d9a-145">System.object</span><span class="sxs-lookup"><span data-stu-id="71d9a-145">System.Boolean</span></span>

## <span data-ttu-id="71d9a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="71d9a-146">NOTES</span></span>

## <span data-ttu-id="71d9a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="71d9a-147">RELATED LINKS</span></span>
