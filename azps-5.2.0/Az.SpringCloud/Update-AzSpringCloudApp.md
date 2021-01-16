---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276047"
---
# <span data-ttu-id="1eb9a-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="1eb9a-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="1eb9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1eb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb9a-103">更新現有應用程式的操作。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="1eb9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1eb9a-104">SYNTAX</span></span>

### <span data-ttu-id="1eb9a-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1eb9a-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1eb9a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1eb9a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1eb9a-107">說明</span><span class="sxs-lookup"><span data-stu-id="1eb9a-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb9a-108">更新現有應用程式的操作。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="1eb9a-109">示例</span><span class="sxs-lookup"><span data-stu-id="1eb9a-109">EXAMPLES</span></span>

### <span data-ttu-id="1eb9a-110">範例1：依名稱更新彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="1eb9a-111">依名稱更新彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="1eb9a-112">範例2：從管道更新彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="1eb9a-113">從管道更新彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="1eb9a-114">參數</span><span class="sxs-lookup"><span data-stu-id="1eb9a-114">PARAMETERS</span></span>

### <span data-ttu-id="1eb9a-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="1eb9a-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="1eb9a-116">App 作用中部署的名稱</span><span class="sxs-lookup"><span data-stu-id="1eb9a-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="1eb9a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb9a-117">-AsJob</span></span>
<span data-ttu-id="1eb9a-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="1eb9a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1eb9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb9a-119">-DefaultProfile</span></span>
<span data-ttu-id="1eb9a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb9a-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="1eb9a-121">-Fqdn</span></span>
<span data-ttu-id="1eb9a-122">完全合格的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="1eb9a-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1eb9a-123">-HttpsOnly</span></span>
<span data-ttu-id="1eb9a-124">指出是否允許只有 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="1eb9a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb9a-125">-InputObject</span></span>
<span data-ttu-id="1eb9a-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1eb9a-127">-位置</span><span class="sxs-lookup"><span data-stu-id="1eb9a-127">-Location</span></span>
<span data-ttu-id="1eb9a-128">應用程式的地理位置，與其父項資源永遠相同</span><span class="sxs-lookup"><span data-stu-id="1eb9a-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="1eb9a-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1eb9a-129">-Name</span></span>
<span data-ttu-id="1eb9a-130">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="1eb9a-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1eb9a-131">-NoWait</span></span>
<span data-ttu-id="1eb9a-132">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="1eb9a-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1eb9a-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="1eb9a-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="1eb9a-134">持久性磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="1eb9a-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="1eb9a-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="1eb9a-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="1eb9a-136">持久性磁片大小（GB）</span><span class="sxs-lookup"><span data-stu-id="1eb9a-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="1eb9a-137">-公開</span><span class="sxs-lookup"><span data-stu-id="1eb9a-137">-Public</span></span>
<span data-ttu-id="1eb9a-138">指出 App 是否公開公用端點</span><span class="sxs-lookup"><span data-stu-id="1eb9a-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="1eb9a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb9a-139">-ResourceGroupName</span></span>
<span data-ttu-id="1eb9a-140">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1eb9a-141">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1eb9a-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1eb9a-142">-ServiceName</span></span>
<span data-ttu-id="1eb9a-143">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="1eb9a-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1eb9a-144">-SubscriptionId</span></span>
<span data-ttu-id="1eb9a-145">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1eb9a-146">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1eb9a-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="1eb9a-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="1eb9a-148">臨時磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="1eb9a-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="1eb9a-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="1eb9a-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="1eb9a-150">暫時磁片大小（GB）</span><span class="sxs-lookup"><span data-stu-id="1eb9a-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="1eb9a-151">-確認</span><span class="sxs-lookup"><span data-stu-id="1eb9a-151">-Confirm</span></span>
<span data-ttu-id="1eb9a-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb9a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb9a-153">-WhatIf</span></span>
<span data-ttu-id="1eb9a-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb9a-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb9a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb9a-156">CommonParameters</span></span>
<span data-ttu-id="1eb9a-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb9a-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb9a-159">輸入</span><span class="sxs-lookup"><span data-stu-id="1eb9a-159">INPUTS</span></span>

### <span data-ttu-id="1eb9a-160">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="1eb9a-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1eb9a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="1eb9a-161">OUTPUTS</span></span>

### <span data-ttu-id="1eb9a-162">IAppResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="1eb9a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="1eb9a-163">NOTES</span></span>

<span data-ttu-id="1eb9a-164">別名</span><span class="sxs-lookup"><span data-stu-id="1eb9a-164">ALIASES</span></span>

<span data-ttu-id="1eb9a-165">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1eb9a-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1eb9a-166">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1eb9a-167">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1eb9a-168">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1eb9a-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1eb9a-169">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1eb9a-170">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1eb9a-171">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1eb9a-172">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1eb9a-173">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1eb9a-174">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1eb9a-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1eb9a-175">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="1eb9a-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1eb9a-176">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1eb9a-177">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1eb9a-178">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1eb9a-179">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1eb9a-180">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1eb9a-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1eb9a-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="1eb9a-181">RELATED LINKS</span></span>

