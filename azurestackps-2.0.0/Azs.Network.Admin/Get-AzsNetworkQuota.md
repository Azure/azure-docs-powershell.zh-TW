---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794869"
---
# <span data-ttu-id="ad5de-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ad5de-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="ad5de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad5de-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5de-103">依名稱取得配額。</span><span class="sxs-lookup"><span data-stu-id="ad5de-103">Get a quota by name.</span></span>

## <span data-ttu-id="ad5de-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad5de-104">SYNTAX</span></span>

### <span data-ttu-id="ad5de-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ad5de-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ad5de-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ad5de-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ad5de-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad5de-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ad5de-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad5de-108">DESCRIPTION</span></span>
<span data-ttu-id="ad5de-109">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="ad5de-109">List all quotas.</span></span>
<span data-ttu-id="ad5de-110">傳送名稱或篩選限制清單。</span><span class="sxs-lookup"><span data-stu-id="ad5de-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="ad5de-111">示例</span><span class="sxs-lookup"><span data-stu-id="ad5de-111">EXAMPLES</span></span>

### <span data-ttu-id="ad5de-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad5de-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="ad5de-113">列出所有網路配額。</span><span class="sxs-lookup"><span data-stu-id="ad5de-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="ad5de-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad5de-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="ad5de-115">取得指定的網路配額。</span><span class="sxs-lookup"><span data-stu-id="ad5de-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="ad5de-116">參數</span><span class="sxs-lookup"><span data-stu-id="ad5de-116">PARAMETERS</span></span>

### <span data-ttu-id="ad5de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5de-117">-DefaultProfile</span></span>
<span data-ttu-id="ad5de-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad5de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad5de-119">-篩選</span><span class="sxs-lookup"><span data-stu-id="ad5de-119">-Filter</span></span>
<span data-ttu-id="ad5de-120">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ad5de-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="ad5de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad5de-121">-InputObject</span></span>
<span data-ttu-id="ad5de-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ad5de-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ad5de-123">-位置</span><span class="sxs-lookup"><span data-stu-id="ad5de-123">-Location</span></span>
<span data-ttu-id="ad5de-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ad5de-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ad5de-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad5de-125">-Name</span></span>
<span data-ttu-id="ad5de-126">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5de-126">Name of the resource.</span></span>

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

### <span data-ttu-id="ad5de-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad5de-127">-PassThru</span></span>
<span data-ttu-id="ad5de-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ad5de-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad5de-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad5de-129">-SubscriptionId</span></span>
<span data-ttu-id="ad5de-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ad5de-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad5de-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ad5de-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad5de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5de-132">CommonParameters</span></span>
<span data-ttu-id="ad5de-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad5de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5de-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad5de-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5de-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ad5de-135">INPUTS</span></span>

### <span data-ttu-id="ad5de-136">INetworkAdminIdentity （NetworkAdmin）的</span><span class="sxs-lookup"><span data-stu-id="ad5de-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="ad5de-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ad5de-137">OUTPUTS</span></span>

### <span data-ttu-id="ad5de-138">IQuota （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="ad5de-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="ad5de-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ad5de-139">NOTES</span></span>

<span data-ttu-id="ad5de-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ad5de-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad5de-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ad5de-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ad5de-142">INPUTOBJECT <INetworkAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ad5de-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad5de-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ad5de-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad5de-144">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ad5de-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ad5de-145">`[ResourceName <String>]`：資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5de-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="ad5de-146">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ad5de-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ad5de-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ad5de-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ad5de-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad5de-148">RELATED LINKS</span></span>

