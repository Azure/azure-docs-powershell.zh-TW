---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452408"
---
# <span data-ttu-id="e5d4d-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5d4d-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e5d4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d4d-103">取得資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5d4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5d4d-104">SYNTAX</span></span>

### <span data-ttu-id="e5d4d-105">已設定部署名稱參數。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-105">The deployment name parameter set.</span></span> <span data-ttu-id="e5d4d-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="e5d4d-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d4d-107">已設定部署識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d4d-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="e5d4d-109">**AzureRmResourceGroupDeployment** Cmdlet 會取得 Azure 資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="e5d4d-110">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="e5d4d-111">根據預設， **AzureRmResourceGroupDeployment 會取得** 指定資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="e5d4d-112">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="e5d4d-113">Azure 資源群組是一個以單位形式部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="e5d4d-114">部署是使資源群組中的資源可供使用的作業。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="e5d4d-115">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="e5d4d-116">您可以使用此 Cmdlet 進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="e5d4d-117">針對調試，請將此 Cmdlet 與 Get-AzureRmLog Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="e5d4d-118">示例</span><span class="sxs-lookup"><span data-stu-id="e5d4d-118">EXAMPLES</span></span>

### <span data-ttu-id="e5d4d-119">範例1：取得資源群組的所有部署</span><span class="sxs-lookup"><span data-stu-id="e5d4d-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="e5d4d-120">這個命令會取得 ContosoLabsRG 資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e5d4d-121">[輸出] 會顯示使用圖庫範本之 WordPress 博客的部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="e5d4d-122">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="e5d4d-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="e5d4d-123">這個命令會取得 ContosoLabsRG 資源群組的 DeployWebsite01 部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e5d4d-124">您可以使用 **新的 AzureRmResourceGroup** 或 **AzureRmResourceGroupDeployment** Cmdlet，在建立部署時指派名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="e5d4d-125">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="e5d4d-126">範例3：取得所有資源群組的部署</span><span class="sxs-lookup"><span data-stu-id="e5d4d-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="e5d4d-127">這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="e5d4d-128">命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5d4d-129">目前的 Cmdlet 會取得訂閱中所有資源群組的所有部署，並將結果傳遞給 Format-Table Cmdlet，以顯示其 **ResourceGroupName** 、 **DeploymentName** 和 **ProvisioningState** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="e5d4d-130">參數</span><span class="sxs-lookup"><span data-stu-id="e5d4d-130">PARAMETERS</span></span>

### <span data-ttu-id="e5d4d-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5d4d-131">-ApiVersion</span></span>
<span data-ttu-id="e5d4d-132">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e5d4d-133">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e5d4d-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e5d4d-134">-Id</span></span>
<span data-ttu-id="e5d4d-135">指定要取得之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-135">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="e5d4d-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5d4d-136">-Name</span></span>
<span data-ttu-id="e5d4d-137">指定要取得之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="e5d4d-138">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d4d-139">-預先</span><span class="sxs-lookup"><span data-stu-id="e5d4d-139">-Pre</span></span>
<span data-ttu-id="e5d4d-140">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5d4d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d4d-141">-ResourceGroupName</span></span>
<span data-ttu-id="e5d4d-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e5d4d-143">此 Cmdlet 會取得此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="e5d4d-144">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="e5d4d-145">這個參數是必要的，而且您只能在每個命令中指定一個資源群組。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-145">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="e5d4d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d4d-146">-DefaultProfile</span></span>
<span data-ttu-id="e5d4d-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5d4d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d4d-148">CommonParameters</span></span>
<span data-ttu-id="e5d4d-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d4d-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d4d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="e5d4d-151">INPUTS</span></span>

### <span data-ttu-id="e5d4d-152">所有</span><span class="sxs-lookup"><span data-stu-id="e5d4d-152">None</span></span>

## <span data-ttu-id="e5d4d-153">輸出</span><span class="sxs-lookup"><span data-stu-id="e5d4d-153">OUTPUTS</span></span>

### <span data-ttu-id="e5d4d-154">PSResourceGroupDeployment 中的 ResourceManagement。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="e5d4d-155">這個 Cmdlet 會傳回資源群組部署。</span><span class="sxs-lookup"><span data-stu-id="e5d4d-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="e5d4d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="e5d4d-156">NOTES</span></span>

## <span data-ttu-id="e5d4d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5d4d-157">RELATED LINKS</span></span>

[<span data-ttu-id="e5d4d-158">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5d4d-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="e5d4d-159">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5d4d-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e5d4d-160">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5d4d-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5d4d-161">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5d4d-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5d4d-162">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5d4d-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e5d4d-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e5d4d-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


