---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 38f9aef513e13b2676569d434977752f3d193062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910197"
---
# <span data-ttu-id="e47cb-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e47cb-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e47cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e47cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e47cb-103">取得 DigitalTwinsInstances 資源。</span><span class="sxs-lookup"><span data-stu-id="e47cb-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="e47cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="e47cb-104">SYNTAX</span></span>

### <span data-ttu-id="e47cb-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e47cb-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e47cb-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e47cb-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e47cb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e47cb-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e47cb-108">清單1</span><span class="sxs-lookup"><span data-stu-id="e47cb-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e47cb-109">描述</span><span class="sxs-lookup"><span data-stu-id="e47cb-109">DESCRIPTION</span></span>
<span data-ttu-id="e47cb-110">取得 DigitalTwinsInstances 資源。</span><span class="sxs-lookup"><span data-stu-id="e47cb-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="e47cb-111">例子</span><span class="sxs-lookup"><span data-stu-id="e47cb-111">EXAMPLES</span></span>

### <span data-ttu-id="e47cb-112">範例 1：清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e47cb-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e47cb-113">根據預設取得所有 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e47cb-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="e47cb-114">範例 2：取得</span><span class="sxs-lookup"><span data-stu-id="e47cb-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e47cb-115">使用 ResourceName 取得指定的 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e47cb-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="e47cb-116">範例 3：GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e47cb-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e47cb-117">取得指定的 AzDigitalTwinsInstance by Object</span><span class="sxs-lookup"><span data-stu-id="e47cb-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="e47cb-118">範例 4：清單1</span><span class="sxs-lookup"><span data-stu-id="e47cb-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e47cb-119">取得 ResourceGroupName 的所有 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e47cb-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="e47cb-120">參數</span><span class="sxs-lookup"><span data-stu-id="e47cb-120">PARAMETERS</span></span>

### <span data-ttu-id="e47cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47cb-121">-DefaultProfile</span></span>
<span data-ttu-id="e47cb-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e47cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e47cb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e47cb-123">-InputObject</span></span>
<span data-ttu-id="e47cb-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e47cb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e47cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e47cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="e47cb-126">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e47cb-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47cb-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e47cb-127">-ResourceName</span></span>
<span data-ttu-id="e47cb-128">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e47cb-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="e47cb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e47cb-129">-SubscriptionId</span></span>
<span data-ttu-id="e47cb-130">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e47cb-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="e47cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47cb-131">CommonParameters</span></span>
<span data-ttu-id="e47cb-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e47cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47cb-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e47cb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47cb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e47cb-134">INPUTS</span></span>

### <span data-ttu-id="e47cb-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e47cb-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e47cb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e47cb-136">OUTPUTS</span></span>

### <span data-ttu-id="e47cb-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="e47cb-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="e47cb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e47cb-138">NOTES</span></span>

<span data-ttu-id="e47cb-139">別名</span><span class="sxs-lookup"><span data-stu-id="e47cb-139">ALIASES</span></span>

<span data-ttu-id="e47cb-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e47cb-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e47cb-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e47cb-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e47cb-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e47cb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e47cb-143">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e47cb-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e47cb-144">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e47cb-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e47cb-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e47cb-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e47cb-146">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="e47cb-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e47cb-147">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e47cb-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e47cb-148">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e47cb-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e47cb-149">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e47cb-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e47cb-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e47cb-150">RELATED LINKS</span></span>

