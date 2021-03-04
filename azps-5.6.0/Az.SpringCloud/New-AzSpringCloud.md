---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: a331e083075d7ed5fa3f148bc405226d85ddc960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916708"
---
# <span data-ttu-id="f2068-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f2068-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="f2068-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2068-102">SYNOPSIS</span></span>
<span data-ttu-id="f2068-103">建立新服務或更新離開的服務。</span><span class="sxs-lookup"><span data-stu-id="f2068-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="f2068-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2068-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2068-105">描述</span><span class="sxs-lookup"><span data-stu-id="f2068-105">DESCRIPTION</span></span>
<span data-ttu-id="f2068-106">建立新服務或更新離開的服務。</span><span class="sxs-lookup"><span data-stu-id="f2068-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="f2068-107">例子</span><span class="sxs-lookup"><span data-stu-id="f2068-107">EXAMPLES</span></span>

### <span data-ttu-id="f2068-108">範例 1：建立春意雲服務。</span><span class="sxs-lookup"><span data-stu-id="f2068-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="f2068-109">建立春假雲端服務。</span><span class="sxs-lookup"><span data-stu-id="f2068-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="f2068-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2068-110">PARAMETERS</span></span>

### <span data-ttu-id="f2068-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2068-111">-AsJob</span></span>
<span data-ttu-id="f2068-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="f2068-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f2068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2068-113">-DefaultProfile</span></span>
<span data-ttu-id="f2068-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2068-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2068-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="f2068-115">-GitPropertyUri</span></span>
<span data-ttu-id="f2068-116">存放庫的 URI</span><span class="sxs-lookup"><span data-stu-id="f2068-116">URI of the repository</span></span>

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

### <span data-ttu-id="f2068-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f2068-117">-Location</span></span>
<span data-ttu-id="f2068-118">資源的 GEO 位置。</span><span class="sxs-lookup"><span data-stu-id="f2068-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="f2068-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2068-119">-Name</span></span>
<span data-ttu-id="f2068-120">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2068-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f2068-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2068-121">-NoWait</span></span>
<span data-ttu-id="f2068-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="f2068-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2068-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2068-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2068-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2068-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f2068-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f2068-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f2068-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="f2068-126">-SkuName</span></span>
<span data-ttu-id="f2068-127">SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="f2068-127">Name of the Sku</span></span>

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

### <span data-ttu-id="f2068-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f2068-128">-SkuTier</span></span>
<span data-ttu-id="f2068-129">SKU 層級</span><span class="sxs-lookup"><span data-stu-id="f2068-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="f2068-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2068-130">-SubscriptionId</span></span>
<span data-ttu-id="f2068-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2068-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2068-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2068-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f2068-133">-標記</span><span class="sxs-lookup"><span data-stu-id="f2068-133">-Tag</span></span>
<span data-ttu-id="f2068-134">服務標記，這是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="f2068-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="f2068-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f2068-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="f2068-136">目標應用程式深入資訊便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f2068-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="f2068-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="f2068-137">-TraceEnabled</span></span>
<span data-ttu-id="f2068-138">指出是否啟用追蹤功能</span><span class="sxs-lookup"><span data-stu-id="f2068-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="f2068-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f2068-139">-Confirm</span></span>
<span data-ttu-id="f2068-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f2068-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2068-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2068-141">-WhatIf</span></span>
<span data-ttu-id="f2068-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2068-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2068-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2068-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2068-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2068-144">CommonParameters</span></span>
<span data-ttu-id="f2068-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2068-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2068-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2068-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2068-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f2068-147">INPUTS</span></span>

## <span data-ttu-id="f2068-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f2068-148">OUTPUTS</span></span>

### <span data-ttu-id="f2068-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="f2068-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f2068-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f2068-150">NOTES</span></span>

<span data-ttu-id="f2068-151">別名</span><span class="sxs-lookup"><span data-stu-id="f2068-151">ALIASES</span></span>

## <span data-ttu-id="f2068-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2068-152">RELATED LINKS</span></span>

