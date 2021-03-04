---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905525"
---
# <span data-ttu-id="00862-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="00862-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="00862-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00862-102">SYNOPSIS</span></span>
<span data-ttu-id="00862-103">獲得指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="00862-104">語法</span><span class="sxs-lookup"><span data-stu-id="00862-104">SYNTAX</span></span>

### <span data-ttu-id="00862-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="00862-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="00862-106">獲取</span><span class="sxs-lookup"><span data-stu-id="00862-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00862-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00862-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00862-108">清單</span><span class="sxs-lookup"><span data-stu-id="00862-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="00862-109">描述</span><span class="sxs-lookup"><span data-stu-id="00862-109">DESCRIPTION</span></span>
<span data-ttu-id="00862-110">獲得指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="00862-111">例子</span><span class="sxs-lookup"><span data-stu-id="00862-111">EXAMPLES</span></span>

### <span data-ttu-id="00862-112">範例 1：取得訂閱下的所有專用 HSM</span><span class="sxs-lookup"><span data-stu-id="00862-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="00862-113">此命令會獲得訂閱下的所有專用 HSM</span><span class="sxs-lookup"><span data-stu-id="00862-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="00862-114">範例 2：在資源群組下取得所有專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="00862-115">此命令會獲得資源群組下的所有專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="00862-116">範例 3：取得專用 HSM by name</span><span class="sxs-lookup"><span data-stu-id="00862-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="00862-117">此命令會按名稱獲得專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="00862-118">範例 4：取得物件的專用 HSM</span><span class="sxs-lookup"><span data-stu-id="00862-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="00862-119">此命令會按物件獲得專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="00862-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="00862-120">參數</span><span class="sxs-lookup"><span data-stu-id="00862-120">PARAMETERS</span></span>

### <span data-ttu-id="00862-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00862-121">-DefaultProfile</span></span>
<span data-ttu-id="00862-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00862-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00862-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00862-123">-InputObject</span></span>
<span data-ttu-id="00862-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="00862-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00862-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="00862-125">-Name</span></span>
<span data-ttu-id="00862-126">專用 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="00862-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="00862-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00862-127">-ResourceGroupName</span></span>
<span data-ttu-id="00862-128">專用 hsm 所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="00862-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="00862-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00862-129">-SubscriptionId</span></span>
<span data-ttu-id="00862-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="00862-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="00862-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="00862-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00862-132">-頂端</span><span class="sxs-lookup"><span data-stu-id="00862-132">-Top</span></span>
<span data-ttu-id="00862-133">要返回的結果數目上限。</span><span class="sxs-lookup"><span data-stu-id="00862-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00862-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00862-134">CommonParameters</span></span>
<span data-ttu-id="00862-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00862-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00862-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00862-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00862-137">輸入</span><span class="sxs-lookup"><span data-stu-id="00862-137">INPUTS</span></span>

### <span data-ttu-id="00862-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.IDedicatedSoftmIdentity</span><span class="sxs-lookup"><span data-stu-id="00862-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="00862-139">輸出</span><span class="sxs-lookup"><span data-stu-id="00862-139">OUTPUTS</span></span>

### <span data-ttu-id="00862-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedVtm.models.Api20181031.IDedicatedSoftm</span><span class="sxs-lookup"><span data-stu-id="00862-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="00862-141">筆記</span><span class="sxs-lookup"><span data-stu-id="00862-141">NOTES</span></span>

<span data-ttu-id="00862-142">別名</span><span class="sxs-lookup"><span data-stu-id="00862-142">ALIASES</span></span>

<span data-ttu-id="00862-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="00862-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00862-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="00862-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00862-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="00862-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00862-146">INPUTOBJECT： <IDedicatedHsmIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="00862-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00862-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="00862-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00862-148">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="00862-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="00862-149">`[ResourceGroupName <String>]`：資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="00862-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="00862-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="00862-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="00862-151">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="00862-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="00862-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="00862-152">RELATED LINKS</span></span>

