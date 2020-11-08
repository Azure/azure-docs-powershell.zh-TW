---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140709"
---
# <span data-ttu-id="43d9d-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="43d9d-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="43d9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="43d9d-103">依區域傳回訂閱配額</span><span class="sxs-lookup"><span data-stu-id="43d9d-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="43d9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="43d9d-104">SYNTAX</span></span>

### <span data-ttu-id="43d9d-105">檢查 (預設) </span><span class="sxs-lookup"><span data-stu-id="43d9d-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43d9d-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43d9d-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43d9d-107">說明</span><span class="sxs-lookup"><span data-stu-id="43d9d-107">DESCRIPTION</span></span>
<span data-ttu-id="43d9d-108">依區域傳回訂閱配額</span><span class="sxs-lookup"><span data-stu-id="43d9d-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="43d9d-109">示例</span><span class="sxs-lookup"><span data-stu-id="43d9d-109">EXAMPLES</span></span>

### <span data-ttu-id="43d9d-110">範例1：檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="43d9d-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="43d9d-111">檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="43d9d-111">Check quota availability</span></span>

## <span data-ttu-id="43d9d-112">參數</span><span class="sxs-lookup"><span data-stu-id="43d9d-112">PARAMETERS</span></span>

### <span data-ttu-id="43d9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d9d-113">-DefaultProfile</span></span>
<span data-ttu-id="43d9d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43d9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d9d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d9d-115">-InputObject</span></span>
<span data-ttu-id="43d9d-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="43d9d-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d9d-117">-位置</span><span class="sxs-lookup"><span data-stu-id="43d9d-117">-Location</span></span>
<span data-ttu-id="43d9d-118">Azure 區域</span><span class="sxs-lookup"><span data-stu-id="43d9d-118">Azure region</span></span>

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

### <span data-ttu-id="43d9d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43d9d-119">-SubscriptionId</span></span>
<span data-ttu-id="43d9d-120">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="43d9d-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43d9d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="43d9d-121">-Confirm</span></span>
<span data-ttu-id="43d9d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43d9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d9d-123">-WhatIf</span></span>
<span data-ttu-id="43d9d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43d9d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d9d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43d9d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d9d-126">CommonParameters</span></span>
<span data-ttu-id="43d9d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43d9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d9d-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43d9d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d9d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="43d9d-129">INPUTS</span></span>

### <span data-ttu-id="43d9d-130">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43d9d-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="43d9d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="43d9d-131">OUTPUTS</span></span>

### <span data-ttu-id="43d9d-132">IQuota 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="43d9d-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="43d9d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="43d9d-133">NOTES</span></span>

<span data-ttu-id="43d9d-134">別名</span><span class="sxs-lookup"><span data-stu-id="43d9d-134">ALIASES</span></span>

<span data-ttu-id="43d9d-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="43d9d-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43d9d-136">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="43d9d-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d9d-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="43d9d-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43d9d-138">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="43d9d-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d9d-139">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="43d9d-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="43d9d-140">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="43d9d-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="43d9d-141">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="43d9d-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="43d9d-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="43d9d-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d9d-143">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="43d9d-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="43d9d-144">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="43d9d-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="43d9d-145">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43d9d-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43d9d-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="43d9d-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="43d9d-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43d9d-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="43d9d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="43d9d-148">RELATED LINKS</span></span>

