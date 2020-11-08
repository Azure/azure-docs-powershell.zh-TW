---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140726"
---
# <span data-ttu-id="55d2c-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55d2c-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="55d2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="55d2c-103">在指定的環境中建立或更新訪問原則。</span><span class="sxs-lookup"><span data-stu-id="55d2c-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="55d2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="55d2c-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55d2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="55d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="55d2c-106">在指定的環境中建立或更新訪問原則。</span><span class="sxs-lookup"><span data-stu-id="55d2c-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="55d2c-107">示例</span><span class="sxs-lookup"><span data-stu-id="55d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="55d2c-108">範例1：建立指定環境的存取原則</span><span class="sxs-lookup"><span data-stu-id="55d2c-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="55d2c-109">這個命令會建立指定環境的存取原則。</span><span class="sxs-lookup"><span data-stu-id="55d2c-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="55d2c-110">參數</span><span class="sxs-lookup"><span data-stu-id="55d2c-110">PARAMETERS</span></span>

### <span data-ttu-id="55d2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d2c-111">-DefaultProfile</span></span>
<span data-ttu-id="55d2c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55d2c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55d2c-113">-描述</span><span class="sxs-lookup"><span data-stu-id="55d2c-113">-Description</span></span>
<span data-ttu-id="55d2c-114">存取原則的描述。</span><span class="sxs-lookup"><span data-stu-id="55d2c-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="55d2c-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="55d2c-115">-EnvironmentName</span></span>
<span data-ttu-id="55d2c-116">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="55d2c-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="55d2c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="55d2c-117">-Name</span></span>
<span data-ttu-id="55d2c-118">存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="55d2c-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="55d2c-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="55d2c-119">-PrincipalObjectId</span></span>
<span data-ttu-id="55d2c-120">Azure Active Directory 中主體的 objectId。</span><span class="sxs-lookup"><span data-stu-id="55d2c-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="55d2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="55d2c-122">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55d2c-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="55d2c-123">-角色</span><span class="sxs-lookup"><span data-stu-id="55d2c-123">-Role</span></span>
<span data-ttu-id="55d2c-124">在環境中指派主體的角色清單。</span><span class="sxs-lookup"><span data-stu-id="55d2c-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="55d2c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55d2c-125">-SubscriptionId</span></span>
<span data-ttu-id="55d2c-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="55d2c-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="55d2c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="55d2c-127">-Confirm</span></span>
<span data-ttu-id="55d2c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55d2c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d2c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d2c-129">-WhatIf</span></span>
<span data-ttu-id="55d2c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55d2c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55d2c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55d2c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d2c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d2c-132">CommonParameters</span></span>
<span data-ttu-id="55d2c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55d2c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d2c-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55d2c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d2c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="55d2c-135">INPUTS</span></span>

## <span data-ttu-id="55d2c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="55d2c-136">OUTPUTS</span></span>

### <span data-ttu-id="55d2c-137">IAccessPolicyResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="55d2c-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="55d2c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="55d2c-138">NOTES</span></span>

<span data-ttu-id="55d2c-139">別名</span><span class="sxs-lookup"><span data-stu-id="55d2c-139">ALIASES</span></span>

## <span data-ttu-id="55d2c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="55d2c-140">RELATED LINKS</span></span>
