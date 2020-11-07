---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 49ea711740eff624a9560b6d70239edb476dc989
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800677"
---
# <span data-ttu-id="364bf-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="364bf-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="364bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="364bf-102">SYNOPSIS</span></span>
<span data-ttu-id="364bf-103">Cancal 正在執行的部署</span><span class="sxs-lookup"><span data-stu-id="364bf-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="364bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="364bf-104">SYNTAX</span></span>

### <span data-ttu-id="364bf-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="364bf-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="364bf-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="364bf-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="364bf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="364bf-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="364bf-108">說明</span><span class="sxs-lookup"><span data-stu-id="364bf-108">DESCRIPTION</span></span>
<span data-ttu-id="364bf-109">**AzureRmDeployment** Cmdlet 會在已開始但尚未完成的訂閱範圍中取消部署。</span><span class="sxs-lookup"><span data-stu-id="364bf-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="364bf-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="364bf-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="364bf-111">若要在訂閱範圍建立部署，請使用 New-AzureRmDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="364bf-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="364bf-112">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="364bf-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="364bf-113">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="364bf-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="364bf-114">示例</span><span class="sxs-lookup"><span data-stu-id="364bf-114">EXAMPLES</span></span>

### <span data-ttu-id="364bf-115">範例1</span><span class="sxs-lookup"><span data-stu-id="364bf-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="364bf-116">這個命令會在目前的訂閱範圍中取消正在執行的部署 "deployment01"。</span><span class="sxs-lookup"><span data-stu-id="364bf-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="364bf-117">範例2</span><span class="sxs-lookup"><span data-stu-id="364bf-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="364bf-118">這個命令會在目前的訂閱範圍中取得部署 "deployment01"，並加以取消。</span><span class="sxs-lookup"><span data-stu-id="364bf-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="364bf-119">參數</span><span class="sxs-lookup"><span data-stu-id="364bf-119">PARAMETERS</span></span>

### <span data-ttu-id="364bf-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="364bf-120">-ApiVersion</span></span>
<span data-ttu-id="364bf-121">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="364bf-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="364bf-122">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="364bf-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="364bf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364bf-123">-DefaultProfile</span></span>
<span data-ttu-id="364bf-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="364bf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364bf-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="364bf-125">-Id</span></span>
<span data-ttu-id="364bf-126">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="364bf-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="364bf-127">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="364bf-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="364bf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="364bf-128">-InputObject</span></span>
<span data-ttu-id="364bf-129">部署物件。</span><span class="sxs-lookup"><span data-stu-id="364bf-129">The deployment object.</span></span>

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

### <span data-ttu-id="364bf-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="364bf-130">-Name</span></span>
<span data-ttu-id="364bf-131">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="364bf-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="364bf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="364bf-132">-PassThru</span></span>
<span data-ttu-id="364bf-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="364bf-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="364bf-134">-預先</span><span class="sxs-lookup"><span data-stu-id="364bf-134">-Pre</span></span>
<span data-ttu-id="364bf-135">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="364bf-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="364bf-136">-確認</span><span class="sxs-lookup"><span data-stu-id="364bf-136">-Confirm</span></span>
<span data-ttu-id="364bf-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="364bf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364bf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364bf-138">-WhatIf</span></span>
<span data-ttu-id="364bf-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="364bf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="364bf-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="364bf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364bf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364bf-141">CommonParameters</span></span>
<span data-ttu-id="364bf-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="364bf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364bf-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="364bf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364bf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="364bf-144">INPUTS</span></span>

### <span data-ttu-id="364bf-145">System.object</span><span class="sxs-lookup"><span data-stu-id="364bf-145">System.String</span></span>

## <span data-ttu-id="364bf-146">輸出</span><span class="sxs-lookup"><span data-stu-id="364bf-146">OUTPUTS</span></span>

### <span data-ttu-id="364bf-147">System.object</span><span class="sxs-lookup"><span data-stu-id="364bf-147">System.Boolean</span></span>

## <span data-ttu-id="364bf-148">筆記</span><span class="sxs-lookup"><span data-stu-id="364bf-148">NOTES</span></span>

## <span data-ttu-id="364bf-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="364bf-149">RELATED LINKS</span></span>
