---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136670"
---
# <span data-ttu-id="47cf8-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="47cf8-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="47cf8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="47cf8-103">取得 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="47cf8-103">Get application insights resources</span></span>

## <span data-ttu-id="47cf8-104">句法</span><span class="sxs-lookup"><span data-stu-id="47cf8-104">SYNTAX</span></span>

### <span data-ttu-id="47cf8-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="47cf8-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47cf8-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47cf8-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47cf8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47cf8-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47cf8-108">說明</span><span class="sxs-lookup"><span data-stu-id="47cf8-108">DESCRIPTION</span></span>
<span data-ttu-id="47cf8-109">取得資源群組或特定資源中的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="47cf8-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="47cf8-110">示例</span><span class="sxs-lookup"><span data-stu-id="47cf8-110">EXAMPLES</span></span>

### <span data-ttu-id="47cf8-111">範例1取得 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="47cf8-111">Example 1 Get application insights resource</span></span>
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

<span data-ttu-id="47cf8-112">在資源群組 "testgroup" 中取得名為「test」的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="47cf8-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="47cf8-113">範例2取得含定價方案資訊的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="47cf8-113">Example 2 Get application insights resource with pricing plan information</span></span>
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

<span data-ttu-id="47cf8-114">取得 application insights 資源，並包含資源群組 "testgroup" 中名為「test」之資源的定價方案資訊</span><span class="sxs-lookup"><span data-stu-id="47cf8-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="47cf8-115">參數</span><span class="sxs-lookup"><span data-stu-id="47cf8-115">PARAMETERS</span></span>

### <span data-ttu-id="47cf8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cf8-116">-DefaultProfile</span></span>
<span data-ttu-id="47cf8-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47cf8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47cf8-118">-完整</span><span class="sxs-lookup"><span data-stu-id="47cf8-118">-Full</span></span>
<span data-ttu-id="47cf8-119">如果已指定，它將會傳回定價方案/每日 cap，以及 application insights 元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="47cf8-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="47cf8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="47cf8-120">-Name</span></span>
<span data-ttu-id="47cf8-121">Application Insights 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="47cf8-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="47cf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47cf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="47cf8-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="47cf8-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="47cf8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47cf8-124">-ResourceId</span></span>
<span data-ttu-id="47cf8-125">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="47cf8-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="47cf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cf8-126">CommonParameters</span></span>
<span data-ttu-id="47cf8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47cf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cf8-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47cf8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cf8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="47cf8-129">INPUTS</span></span>

### <span data-ttu-id="47cf8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="47cf8-130">System.String</span></span>

## <span data-ttu-id="47cf8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="47cf8-131">OUTPUTS</span></span>

### <span data-ttu-id="47cf8-132">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="47cf8-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="47cf8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="47cf8-133">NOTES</span></span>

## <span data-ttu-id="47cf8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="47cf8-134">RELATED LINKS</span></span>
