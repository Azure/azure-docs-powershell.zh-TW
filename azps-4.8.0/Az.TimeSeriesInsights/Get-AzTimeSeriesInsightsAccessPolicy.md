---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970781"
---
# <span data-ttu-id="8ff96-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ff96-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="8ff96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ff96-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff96-103">在指定的環境中取得具有指定名稱的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="8ff96-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8ff96-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ff96-104">SYNTAX</span></span>

### <span data-ttu-id="8ff96-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8ff96-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ff96-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8ff96-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ff96-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ff96-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff96-108">說明</span><span class="sxs-lookup"><span data-stu-id="8ff96-108">DESCRIPTION</span></span>
<span data-ttu-id="8ff96-109">在指定的環境中取得具有指定名稱的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="8ff96-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8ff96-110">示例</span><span class="sxs-lookup"><span data-stu-id="8ff96-110">EXAMPLES</span></span>

### <span data-ttu-id="8ff96-111">範例1：列出指定環境下的所有存取原則</span><span class="sxs-lookup"><span data-stu-id="8ff96-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="8ff96-112">這個命令會列出指定環境下的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ff96-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="8ff96-113">範例2：依名稱取得指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="8ff96-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="8ff96-114">這個命令會取得指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ff96-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="8ff96-115">範例3：依物件取得指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="8ff96-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="8ff96-116">這個命令會取得指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ff96-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="8ff96-117">參數</span><span class="sxs-lookup"><span data-stu-id="8ff96-117">PARAMETERS</span></span>

### <span data-ttu-id="8ff96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff96-118">-DefaultProfile</span></span>
<span data-ttu-id="8ff96-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff96-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8ff96-120">-EnvironmentName</span></span>
<span data-ttu-id="8ff96-121">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="8ff96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ff96-122">-InputObject</span></span>
<span data-ttu-id="8ff96-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8ff96-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ff96-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ff96-124">-Name</span></span>
<span data-ttu-id="8ff96-125">與指定環境相關聯之時間序列 Insights 存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="8ff96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff96-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ff96-127">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8ff96-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ff96-128">-SubscriptionId</span></span>
<span data-ttu-id="8ff96-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8ff96-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8ff96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff96-130">CommonParameters</span></span>
<span data-ttu-id="8ff96-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ff96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff96-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ff96-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff96-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8ff96-133">INPUTS</span></span>

### <span data-ttu-id="8ff96-134">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="8ff96-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="8ff96-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8ff96-135">OUTPUTS</span></span>

### <span data-ttu-id="8ff96-136">IAccessPolicyResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="8ff96-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="8ff96-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8ff96-137">NOTES</span></span>

<span data-ttu-id="8ff96-138">別名</span><span class="sxs-lookup"><span data-stu-id="8ff96-138">ALIASES</span></span>

<span data-ttu-id="8ff96-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8ff96-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ff96-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8ff96-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ff96-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8ff96-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ff96-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8ff96-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ff96-143">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="8ff96-144">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="8ff96-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="8ff96-145">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="8ff96-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8ff96-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ff96-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="8ff96-148">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff96-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="8ff96-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8ff96-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8ff96-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ff96-150">RELATED LINKS</span></span>

