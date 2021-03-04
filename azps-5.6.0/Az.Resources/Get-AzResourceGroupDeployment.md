---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911318"
---
# <span data-ttu-id="02682-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="02682-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02682-102">SYNOPSIS</span></span>
<span data-ttu-id="02682-103">在資源群組中進行部署。</span><span class="sxs-lookup"><span data-stu-id="02682-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="02682-104">語法</span><span class="sxs-lookup"><span data-stu-id="02682-104">SYNTAX</span></span>

### <span data-ttu-id="02682-105">GetByResourceGroupDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="02682-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02682-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="02682-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02682-107">描述</span><span class="sxs-lookup"><span data-stu-id="02682-107">DESCRIPTION</span></span>
<span data-ttu-id="02682-108">**Get-AzResourceGroupDeployment** Cmdlet 取得 Azure 資源群組中的部署。</span><span class="sxs-lookup"><span data-stu-id="02682-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="02682-109">指定 *名稱* 或 *Id* 參數以篩選結果。</span><span class="sxs-lookup"><span data-stu-id="02682-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="02682-110">根據預設 **，Get-AzResourceGroupDeployment 會** 取得指定資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="02682-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="02682-111">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。</span><span class="sxs-lookup"><span data-stu-id="02682-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="02682-112">Azure 資源群組是部署為一個單位的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="02682-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="02682-113">部署是一項作業，可讓資源群組中的資源可供使用。</span><span class="sxs-lookup"><span data-stu-id="02682-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="02682-114">有關 Azure 資源與 Azure 資源群組的資訊，請參閱 New-AzResourceGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02682-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="02682-115">您可以使用此 Cmdlet 進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="02682-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="02682-116">如要進行比對，請使用此 Cmdlet Get-AzLog Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02682-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="02682-117">例子</span><span class="sxs-lookup"><span data-stu-id="02682-117">EXAMPLES</span></span>

### <span data-ttu-id="02682-118">範例 1：取得資源群組的所有部署</span><span class="sxs-lookup"><span data-stu-id="02682-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="02682-119">此命令會獲得 ContosoLabsRG 資源群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="02682-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="02682-120">輸出顯示使用圖庫範本之 WordPress 部落格的部署。</span><span class="sxs-lookup"><span data-stu-id="02682-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="02682-121">範例 2：根據名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="02682-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="02682-122">此命令會獲得 ContosoLabsRG 資源群組的 DeployWebsite01 部署。</span><span class="sxs-lookup"><span data-stu-id="02682-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="02682-123">您可以使用 **New-AzResourceGroup** 或 **New-AzResourceGroupDeployment** Cmdlet 為部署指派名稱。</span><span class="sxs-lookup"><span data-stu-id="02682-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="02682-124">如果您沒有指派名稱，Cmdlet 會根據用來建立部署的範本提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="02682-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="02682-125">範例 3：取得所有資源群組的部署</span><span class="sxs-lookup"><span data-stu-id="02682-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="02682-126">此命令會使用 Cmdlet，在訂閱中Get-AzResourceGroup群組。</span><span class="sxs-lookup"><span data-stu-id="02682-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="02682-127">該命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02682-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02682-128">目前的 Cmdlet 會取得訂閱中所有資源群組的所有部署，並且將結果傳遞至 Format-Table Cmdlet 以顯示 **其 ResourceGroupName、DeploymentName** 和 **ProvisioningState** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="02682-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="02682-129">參數</span><span class="sxs-lookup"><span data-stu-id="02682-129">PARAMETERS</span></span>

### <span data-ttu-id="02682-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02682-130">-DefaultProfile</span></span>
<span data-ttu-id="02682-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="02682-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02682-132">-Id</span><span class="sxs-lookup"><span data-stu-id="02682-132">-Id</span></span>
<span data-ttu-id="02682-133">指定要取得的資源群組部署識別碼。</span><span class="sxs-lookup"><span data-stu-id="02682-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="02682-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="02682-134">-Name</span></span>
<span data-ttu-id="02682-135">指定要取得之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="02682-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="02682-136">不允許萬用字元。</span><span class="sxs-lookup"><span data-stu-id="02682-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="02682-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="02682-137">-Pre</span></span>
<span data-ttu-id="02682-138">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="02682-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="02682-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02682-139">-ResourceGroupName</span></span>
<span data-ttu-id="02682-140">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02682-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="02682-141">Cmdlet 會針對此參數指定的資源群組獲得部署。</span><span class="sxs-lookup"><span data-stu-id="02682-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="02682-142">不允許萬用字元。</span><span class="sxs-lookup"><span data-stu-id="02682-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="02682-143">此參數為必填項，而且每個命令中只能指定一個資源群組。</span><span class="sxs-lookup"><span data-stu-id="02682-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="02682-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02682-144">CommonParameters</span></span>
<span data-ttu-id="02682-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02682-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02682-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02682-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02682-147">輸入</span><span class="sxs-lookup"><span data-stu-id="02682-147">INPUTS</span></span>

### <span data-ttu-id="02682-148">System.String</span><span class="sxs-lookup"><span data-stu-id="02682-148">System.String</span></span>

## <span data-ttu-id="02682-149">輸出</span><span class="sxs-lookup"><span data-stu-id="02682-149">OUTPUTS</span></span>

### <span data-ttu-id="02682-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="02682-151">筆記</span><span class="sxs-lookup"><span data-stu-id="02682-151">NOTES</span></span>

## <span data-ttu-id="02682-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="02682-152">RELATED LINKS</span></span>

[<span data-ttu-id="02682-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02682-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="02682-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02682-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="02682-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="02682-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="02682-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="02682-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02682-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


