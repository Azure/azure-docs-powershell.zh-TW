---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284833"
---
# <span data-ttu-id="8189e-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="8189e-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="8189e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8189e-102">SYNOPSIS</span></span>
<span data-ttu-id="8189e-103">取得指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="8189e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8189e-104">SYNTAX</span></span>

### <span data-ttu-id="8189e-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="8189e-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8189e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8189e-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8189e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8189e-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8189e-108">清單</span><span class="sxs-lookup"><span data-stu-id="8189e-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8189e-109">說明</span><span class="sxs-lookup"><span data-stu-id="8189e-109">DESCRIPTION</span></span>
<span data-ttu-id="8189e-110">取得指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="8189e-111">示例</span><span class="sxs-lookup"><span data-stu-id="8189e-111">EXAMPLES</span></span>

### <span data-ttu-id="8189e-112">範例1：取得訂閱的所有專用 HSM</span><span class="sxs-lookup"><span data-stu-id="8189e-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8189e-113">這個命令會取得訂閱的所有專用 HSM</span><span class="sxs-lookup"><span data-stu-id="8189e-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="8189e-114">範例2：取得資源群組底下的所有專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8189e-115">這個命令會取得資源群組下的所有專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="8189e-116">範例3：依名稱取得專用 HSM</span><span class="sxs-lookup"><span data-stu-id="8189e-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8189e-117">這個命令會透過名稱取得專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="8189e-118">範例4：透過物件取得專用的 HSM</span><span class="sxs-lookup"><span data-stu-id="8189e-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="8189e-119">這個命令會透過物件取得專用的 HSM。</span><span class="sxs-lookup"><span data-stu-id="8189e-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="8189e-120">參數</span><span class="sxs-lookup"><span data-stu-id="8189e-120">PARAMETERS</span></span>

### <span data-ttu-id="8189e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8189e-121">-DefaultProfile</span></span>
<span data-ttu-id="8189e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8189e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8189e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8189e-123">-InputObject</span></span>
<span data-ttu-id="8189e-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8189e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8189e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8189e-125">-Name</span></span>
<span data-ttu-id="8189e-126">專用 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8189e-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="8189e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8189e-127">-ResourceGroupName</span></span>
<span data-ttu-id="8189e-128">專用 hsm 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8189e-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="8189e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8189e-129">-SubscriptionId</span></span>
<span data-ttu-id="8189e-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8189e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8189e-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8189e-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8189e-132">-上方</span><span class="sxs-lookup"><span data-stu-id="8189e-132">-Top</span></span>
<span data-ttu-id="8189e-133">要傳回的結果數目上限。</span><span class="sxs-lookup"><span data-stu-id="8189e-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="8189e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8189e-134">CommonParameters</span></span>
<span data-ttu-id="8189e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8189e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8189e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8189e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8189e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8189e-137">INPUTS</span></span>

### <span data-ttu-id="8189e-138">IDedicatedHsmIdentity （DedicatedHsm）的</span><span class="sxs-lookup"><span data-stu-id="8189e-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="8189e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8189e-139">OUTPUTS</span></span>

### <span data-ttu-id="8189e-140">IDedicatedHsm （DedicatedHsm）。 Api20181031。</span><span class="sxs-lookup"><span data-stu-id="8189e-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="8189e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8189e-141">NOTES</span></span>

<span data-ttu-id="8189e-142">別名</span><span class="sxs-lookup"><span data-stu-id="8189e-142">ALIASES</span></span>

<span data-ttu-id="8189e-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8189e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8189e-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8189e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8189e-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8189e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8189e-146">INPUTOBJECT <IDedicatedHsmIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8189e-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8189e-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8189e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8189e-148">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="8189e-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="8189e-149">`[ResourceGroupName <String>]`：資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8189e-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="8189e-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8189e-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8189e-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8189e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8189e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8189e-152">RELATED LINKS</span></span>

