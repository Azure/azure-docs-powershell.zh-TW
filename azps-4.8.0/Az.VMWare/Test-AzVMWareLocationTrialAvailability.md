---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968888"
---
# <span data-ttu-id="ce865-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="ce865-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="ce865-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce865-102">SYNOPSIS</span></span>
<span data-ttu-id="ce865-103">傳回訂閱的試用狀態（依地區）</span><span class="sxs-lookup"><span data-stu-id="ce865-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="ce865-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce865-104">SYNTAX</span></span>

### <span data-ttu-id="ce865-105">檢查 (預設) </span><span class="sxs-lookup"><span data-stu-id="ce865-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce865-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce865-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce865-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce865-107">DESCRIPTION</span></span>
<span data-ttu-id="ce865-108">傳回訂閱的試用狀態（依地區）</span><span class="sxs-lookup"><span data-stu-id="ce865-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="ce865-109">示例</span><span class="sxs-lookup"><span data-stu-id="ce865-109">EXAMPLES</span></span>

### <span data-ttu-id="ce865-110">範例1：檢查試用版可用性</span><span class="sxs-lookup"><span data-stu-id="ce865-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="ce865-111">檢查試用版可用性</span><span class="sxs-lookup"><span data-stu-id="ce865-111">Check trial availability</span></span>

## <span data-ttu-id="ce865-112">參數</span><span class="sxs-lookup"><span data-stu-id="ce865-112">PARAMETERS</span></span>

### <span data-ttu-id="ce865-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce865-113">-DefaultProfile</span></span>
<span data-ttu-id="ce865-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce865-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce865-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce865-115">-InputObject</span></span>
<span data-ttu-id="ce865-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ce865-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce865-117">-位置</span><span class="sxs-lookup"><span data-stu-id="ce865-117">-Location</span></span>
<span data-ttu-id="ce865-118">Azure 區域</span><span class="sxs-lookup"><span data-stu-id="ce865-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce865-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce865-119">-SubscriptionId</span></span>
<span data-ttu-id="ce865-120">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ce865-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce865-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ce865-121">-Confirm</span></span>
<span data-ttu-id="ce865-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce865-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce865-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce865-123">-WhatIf</span></span>
<span data-ttu-id="ce865-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce865-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce865-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce865-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce865-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce865-126">CommonParameters</span></span>
<span data-ttu-id="ce865-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce865-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce865-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce865-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce865-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ce865-129">INPUTS</span></span>

### <span data-ttu-id="ce865-130">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ce865-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ce865-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ce865-131">OUTPUTS</span></span>

### <span data-ttu-id="ce865-132">ITrial 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="ce865-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="ce865-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ce865-133">NOTES</span></span>

<span data-ttu-id="ce865-134">別名</span><span class="sxs-lookup"><span data-stu-id="ce865-134">ALIASES</span></span>

<span data-ttu-id="ce865-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ce865-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce865-136">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ce865-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce865-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ce865-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce865-138">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ce865-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce865-139">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="ce865-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ce865-140">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="ce865-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ce865-141">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="ce865-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ce865-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ce865-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce865-143">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="ce865-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ce865-144">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="ce865-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ce865-145">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce865-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ce865-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ce865-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ce865-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce865-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ce865-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce865-148">RELATED LINKS</span></span>

