---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130326"
---
# <span data-ttu-id="18758-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18758-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="18758-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18758-102">SYNOPSIS</span></span>
<span data-ttu-id="18758-103">在指定的環境中取得具有指定名稱的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="18758-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="18758-104">句法</span><span class="sxs-lookup"><span data-stu-id="18758-104">SYNTAX</span></span>

### <span data-ttu-id="18758-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="18758-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18758-106">獲取</span><span class="sxs-lookup"><span data-stu-id="18758-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18758-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18758-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="18758-108">說明</span><span class="sxs-lookup"><span data-stu-id="18758-108">DESCRIPTION</span></span>
<span data-ttu-id="18758-109">在指定的環境中取得具有指定名稱的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="18758-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="18758-110">示例</span><span class="sxs-lookup"><span data-stu-id="18758-110">EXAMPLES</span></span>

### <span data-ttu-id="18758-111">範例1：列出指定環境下的所有存取原則</span><span class="sxs-lookup"><span data-stu-id="18758-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="18758-112">這個命令會列出指定環境下的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="18758-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="18758-113">範例2：依名稱取得指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="18758-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="18758-114">這個命令會取得指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="18758-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="18758-115">範例3：依物件取得指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="18758-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="18758-116">這個命令會取得指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="18758-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="18758-117">參數</span><span class="sxs-lookup"><span data-stu-id="18758-117">PARAMETERS</span></span>

### <span data-ttu-id="18758-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18758-118">-DefaultProfile</span></span>
<span data-ttu-id="18758-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18758-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18758-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="18758-120">-EnvironmentName</span></span>
<span data-ttu-id="18758-121">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="18758-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18758-122">-InputObject</span></span>
<span data-ttu-id="18758-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="18758-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18758-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="18758-124">-Name</span></span>
<span data-ttu-id="18758-125">與指定環境相關聯之時間序列 Insights 存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18758-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18758-126">-ResourceGroupName</span></span>
<span data-ttu-id="18758-127">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="18758-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18758-128">-SubscriptionId</span></span>
<span data-ttu-id="18758-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="18758-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="18758-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18758-130">CommonParameters</span></span>
<span data-ttu-id="18758-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18758-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18758-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18758-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18758-133">輸入</span><span class="sxs-lookup"><span data-stu-id="18758-133">INPUTS</span></span>

### <span data-ttu-id="18758-134">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="18758-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="18758-135">輸出</span><span class="sxs-lookup"><span data-stu-id="18758-135">OUTPUTS</span></span>

### <span data-ttu-id="18758-136">IAccessPolicyResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="18758-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="18758-137">筆記</span><span class="sxs-lookup"><span data-stu-id="18758-137">NOTES</span></span>

<span data-ttu-id="18758-138">別名</span><span class="sxs-lookup"><span data-stu-id="18758-138">ALIASES</span></span>

<span data-ttu-id="18758-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="18758-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18758-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="18758-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18758-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="18758-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18758-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="18758-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18758-143">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="18758-144">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="18758-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="18758-145">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="18758-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="18758-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18758-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="18758-148">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18758-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="18758-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="18758-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="18758-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="18758-150">RELATED LINKS</span></span>

