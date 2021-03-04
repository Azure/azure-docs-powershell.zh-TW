---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911346"
---
# <span data-ttu-id="4239e-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="4239e-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="4239e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4239e-102">SYNOPSIS</span></span>
<span data-ttu-id="4239e-103">獲得儀表板。</span><span class="sxs-lookup"><span data-stu-id="4239e-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="4239e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4239e-104">SYNTAX</span></span>

### <span data-ttu-id="4239e-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="4239e-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4239e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4239e-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4239e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4239e-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4239e-108">清單</span><span class="sxs-lookup"><span data-stu-id="4239e-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4239e-109">描述</span><span class="sxs-lookup"><span data-stu-id="4239e-109">DESCRIPTION</span></span>
<span data-ttu-id="4239e-110">獲得儀表板。</span><span class="sxs-lookup"><span data-stu-id="4239e-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="4239e-111">例子</span><span class="sxs-lookup"><span data-stu-id="4239e-111">EXAMPLES</span></span>

### <span data-ttu-id="4239e-112">範例 1：列出訂閱中所有的儀表板</span><span class="sxs-lookup"><span data-stu-id="4239e-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="4239e-113">列出訂閱中所有的儀表板</span><span class="sxs-lookup"><span data-stu-id="4239e-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="4239e-114">範例 2：取得單一入口網站儀表板的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="4239e-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="4239e-115">取得單一儀表板的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="4239e-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="4239e-116">參數</span><span class="sxs-lookup"><span data-stu-id="4239e-116">PARAMETERS</span></span>

### <span data-ttu-id="4239e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4239e-117">-DefaultProfile</span></span>
<span data-ttu-id="4239e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4239e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4239e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4239e-119">-InputObject</span></span>
<span data-ttu-id="4239e-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4239e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4239e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4239e-121">-Name</span></span>
<span data-ttu-id="4239e-122">儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="4239e-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="4239e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4239e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4239e-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4239e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4239e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4239e-125">-SubscriptionId</span></span>
<span data-ttu-id="4239e-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4239e-126">The Azure subscription ID.</span></span>
<span data-ttu-id="4239e-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="4239e-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4239e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4239e-128">CommonParameters</span></span>
<span data-ttu-id="4239e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4239e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4239e-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4239e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4239e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4239e-131">INPUTS</span></span>

### <span data-ttu-id="4239e-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="4239e-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="4239e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4239e-133">OUTPUTS</span></span>

### <span data-ttu-id="4239e-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="4239e-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="4239e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4239e-135">NOTES</span></span>

<span data-ttu-id="4239e-136">別名</span><span class="sxs-lookup"><span data-stu-id="4239e-136">ALIASES</span></span>

<span data-ttu-id="4239e-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4239e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4239e-138">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4239e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4239e-139">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4239e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4239e-140">INPUTOBJECT： <IPortalIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4239e-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4239e-141">`[DashboardName <String>]`：儀表板的名稱。</span><span class="sxs-lookup"><span data-stu-id="4239e-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="4239e-142">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4239e-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4239e-143">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4239e-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4239e-144">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4239e-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4239e-145">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="4239e-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4239e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4239e-146">RELATED LINKS</span></span>

