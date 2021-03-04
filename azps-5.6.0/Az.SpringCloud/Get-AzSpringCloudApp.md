---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 62a0398ca117ac623d0b21cc89908b25a4e7e1e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902750"
---
# <span data-ttu-id="8e0d7-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="8e0d7-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="8e0d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0d7-103">取得應用程式及其屬性。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-103">Get an App and its properties.</span></span>

## <span data-ttu-id="8e0d7-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e0d7-104">SYNTAX</span></span>

### <span data-ttu-id="8e0d7-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="8e0d7-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e0d7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8e0d7-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e0d7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e0d7-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e0d7-108">描述</span><span class="sxs-lookup"><span data-stu-id="8e0d7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e0d7-109">取得應用程式及其屬性。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-109">Get an App and its properties.</span></span>

## <span data-ttu-id="8e0d7-110">例子</span><span class="sxs-lookup"><span data-stu-id="8e0d7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e0d7-111">範例 1：按名稱取得 Spring Cloud App。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="8e0d7-112">取得春雲 App 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="8e0d7-113">範例 2：列出給定之春雲服務下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="8e0d7-114">列出在一個給定之春雲服務下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="8e0d7-115">參數</span><span class="sxs-lookup"><span data-stu-id="8e0d7-115">PARAMETERS</span></span>

### <span data-ttu-id="8e0d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0d7-116">-DefaultProfile</span></span>
<span data-ttu-id="8e0d7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e0d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e0d7-118">-InputObject</span></span>
<span data-ttu-id="8e0d7-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e0d7-120">-Name</span></span>
<span data-ttu-id="8e0d7-121">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e0d7-123">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8e0d7-124">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e0d7-125">-ServiceName</span></span>
<span data-ttu-id="8e0d7-126">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e0d7-127">-SubscriptionId</span></span>
<span data-ttu-id="8e0d7-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e0d7-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="8e0d7-130">-SyncStatus</span></span>
<span data-ttu-id="8e0d7-131">指出同步狀態是否</span><span class="sxs-lookup"><span data-stu-id="8e0d7-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0d7-132">CommonParameters</span></span>
<span data-ttu-id="8e0d7-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0d7-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e0d7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0d7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8e0d7-135">INPUTS</span></span>

### <span data-ttu-id="8e0d7-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8e0d7-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8e0d7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8e0d7-137">OUTPUTS</span></span>

### <span data-ttu-id="8e0d7-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="8e0d7-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="8e0d7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8e0d7-139">NOTES</span></span>

<span data-ttu-id="8e0d7-140">別名</span><span class="sxs-lookup"><span data-stu-id="8e0d7-140">ALIASES</span></span>

<span data-ttu-id="8e0d7-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8e0d7-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e0d7-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e0d7-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e0d7-144">INPUTOBJECT： <ISpringCloudIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8e0d7-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e0d7-145">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8e0d7-146">`[BindingName <String>]`：裝訂資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8e0d7-147">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8e0d7-148">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8e0d7-149">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8e0d7-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8e0d7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e0d7-151">`[Location <String>]`：地區</span><span class="sxs-lookup"><span data-stu-id="8e0d7-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8e0d7-152">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8e0d7-153">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8e0d7-154">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8e0d7-155">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8e0d7-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e0d7-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e0d7-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e0d7-157">RELATED LINKS</span></span>

