---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135728"
---
# <span data-ttu-id="2b722-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="2b722-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="2b722-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b722-102">SYNOPSIS</span></span>
<span data-ttu-id="2b722-103">取得儀表板。</span><span class="sxs-lookup"><span data-stu-id="2b722-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="2b722-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b722-104">SYNTAX</span></span>

### <span data-ttu-id="2b722-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b722-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b722-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2b722-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b722-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b722-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b722-108">清單</span><span class="sxs-lookup"><span data-stu-id="2b722-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b722-109">說明</span><span class="sxs-lookup"><span data-stu-id="2b722-109">DESCRIPTION</span></span>
<span data-ttu-id="2b722-110">取得儀表板。</span><span class="sxs-lookup"><span data-stu-id="2b722-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="2b722-111">示例</span><span class="sxs-lookup"><span data-stu-id="2b722-111">EXAMPLES</span></span>

### <span data-ttu-id="2b722-112">範例1：列出訂閱中的所有儀表板</span><span class="sxs-lookup"><span data-stu-id="2b722-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="2b722-113">列出訂閱中的所有儀表板</span><span class="sxs-lookup"><span data-stu-id="2b722-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="2b722-114">範例2：取得單一入口網站儀表板的詳細資料</span><span class="sxs-lookup"><span data-stu-id="2b722-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="2b722-115">取得單一儀表板的詳細資料</span><span class="sxs-lookup"><span data-stu-id="2b722-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="2b722-116">參數</span><span class="sxs-lookup"><span data-stu-id="2b722-116">PARAMETERS</span></span>

### <span data-ttu-id="2b722-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b722-117">-DefaultProfile</span></span>
<span data-ttu-id="2b722-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b722-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b722-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b722-119">-InputObject</span></span>
<span data-ttu-id="2b722-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b722-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b722-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b722-121">-Name</span></span>
<span data-ttu-id="2b722-122">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b722-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b722-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b722-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b722-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b722-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b722-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b722-125">-SubscriptionId</span></span>
<span data-ttu-id="2b722-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2b722-126">The Azure subscription ID.</span></span>
<span data-ttu-id="2b722-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="2b722-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b722-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b722-128">CommonParameters</span></span>
<span data-ttu-id="2b722-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b722-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b722-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b722-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b722-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2b722-131">INPUTS</span></span>

### <span data-ttu-id="2b722-132">IPortalIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b722-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="2b722-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2b722-133">OUTPUTS</span></span>

### <span data-ttu-id="2b722-134">[Api201901Preview. IDashboard] （）</span><span class="sxs-lookup"><span data-stu-id="2b722-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="2b722-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2b722-135">NOTES</span></span>

<span data-ttu-id="2b722-136">別名</span><span class="sxs-lookup"><span data-stu-id="2b722-136">ALIASES</span></span>

<span data-ttu-id="2b722-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2b722-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b722-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2b722-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b722-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2b722-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b722-140">INPUTOBJECT <IPortalIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2b722-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b722-141">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b722-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="2b722-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2b722-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b722-143">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b722-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2b722-144">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2b722-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2b722-145">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="2b722-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2b722-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b722-146">RELATED LINKS</span></span>
