---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626223"
---
# <span data-ttu-id="45666-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45666-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="45666-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45666-102">SYNOPSIS</span></span>
<span data-ttu-id="45666-103">取消資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="45666-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45666-104">句法</span><span class="sxs-lookup"><span data-stu-id="45666-104">SYNTAX</span></span>

### <span data-ttu-id="45666-105">已設定部署名稱參數。</span><span class="sxs-lookup"><span data-stu-id="45666-105">The deployment name parameter set.</span></span> <span data-ttu-id="45666-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="45666-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45666-107">已設定部署識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="45666-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45666-108">說明</span><span class="sxs-lookup"><span data-stu-id="45666-108">DESCRIPTION</span></span>
<span data-ttu-id="45666-109">**AzureRmResourceGroupDeployment** Cmdlet 會取消已啟動但尚未完成的 Azure 資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="45666-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="45666-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="45666-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="45666-111">Azure 資源是使用者管理的實體，例如網站、資料庫或資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="45666-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="45666-112">[資源群組] 是以單位部署的資源集合。</span><span class="sxs-lookup"><span data-stu-id="45666-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="45666-113">若要部署資源群組，請使用 New-AzureRmResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45666-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="45666-114">New-AzureRmResource Cmdlet 會建立新的資源，但不會觸發此 Cmdlet 可以停止的資源群組部署作業。</span><span class="sxs-lookup"><span data-stu-id="45666-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="45666-115">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="45666-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="45666-116">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="45666-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="45666-117">如果您省略 *Name* 參數，請 **停止 AzureRmResourceGroupDeployment** 搜尋執行中的部署並停止它。</span><span class="sxs-lookup"><span data-stu-id="45666-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="45666-118">如果 Cmdlet 發現一個以上的執行部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="45666-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="45666-119">示例</span><span class="sxs-lookup"><span data-stu-id="45666-119">EXAMPLES</span></span>

## <span data-ttu-id="45666-120">參數</span><span class="sxs-lookup"><span data-stu-id="45666-120">PARAMETERS</span></span>

### <span data-ttu-id="45666-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="45666-121">-ApiVersion</span></span>
<span data-ttu-id="45666-122">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="45666-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="45666-123">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="45666-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="45666-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="45666-124">-Id</span></span>
<span data-ttu-id="45666-125">指定要停止之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="45666-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="45666-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="45666-126">-Name</span></span>
<span data-ttu-id="45666-127">指定要停止之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="45666-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="45666-128">如果您沒有指定此參數，這個 Cmdlet 會在資源群組中搜尋執行中的部署並停止。</span><span class="sxs-lookup"><span data-stu-id="45666-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="45666-129">如果它找到一個以上正在執行的部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="45666-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="45666-130">若要取得部署名稱，請使用 Get-AzureRmResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45666-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45666-131">-預先</span><span class="sxs-lookup"><span data-stu-id="45666-131">-Pre</span></span>
<span data-ttu-id="45666-132">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="45666-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="45666-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45666-133">-ResourceGroupName</span></span>
<span data-ttu-id="45666-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45666-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="45666-135">這個 Cmdlet 會停止此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="45666-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45666-136">-確認</span><span class="sxs-lookup"><span data-stu-id="45666-136">-Confirm</span></span>
<span data-ttu-id="45666-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45666-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45666-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45666-138">-WhatIf</span></span>
<span data-ttu-id="45666-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45666-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45666-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45666-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45666-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45666-141">-DefaultProfile</span></span>
<span data-ttu-id="45666-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45666-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45666-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45666-143">CommonParameters</span></span>
<span data-ttu-id="45666-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45666-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45666-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45666-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45666-146">輸入</span><span class="sxs-lookup"><span data-stu-id="45666-146">INPUTS</span></span>

### <span data-ttu-id="45666-147">所有</span><span class="sxs-lookup"><span data-stu-id="45666-147">None</span></span>

## <span data-ttu-id="45666-148">輸出</span><span class="sxs-lookup"><span data-stu-id="45666-148">OUTPUTS</span></span>

### <span data-ttu-id="45666-149">布林值</span><span class="sxs-lookup"><span data-stu-id="45666-149">Boolean</span></span>

## <span data-ttu-id="45666-150">筆記</span><span class="sxs-lookup"><span data-stu-id="45666-150">NOTES</span></span>

## <span data-ttu-id="45666-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="45666-151">RELATED LINKS</span></span>

[<span data-ttu-id="45666-152">AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45666-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45666-153">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="45666-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="45666-154">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45666-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="45666-155">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45666-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45666-156">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45666-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45666-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45666-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


