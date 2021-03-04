---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 9a57b38f77d299a69cbb1f38b006d616b9c9b825
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909265"
---
# <span data-ttu-id="a987b-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a987b-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="a987b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a987b-102">SYNOPSIS</span></span>
<span data-ttu-id="a987b-103">在指定的環境中建立或更新存取策略。</span><span class="sxs-lookup"><span data-stu-id="a987b-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="a987b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a987b-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a987b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a987b-105">DESCRIPTION</span></span>
<span data-ttu-id="a987b-106">在指定的環境中建立或更新存取策略。</span><span class="sxs-lookup"><span data-stu-id="a987b-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="a987b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a987b-107">EXAMPLES</span></span>

### <span data-ttu-id="a987b-108">範例 1：為指定的環境建立存取策略</span><span class="sxs-lookup"><span data-stu-id="a987b-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a987b-109">此命令會為指定的環境建立存取策略。</span><span class="sxs-lookup"><span data-stu-id="a987b-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="a987b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a987b-110">PARAMETERS</span></span>

### <span data-ttu-id="a987b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a987b-111">-DefaultProfile</span></span>
<span data-ttu-id="a987b-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a987b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a987b-113">-描述</span><span class="sxs-lookup"><span data-stu-id="a987b-113">-Description</span></span>
<span data-ttu-id="a987b-114">存取策略的描述。</span><span class="sxs-lookup"><span data-stu-id="a987b-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="a987b-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a987b-115">-EnvironmentName</span></span>
<span data-ttu-id="a987b-116">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="a987b-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a987b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a987b-117">-Name</span></span>
<span data-ttu-id="a987b-118">存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="a987b-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987b-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="a987b-119">-PrincipalObjectId</span></span>
<span data-ttu-id="a987b-120">Azure Active Directory 中主體的物件Id。</span><span class="sxs-lookup"><span data-stu-id="a987b-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="a987b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a987b-121">-ResourceGroupName</span></span>
<span data-ttu-id="a987b-122">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a987b-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a987b-123">-角色</span><span class="sxs-lookup"><span data-stu-id="a987b-123">-Role</span></span>
<span data-ttu-id="a987b-124">主體在環境中指派的角色清單。</span><span class="sxs-lookup"><span data-stu-id="a987b-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a987b-125">-SubscriptionId</span></span>
<span data-ttu-id="a987b-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a987b-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a987b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a987b-127">-Confirm</span></span>
<span data-ttu-id="a987b-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a987b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a987b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a987b-129">-WhatIf</span></span>
<span data-ttu-id="a987b-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a987b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a987b-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a987b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a987b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a987b-132">CommonParameters</span></span>
<span data-ttu-id="a987b-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a987b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a987b-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a987b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a987b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a987b-135">INPUTS</span></span>

## <span data-ttu-id="a987b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a987b-136">OUTPUTS</span></span>

### <span data-ttu-id="a987b-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="a987b-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="a987b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a987b-138">NOTES</span></span>

<span data-ttu-id="a987b-139">別名</span><span class="sxs-lookup"><span data-stu-id="a987b-139">ALIASES</span></span>

## <span data-ttu-id="a987b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a987b-140">RELATED LINKS</span></span>

