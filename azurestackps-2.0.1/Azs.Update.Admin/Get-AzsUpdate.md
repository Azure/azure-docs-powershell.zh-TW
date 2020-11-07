---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966619"
---
# <span data-ttu-id="ada2d-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="ada2d-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="ada2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ada2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ada2d-103">在更新位置取得特定更新。</span><span class="sxs-lookup"><span data-stu-id="ada2d-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="ada2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ada2d-104">SYNTAX</span></span>

### <span data-ttu-id="ada2d-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ada2d-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ada2d-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ada2d-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ada2d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ada2d-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ada2d-108">說明</span><span class="sxs-lookup"><span data-stu-id="ada2d-108">DESCRIPTION</span></span>
<span data-ttu-id="ada2d-109">在更新位置取得特定更新。</span><span class="sxs-lookup"><span data-stu-id="ada2d-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="ada2d-110">示例</span><span class="sxs-lookup"><span data-stu-id="ada2d-110">EXAMPLES</span></span>

### <span data-ttu-id="ada2d-111">範例1：取得所有更新</span><span class="sxs-lookup"><span data-stu-id="ada2d-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="ada2d-112">如果沒有任何參數，Get-AzsUpdate 會列出戳記可以探索的所有更新</span><span class="sxs-lookup"><span data-stu-id="ada2d-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="ada2d-113">範例2：透過名稱取得更新</span><span class="sxs-lookup"><span data-stu-id="ada2d-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="ada2d-114">將會檢索對應至指定名稱的所有更新</span><span class="sxs-lookup"><span data-stu-id="ada2d-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="ada2d-115">範例3：依位置取得所有更新</span><span class="sxs-lookup"><span data-stu-id="ada2d-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="ada2d-116">會在指定位置中檢索所有更新。</span><span class="sxs-lookup"><span data-stu-id="ada2d-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="ada2d-117">目前只支援一個位置，所以這只會受到相當 Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="ada2d-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="ada2d-118">參數</span><span class="sxs-lookup"><span data-stu-id="ada2d-118">PARAMETERS</span></span>

### <span data-ttu-id="ada2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada2d-119">-DefaultProfile</span></span>
<span data-ttu-id="ada2d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada2d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ada2d-121">-InputObject</span></span>
<span data-ttu-id="ada2d-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ada2d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ada2d-123">-位置</span><span class="sxs-lookup"><span data-stu-id="ada2d-123">-Location</span></span>
<span data-ttu-id="ada2d-124">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-124">The name of the update location.</span></span>

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

### <span data-ttu-id="ada2d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ada2d-125">-Name</span></span>
<span data-ttu-id="ada2d-126">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-126">Name of the update.</span></span>

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

### <span data-ttu-id="ada2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ada2d-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-128">Resource group name.</span></span>

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

### <span data-ttu-id="ada2d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ada2d-129">-SubscriptionId</span></span>
<span data-ttu-id="ada2d-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ada2d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ada2d-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ada2d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ada2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada2d-132">CommonParameters</span></span>
<span data-ttu-id="ada2d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ada2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada2d-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ada2d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada2d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ada2d-135">INPUTS</span></span>

### <span data-ttu-id="ada2d-136">IUpdateAdminIdentity （UpdateAdmin）的</span><span class="sxs-lookup"><span data-stu-id="ada2d-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="ada2d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ada2d-137">OUTPUTS</span></span>

### <span data-ttu-id="ada2d-138">IUpdate （UpdateAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="ada2d-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="ada2d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ada2d-139">NOTES</span></span>

<span data-ttu-id="ada2d-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ada2d-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ada2d-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ada2d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ada2d-142">INPUTOBJECT <IUpdateAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ada2d-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ada2d-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ada2d-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ada2d-144">`[ResourceGroupName <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="ada2d-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ada2d-145">`[RunName <String>]`：更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ada2d-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="ada2d-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ada2d-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="ada2d-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ada2d-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ada2d-148">`[UpdateLocation <String>]`：更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="ada2d-149">`[UpdateName <String>]`：更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="ada2d-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="ada2d-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ada2d-150">RELATED LINKS</span></span>

