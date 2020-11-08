---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 01f2aa36a063caec233aa8c1600d4a01727a549b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127345"
---
# <span data-ttu-id="38350-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38350-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="38350-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38350-102">SYNOPSIS</span></span>
<span data-ttu-id="38350-103">取消資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="38350-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="38350-104">句法</span><span class="sxs-lookup"><span data-stu-id="38350-104">SYNTAX</span></span>

### <span data-ttu-id="38350-105">StopByResourceGroupDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="38350-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38350-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="38350-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38350-107">說明</span><span class="sxs-lookup"><span data-stu-id="38350-107">DESCRIPTION</span></span>
<span data-ttu-id="38350-108">**AzResourceGroupDeployment** Cmdlet 會取消已啟動但尚未完成的 Azure 資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="38350-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="38350-109">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="38350-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="38350-110">Azure 資源是使用者管理的實體，例如網站、資料庫或資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="38350-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="38350-111">[資源群組] 是以單位部署的資源集合。</span><span class="sxs-lookup"><span data-stu-id="38350-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="38350-112">若要部署資源群組，請使用 New-AzResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38350-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="38350-113">New-AzResource Cmdlet 會建立新的資源，但不會觸發此 Cmdlet 可以停止的資源群組部署作業。</span><span class="sxs-lookup"><span data-stu-id="38350-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="38350-114">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="38350-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="38350-115">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="38350-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="38350-116">如果您省略 *Name* 參數，請 **停止 AzResourceGroupDeployment** 搜尋執行中的部署並停止它。</span><span class="sxs-lookup"><span data-stu-id="38350-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="38350-117">如果 Cmdlet 發現一個以上的執行部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="38350-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="38350-118">示例</span><span class="sxs-lookup"><span data-stu-id="38350-118">EXAMPLES</span></span>

### <span data-ttu-id="38350-119">範例1：啟動和停止資源群組部署</span><span class="sxs-lookup"><span data-stu-id="38350-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="38350-120">參數</span><span class="sxs-lookup"><span data-stu-id="38350-120">PARAMETERS</span></span>

### <span data-ttu-id="38350-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38350-121">-ApiVersion</span></span>
<span data-ttu-id="38350-122">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="38350-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="38350-123">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="38350-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="38350-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38350-124">-DefaultProfile</span></span>
<span data-ttu-id="38350-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="38350-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38350-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="38350-126">-Id</span></span>
<span data-ttu-id="38350-127">指定要停止之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="38350-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="38350-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="38350-128">-Name</span></span>
<span data-ttu-id="38350-129">指定要停止之資源群組部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="38350-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="38350-130">如果您沒有指定此參數，這個 Cmdlet 會在資源群組中搜尋執行中的部署並停止。</span><span class="sxs-lookup"><span data-stu-id="38350-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="38350-131">如果它找到一個以上正在執行的部署，命令就會失敗。</span><span class="sxs-lookup"><span data-stu-id="38350-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="38350-132">若要取得部署名稱，請使用 Get-AzResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38350-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="38350-133">-預先</span><span class="sxs-lookup"><span data-stu-id="38350-133">-Pre</span></span>
<span data-ttu-id="38350-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="38350-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="38350-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38350-135">-ResourceGroupName</span></span>
<span data-ttu-id="38350-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38350-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="38350-137">這個 Cmdlet 會停止此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="38350-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="38350-138">-確認</span><span class="sxs-lookup"><span data-stu-id="38350-138">-Confirm</span></span>
<span data-ttu-id="38350-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38350-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38350-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38350-140">-WhatIf</span></span>
<span data-ttu-id="38350-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38350-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38350-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38350-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38350-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38350-143">CommonParameters</span></span>
<span data-ttu-id="38350-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38350-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38350-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38350-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38350-146">輸入</span><span class="sxs-lookup"><span data-stu-id="38350-146">INPUTS</span></span>

### <span data-ttu-id="38350-147">System.object</span><span class="sxs-lookup"><span data-stu-id="38350-147">System.String</span></span>

## <span data-ttu-id="38350-148">輸出</span><span class="sxs-lookup"><span data-stu-id="38350-148">OUTPUTS</span></span>

### <span data-ttu-id="38350-149">System.object</span><span class="sxs-lookup"><span data-stu-id="38350-149">System.Boolean</span></span>

## <span data-ttu-id="38350-150">筆記</span><span class="sxs-lookup"><span data-stu-id="38350-150">NOTES</span></span>

## <span data-ttu-id="38350-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="38350-151">RELATED LINKS</span></span>

[<span data-ttu-id="38350-152">AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38350-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="38350-153">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="38350-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="38350-154">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38350-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="38350-155">新-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38350-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="38350-156">移除-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38350-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="38350-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="38350-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


