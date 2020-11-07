---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966641"
---
# <span data-ttu-id="367ea-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="367ea-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="367ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="367ea-102">SYNOPSIS</span></span>
<span data-ttu-id="367ea-103">根據名稱取得更新位置。</span><span class="sxs-lookup"><span data-stu-id="367ea-103">Get an update location based on name.</span></span>

## <span data-ttu-id="367ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="367ea-104">SYNTAX</span></span>

### <span data-ttu-id="367ea-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="367ea-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="367ea-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="367ea-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="367ea-107">清單</span><span class="sxs-lookup"><span data-stu-id="367ea-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="367ea-108">說明</span><span class="sxs-lookup"><span data-stu-id="367ea-108">DESCRIPTION</span></span>
<span data-ttu-id="367ea-109">根據名稱取得更新位置。</span><span class="sxs-lookup"><span data-stu-id="367ea-109">Get an update location based on name.</span></span>

## <span data-ttu-id="367ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="367ea-110">EXAMPLES</span></span>

### <span data-ttu-id="367ea-111">範例1：取得所有更新位置</span><span class="sxs-lookup"><span data-stu-id="367ea-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="367ea-112">如果沒有任何參數，此 commandlet 將會檢索所有更新位置</span><span class="sxs-lookup"><span data-stu-id="367ea-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="367ea-113">範例2：依名稱取得所有更新位置</span><span class="sxs-lookup"><span data-stu-id="367ea-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="367ea-114">將會檢索符合指定 Name 參數的所有更新位置</span><span class="sxs-lookup"><span data-stu-id="367ea-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="367ea-115">參數</span><span class="sxs-lookup"><span data-stu-id="367ea-115">PARAMETERS</span></span>

### <span data-ttu-id="367ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367ea-116">-DefaultProfile</span></span>
<span data-ttu-id="367ea-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="367ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="367ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="367ea-118">-InputObject</span></span>
<span data-ttu-id="367ea-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="367ea-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="367ea-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="367ea-120">-Name</span></span>
<span data-ttu-id="367ea-121">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="367ea-121">The name of the update location.</span></span>

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

### <span data-ttu-id="367ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="367ea-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="367ea-123">Resource group name.</span></span>

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

### <span data-ttu-id="367ea-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="367ea-124">-SubscriptionId</span></span>
<span data-ttu-id="367ea-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="367ea-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="367ea-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="367ea-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="367ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367ea-127">CommonParameters</span></span>
<span data-ttu-id="367ea-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="367ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367ea-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="367ea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367ea-130">輸入</span><span class="sxs-lookup"><span data-stu-id="367ea-130">INPUTS</span></span>

### <span data-ttu-id="367ea-131">IUpdateAdminIdentity （UpdateAdmin）的</span><span class="sxs-lookup"><span data-stu-id="367ea-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="367ea-132">輸出</span><span class="sxs-lookup"><span data-stu-id="367ea-132">OUTPUTS</span></span>

### <span data-ttu-id="367ea-133">IUpdateLocation （UpdateAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="367ea-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="367ea-134">筆記</span><span class="sxs-lookup"><span data-stu-id="367ea-134">NOTES</span></span>

<span data-ttu-id="367ea-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="367ea-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="367ea-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="367ea-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="367ea-137">INPUTOBJECT <IUpdateAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="367ea-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="367ea-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="367ea-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="367ea-139">`[ResourceGroupName <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="367ea-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="367ea-140">`[RunName <String>]`：更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="367ea-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="367ea-141">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="367ea-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="367ea-142">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="367ea-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="367ea-143">`[UpdateLocation <String>]`：更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="367ea-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="367ea-144">`[UpdateName <String>]`：更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="367ea-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="367ea-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="367ea-145">RELATED LINKS</span></span>

