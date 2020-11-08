---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137137"
---
# <span data-ttu-id="28d10-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="28d10-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="28d10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28d10-102">SYNOPSIS</span></span>
<span data-ttu-id="28d10-103">取消資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="28d10-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="28d10-104">句法</span><span class="sxs-lookup"><span data-stu-id="28d10-104">SYNTAX</span></span>

### <span data-ttu-id="28d10-105">StopByResourceGroupDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="28d10-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d10-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="28d10-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d10-107">說明</span><span class="sxs-lookup"><span data-stu-id="28d10-107">DESCRIPTION</span></span>
<span data-ttu-id="28d10-108">**AzResourceGroupDeployment** Cmdlet 會取消已啟動但尚未完成的 Azure 資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="28d10-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="28d10-109">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="28d10-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="28d10-110">Azure 資源是使用者管理的實體，例如網站、資料庫或資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="28d10-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="28d10-111">[資源群組] 是以單位部署的資源集合。</span><span class="sxs-lookup"><span data-stu-id="28d10-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="28d10-112">若要部署資源群組，請使用 New-AzResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28d10-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="28d10-113">New-AzResource Cmdlet 會建立新的資源，但不會觸發此 Cmdlet 可以停止的資源群組部署作業。</span><span class="sxs-lookup"><span data-stu-id="28d10-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="28d10-114">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="28d10-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="28d10-115">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="28d10-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="28d10-116">如果您省略 *Name* 參數，請 **停止 AzResourceGroupDeployment** 搜尋執行中的部署並停止它。</span><span class="sxs-lookup"><span data-stu-id="28d10-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="28d10-117">如果 Cmdlet 發現一個以上的執行部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="28d10-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="28d10-118">示例</span><span class="sxs-lookup"><span data-stu-id="28d10-118">EXAMPLES</span></span>

### <span data-ttu-id="28d10-119">範例1：啟動和停止資源群組部署</span><span class="sxs-lookup"><span data-stu-id="28d10-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="28d10-120">參數</span><span class="sxs-lookup"><span data-stu-id="28d10-120">PARAMETERS</span></span>

### <span data-ttu-id="28d10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d10-121">-DefaultProfile</span></span>
<span data-ttu-id="28d10-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="28d10-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28d10-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="28d10-123">-Id</span></span>
<span data-ttu-id="28d10-124">指定要停止之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="28d10-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d10-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="28d10-125">-Name</span></span>
<span data-ttu-id="28d10-126">指定要停止之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="28d10-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="28d10-127">如果您沒有指定此參數，這個 Cmdlet 會在資源群組中搜尋執行中的部署並停止。</span><span class="sxs-lookup"><span data-stu-id="28d10-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="28d10-128">如果它找到一個以上正在執行的部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="28d10-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="28d10-129">若要取得部署名稱，請使用 Get-AzResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28d10-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d10-130">-預先</span><span class="sxs-lookup"><span data-stu-id="28d10-130">-Pre</span></span>
<span data-ttu-id="28d10-131">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="28d10-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="28d10-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d10-132">-ResourceGroupName</span></span>
<span data-ttu-id="28d10-133">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28d10-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="28d10-134">這個 Cmdlet 會停止此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="28d10-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d10-135">-確認</span><span class="sxs-lookup"><span data-stu-id="28d10-135">-Confirm</span></span>
<span data-ttu-id="28d10-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28d10-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d10-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d10-137">-WhatIf</span></span>
<span data-ttu-id="28d10-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28d10-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d10-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28d10-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d10-140">CommonParameters</span></span>
<span data-ttu-id="28d10-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28d10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d10-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="28d10-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d10-143">輸入</span><span class="sxs-lookup"><span data-stu-id="28d10-143">INPUTS</span></span>

### <span data-ttu-id="28d10-144">System.object</span><span class="sxs-lookup"><span data-stu-id="28d10-144">System.String</span></span>

## <span data-ttu-id="28d10-145">輸出</span><span class="sxs-lookup"><span data-stu-id="28d10-145">OUTPUTS</span></span>

### <span data-ttu-id="28d10-146">System.object</span><span class="sxs-lookup"><span data-stu-id="28d10-146">System.Boolean</span></span>

## <span data-ttu-id="28d10-147">筆記</span><span class="sxs-lookup"><span data-stu-id="28d10-147">NOTES</span></span>

## <span data-ttu-id="28d10-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="28d10-148">RELATED LINKS</span></span>

[<span data-ttu-id="28d10-149">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="28d10-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="28d10-150">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="28d10-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="28d10-151">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28d10-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="28d10-152">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="28d10-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="28d10-153">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="28d10-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="28d10-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="28d10-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

