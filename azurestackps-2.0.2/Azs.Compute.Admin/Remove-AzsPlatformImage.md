---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968173"
---
# <span data-ttu-id="cb30e-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="cb30e-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="cb30e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb30e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb30e-103">刪除平臺影像</span><span class="sxs-lookup"><span data-stu-id="cb30e-103">Delete a platform image</span></span>

## <span data-ttu-id="cb30e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb30e-104">SYNTAX</span></span>

### <span data-ttu-id="cb30e-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="cb30e-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cb30e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb30e-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb30e-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb30e-107">DESCRIPTION</span></span>
<span data-ttu-id="cb30e-108">刪除平臺影像</span><span class="sxs-lookup"><span data-stu-id="cb30e-108">Delete a platform image</span></span>

## <span data-ttu-id="cb30e-109">示例</span><span class="sxs-lookup"><span data-stu-id="cb30e-109">EXAMPLES</span></span>

### <span data-ttu-id="cb30e-110">範例1：移除平臺影像</span><span class="sxs-lookup"><span data-stu-id="cb30e-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="cb30e-111">成功呼叫移除平臺影像時，不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="cb30e-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="cb30e-112">範例2：移除平臺圖像不存在</span><span class="sxs-lookup"><span data-stu-id="cb30e-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="cb30e-113">若要移除不存在的平臺影像，成功的呼叫就不會傳回任何輸出</span><span class="sxs-lookup"><span data-stu-id="cb30e-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="cb30e-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb30e-114">PARAMETERS</span></span>

### <span data-ttu-id="cb30e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb30e-115">-DefaultProfile</span></span>
<span data-ttu-id="cb30e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb30e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb30e-117">-InputObject</span></span>
<span data-ttu-id="cb30e-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cb30e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb30e-119">-位置</span><span class="sxs-lookup"><span data-stu-id="cb30e-119">-Location</span></span>
<span data-ttu-id="cb30e-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cb30e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="cb30e-121">-優惠</span><span class="sxs-lookup"><span data-stu-id="cb30e-121">-Offer</span></span>
<span data-ttu-id="cb30e-122">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-122">Name of the offer.</span></span>

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

### <span data-ttu-id="cb30e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb30e-123">-PassThru</span></span>
<span data-ttu-id="cb30e-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="cb30e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb30e-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cb30e-125">-Publisher</span></span>
<span data-ttu-id="cb30e-126">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="cb30e-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="cb30e-127">-Sku</span></span>
<span data-ttu-id="cb30e-128">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="cb30e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb30e-129">-SubscriptionId</span></span>
<span data-ttu-id="cb30e-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cb30e-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb30e-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cb30e-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb30e-132">-版本</span><span class="sxs-lookup"><span data-stu-id="cb30e-132">-Version</span></span>
<span data-ttu-id="cb30e-133">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="cb30e-133">The version of the resource.</span></span>

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

### <span data-ttu-id="cb30e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="cb30e-134">-Confirm</span></span>
<span data-ttu-id="cb30e-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb30e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb30e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb30e-136">-WhatIf</span></span>
<span data-ttu-id="cb30e-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb30e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb30e-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb30e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb30e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb30e-139">CommonParameters</span></span>
<span data-ttu-id="cb30e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb30e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb30e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb30e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb30e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="cb30e-142">INPUTS</span></span>

### <span data-ttu-id="cb30e-143">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cb30e-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="cb30e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="cb30e-144">OUTPUTS</span></span>

### <span data-ttu-id="cb30e-145">System.object</span><span class="sxs-lookup"><span data-stu-id="cb30e-145">System.Boolean</span></span>



## <span data-ttu-id="cb30e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="cb30e-146">NOTES</span></span>

<span data-ttu-id="cb30e-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cb30e-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb30e-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cb30e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cb30e-149">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cb30e-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb30e-150">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="cb30e-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="cb30e-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cb30e-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb30e-152">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cb30e-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cb30e-153">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="cb30e-154">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="cb30e-155">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="cb30e-156">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cb30e-157">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb30e-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="cb30e-158">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cb30e-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb30e-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cb30e-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb30e-160">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="cb30e-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="cb30e-161">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="cb30e-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="cb30e-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb30e-162">RELATED LINKS</span></span>

