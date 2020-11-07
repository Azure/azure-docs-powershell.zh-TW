---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966734"
---
# <span data-ttu-id="d804c-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="d804c-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="d804c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d804c-102">SYNOPSIS</span></span>
<span data-ttu-id="d804c-103">傳回區域的要求健康情況。</span><span class="sxs-lookup"><span data-stu-id="d804c-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="d804c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d804c-104">SYNTAX</span></span>

### <span data-ttu-id="d804c-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="d804c-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d804c-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d804c-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d804c-107">清單</span><span class="sxs-lookup"><span data-stu-id="d804c-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d804c-108">說明</span><span class="sxs-lookup"><span data-stu-id="d804c-108">DESCRIPTION</span></span>
<span data-ttu-id="d804c-109">傳回區域的要求健康情況。</span><span class="sxs-lookup"><span data-stu-id="d804c-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="d804c-110">示例</span><span class="sxs-lookup"><span data-stu-id="d804c-110">EXAMPLES</span></span>

### <span data-ttu-id="d804c-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="d804c-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="d804c-112">傳回區域健康狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="d804c-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="d804c-113">參數</span><span class="sxs-lookup"><span data-stu-id="d804c-113">PARAMETERS</span></span>

### <span data-ttu-id="d804c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d804c-114">-DefaultProfile</span></span>
<span data-ttu-id="d804c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d804c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d804c-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="d804c-116">-Filter</span></span>
<span data-ttu-id="d804c-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="d804c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="d804c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d804c-118">-InputObject</span></span>
<span data-ttu-id="d804c-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d804c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d804c-120">-位置</span><span class="sxs-lookup"><span data-stu-id="d804c-120">-Location</span></span>
<span data-ttu-id="d804c-121">地區名稱</span><span class="sxs-lookup"><span data-stu-id="d804c-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d804c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d804c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d804c-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d804c-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d804c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d804c-124">-SubscriptionId</span></span>
<span data-ttu-id="d804c-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d804c-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d804c-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d804c-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d804c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d804c-127">CommonParameters</span></span>
<span data-ttu-id="d804c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d804c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d804c-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d804c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d804c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d804c-130">INPUTS</span></span>

### <span data-ttu-id="d804c-131">IInfrastructureInsightsAdminIdentity （InfrastructureInsightsAdmin）的</span><span class="sxs-lookup"><span data-stu-id="d804c-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="d804c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d804c-132">OUTPUTS</span></span>

### <span data-ttu-id="d804c-133">IRegionHealth （InfrastructureInsightsAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="d804c-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="d804c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d804c-134">NOTES</span></span>

<span data-ttu-id="d804c-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d804c-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d804c-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d804c-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d804c-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d804c-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d804c-138">`[AlertName <String>]`：警示的名稱。</span><span class="sxs-lookup"><span data-stu-id="d804c-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="d804c-139">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d804c-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d804c-140">`[Location <String>]`：區域的名稱</span><span class="sxs-lookup"><span data-stu-id="d804c-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="d804c-141">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d804c-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d804c-142">`[ResourceRegistrationId <String>]`：資源註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="d804c-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="d804c-143">`[ServiceHealth <String>]`：服務健康情況名稱。</span><span class="sxs-lookup"><span data-stu-id="d804c-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="d804c-144">`[ServiceRegistrationId <String>]`：服務註冊 ID。</span><span class="sxs-lookup"><span data-stu-id="d804c-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="d804c-145">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d804c-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d804c-146">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d804c-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d804c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d804c-147">RELATED LINKS</span></span>

