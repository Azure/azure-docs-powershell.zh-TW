---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966749"
---
# <span data-ttu-id="7e946-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="7e946-101">New-AzsIPPool</span></span>

## <span data-ttu-id="7e946-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e946-102">SYNOPSIS</span></span>
<span data-ttu-id="7e946-103">建立 IP 池。</span><span class="sxs-lookup"><span data-stu-id="7e946-103">Create an IP pool.</span></span>
<span data-ttu-id="7e946-104">建立 IP 池之後，就無法刪除。</span><span class="sxs-lookup"><span data-stu-id="7e946-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="7e946-105">句法</span><span class="sxs-lookup"><span data-stu-id="7e946-105">SYNTAX</span></span>

### <span data-ttu-id="7e946-106">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7e946-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e946-107">建立</span><span class="sxs-lookup"><span data-stu-id="7e946-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7e946-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e946-108">DESCRIPTION</span></span>
<span data-ttu-id="7e946-109">建立 IP 池。</span><span class="sxs-lookup"><span data-stu-id="7e946-109">Create an IP pool.</span></span>
<span data-ttu-id="7e946-110">建立 IP 池之後，就無法刪除。</span><span class="sxs-lookup"><span data-stu-id="7e946-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="7e946-111">示例</span><span class="sxs-lookup"><span data-stu-id="7e946-111">EXAMPLES</span></span>

### <span data-ttu-id="7e946-112">範例1：</span><span class="sxs-lookup"><span data-stu-id="7e946-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="7e946-113">建立新的 IP 池。</span><span class="sxs-lookup"><span data-stu-id="7e946-113">Create a new IP pool.</span></span>



## <span data-ttu-id="7e946-114">參數</span><span class="sxs-lookup"><span data-stu-id="7e946-114">PARAMETERS</span></span>

### <span data-ttu-id="7e946-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7e946-115">-AddressPrefix</span></span>
<span data-ttu-id="7e946-116">位址首碼。</span><span class="sxs-lookup"><span data-stu-id="7e946-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e946-117">-AsJob</span></span>
<span data-ttu-id="7e946-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7e946-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7e946-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e946-119">-DefaultProfile</span></span>
<span data-ttu-id="7e946-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e946-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e946-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="7e946-121">-EndIPAddress</span></span>
<span data-ttu-id="7e946-122">結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7e946-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-123">-位置</span><span class="sxs-lookup"><span data-stu-id="7e946-123">-Location</span></span>
<span data-ttu-id="7e946-124">資源所在的地區。</span><span class="sxs-lookup"><span data-stu-id="7e946-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e946-125">-Name</span></span>
<span data-ttu-id="7e946-126">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="7e946-126">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7e946-127">-NoWait</span></span>
<span data-ttu-id="7e946-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7e946-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7e946-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="7e946-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="7e946-130">目前已分配 IP 位址的數目。</span><span class="sxs-lookup"><span data-stu-id="7e946-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="7e946-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="7e946-132">IP 位址的總數。</span><span class="sxs-lookup"><span data-stu-id="7e946-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="7e946-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="7e946-134">[轉換] 中的目前 IP 位址數。</span><span class="sxs-lookup"><span data-stu-id="7e946-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="7e946-135">-Pool</span></span>
<span data-ttu-id="7e946-136">此資源定義 IP 位址的範圍，這些位址是針對子網中的節點所指派的位址。</span><span class="sxs-lookup"><span data-stu-id="7e946-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="7e946-137">若要建立，請參閱 POOL 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="7e946-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e946-138">-ResourceGroupName</span></span>
<span data-ttu-id="7e946-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e946-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="7e946-140">-StartIPAddress</span></span>
<span data-ttu-id="7e946-141">起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7e946-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e946-142">-SubscriptionId</span></span>
<span data-ttu-id="7e946-143">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7e946-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7e946-144">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7e946-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e946-145">-Tag</span></span>
<span data-ttu-id="7e946-146">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="7e946-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7e946-147">-確認</span><span class="sxs-lookup"><span data-stu-id="7e946-147">-Confirm</span></span>
<span data-ttu-id="7e946-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e946-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e946-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e946-149">-WhatIf</span></span>
<span data-ttu-id="7e946-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e946-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e946-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e946-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e946-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e946-152">CommonParameters</span></span>
<span data-ttu-id="7e946-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e946-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e946-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7e946-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e946-155">輸入</span><span class="sxs-lookup"><span data-stu-id="7e946-155">INPUTS</span></span>

### <span data-ttu-id="7e946-156">IIPPool （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="7e946-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="7e946-157">輸出</span><span class="sxs-lookup"><span data-stu-id="7e946-157">OUTPUTS</span></span>

### <span data-ttu-id="7e946-158">IIPPool （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="7e946-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="7e946-159">筆記</span><span class="sxs-lookup"><span data-stu-id="7e946-159">NOTES</span></span>

<span data-ttu-id="7e946-160">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7e946-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e946-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7e946-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7e946-162">[泳池] <IIPPool> ：此資源會定義 IP 位址範圍，從此處將位址指派給子網中的節點。</span><span class="sxs-lookup"><span data-stu-id="7e946-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="7e946-163">`[Location <String>]`：資源所在的地區。</span><span class="sxs-lookup"><span data-stu-id="7e946-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="7e946-164">`[Tag <IResourceTags>]`：鍵-值對的清單。</span><span class="sxs-lookup"><span data-stu-id="7e946-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="7e946-165">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="7e946-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7e946-166">`[AddressPrefix <String>]`：位址首碼。</span><span class="sxs-lookup"><span data-stu-id="7e946-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="7e946-167">`[EndIPAddress <String>]`：結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7e946-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="7e946-168">`[NumberOfAllocatedIPAddresses <Int64?>]`：目前已分配 IP 位址的數目。</span><span class="sxs-lookup"><span data-stu-id="7e946-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="7e946-169">`[NumberOfIPAddresses <Int64?>]`： IP 位址的總數。</span><span class="sxs-lookup"><span data-stu-id="7e946-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="7e946-170">`[NumberOfIPAddressesInTransition <Int64?>]`：過渡中的目前 IP 位址數。</span><span class="sxs-lookup"><span data-stu-id="7e946-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="7e946-171">`[StartIPAddress <String>]`：起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7e946-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="7e946-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e946-172">RELATED LINKS</span></span>

