---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968174"
---
# <span data-ttu-id="eafd4-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="eafd4-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="eafd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eafd4-102">SYNOPSIS</span></span>
<span data-ttu-id="eafd4-103">刪除現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="eafd4-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="eafd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="eafd4-104">SYNTAX</span></span>

### <span data-ttu-id="eafd4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="eafd4-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eafd4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eafd4-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eafd4-107">說明</span><span class="sxs-lookup"><span data-stu-id="eafd4-107">DESCRIPTION</span></span>
<span data-ttu-id="eafd4-108">刪除現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="eafd4-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="eafd4-109">示例</span><span class="sxs-lookup"><span data-stu-id="eafd4-109">EXAMPLES</span></span>

### <span data-ttu-id="eafd4-110">範例1：移除計算配額</span><span class="sxs-lookup"><span data-stu-id="eafd4-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="eafd4-111">成功呼叫移除計算配額時，不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="eafd4-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="eafd4-112">參數</span><span class="sxs-lookup"><span data-stu-id="eafd4-112">PARAMETERS</span></span>

### <span data-ttu-id="eafd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafd4-113">-DefaultProfile</span></span>
<span data-ttu-id="eafd4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafd4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eafd4-115">-InputObject</span></span>
<span data-ttu-id="eafd4-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eafd4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-117">-位置</span><span class="sxs-lookup"><span data-stu-id="eafd4-117">-Location</span></span>
<span data-ttu-id="eafd4-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="eafd4-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="eafd4-119">-Name</span></span>
<span data-ttu-id="eafd4-120">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eafd4-121">-PassThru</span></span>
<span data-ttu-id="eafd4-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="eafd4-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eafd4-123">-SubscriptionId</span></span>
<span data-ttu-id="eafd4-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="eafd4-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eafd4-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eafd4-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="eafd4-126">-Confirm</span></span>
<span data-ttu-id="eafd4-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eafd4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafd4-128">-WhatIf</span></span>
<span data-ttu-id="eafd4-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eafd4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafd4-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eafd4-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="eafd4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafd4-131">CommonParameters</span></span>
<span data-ttu-id="eafd4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eafd4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafd4-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eafd4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafd4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="eafd4-134">INPUTS</span></span>

### <span data-ttu-id="eafd4-135">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="eafd4-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="eafd4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="eafd4-136">OUTPUTS</span></span>

### <span data-ttu-id="eafd4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="eafd4-137">System.Boolean</span></span>



## <span data-ttu-id="eafd4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eafd4-138">NOTES</span></span>

<span data-ttu-id="eafd4-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="eafd4-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eafd4-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eafd4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eafd4-141">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="eafd4-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eafd4-142">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="eafd4-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="eafd4-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="eafd4-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eafd4-144">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="eafd4-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="eafd4-145">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="eafd4-146">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="eafd4-147">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="eafd4-148">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="eafd4-149">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafd4-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="eafd4-150">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="eafd4-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eafd4-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="eafd4-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="eafd4-152">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="eafd4-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="eafd4-153">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="eafd4-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="eafd4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="eafd4-154">RELATED LINKS</span></span>

