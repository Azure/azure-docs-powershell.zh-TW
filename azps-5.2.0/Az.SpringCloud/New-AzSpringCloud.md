---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274784"
---
# <span data-ttu-id="f2a6b-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f2a6b-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="f2a6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a6b-103">建立新服務或更新現有服務。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="f2a6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2a6b-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2a6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a6b-106">建立新服務或更新現有服務。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="f2a6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a6b-108">範例1：建立彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="f2a6b-109">建立彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="f2a6b-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2a6b-111">-AsJob</span></span>
<span data-ttu-id="f2a6b-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f2a6b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f2a6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a6b-113">-DefaultProfile</span></span>
<span data-ttu-id="f2a6b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a6b-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="f2a6b-115">-GitPropertyUri</span></span>
<span data-ttu-id="f2a6b-116">儲存庫的 URI</span><span class="sxs-lookup"><span data-stu-id="f2a6b-116">URI of the repository</span></span>

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

### <span data-ttu-id="f2a6b-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f2a6b-117">-Location</span></span>
<span data-ttu-id="f2a6b-118">資源的地理位置。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="f2a6b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2a6b-119">-Name</span></span>
<span data-ttu-id="f2a6b-120">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f2a6b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2a6b-121">-NoWait</span></span>
<span data-ttu-id="f2a6b-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f2a6b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2a6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2a6b-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f2a6b-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f2a6b-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f2a6b-126">-SkuName</span></span>
<span data-ttu-id="f2a6b-127">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="f2a6b-127">Name of the Sku</span></span>

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

### <span data-ttu-id="f2a6b-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f2a6b-128">-SkuTier</span></span>
<span data-ttu-id="f2a6b-129">Sku 的層級</span><span class="sxs-lookup"><span data-stu-id="f2a6b-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="f2a6b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2a6b-130">-SubscriptionId</span></span>
<span data-ttu-id="f2a6b-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2a6b-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f2a6b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2a6b-133">-Tag</span></span>
<span data-ttu-id="f2a6b-134">服務的標記，是描述資源之鍵值對的清單。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="f2a6b-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f2a6b-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="f2a6b-136">目標應用程式洞察力工具金鑰</span><span class="sxs-lookup"><span data-stu-id="f2a6b-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="f2a6b-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="f2a6b-137">-TraceEnabled</span></span>
<span data-ttu-id="f2a6b-138">指出是否啟用追蹤功能</span><span class="sxs-lookup"><span data-stu-id="f2a6b-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="f2a6b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f2a6b-139">-Confirm</span></span>
<span data-ttu-id="f2a6b-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a6b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a6b-141">-WhatIf</span></span>
<span data-ttu-id="f2a6b-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a6b-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a6b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a6b-144">CommonParameters</span></span>
<span data-ttu-id="f2a6b-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a6b-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a6b-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f2a6b-147">INPUTS</span></span>

## <span data-ttu-id="f2a6b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f2a6b-148">OUTPUTS</span></span>

### <span data-ttu-id="f2a6b-149">IServiceResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="f2a6b-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f2a6b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f2a6b-150">NOTES</span></span>

<span data-ttu-id="f2a6b-151">別名</span><span class="sxs-lookup"><span data-stu-id="f2a6b-151">ALIASES</span></span>

## <span data-ttu-id="f2a6b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2a6b-152">RELATED LINKS</span></span>

