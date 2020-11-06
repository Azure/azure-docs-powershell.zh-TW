---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454104"
---
# <span data-ttu-id="e4d74-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d74-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e4d74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4d74-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d74-103">取消資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="e4d74-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4d74-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4d74-104">SYNTAX</span></span>

### <span data-ttu-id="e4d74-105">StopByResourceGroupDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="e4d74-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d74-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e4d74-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d74-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4d74-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d74-108">**AzureRmResourceGroupDeployment** Cmdlet 會取消已啟動但尚未完成的 Azure 資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="e4d74-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="e4d74-109">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="e4d74-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="e4d74-110">Azure 資源是使用者管理的實體，例如網站、資料庫或資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="e4d74-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="e4d74-111">[資源群組] 是以單位部署的資源集合。</span><span class="sxs-lookup"><span data-stu-id="e4d74-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="e4d74-112">若要部署資源群組，請使用 New-AzureRmResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4d74-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="e4d74-113">New-AzureRmResource Cmdlet 會建立新的資源，但不會觸發此 Cmdlet 可以停止的資源群組部署作業。</span><span class="sxs-lookup"><span data-stu-id="e4d74-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="e4d74-114">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="e4d74-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="e4d74-115">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="e4d74-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="e4d74-116">如果您省略 *Name* 參數，請 **停止 AzureRmResourceGroupDeployment** 搜尋執行中的部署並停止它。</span><span class="sxs-lookup"><span data-stu-id="e4d74-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="e4d74-117">如果 Cmdlet 發現一個以上的執行部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="e4d74-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="e4d74-118">示例</span><span class="sxs-lookup"><span data-stu-id="e4d74-118">EXAMPLES</span></span>

## <span data-ttu-id="e4d74-119">參數</span><span class="sxs-lookup"><span data-stu-id="e4d74-119">PARAMETERS</span></span>

### <span data-ttu-id="e4d74-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4d74-120">-ApiVersion</span></span>
<span data-ttu-id="e4d74-121">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e4d74-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e4d74-122">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="e4d74-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e4d74-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d74-123">-DefaultProfile</span></span>
<span data-ttu-id="e4d74-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e4d74-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4d74-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e4d74-125">-Id</span></span>
<span data-ttu-id="e4d74-126">指定要停止之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d74-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4d74-127">-Name</span></span>
<span data-ttu-id="e4d74-128">指定要停止之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d74-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="e4d74-129">如果您沒有指定此參數，這個 Cmdlet 會在資源群組中搜尋執行中的部署並停止。</span><span class="sxs-lookup"><span data-stu-id="e4d74-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="e4d74-130">如果它找到一個以上正在執行的部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="e4d74-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="e4d74-131">若要取得部署名稱，請使用 Get-AzureRmResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4d74-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d74-132">-預先</span><span class="sxs-lookup"><span data-stu-id="e4d74-132">-Pre</span></span>
<span data-ttu-id="e4d74-133">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e4d74-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4d74-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d74-134">-ResourceGroupName</span></span>
<span data-ttu-id="e4d74-135">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d74-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e4d74-136">這個 Cmdlet 會停止此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="e4d74-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d74-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e4d74-137">-Confirm</span></span>
<span data-ttu-id="e4d74-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4d74-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d74-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d74-139">-WhatIf</span></span>
<span data-ttu-id="e4d74-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4d74-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d74-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4d74-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d74-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d74-142">CommonParameters</span></span>
<span data-ttu-id="e4d74-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4d74-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d74-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4d74-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d74-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e4d74-145">INPUTS</span></span>

### <span data-ttu-id="e4d74-146">所有</span><span class="sxs-lookup"><span data-stu-id="e4d74-146">None</span></span>

## <span data-ttu-id="e4d74-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e4d74-147">OUTPUTS</span></span>

### <span data-ttu-id="e4d74-148">布林值</span><span class="sxs-lookup"><span data-stu-id="e4d74-148">Boolean</span></span>

## <span data-ttu-id="e4d74-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e4d74-149">NOTES</span></span>

## <span data-ttu-id="e4d74-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4d74-150">RELATED LINKS</span></span>

[<span data-ttu-id="e4d74-151">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d74-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e4d74-152">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e4d74-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e4d74-153">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4d74-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e4d74-154">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d74-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e4d74-155">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d74-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e4d74-156">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e4d74-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


