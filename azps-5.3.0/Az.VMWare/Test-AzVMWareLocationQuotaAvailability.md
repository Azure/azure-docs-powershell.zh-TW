---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436045"
---
# <span data-ttu-id="f3c8b-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="f3c8b-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="f3c8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c8b-103">依區域傳回訂閱配額</span><span class="sxs-lookup"><span data-stu-id="f3c8b-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="f3c8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3c8b-104">SYNTAX</span></span>

### <span data-ttu-id="f3c8b-105">檢查 (預設) </span><span class="sxs-lookup"><span data-stu-id="f3c8b-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3c8b-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3c8b-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3c8b-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c8b-108">依區域傳回訂閱配額</span><span class="sxs-lookup"><span data-stu-id="f3c8b-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="f3c8b-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3c8b-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c8b-110">範例1：檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="f3c8b-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="f3c8b-111">檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="f3c8b-111">Check quota availability</span></span>

## <span data-ttu-id="f3c8b-112">參數</span><span class="sxs-lookup"><span data-stu-id="f3c8b-112">PARAMETERS</span></span>

### <span data-ttu-id="f3c8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c8b-113">-DefaultProfile</span></span>
<span data-ttu-id="f3c8b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c8b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c8b-115">-InputObject</span></span>
<span data-ttu-id="f3c8b-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3c8b-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f3c8b-117">-Location</span></span>
<span data-ttu-id="f3c8b-118">Azure 區域</span><span class="sxs-lookup"><span data-stu-id="f3c8b-118">Azure region</span></span>

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

### <span data-ttu-id="f3c8b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3c8b-119">-SubscriptionId</span></span>
<span data-ttu-id="f3c8b-120">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f3c8b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f3c8b-121">-Confirm</span></span>
<span data-ttu-id="f3c8b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c8b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c8b-123">-WhatIf</span></span>
<span data-ttu-id="f3c8b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c8b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c8b-126">CommonParameters</span></span>
<span data-ttu-id="f3c8b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c8b-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c8b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f3c8b-129">INPUTS</span></span>

### <span data-ttu-id="f3c8b-130">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3c8b-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f3c8b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f3c8b-131">OUTPUTS</span></span>

### <span data-ttu-id="f3c8b-132">IQuota 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="f3c8b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f3c8b-133">NOTES</span></span>

<span data-ttu-id="f3c8b-134">別名</span><span class="sxs-lookup"><span data-stu-id="f3c8b-134">ALIASES</span></span>

<span data-ttu-id="f3c8b-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f3c8b-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3c8b-136">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3c8b-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3c8b-138">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f3c8b-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3c8b-139">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="f3c8b-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f3c8b-140">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="f3c8b-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f3c8b-141">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="f3c8b-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f3c8b-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f3c8b-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3c8b-143">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="f3c8b-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f3c8b-144">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="f3c8b-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f3c8b-145">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f3c8b-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="f3c8b-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c8b-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f3c8b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3c8b-148">RELATED LINKS</span></span>

