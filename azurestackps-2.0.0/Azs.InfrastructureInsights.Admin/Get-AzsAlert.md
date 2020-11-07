---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796421"
---
# <span data-ttu-id="eac91-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="eac91-101">Get-AzsAlert</span></span>

## <span data-ttu-id="eac91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eac91-102">SYNOPSIS</span></span>
<span data-ttu-id="eac91-103">傳回要求的警示。</span><span class="sxs-lookup"><span data-stu-id="eac91-103">Returns the requested alert.</span></span>

## <span data-ttu-id="eac91-104">句法</span><span class="sxs-lookup"><span data-stu-id="eac91-104">SYNTAX</span></span>

### <span data-ttu-id="eac91-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="eac91-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eac91-106">獲取</span><span class="sxs-lookup"><span data-stu-id="eac91-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eac91-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eac91-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eac91-108">說明</span><span class="sxs-lookup"><span data-stu-id="eac91-108">DESCRIPTION</span></span>
<span data-ttu-id="eac91-109">傳回要求的警示。</span><span class="sxs-lookup"><span data-stu-id="eac91-109">Returns the requested alert.</span></span>

## <span data-ttu-id="eac91-110">示例</span><span class="sxs-lookup"><span data-stu-id="eac91-110">EXAMPLES</span></span>

### <span data-ttu-id="eac91-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="eac91-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="eac91-112">透過名稱取得警示。</span><span class="sxs-lookup"><span data-stu-id="eac91-112">Get an alert by Name.</span></span>

### <span data-ttu-id="eac91-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="eac91-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="eac91-114">取得所有的活動警示，並顯示其錯誤和標題。</span><span class="sxs-lookup"><span data-stu-id="eac91-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="eac91-115">參數</span><span class="sxs-lookup"><span data-stu-id="eac91-115">PARAMETERS</span></span>

### <span data-ttu-id="eac91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac91-116">-DefaultProfile</span></span>
<span data-ttu-id="eac91-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eac91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eac91-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="eac91-118">-Filter</span></span>
<span data-ttu-id="eac91-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="eac91-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eac91-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eac91-120">-InputObject</span></span>
<span data-ttu-id="eac91-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eac91-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eac91-122">-位置</span><span class="sxs-lookup"><span data-stu-id="eac91-122">-Location</span></span>
<span data-ttu-id="eac91-123">地區名稱</span><span class="sxs-lookup"><span data-stu-id="eac91-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eac91-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="eac91-124">-Name</span></span>
<span data-ttu-id="eac91-125">提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="eac91-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eac91-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac91-126">-ResourceGroupName</span></span>
<span data-ttu-id="eac91-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eac91-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eac91-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eac91-128">-SubscriptionId</span></span>
<span data-ttu-id="eac91-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="eac91-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eac91-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eac91-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eac91-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac91-131">CommonParameters</span></span>
<span data-ttu-id="eac91-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eac91-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac91-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eac91-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac91-134">輸入</span><span class="sxs-lookup"><span data-stu-id="eac91-134">INPUTS</span></span>

### <span data-ttu-id="eac91-135">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="eac91-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="eac91-136">輸出</span><span class="sxs-lookup"><span data-stu-id="eac91-136">OUTPUTS</span></span>

### <span data-ttu-id="eac91-137">IAlert （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="eac91-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="eac91-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eac91-138">NOTES</span></span>

<span data-ttu-id="eac91-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="eac91-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eac91-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eac91-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eac91-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="eac91-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eac91-142">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="eac91-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="eac91-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="eac91-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eac91-144">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="eac91-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="eac91-145">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eac91-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="eac91-146">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="eac91-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="eac91-147">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="eac91-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="eac91-148">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="eac91-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="eac91-149">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="eac91-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eac91-150">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eac91-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eac91-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="eac91-151">RELATED LINKS</span></span>

