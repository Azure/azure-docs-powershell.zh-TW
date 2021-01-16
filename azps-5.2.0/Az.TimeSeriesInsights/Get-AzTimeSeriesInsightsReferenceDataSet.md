---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277791"
---
# <span data-ttu-id="8a003-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="8a003-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="8a003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a003-102">SYNOPSIS</span></span>
<span data-ttu-id="8a003-103">在指定的環境中，以指定的名稱取得參考資料集。</span><span class="sxs-lookup"><span data-stu-id="8a003-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8a003-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a003-104">SYNTAX</span></span>

### <span data-ttu-id="8a003-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8a003-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a003-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8a003-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a003-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a003-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a003-108">說明</span><span class="sxs-lookup"><span data-stu-id="8a003-108">DESCRIPTION</span></span>
<span data-ttu-id="8a003-109">在指定的環境中，以指定的名稱取得參考資料集。</span><span class="sxs-lookup"><span data-stu-id="8a003-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8a003-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a003-110">EXAMPLES</span></span>

### <span data-ttu-id="8a003-111">範例1：列出指定環境下的所有參照資料集</span><span class="sxs-lookup"><span data-stu-id="8a003-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a003-112">這個命令會列出指定環境下的所有參照資料集。</span><span class="sxs-lookup"><span data-stu-id="8a003-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="8a003-113">範例2：取得依名稱設定的指定參照資料</span><span class="sxs-lookup"><span data-stu-id="8a003-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a003-114">這個命令會取得指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="8a003-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="8a003-115">範例3：取得依物件設定的指定參照資料</span><span class="sxs-lookup"><span data-stu-id="8a003-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a003-116">這個命令會取得指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="8a003-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="8a003-117">參數</span><span class="sxs-lookup"><span data-stu-id="8a003-117">PARAMETERS</span></span>

### <span data-ttu-id="8a003-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a003-118">-DefaultProfile</span></span>
<span data-ttu-id="8a003-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a003-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a003-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8a003-120">-EnvironmentName</span></span>
<span data-ttu-id="8a003-121">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="8a003-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a003-122">-InputObject</span></span>
<span data-ttu-id="8a003-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8a003-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a003-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a003-124">-Name</span></span>
<span data-ttu-id="8a003-125">與指定環境關聯的時間序列 Insights 參考資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a003-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a003-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a003-127">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8a003-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a003-128">-SubscriptionId</span></span>
<span data-ttu-id="8a003-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8a003-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8a003-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a003-130">CommonParameters</span></span>
<span data-ttu-id="8a003-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a003-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a003-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a003-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a003-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8a003-133">INPUTS</span></span>

### <span data-ttu-id="8a003-134">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="8a003-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="8a003-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8a003-135">OUTPUTS</span></span>

### <span data-ttu-id="8a003-136">IReferenceDataSetResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="8a003-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="8a003-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8a003-137">NOTES</span></span>

<span data-ttu-id="8a003-138">別名</span><span class="sxs-lookup"><span data-stu-id="8a003-138">ALIASES</span></span>

<span data-ttu-id="8a003-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8a003-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a003-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8a003-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a003-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8a003-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a003-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8a003-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a003-143">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="8a003-144">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="8a003-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="8a003-145">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="8a003-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8a003-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a003-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="8a003-148">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a003-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="8a003-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8a003-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8a003-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a003-150">RELATED LINKS</span></span>

