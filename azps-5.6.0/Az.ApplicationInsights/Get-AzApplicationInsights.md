---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: f208722a065399c12facce6907bbcad3b64d46e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905241"
---
# <span data-ttu-id="cd47d-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cd47d-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="cd47d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd47d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd47d-103">取得應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="cd47d-103">Get application insights resources</span></span>

## <span data-ttu-id="cd47d-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd47d-104">SYNTAX</span></span>

### <span data-ttu-id="cd47d-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cd47d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd47d-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd47d-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd47d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd47d-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd47d-108">描述</span><span class="sxs-lookup"><span data-stu-id="cd47d-108">DESCRIPTION</span></span>
<span data-ttu-id="cd47d-109">取得資源群組或特定資源中的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="cd47d-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="cd47d-110">例子</span><span class="sxs-lookup"><span data-stu-id="cd47d-110">EXAMPLES</span></span>

### <span data-ttu-id="cd47d-111">範例 1 取得應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="cd47d-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="cd47d-112">在資源群組「測試群組」中取得名為「測試」的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="cd47d-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="cd47d-113">範例 2 使用定價計畫資訊取得應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="cd47d-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="cd47d-114">取得應用程式深入資訊資源，並包含資源群組「測試群組」中名為「測試」之資源的定價計畫資訊</span><span class="sxs-lookup"><span data-stu-id="cd47d-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="cd47d-115">參數</span><span class="sxs-lookup"><span data-stu-id="cd47d-115">PARAMETERS</span></span>

### <span data-ttu-id="cd47d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd47d-116">-DefaultProfile</span></span>
<span data-ttu-id="cd47d-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd47d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd47d-118">-完整</span><span class="sxs-lookup"><span data-stu-id="cd47d-118">-Full</span></span>
<span data-ttu-id="cd47d-119">如果指定，它會取得應用程式深入資訊元件的價格方案/每日上限和狀態。</span><span class="sxs-lookup"><span data-stu-id="cd47d-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd47d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd47d-120">-Name</span></span>
<span data-ttu-id="cd47d-121">應用程式深入資訊資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cd47d-121">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd47d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd47d-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd47d-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cd47d-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd47d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd47d-124">-ResourceId</span></span>
<span data-ttu-id="cd47d-125">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd47d-125">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd47d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd47d-126">CommonParameters</span></span>
<span data-ttu-id="cd47d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd47d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd47d-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd47d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd47d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cd47d-129">INPUTS</span></span>

### <span data-ttu-id="cd47d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cd47d-130">System.String</span></span>

## <span data-ttu-id="cd47d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cd47d-131">OUTPUTS</span></span>

### <span data-ttu-id="cd47d-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cd47d-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="cd47d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cd47d-133">NOTES</span></span>

## <span data-ttu-id="cd47d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd47d-134">RELATED LINKS</span></span>
