---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968152"
---
# <span data-ttu-id="1dba7-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="1dba7-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="1dba7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dba7-102">SYNOPSIS</span></span>
<span data-ttu-id="1dba7-103">傳回資源的要求健康情況資訊。</span><span class="sxs-lookup"><span data-stu-id="1dba7-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="1dba7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dba7-104">SYNTAX</span></span>

### <span data-ttu-id="1dba7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1dba7-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1dba7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1dba7-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1dba7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1dba7-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1dba7-108">說明</span><span class="sxs-lookup"><span data-stu-id="1dba7-108">DESCRIPTION</span></span>
<span data-ttu-id="1dba7-109">傳回資源的要求健康情況資訊。</span><span class="sxs-lookup"><span data-stu-id="1dba7-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="1dba7-110">示例</span><span class="sxs-lookup"><span data-stu-id="1dba7-110">EXAMPLES</span></span>

### <span data-ttu-id="1dba7-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="1dba7-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="1dba7-112">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="1dba7-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="1dba7-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="1dba7-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="1dba7-114">傳回 [for Microsoft Fabric.] 下的 [健康情況] 狀態。</span><span class="sxs-lookup"><span data-stu-id="1dba7-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="1dba7-115">參數</span><span class="sxs-lookup"><span data-stu-id="1dba7-115">PARAMETERS</span></span>

### <span data-ttu-id="1dba7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dba7-116">-DefaultProfile</span></span>
<span data-ttu-id="1dba7-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dba7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dba7-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="1dba7-118">-Filter</span></span>
<span data-ttu-id="1dba7-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1dba7-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="1dba7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dba7-120">-InputObject</span></span>
<span data-ttu-id="1dba7-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1dba7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1dba7-122">-位置</span><span class="sxs-lookup"><span data-stu-id="1dba7-122">-Location</span></span>
<span data-ttu-id="1dba7-123">地區名稱</span><span class="sxs-lookup"><span data-stu-id="1dba7-123">Name of the region</span></span>

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

### <span data-ttu-id="1dba7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dba7-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dba7-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dba7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dba7-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="1dba7-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="1dba7-127">[資源註冊識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1dba7-127">Resource registration ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1dba7-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="1dba7-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="1dba7-129">[服務註冊識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1dba7-129">Service registration ID.</span></span>

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

### <span data-ttu-id="1dba7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1dba7-130">-SubscriptionId</span></span>
<span data-ttu-id="1dba7-131">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1dba7-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1dba7-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1dba7-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1dba7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dba7-133">CommonParameters</span></span>
<span data-ttu-id="1dba7-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dba7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dba7-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1dba7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dba7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1dba7-136">INPUTS</span></span>

### <span data-ttu-id="1dba7-137">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="1dba7-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="1dba7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1dba7-138">OUTPUTS</span></span>

### <span data-ttu-id="1dba7-139">IResourceHealth （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="1dba7-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="1dba7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1dba7-140">NOTES</span></span>

<span data-ttu-id="1dba7-141">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1dba7-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1dba7-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1dba7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1dba7-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1dba7-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1dba7-144">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dba7-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="1dba7-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1dba7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1dba7-146">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="1dba7-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="1dba7-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dba7-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1dba7-148">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dba7-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="1dba7-149">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="1dba7-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="1dba7-150">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="1dba7-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="1dba7-151">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1dba7-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1dba7-152">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1dba7-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1dba7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dba7-153">RELATED LINKS</span></span>

