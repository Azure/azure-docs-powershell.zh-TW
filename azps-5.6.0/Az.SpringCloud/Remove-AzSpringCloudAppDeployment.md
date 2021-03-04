---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: e1fff88e6d591f7ffd3d7b602e8d60febf5b1c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908446"
---
# <span data-ttu-id="11250-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="11250-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="11250-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11250-102">SYNOPSIS</span></span>
<span data-ttu-id="11250-103">刪除部署的操作。</span><span class="sxs-lookup"><span data-stu-id="11250-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="11250-104">語法</span><span class="sxs-lookup"><span data-stu-id="11250-104">SYNTAX</span></span>

### <span data-ttu-id="11250-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="11250-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="11250-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11250-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11250-107">描述</span><span class="sxs-lookup"><span data-stu-id="11250-107">DESCRIPTION</span></span>
<span data-ttu-id="11250-108">刪除部署的操作。</span><span class="sxs-lookup"><span data-stu-id="11250-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="11250-109">例子</span><span class="sxs-lookup"><span data-stu-id="11250-109">EXAMPLES</span></span>

### <span data-ttu-id="11250-110">範例 1：根據名稱移除春雲部署。</span><span class="sxs-lookup"><span data-stu-id="11250-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="11250-111">按名稱移除春雲部署。</span><span class="sxs-lookup"><span data-stu-id="11250-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="11250-112">範例 2：從管道移除 Spring Cloud 部署。</span><span class="sxs-lookup"><span data-stu-id="11250-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="11250-113">從管道移除 Spring Cloud 部署。</span><span class="sxs-lookup"><span data-stu-id="11250-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="11250-114">參數</span><span class="sxs-lookup"><span data-stu-id="11250-114">PARAMETERS</span></span>

### <span data-ttu-id="11250-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="11250-115">-AppName</span></span>
<span data-ttu-id="11250-116">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11250-117">-AsJob</span></span>
<span data-ttu-id="11250-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="11250-118">Run the command as a job</span></span>

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

### <span data-ttu-id="11250-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11250-119">-DefaultProfile</span></span>
<span data-ttu-id="11250-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11250-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11250-121">-InputObject</span></span>
<span data-ttu-id="11250-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="11250-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11250-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="11250-123">-Name</span></span>
<span data-ttu-id="11250-124">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11250-125">-NoWait</span></span>
<span data-ttu-id="11250-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="11250-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11250-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11250-127">-PassThru</span></span>
<span data-ttu-id="11250-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="11250-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="11250-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11250-129">-ResourceGroupName</span></span>
<span data-ttu-id="11250-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="11250-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="11250-131">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="11250-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11250-132">-ServiceName</span></span>
<span data-ttu-id="11250-133">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11250-134">-SubscriptionId</span></span>
<span data-ttu-id="11250-135">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="11250-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="11250-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="11250-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-137">-確認</span><span class="sxs-lookup"><span data-stu-id="11250-137">-Confirm</span></span>
<span data-ttu-id="11250-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11250-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11250-139">-WhatIf</span></span>
<span data-ttu-id="11250-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11250-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11250-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11250-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11250-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11250-142">CommonParameters</span></span>
<span data-ttu-id="11250-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11250-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11250-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11250-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11250-145">輸入</span><span class="sxs-lookup"><span data-stu-id="11250-145">INPUTS</span></span>

### <span data-ttu-id="11250-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="11250-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="11250-147">輸出</span><span class="sxs-lookup"><span data-stu-id="11250-147">OUTPUTS</span></span>

### <span data-ttu-id="11250-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11250-148">System.Boolean</span></span>

## <span data-ttu-id="11250-149">筆記</span><span class="sxs-lookup"><span data-stu-id="11250-149">NOTES</span></span>

<span data-ttu-id="11250-150">別名</span><span class="sxs-lookup"><span data-stu-id="11250-150">ALIASES</span></span>

<span data-ttu-id="11250-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="11250-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11250-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="11250-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11250-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="11250-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11250-154">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="11250-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11250-155">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="11250-156">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="11250-157">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="11250-158">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="11250-159">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="11250-160">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="11250-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11250-161">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="11250-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="11250-162">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="11250-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="11250-163">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="11250-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="11250-164">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="11250-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="11250-165">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="11250-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="11250-166">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="11250-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11250-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="11250-167">RELATED LINKS</span></span>

