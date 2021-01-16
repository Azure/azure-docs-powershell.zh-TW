---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279699"
---
# <span data-ttu-id="21fb8-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="21fb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="21fb8-103">取得 DigitalTwinsInstances 端點。</span><span class="sxs-lookup"><span data-stu-id="21fb8-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="21fb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="21fb8-104">SYNTAX</span></span>

### <span data-ttu-id="21fb8-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="21fb8-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21fb8-106">獲取</span><span class="sxs-lookup"><span data-stu-id="21fb8-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21fb8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21fb8-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="21fb8-108">說明</span><span class="sxs-lookup"><span data-stu-id="21fb8-108">DESCRIPTION</span></span>
<span data-ttu-id="21fb8-109">取得 DigitalTwinsInstances 端點。</span><span class="sxs-lookup"><span data-stu-id="21fb8-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="21fb8-110">示例</span><span class="sxs-lookup"><span data-stu-id="21fb8-110">EXAMPLES</span></span>

### <span data-ttu-id="21fb8-111">範例1：在 ResourceGroup 中列出 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="21fb8-112">依 ResourceGroupName 列出所有 AzDigitalTwinsEndpoints</span><span class="sxs-lookup"><span data-stu-id="21fb8-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="21fb8-113">範例2：依終結點取得 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="21fb8-114">在 ResourceGroup 中透過終結點取得 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="21fb8-115">範例3：透過 "AzDigitalTwinsEndpoint" 物件取得 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="21fb8-116">透過 "AzDigitalTwinsEndpoint" 物件取得 AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="21fb8-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="21fb8-117">參數</span><span class="sxs-lookup"><span data-stu-id="21fb8-117">PARAMETERS</span></span>

### <span data-ttu-id="21fb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fb8-118">-DefaultProfile</span></span>
<span data-ttu-id="21fb8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fb8-120">-終結點</span><span class="sxs-lookup"><span data-stu-id="21fb8-120">-EndpointName</span></span>
<span data-ttu-id="21fb8-121">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="21fb8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21fb8-122">-InputObject</span></span>
<span data-ttu-id="21fb8-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="21fb8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21fb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="21fb8-125">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="21fb8-126">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="21fb8-126">-ResourceName</span></span>
<span data-ttu-id="21fb8-127">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="21fb8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21fb8-128">-SubscriptionId</span></span>
<span data-ttu-id="21fb8-129">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="21fb8-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="21fb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fb8-130">CommonParameters</span></span>
<span data-ttu-id="21fb8-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21fb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fb8-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21fb8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fb8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="21fb8-133">INPUTS</span></span>

### <span data-ttu-id="21fb8-134">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="21fb8-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="21fb8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="21fb8-135">OUTPUTS</span></span>

### <span data-ttu-id="21fb8-136">IDigitalTwinsEndpointResource （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="21fb8-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="21fb8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="21fb8-137">NOTES</span></span>

<span data-ttu-id="21fb8-138">別名</span><span class="sxs-lookup"><span data-stu-id="21fb8-138">ALIASES</span></span>

<span data-ttu-id="21fb8-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="21fb8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21fb8-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="21fb8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21fb8-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="21fb8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21fb8-142">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="21fb8-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21fb8-143">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="21fb8-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="21fb8-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21fb8-145">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="21fb8-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21fb8-146">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21fb8-147">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb8-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21fb8-148">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="21fb8-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="21fb8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="21fb8-149">RELATED LINKS</span></span>

