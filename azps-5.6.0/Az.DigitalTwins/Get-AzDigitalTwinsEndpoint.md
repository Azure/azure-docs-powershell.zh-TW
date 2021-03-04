---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 35ba036e38b54a335cbdcdd923008a5a4ce055fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910201"
---
# <span data-ttu-id="3697e-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3697e-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="3697e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3697e-102">SYNOPSIS</span></span>
<span data-ttu-id="3697e-103">取得 DigitalTwinsInstances 端點。</span><span class="sxs-lookup"><span data-stu-id="3697e-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="3697e-104">語法</span><span class="sxs-lookup"><span data-stu-id="3697e-104">SYNTAX</span></span>

### <span data-ttu-id="3697e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="3697e-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3697e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3697e-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3697e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3697e-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3697e-108">描述</span><span class="sxs-lookup"><span data-stu-id="3697e-108">DESCRIPTION</span></span>
<span data-ttu-id="3697e-109">取得 DigitalTwinsInstances 端點。</span><span class="sxs-lookup"><span data-stu-id="3697e-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="3697e-110">例子</span><span class="sxs-lookup"><span data-stu-id="3697e-110">EXAMPLES</span></span>

### <span data-ttu-id="3697e-111">範例 1：在 ResourceGroup 中列出 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3697e-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3697e-112">按 ResourceGroupName 列出所有 AzDigitalTwinsEndpoints</span><span class="sxs-lookup"><span data-stu-id="3697e-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="3697e-113">範例 2：Get AzDigitalTwinsEndpoint by EndpointName</span><span class="sxs-lookup"><span data-stu-id="3697e-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3697e-114">在 ResourceGroup 中取得 AzDigitalTwinsEndpoint by EndpointName</span><span class="sxs-lookup"><span data-stu-id="3697e-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="3697e-115">範例 3：Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span><span class="sxs-lookup"><span data-stu-id="3697e-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="3697e-116">使用 AzDigitalTwinsEndpoint 物件取得 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3697e-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="3697e-117">參數</span><span class="sxs-lookup"><span data-stu-id="3697e-117">PARAMETERS</span></span>

### <span data-ttu-id="3697e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3697e-118">-DefaultProfile</span></span>
<span data-ttu-id="3697e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3697e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3697e-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3697e-120">-EndpointName</span></span>
<span data-ttu-id="3697e-121">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3697e-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="3697e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3697e-122">-InputObject</span></span>
<span data-ttu-id="3697e-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3697e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3697e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3697e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3697e-125">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3697e-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="3697e-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3697e-126">-ResourceName</span></span>
<span data-ttu-id="3697e-127">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3697e-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="3697e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3697e-128">-SubscriptionId</span></span>
<span data-ttu-id="3697e-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3697e-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="3697e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3697e-130">CommonParameters</span></span>
<span data-ttu-id="3697e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3697e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3697e-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3697e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3697e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3697e-133">INPUTS</span></span>

### <span data-ttu-id="3697e-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="3697e-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="3697e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3697e-135">OUTPUTS</span></span>

### <span data-ttu-id="3697e-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="3697e-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="3697e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="3697e-137">NOTES</span></span>

<span data-ttu-id="3697e-138">別名</span><span class="sxs-lookup"><span data-stu-id="3697e-138">ALIASES</span></span>

<span data-ttu-id="3697e-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3697e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3697e-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3697e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3697e-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3697e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3697e-142">INPUTOBJECT： <IDigitalTwinsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3697e-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3697e-143">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3697e-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="3697e-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3697e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3697e-145">`[Location <String>]`：DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="3697e-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="3697e-146">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3697e-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="3697e-147">`[ResourceName <String>]`：DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3697e-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="3697e-148">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3697e-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="3697e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="3697e-149">RELATED LINKS</span></span>

