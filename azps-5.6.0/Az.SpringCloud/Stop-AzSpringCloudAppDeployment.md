---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0de600b2b21d634e85b4ed0266a3b72c95266f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904825"
---
# <span data-ttu-id="06d21-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="06d21-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="06d21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06d21-102">SYNOPSIS</span></span>
<span data-ttu-id="06d21-103">停止部署。</span><span class="sxs-lookup"><span data-stu-id="06d21-103">Stop the deployment.</span></span>

## <span data-ttu-id="06d21-104">語法</span><span class="sxs-lookup"><span data-stu-id="06d21-104">SYNTAX</span></span>

### <span data-ttu-id="06d21-105">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="06d21-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06d21-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06d21-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06d21-107">描述</span><span class="sxs-lookup"><span data-stu-id="06d21-107">DESCRIPTION</span></span>
<span data-ttu-id="06d21-108">停止部署。</span><span class="sxs-lookup"><span data-stu-id="06d21-108">Stop the deployment.</span></span>

## <span data-ttu-id="06d21-109">例子</span><span class="sxs-lookup"><span data-stu-id="06d21-109">EXAMPLES</span></span>

### <span data-ttu-id="06d21-110">範例 1：按名稱停止 Spring Cloud Service。</span><span class="sxs-lookup"><span data-stu-id="06d21-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="06d21-111">以名稱停止春雲服務。</span><span class="sxs-lookup"><span data-stu-id="06d21-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="06d21-112">範例 2：停止 Spring Cloud Service 從管道。</span><span class="sxs-lookup"><span data-stu-id="06d21-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="06d21-113">停止從管道使用春雲服務。</span><span class="sxs-lookup"><span data-stu-id="06d21-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="06d21-114">參數</span><span class="sxs-lookup"><span data-stu-id="06d21-114">PARAMETERS</span></span>

### <span data-ttu-id="06d21-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="06d21-115">-AppName</span></span>
<span data-ttu-id="06d21-116">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d21-117">-AsJob</span></span>
<span data-ttu-id="06d21-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="06d21-118">Run the command as a job</span></span>

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

### <span data-ttu-id="06d21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d21-119">-DefaultProfile</span></span>
<span data-ttu-id="06d21-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06d21-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d21-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d21-121">-InputObject</span></span>
<span data-ttu-id="06d21-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="06d21-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="06d21-123">-Name</span></span>
<span data-ttu-id="06d21-124">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06d21-125">-NoWait</span></span>
<span data-ttu-id="06d21-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="06d21-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06d21-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06d21-127">-PassThru</span></span>
<span data-ttu-id="06d21-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="06d21-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06d21-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d21-129">-ResourceGroupName</span></span>
<span data-ttu-id="06d21-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="06d21-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="06d21-131">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="06d21-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="06d21-132">-ServiceName</span></span>
<span data-ttu-id="06d21-133">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06d21-134">-SubscriptionId</span></span>
<span data-ttu-id="06d21-135">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="06d21-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="06d21-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="06d21-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d21-137">-確認</span><span class="sxs-lookup"><span data-stu-id="06d21-137">-Confirm</span></span>
<span data-ttu-id="06d21-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06d21-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d21-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d21-139">-WhatIf</span></span>
<span data-ttu-id="06d21-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06d21-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d21-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06d21-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d21-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d21-142">CommonParameters</span></span>
<span data-ttu-id="06d21-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06d21-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d21-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06d21-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d21-145">輸入</span><span class="sxs-lookup"><span data-stu-id="06d21-145">INPUTS</span></span>

### <span data-ttu-id="06d21-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="06d21-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="06d21-147">輸出</span><span class="sxs-lookup"><span data-stu-id="06d21-147">OUTPUTS</span></span>

### <span data-ttu-id="06d21-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06d21-148">System.Boolean</span></span>

## <span data-ttu-id="06d21-149">筆記</span><span class="sxs-lookup"><span data-stu-id="06d21-149">NOTES</span></span>

<span data-ttu-id="06d21-150">別名</span><span class="sxs-lookup"><span data-stu-id="06d21-150">ALIASES</span></span>

<span data-ttu-id="06d21-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="06d21-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06d21-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="06d21-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06d21-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="06d21-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06d21-154">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="06d21-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06d21-155">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="06d21-156">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="06d21-157">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="06d21-158">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="06d21-159">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="06d21-160">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="06d21-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06d21-161">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="06d21-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="06d21-162">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="06d21-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="06d21-163">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="06d21-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="06d21-164">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d21-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="06d21-165">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="06d21-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="06d21-166">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="06d21-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06d21-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="06d21-167">RELATED LINKS</span></span>

