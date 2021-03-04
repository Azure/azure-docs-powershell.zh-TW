---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: 2ea144ec36830286919f9cb512ccec01008428a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915785"
---
# <span data-ttu-id="33cf2-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="33cf2-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="33cf2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="33cf2-103">更新即將離開的 App 的作業。</span><span class="sxs-lookup"><span data-stu-id="33cf2-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="33cf2-104">語法</span><span class="sxs-lookup"><span data-stu-id="33cf2-104">SYNTAX</span></span>

### <span data-ttu-id="33cf2-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="33cf2-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33cf2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="33cf2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33cf2-107">描述</span><span class="sxs-lookup"><span data-stu-id="33cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="33cf2-108">更新即將離開的 App 的作業。</span><span class="sxs-lookup"><span data-stu-id="33cf2-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="33cf2-109">例子</span><span class="sxs-lookup"><span data-stu-id="33cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="33cf2-110">範例 1：按名稱更新 Spring Cloud App。</span><span class="sxs-lookup"><span data-stu-id="33cf2-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="33cf2-111">按名稱更新 Spring Cloud App。</span><span class="sxs-lookup"><span data-stu-id="33cf2-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="33cf2-112">範例 2：從管道更新 Spring Cloud App。</span><span class="sxs-lookup"><span data-stu-id="33cf2-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="33cf2-113">從管道更新 Spring Cloud App。</span><span class="sxs-lookup"><span data-stu-id="33cf2-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="33cf2-114">參數</span><span class="sxs-lookup"><span data-stu-id="33cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="33cf2-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="33cf2-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="33cf2-116">應用程式使用中部署的名稱</span><span class="sxs-lookup"><span data-stu-id="33cf2-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="33cf2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33cf2-117">-AsJob</span></span>
<span data-ttu-id="33cf2-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="33cf2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="33cf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33cf2-119">-DefaultProfile</span></span>
<span data-ttu-id="33cf2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33cf2-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="33cf2-121">-Fqdn</span></span>
<span data-ttu-id="33cf2-122">完整 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="33cf2-123">-HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="33cf2-123">-HttpsOnly</span></span>
<span data-ttu-id="33cf2-124">指出是否僅允許 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="33cf2-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="33cf2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33cf2-125">-InputObject</span></span>
<span data-ttu-id="33cf2-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="33cf2-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-127">-位置</span><span class="sxs-lookup"><span data-stu-id="33cf2-127">-Location</span></span>
<span data-ttu-id="33cf2-128">應用程式的 GEO 位置，一定與它的父資源相同</span><span class="sxs-lookup"><span data-stu-id="33cf2-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="33cf2-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="33cf2-129">-Name</span></span>
<span data-ttu-id="33cf2-130">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33cf2-131">-NoWait</span></span>
<span data-ttu-id="33cf2-132">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="33cf2-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33cf2-133">-PersistentMountPath</span><span class="sxs-lookup"><span data-stu-id="33cf2-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="33cf2-134">持續性磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="33cf2-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="33cf2-135">-Persistent以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="33cf2-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="33cf2-136">以 GB 為單位的永久磁片大小</span><span class="sxs-lookup"><span data-stu-id="33cf2-136">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-137">-公用</span><span class="sxs-lookup"><span data-stu-id="33cf2-137">-Public</span></span>
<span data-ttu-id="33cf2-138">指出應用程式是否公開公用端點</span><span class="sxs-lookup"><span data-stu-id="33cf2-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="33cf2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33cf2-139">-ResourceGroupName</span></span>
<span data-ttu-id="33cf2-140">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="33cf2-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="33cf2-141">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="33cf2-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="33cf2-142">-ServiceName</span></span>
<span data-ttu-id="33cf2-143">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-143">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33cf2-144">-SubscriptionId</span></span>
<span data-ttu-id="33cf2-145">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="33cf2-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="33cf2-146">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="33cf2-146">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-147">-TemporaryMountPath</span><span class="sxs-lookup"><span data-stu-id="33cf2-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="33cf2-148">暫用磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="33cf2-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="33cf2-149">-Temporary以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="33cf2-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="33cf2-150">暫用磁片的大小 ，以 GB 為單位</span><span class="sxs-lookup"><span data-stu-id="33cf2-150">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33cf2-151">-確認</span><span class="sxs-lookup"><span data-stu-id="33cf2-151">-Confirm</span></span>
<span data-ttu-id="33cf2-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33cf2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33cf2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33cf2-153">-WhatIf</span></span>
<span data-ttu-id="33cf2-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33cf2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33cf2-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33cf2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33cf2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33cf2-156">CommonParameters</span></span>
<span data-ttu-id="33cf2-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33cf2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33cf2-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33cf2-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33cf2-159">輸入</span><span class="sxs-lookup"><span data-stu-id="33cf2-159">INPUTS</span></span>

### <span data-ttu-id="33cf2-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="33cf2-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="33cf2-161">輸出</span><span class="sxs-lookup"><span data-stu-id="33cf2-161">OUTPUTS</span></span>

### <span data-ttu-id="33cf2-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="33cf2-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="33cf2-163">筆記</span><span class="sxs-lookup"><span data-stu-id="33cf2-163">NOTES</span></span>

<span data-ttu-id="33cf2-164">別名</span><span class="sxs-lookup"><span data-stu-id="33cf2-164">ALIASES</span></span>

<span data-ttu-id="33cf2-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="33cf2-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33cf2-166">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="33cf2-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33cf2-167">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="33cf2-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33cf2-168">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="33cf2-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33cf2-169">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="33cf2-170">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="33cf2-171">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="33cf2-172">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="33cf2-173">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="33cf2-174">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="33cf2-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33cf2-175">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="33cf2-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="33cf2-176">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="33cf2-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="33cf2-177">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="33cf2-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="33cf2-178">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf2-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="33cf2-179">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="33cf2-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="33cf2-180">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="33cf2-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="33cf2-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="33cf2-181">RELATED LINKS</span></span>

