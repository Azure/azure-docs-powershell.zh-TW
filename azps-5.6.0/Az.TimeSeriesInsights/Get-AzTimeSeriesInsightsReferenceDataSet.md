---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1fef5f018791fba9369ce7ab18a4b0c3a2440cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901629"
---
# <span data-ttu-id="f6e5b-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="f6e5b-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="f6e5b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e5b-103">在指定的環境中，使用指定名稱來獲取參照資料集。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f6e5b-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6e5b-104">SYNTAX</span></span>

### <span data-ttu-id="f6e5b-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="f6e5b-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6e5b-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f6e5b-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6e5b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6e5b-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f6e5b-108">描述</span><span class="sxs-lookup"><span data-stu-id="f6e5b-108">DESCRIPTION</span></span>
<span data-ttu-id="f6e5b-109">在指定的環境中，使用指定的名稱來獲取參照資料集。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f6e5b-110">例子</span><span class="sxs-lookup"><span data-stu-id="f6e5b-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e5b-111">範例 1：列出指定環境中的所有參照資料集</span><span class="sxs-lookup"><span data-stu-id="f6e5b-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="f6e5b-112">此命令會列出指定環境下的所有參照資料集。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="f6e5b-113">範例 2：根據名稱取得指定的參照資料集</span><span class="sxs-lookup"><span data-stu-id="f6e5b-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="f6e5b-114">此命令會獲得指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="f6e5b-115">範例 3：根據物件取得指定的參照資料集</span><span class="sxs-lookup"><span data-stu-id="f6e5b-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="f6e5b-116">此命令會獲得指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="f6e5b-117">參數</span><span class="sxs-lookup"><span data-stu-id="f6e5b-117">PARAMETERS</span></span>

### <span data-ttu-id="f6e5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e5b-118">-DefaultProfile</span></span>
<span data-ttu-id="f6e5b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e5b-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f6e5b-120">-EnvironmentName</span></span>
<span data-ttu-id="f6e5b-121">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f6e5b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6e5b-122">-InputObject</span></span>
<span data-ttu-id="f6e5b-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6e5b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6e5b-124">-Name</span></span>
<span data-ttu-id="f6e5b-125">時間序列深入資訊參照資料集的名稱與指定環境相關聯。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="f6e5b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e5b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6e5b-127">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f6e5b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6e5b-128">-SubscriptionId</span></span>
<span data-ttu-id="f6e5b-129">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f6e5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e5b-130">CommonParameters</span></span>
<span data-ttu-id="f6e5b-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e5b-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6e5b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e5b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f6e5b-133">INPUTS</span></span>

### <span data-ttu-id="f6e5b-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f6e5b-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f6e5b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f6e5b-135">OUTPUTS</span></span>

### <span data-ttu-id="f6e5b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="f6e5b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="f6e5b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f6e5b-137">NOTES</span></span>

<span data-ttu-id="f6e5b-138">別名</span><span class="sxs-lookup"><span data-stu-id="f6e5b-138">ALIASES</span></span>

<span data-ttu-id="f6e5b-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f6e5b-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6e5b-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6e5b-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6e5b-142">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6e5b-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6e5b-143">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f6e5b-144">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="f6e5b-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f6e5b-145">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f6e5b-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6e5b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6e5b-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f6e5b-148">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f6e5b-149">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6e5b-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f6e5b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6e5b-150">RELATED LINKS</span></span>

