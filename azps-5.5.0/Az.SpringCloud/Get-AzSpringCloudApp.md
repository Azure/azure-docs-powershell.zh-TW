---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138330"
---
# <span data-ttu-id="aacaa-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="aacaa-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="aacaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aacaa-102">SYNOPSIS</span></span>
<span data-ttu-id="aacaa-103">取得 App 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="aacaa-103">Get an App and its properties.</span></span>

## <span data-ttu-id="aacaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="aacaa-104">SYNTAX</span></span>

### <span data-ttu-id="aacaa-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="aacaa-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aacaa-106">獲取</span><span class="sxs-lookup"><span data-stu-id="aacaa-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aacaa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aacaa-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aacaa-108">說明</span><span class="sxs-lookup"><span data-stu-id="aacaa-108">DESCRIPTION</span></span>
<span data-ttu-id="aacaa-109">取得 App 及其屬性。</span><span class="sxs-lookup"><span data-stu-id="aacaa-109">Get an App and its properties.</span></span>

## <span data-ttu-id="aacaa-110">示例</span><span class="sxs-lookup"><span data-stu-id="aacaa-110">EXAMPLES</span></span>

### <span data-ttu-id="aacaa-111">範例1：透過名稱取得彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="aacaa-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="aacaa-112">透過名稱取得彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="aacaa-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="aacaa-113">範例2：列出指定彈簧雲端服務下的所有 app。</span><span class="sxs-lookup"><span data-stu-id="aacaa-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="aacaa-114">列出指定春季雲端服務下的所有 app。</span><span class="sxs-lookup"><span data-stu-id="aacaa-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="aacaa-115">參數</span><span class="sxs-lookup"><span data-stu-id="aacaa-115">PARAMETERS</span></span>

### <span data-ttu-id="aacaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacaa-116">-DefaultProfile</span></span>
<span data-ttu-id="aacaa-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacaa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aacaa-118">-InputObject</span></span>
<span data-ttu-id="aacaa-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="aacaa-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aacaa-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="aacaa-120">-Name</span></span>
<span data-ttu-id="aacaa-121">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="aacaa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aacaa-122">-ResourceGroupName</span></span>
<span data-ttu-id="aacaa-123">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aacaa-124">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="aacaa-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aacaa-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aacaa-125">-ServiceName</span></span>
<span data-ttu-id="aacaa-126">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="aacaa-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aacaa-127">-SubscriptionId</span></span>
<span data-ttu-id="aacaa-128">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aacaa-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aacaa-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="aacaa-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aacaa-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="aacaa-130">-SyncStatus</span></span>
<span data-ttu-id="aacaa-131">指出是否同步處理狀態</span><span class="sxs-lookup"><span data-stu-id="aacaa-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="aacaa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacaa-132">CommonParameters</span></span>
<span data-ttu-id="aacaa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aacaa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacaa-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aacaa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacaa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="aacaa-135">INPUTS</span></span>

### <span data-ttu-id="aacaa-136">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="aacaa-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="aacaa-137">輸出</span><span class="sxs-lookup"><span data-stu-id="aacaa-137">OUTPUTS</span></span>

### <span data-ttu-id="aacaa-138">IAppResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="aacaa-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="aacaa-139">筆記</span><span class="sxs-lookup"><span data-stu-id="aacaa-139">NOTES</span></span>

<span data-ttu-id="aacaa-140">別名</span><span class="sxs-lookup"><span data-stu-id="aacaa-140">ALIASES</span></span>

<span data-ttu-id="aacaa-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="aacaa-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aacaa-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="aacaa-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aacaa-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="aacaa-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aacaa-144">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="aacaa-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aacaa-145">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="aacaa-146">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="aacaa-147">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="aacaa-148">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="aacaa-149">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="aacaa-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="aacaa-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aacaa-151">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="aacaa-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="aacaa-152">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="aacaa-153">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="aacaa-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="aacaa-154">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aacaa-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="aacaa-155">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aacaa-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="aacaa-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="aacaa-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aacaa-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="aacaa-157">RELATED LINKS</span></span>

