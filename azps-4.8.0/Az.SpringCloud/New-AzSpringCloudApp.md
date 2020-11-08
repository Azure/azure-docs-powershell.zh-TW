---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: 966a0c0243d8ca8cd982420a9a3018f9d41ab52e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129874"
---
# <span data-ttu-id="35229-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="35229-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="35229-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35229-102">SYNOPSIS</span></span>
<span data-ttu-id="35229-103">建立新的 App 或更新現有的 App。</span><span class="sxs-lookup"><span data-stu-id="35229-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="35229-104">句法</span><span class="sxs-lookup"><span data-stu-id="35229-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35229-105">說明</span><span class="sxs-lookup"><span data-stu-id="35229-105">DESCRIPTION</span></span>
<span data-ttu-id="35229-106">建立新的 App 或更新現有的 App。</span><span class="sxs-lookup"><span data-stu-id="35229-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="35229-107">示例</span><span class="sxs-lookup"><span data-stu-id="35229-107">EXAMPLES</span></span>

### <span data-ttu-id="35229-108">範例1：建立彈簧雲端 app。</span><span class="sxs-lookup"><span data-stu-id="35229-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="35229-109">建立彈簧雲端 app。</span><span class="sxs-lookup"><span data-stu-id="35229-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="35229-110">參數</span><span class="sxs-lookup"><span data-stu-id="35229-110">PARAMETERS</span></span>

### <span data-ttu-id="35229-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="35229-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="35229-112">App 作用中部署的名稱</span><span class="sxs-lookup"><span data-stu-id="35229-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="35229-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35229-113">-AsJob</span></span>
<span data-ttu-id="35229-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="35229-114">Run the command as a job</span></span>

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

### <span data-ttu-id="35229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35229-115">-DefaultProfile</span></span>
<span data-ttu-id="35229-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35229-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35229-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="35229-117">-Fqdn</span></span>
<span data-ttu-id="35229-118">完全合格的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="35229-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="35229-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="35229-119">-HttpsOnly</span></span>
<span data-ttu-id="35229-120">指出是否允許只有 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="35229-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="35229-121">-位置</span><span class="sxs-lookup"><span data-stu-id="35229-121">-Location</span></span>
<span data-ttu-id="35229-122">應用程式的地理位置，與其父項資源永遠相同</span><span class="sxs-lookup"><span data-stu-id="35229-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="35229-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="35229-123">-Name</span></span>
<span data-ttu-id="35229-124">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="35229-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="35229-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="35229-125">-NoWait</span></span>
<span data-ttu-id="35229-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="35229-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35229-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="35229-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="35229-128">持久性磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="35229-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="35229-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="35229-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="35229-130">持久性磁片大小（GB）</span><span class="sxs-lookup"><span data-stu-id="35229-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="35229-131">-公開</span><span class="sxs-lookup"><span data-stu-id="35229-131">-Public</span></span>
<span data-ttu-id="35229-132">指出 App 是否公開公用端點</span><span class="sxs-lookup"><span data-stu-id="35229-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="35229-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35229-133">-ResourceGroupName</span></span>
<span data-ttu-id="35229-134">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35229-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="35229-135">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="35229-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="35229-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="35229-136">-ServiceName</span></span>
<span data-ttu-id="35229-137">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="35229-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="35229-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35229-138">-SubscriptionId</span></span>
<span data-ttu-id="35229-139">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="35229-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="35229-140">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="35229-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35229-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="35229-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="35229-142">臨時磁片的安裝路徑</span><span class="sxs-lookup"><span data-stu-id="35229-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="35229-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="35229-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="35229-144">暫時磁片大小（GB）</span><span class="sxs-lookup"><span data-stu-id="35229-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="35229-145">-確認</span><span class="sxs-lookup"><span data-stu-id="35229-145">-Confirm</span></span>
<span data-ttu-id="35229-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35229-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35229-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35229-147">-WhatIf</span></span>
<span data-ttu-id="35229-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35229-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35229-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35229-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35229-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35229-150">CommonParameters</span></span>
<span data-ttu-id="35229-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35229-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35229-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="35229-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35229-153">輸入</span><span class="sxs-lookup"><span data-stu-id="35229-153">INPUTS</span></span>

## <span data-ttu-id="35229-154">輸出</span><span class="sxs-lookup"><span data-stu-id="35229-154">OUTPUTS</span></span>

### <span data-ttu-id="35229-155">IAppResource （SpringCloud）。 Api20190501Preview。</span><span class="sxs-lookup"><span data-stu-id="35229-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="35229-156">筆記</span><span class="sxs-lookup"><span data-stu-id="35229-156">NOTES</span></span>

<span data-ttu-id="35229-157">別名</span><span class="sxs-lookup"><span data-stu-id="35229-157">ALIASES</span></span>

## <span data-ttu-id="35229-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="35229-158">RELATED LINKS</span></span>

