---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: 94311d2378e5b91fb09bdb6569fbd05010518292
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916701"
---
# <span data-ttu-id="bf190-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="bf190-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="bf190-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf190-102">SYNOPSIS</span></span>
<span data-ttu-id="bf190-103">建立新 App 或更新即將離開的 App。</span><span class="sxs-lookup"><span data-stu-id="bf190-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="bf190-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf190-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf190-105">描述</span><span class="sxs-lookup"><span data-stu-id="bf190-105">DESCRIPTION</span></span>
<span data-ttu-id="bf190-106">建立新 App 或更新即將離開的 App。</span><span class="sxs-lookup"><span data-stu-id="bf190-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="bf190-107">例子</span><span class="sxs-lookup"><span data-stu-id="bf190-107">EXAMPLES</span></span>

### <span data-ttu-id="bf190-108">範例 1：建立春意雲應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf190-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="bf190-109">建立春意雲應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf190-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="bf190-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf190-110">PARAMETERS</span></span>

### <span data-ttu-id="bf190-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="bf190-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="bf190-112">應用程式使用中部署的名稱</span><span class="sxs-lookup"><span data-stu-id="bf190-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="bf190-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf190-113">-AsJob</span></span>
<span data-ttu-id="bf190-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="bf190-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bf190-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf190-115">-DefaultProfile</span></span>
<span data-ttu-id="bf190-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf190-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf190-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="bf190-117">-Fqdn</span></span>
<span data-ttu-id="bf190-118">完整 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="bf190-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="bf190-119">-HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="bf190-119">-HttpsOnly</span></span>
<span data-ttu-id="bf190-120">指出是否僅允許 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="bf190-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="bf190-121">-位置</span><span class="sxs-lookup"><span data-stu-id="bf190-121">-Location</span></span>
<span data-ttu-id="bf190-122">應用程式的 GEO 位置，一定與它的父資源相同</span><span class="sxs-lookup"><span data-stu-id="bf190-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="bf190-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf190-123">-Name</span></span>
<span data-ttu-id="bf190-124">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf190-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf190-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf190-125">-NoWait</span></span>
<span data-ttu-id="bf190-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="bf190-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bf190-127">-PersistentMountPath</span><span class="sxs-lookup"><span data-stu-id="bf190-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="bf190-128">持續性磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="bf190-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="bf190-129">-Persistent以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="bf190-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="bf190-130">以 GB 為單位的永久磁片大小</span><span class="sxs-lookup"><span data-stu-id="bf190-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="bf190-131">-公用</span><span class="sxs-lookup"><span data-stu-id="bf190-131">-Public</span></span>
<span data-ttu-id="bf190-132">指出應用程式是否公開公用端點</span><span class="sxs-lookup"><span data-stu-id="bf190-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="bf190-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf190-133">-ResourceGroupName</span></span>
<span data-ttu-id="bf190-134">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bf190-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bf190-135">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="bf190-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf190-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bf190-136">-ServiceName</span></span>
<span data-ttu-id="bf190-137">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf190-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf190-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf190-138">-SubscriptionId</span></span>
<span data-ttu-id="bf190-139">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf190-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf190-140">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bf190-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf190-141">-TemporaryMountPath</span><span class="sxs-lookup"><span data-stu-id="bf190-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="bf190-142">暫用磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="bf190-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="bf190-143">-Temporary以SizeInGb</span><span class="sxs-lookup"><span data-stu-id="bf190-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="bf190-144">暫用磁片的大小 ，以 GB 為單位</span><span class="sxs-lookup"><span data-stu-id="bf190-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="bf190-145">-確認</span><span class="sxs-lookup"><span data-stu-id="bf190-145">-Confirm</span></span>
<span data-ttu-id="bf190-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bf190-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf190-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf190-147">-WhatIf</span></span>
<span data-ttu-id="bf190-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf190-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf190-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf190-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf190-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf190-150">CommonParameters</span></span>
<span data-ttu-id="bf190-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf190-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf190-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf190-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf190-153">輸入</span><span class="sxs-lookup"><span data-stu-id="bf190-153">INPUTS</span></span>

## <span data-ttu-id="bf190-154">輸出</span><span class="sxs-lookup"><span data-stu-id="bf190-154">OUTPUTS</span></span>

### <span data-ttu-id="bf190-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="bf190-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="bf190-156">筆記</span><span class="sxs-lookup"><span data-stu-id="bf190-156">NOTES</span></span>

<span data-ttu-id="bf190-157">別名</span><span class="sxs-lookup"><span data-stu-id="bf190-157">ALIASES</span></span>

## <span data-ttu-id="bf190-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf190-158">RELATED LINKS</span></span>

