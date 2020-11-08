---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800045"
---
# <span data-ttu-id="b0597-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b0597-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0597-102">SYNOPSIS</span></span>
<span data-ttu-id="b0597-103">取得資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0597-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0597-104">SYNTAX</span></span>

### <span data-ttu-id="b0597-105">GetByResourceGroupDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="b0597-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0597-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b0597-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0597-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0597-107">DESCRIPTION</span></span>
<span data-ttu-id="b0597-108">**AzureRmResourceGroupDeployment** Cmdlet 會取得 Azure 資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="b0597-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="b0597-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="b0597-110">根據預設， **AzureRmResourceGroupDeployment 會取得** 指定資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="b0597-111">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。</span><span class="sxs-lookup"><span data-stu-id="b0597-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="b0597-112">Azure 資源群組是一個以單位形式部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="b0597-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="b0597-113">部署是使資源群組中的資源可供使用的作業。</span><span class="sxs-lookup"><span data-stu-id="b0597-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="b0597-114">如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0597-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="b0597-115">您可以使用此 Cmdlet 進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="b0597-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="b0597-116">針對調試，請將此 Cmdlet 與 Get-AzureRmLog Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b0597-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="b0597-117">示例</span><span class="sxs-lookup"><span data-stu-id="b0597-117">EXAMPLES</span></span>

### <span data-ttu-id="b0597-118">範例1：取得資源群組的所有部署</span><span class="sxs-lookup"><span data-stu-id="b0597-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="b0597-119">這個命令會取得 ContosoLabsRG 資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="b0597-120">[輸出] 會顯示使用圖庫範本之 WordPress 博客的部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="b0597-121">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="b0597-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="b0597-122">這個命令會取得 ContosoLabsRG 資源群組的 DeployWebsite01 部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="b0597-123">您可以使用 **新的 AzureRmResourceGroup** 或 **AzureRmResourceGroupDeployment** Cmdlet，在建立部署時指派名稱。</span><span class="sxs-lookup"><span data-stu-id="b0597-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="b0597-124">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="b0597-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="b0597-125">範例3：取得所有資源群組的部署</span><span class="sxs-lookup"><span data-stu-id="b0597-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="b0597-126">這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得訂閱中的所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="b0597-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="b0597-127">命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0597-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0597-128">目前的 Cmdlet 會取得訂閱中所有資源群組的所有部署，並將結果傳遞給 Format-Table Cmdlet，以顯示其 **ResourceGroupName** 、 **DeploymentName** 和 **ProvisioningState** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="b0597-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="b0597-129">參數</span><span class="sxs-lookup"><span data-stu-id="b0597-129">PARAMETERS</span></span>

### <span data-ttu-id="b0597-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b0597-130">-ApiVersion</span></span>
<span data-ttu-id="b0597-131">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b0597-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b0597-132">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="b0597-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b0597-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0597-133">-DefaultProfile</span></span>
<span data-ttu-id="b0597-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0597-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0597-135">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b0597-135">-Id</span></span>
<span data-ttu-id="b0597-136">指定要取得之資源群組部署的 ID。</span><span class="sxs-lookup"><span data-stu-id="b0597-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0597-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0597-137">-Name</span></span>
<span data-ttu-id="b0597-138">指定要取得之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0597-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="b0597-139">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="b0597-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0597-140">-預先</span><span class="sxs-lookup"><span data-stu-id="b0597-140">-Pre</span></span>
<span data-ttu-id="b0597-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b0597-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b0597-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0597-142">-ResourceGroupName</span></span>
<span data-ttu-id="b0597-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0597-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b0597-144">此 Cmdlet 會取得此參數指定之資源群組的部署。</span><span class="sxs-lookup"><span data-stu-id="b0597-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="b0597-145">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="b0597-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="b0597-146">這個參數是必要的，而且您只能在每個命令中指定一個資源群組。</span><span class="sxs-lookup"><span data-stu-id="b0597-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0597-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0597-147">CommonParameters</span></span>
<span data-ttu-id="b0597-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0597-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0597-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0597-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0597-150">輸入</span><span class="sxs-lookup"><span data-stu-id="b0597-150">INPUTS</span></span>

### <span data-ttu-id="b0597-151">所有</span><span class="sxs-lookup"><span data-stu-id="b0597-151">None</span></span>

## <span data-ttu-id="b0597-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b0597-152">OUTPUTS</span></span>

### <span data-ttu-id="b0597-153">ResourceManagement 的模型。</span><span class="sxs-lookup"><span data-stu-id="b0597-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="b0597-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="b0597-155">筆記</span><span class="sxs-lookup"><span data-stu-id="b0597-155">NOTES</span></span>

## <span data-ttu-id="b0597-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0597-156">RELATED LINKS</span></span>

[<span data-ttu-id="b0597-157">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0597-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="b0597-158">新-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0597-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="b0597-159">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0597-160">移除-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0597-161">停止 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0597-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0597-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)

