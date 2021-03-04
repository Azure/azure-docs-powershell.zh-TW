---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 61ecab0a22df339af7c790fd51def5a880d9b607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911233"
---
# <span data-ttu-id="28a57-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="28a57-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="28a57-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28a57-102">SYNOPSIS</span></span>
<span data-ttu-id="28a57-103">按地區針對訂閱的退貨配額</span><span class="sxs-lookup"><span data-stu-id="28a57-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="28a57-104">語法</span><span class="sxs-lookup"><span data-stu-id="28a57-104">SYNTAX</span></span>

### <span data-ttu-id="28a57-105">檢查 (預設) </span><span class="sxs-lookup"><span data-stu-id="28a57-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28a57-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="28a57-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28a57-107">描述</span><span class="sxs-lookup"><span data-stu-id="28a57-107">DESCRIPTION</span></span>
<span data-ttu-id="28a57-108">按地區針對訂閱的退貨配額</span><span class="sxs-lookup"><span data-stu-id="28a57-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="28a57-109">例子</span><span class="sxs-lookup"><span data-stu-id="28a57-109">EXAMPLES</span></span>

### <span data-ttu-id="28a57-110">範例 1：檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="28a57-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="28a57-111">檢查配額可用性</span><span class="sxs-lookup"><span data-stu-id="28a57-111">Check quota availability</span></span>

## <span data-ttu-id="28a57-112">參數</span><span class="sxs-lookup"><span data-stu-id="28a57-112">PARAMETERS</span></span>

### <span data-ttu-id="28a57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a57-113">-DefaultProfile</span></span>
<span data-ttu-id="28a57-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28a57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a57-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a57-115">-InputObject</span></span>
<span data-ttu-id="28a57-116">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28a57-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28a57-117">-位置</span><span class="sxs-lookup"><span data-stu-id="28a57-117">-Location</span></span>
<span data-ttu-id="28a57-118">Azure 地區</span><span class="sxs-lookup"><span data-stu-id="28a57-118">Azure region</span></span>

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

### <span data-ttu-id="28a57-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28a57-119">-SubscriptionId</span></span>
<span data-ttu-id="28a57-120">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="28a57-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="28a57-121">-確認</span><span class="sxs-lookup"><span data-stu-id="28a57-121">-Confirm</span></span>
<span data-ttu-id="28a57-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28a57-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a57-123">-WhatIf</span></span>
<span data-ttu-id="28a57-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28a57-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28a57-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28a57-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a57-126">CommonParameters</span></span>
<span data-ttu-id="28a57-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28a57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a57-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a57-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a57-129">輸入</span><span class="sxs-lookup"><span data-stu-id="28a57-129">INPUTS</span></span>

### <span data-ttu-id="28a57-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="28a57-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="28a57-131">輸出</span><span class="sxs-lookup"><span data-stu-id="28a57-131">OUTPUTS</span></span>

### <span data-ttu-id="28a57-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="28a57-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="28a57-133">筆記</span><span class="sxs-lookup"><span data-stu-id="28a57-133">NOTES</span></span>

<span data-ttu-id="28a57-134">別名</span><span class="sxs-lookup"><span data-stu-id="28a57-134">ALIASES</span></span>

<span data-ttu-id="28a57-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="28a57-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28a57-136">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28a57-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28a57-137">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="28a57-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28a57-138">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="28a57-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28a57-139">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="28a57-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="28a57-140">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="28a57-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="28a57-141">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="28a57-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="28a57-142">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="28a57-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28a57-143">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="28a57-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="28a57-144">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="28a57-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="28a57-145">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28a57-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="28a57-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="28a57-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="28a57-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="28a57-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="28a57-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="28a57-148">RELATED LINKS</span></span>

