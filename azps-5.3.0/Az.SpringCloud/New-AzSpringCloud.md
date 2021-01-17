---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439043"
---
# <span data-ttu-id="4a356-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="4a356-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="4a356-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a356-102">SYNOPSIS</span></span>
<span data-ttu-id="4a356-103">建立新服務或更新現有服務。</span><span class="sxs-lookup"><span data-stu-id="4a356-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="4a356-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a356-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a356-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a356-105">DESCRIPTION</span></span>
<span data-ttu-id="4a356-106">建立新服務或更新現有服務。</span><span class="sxs-lookup"><span data-stu-id="4a356-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="4a356-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a356-107">EXAMPLES</span></span>

### <span data-ttu-id="4a356-108">範例1：建立彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="4a356-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="4a356-109">建立彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="4a356-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="4a356-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a356-110">PARAMETERS</span></span>

### <span data-ttu-id="4a356-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a356-111">-AsJob</span></span>
<span data-ttu-id="4a356-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="4a356-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4a356-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a356-113">-DefaultProfile</span></span>
<span data-ttu-id="4a356-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a356-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a356-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="4a356-115">-GitPropertyUri</span></span>
<span data-ttu-id="4a356-116">儲存庫的 URI</span><span class="sxs-lookup"><span data-stu-id="4a356-116">URI of the repository</span></span>

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

### <span data-ttu-id="4a356-117">-位置</span><span class="sxs-lookup"><span data-stu-id="4a356-117">-Location</span></span>
<span data-ttu-id="4a356-118">資源的地理位置。</span><span class="sxs-lookup"><span data-stu-id="4a356-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="4a356-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a356-119">-Name</span></span>
<span data-ttu-id="4a356-120">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a356-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a356-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a356-121">-NoWait</span></span>
<span data-ttu-id="4a356-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="4a356-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a356-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a356-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a356-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a356-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4a356-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="4a356-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4a356-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4a356-126">-SkuName</span></span>
<span data-ttu-id="4a356-127">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="4a356-127">Name of the Sku</span></span>

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

### <span data-ttu-id="4a356-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4a356-128">-SkuTier</span></span>
<span data-ttu-id="4a356-129">Sku 的層級</span><span class="sxs-lookup"><span data-stu-id="4a356-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="4a356-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a356-130">-SubscriptionId</span></span>
<span data-ttu-id="4a356-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4a356-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a356-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4a356-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a356-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a356-133">-Tag</span></span>
<span data-ttu-id="4a356-134">服務的標記，是描述資源之鍵值對的清單。</span><span class="sxs-lookup"><span data-stu-id="4a356-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a356-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="4a356-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="4a356-136">目標應用程式洞察力工具金鑰</span><span class="sxs-lookup"><span data-stu-id="4a356-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="4a356-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="4a356-137">-TraceEnabled</span></span>
<span data-ttu-id="4a356-138">指出是否啟用追蹤功能</span><span class="sxs-lookup"><span data-stu-id="4a356-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="4a356-139">-確認</span><span class="sxs-lookup"><span data-stu-id="4a356-139">-Confirm</span></span>
<span data-ttu-id="4a356-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a356-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a356-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a356-141">-WhatIf</span></span>
<span data-ttu-id="4a356-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a356-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a356-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a356-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a356-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a356-144">CommonParameters</span></span>
<span data-ttu-id="4a356-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a356-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a356-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a356-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a356-147">輸入</span><span class="sxs-lookup"><span data-stu-id="4a356-147">INPUTS</span></span>

## <span data-ttu-id="4a356-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4a356-148">OUTPUTS</span></span>

### <span data-ttu-id="4a356-149">IServiceResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="4a356-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="4a356-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4a356-150">NOTES</span></span>

<span data-ttu-id="4a356-151">別名</span><span class="sxs-lookup"><span data-stu-id="4a356-151">ALIASES</span></span>

## <span data-ttu-id="4a356-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a356-152">RELATED LINKS</span></span>

