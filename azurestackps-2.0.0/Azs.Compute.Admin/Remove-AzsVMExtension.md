---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796505"
---
# <span data-ttu-id="765d5-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="765d5-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="765d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="765d5-102">SYNOPSIS</span></span>
<span data-ttu-id="765d5-103">刪除指定的虛擬電腦延伸影像。</span><span class="sxs-lookup"><span data-stu-id="765d5-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="765d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="765d5-104">SYNTAX</span></span>

### <span data-ttu-id="765d5-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="765d5-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="765d5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="765d5-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="765d5-107">說明</span><span class="sxs-lookup"><span data-stu-id="765d5-107">DESCRIPTION</span></span>
<span data-ttu-id="765d5-108">刪除指定的虛擬電腦延伸影像。</span><span class="sxs-lookup"><span data-stu-id="765d5-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="765d5-109">示例</span><span class="sxs-lookup"><span data-stu-id="765d5-109">EXAMPLES</span></span>

### <span data-ttu-id="765d5-110">範例1：移除存在的 VM 延伸</span><span class="sxs-lookup"><span data-stu-id="765d5-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="765d5-111">成功呼叫移除計算配額時，不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="765d5-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="765d5-112">範例2：移除不存在的 VM 副檔名</span><span class="sxs-lookup"><span data-stu-id="765d5-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="765d5-113">若要移除不存在的平臺影像，成功的呼叫就不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="765d5-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="765d5-114">參數</span><span class="sxs-lookup"><span data-stu-id="765d5-114">PARAMETERS</span></span>

### <span data-ttu-id="765d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765d5-115">-DefaultProfile</span></span>
<span data-ttu-id="765d5-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="765d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="765d5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="765d5-117">-InputObject</span></span>
<span data-ttu-id="765d5-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="765d5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="765d5-119">-位置</span><span class="sxs-lookup"><span data-stu-id="765d5-119">-Location</span></span>
<span data-ttu-id="765d5-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="765d5-120">Location of the resource.</span></span>

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

### <span data-ttu-id="765d5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="765d5-121">-PassThru</span></span>
<span data-ttu-id="765d5-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="765d5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="765d5-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="765d5-123">-Publisher</span></span>
<span data-ttu-id="765d5-124">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="765d5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="765d5-125">-SubscriptionId</span></span>
<span data-ttu-id="765d5-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="765d5-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="765d5-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="765d5-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="765d5-128">-類型</span><span class="sxs-lookup"><span data-stu-id="765d5-128">-Type</span></span>
<span data-ttu-id="765d5-129">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="765d5-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="765d5-130">-版本</span><span class="sxs-lookup"><span data-stu-id="765d5-130">-Version</span></span>
<span data-ttu-id="765d5-131">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="765d5-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="765d5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="765d5-132">-Confirm</span></span>
<span data-ttu-id="765d5-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="765d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="765d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765d5-134">-WhatIf</span></span>
<span data-ttu-id="765d5-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="765d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="765d5-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="765d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="765d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765d5-137">CommonParameters</span></span>
<span data-ttu-id="765d5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="765d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765d5-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="765d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765d5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="765d5-140">INPUTS</span></span>

### <span data-ttu-id="765d5-141">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="765d5-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="765d5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="765d5-142">OUTPUTS</span></span>

### <span data-ttu-id="765d5-143">System.object</span><span class="sxs-lookup"><span data-stu-id="765d5-143">System.Boolean</span></span>



## <span data-ttu-id="765d5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="765d5-144">NOTES</span></span>

<span data-ttu-id="765d5-145">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="765d5-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="765d5-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="765d5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="765d5-147">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="765d5-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="765d5-148">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="765d5-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="765d5-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="765d5-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="765d5-150">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="765d5-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="765d5-151">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="765d5-152">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="765d5-153">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="765d5-154">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="765d5-155">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="765d5-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="765d5-156">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="765d5-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="765d5-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="765d5-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="765d5-158">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="765d5-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="765d5-159">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="765d5-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="765d5-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="765d5-160">RELATED LINKS</span></span>

