---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 1a5cfb9f9bc7edb436d37847fc117565c3b71221
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966769"
---
# <span data-ttu-id="d2bba-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d2bba-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="d2bba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2bba-102">SYNOPSIS</span></span>
<span data-ttu-id="d2bba-103">使用識別碼來取得更新執行的實例。</span><span class="sxs-lookup"><span data-stu-id="d2bba-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="d2bba-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2bba-104">SYNTAX</span></span>

### <span data-ttu-id="d2bba-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="d2bba-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2bba-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d2bba-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2bba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2bba-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d2bba-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2bba-108">DESCRIPTION</span></span>
<span data-ttu-id="d2bba-109">使用識別碼來取得更新執行的實例。</span><span class="sxs-lookup"><span data-stu-id="d2bba-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="d2bba-110">示例</span><span class="sxs-lookup"><span data-stu-id="d2bba-110">EXAMPLES</span></span>

### <span data-ttu-id="d2bba-111">範例1： Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d2bba-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="d2bba-112">如果未指定 UpdateName 值，Get-UpdateRun 將總是要求輸入。</span><span class="sxs-lookup"><span data-stu-id="d2bba-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="d2bba-113">一旦提供，就會輸出所有失敗或成功的 UpdateRun 實例</span><span class="sxs-lookup"><span data-stu-id="d2bba-113">Once provided, it will output all instances of UpdateRun that were Failed or Successfull</span></span>

### <span data-ttu-id="d2bba-114">範例2：依 UpdateName Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d2bba-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="d2bba-115">將會檢索與特定更新相關的所有 UpdateRuns</span><span class="sxs-lookup"><span data-stu-id="d2bba-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="d2bba-116">範例2：依名稱 Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d2bba-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="d2bba-117">將會檢索與特定更新及特定名稱相關聯的所有 UpdateRuns</span><span class="sxs-lookup"><span data-stu-id="d2bba-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="d2bba-118">參數</span><span class="sxs-lookup"><span data-stu-id="d2bba-118">PARAMETERS</span></span>

### <span data-ttu-id="d2bba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2bba-119">-DefaultProfile</span></span>
<span data-ttu-id="d2bba-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2bba-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2bba-121">-InputObject</span></span>
<span data-ttu-id="d2bba-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d2bba-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2bba-123">-位置</span><span class="sxs-lookup"><span data-stu-id="d2bba-123">-Location</span></span>
<span data-ttu-id="d2bba-124">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-124">The name of the update location.</span></span>

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

### <span data-ttu-id="d2bba-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2bba-125">-Name</span></span>
<span data-ttu-id="d2bba-126">更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bba-126">Update run identifier.</span></span>

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

### <span data-ttu-id="d2bba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2bba-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2bba-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-128">Resource group name.</span></span>

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

### <span data-ttu-id="d2bba-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2bba-129">-SubscriptionId</span></span>
<span data-ttu-id="d2bba-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d2bba-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2bba-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d2bba-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2bba-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="d2bba-132">-UpdateName</span></span>
<span data-ttu-id="d2bba-133">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-133">Name of the update.</span></span>

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

### <span data-ttu-id="d2bba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2bba-134">CommonParameters</span></span>
<span data-ttu-id="d2bba-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2bba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2bba-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d2bba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2bba-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d2bba-137">INPUTS</span></span>

### <span data-ttu-id="d2bba-138">IUpdateAdminIdentity （UpdateAdmin）的</span><span class="sxs-lookup"><span data-stu-id="d2bba-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="d2bba-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d2bba-139">OUTPUTS</span></span>

### <span data-ttu-id="d2bba-140">IUpdateRun （UpdateAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="d2bba-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="d2bba-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d2bba-141">NOTES</span></span>

<span data-ttu-id="d2bba-142">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d2bba-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2bba-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d2bba-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d2bba-144">INPUTOBJECT <IUpdateAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d2bba-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2bba-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d2bba-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2bba-146">`[ResourceGroupName <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="d2bba-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="d2bba-147">`[RunName <String>]`：更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bba-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="d2bba-148">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d2bba-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="d2bba-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d2bba-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d2bba-150">`[UpdateLocation <String>]`：更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="d2bba-151">`[UpdateName <String>]`：更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2bba-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="d2bba-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2bba-152">RELATED LINKS</span></span>

