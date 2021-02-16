---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140931"
---
# <span data-ttu-id="0955d-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0955d-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="0955d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0955d-102">SYNOPSIS</span></span>
<span data-ttu-id="0955d-103">取得 DigitalTwinsInstances 資源。</span><span class="sxs-lookup"><span data-stu-id="0955d-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="0955d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0955d-104">SYNTAX</span></span>

### <span data-ttu-id="0955d-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0955d-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0955d-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0955d-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0955d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0955d-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0955d-108">List1</span><span class="sxs-lookup"><span data-stu-id="0955d-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0955d-109">說明</span><span class="sxs-lookup"><span data-stu-id="0955d-109">DESCRIPTION</span></span>
<span data-ttu-id="0955d-110">取得 DigitalTwinsInstances 資源。</span><span class="sxs-lookup"><span data-stu-id="0955d-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="0955d-111">示例</span><span class="sxs-lookup"><span data-stu-id="0955d-111">EXAMPLES</span></span>

### <span data-ttu-id="0955d-112">範例1： (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0955d-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0955d-113">預設取得所有 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0955d-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="0955d-114">範例2：取得</span><span class="sxs-lookup"><span data-stu-id="0955d-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0955d-115">根據使用方式取得指定的 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0955d-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="0955d-116">範例3： GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0955d-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0955d-117">透過物件取得指定的 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0955d-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="0955d-118">範例4： List1</span><span class="sxs-lookup"><span data-stu-id="0955d-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="0955d-119">透過 ResourceGroupName 取得所有 DigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="0955d-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="0955d-120">參數</span><span class="sxs-lookup"><span data-stu-id="0955d-120">PARAMETERS</span></span>

### <span data-ttu-id="0955d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0955d-121">-DefaultProfile</span></span>
<span data-ttu-id="0955d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0955d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0955d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0955d-123">-InputObject</span></span>
<span data-ttu-id="0955d-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0955d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0955d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0955d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0955d-126">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0955d-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0955d-127">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="0955d-127">-ResourceName</span></span>
<span data-ttu-id="0955d-128">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0955d-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0955d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0955d-129">-SubscriptionId</span></span>
<span data-ttu-id="0955d-130">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0955d-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="0955d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0955d-131">CommonParameters</span></span>
<span data-ttu-id="0955d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0955d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0955d-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0955d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0955d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0955d-134">INPUTS</span></span>

### <span data-ttu-id="0955d-135">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="0955d-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="0955d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0955d-136">OUTPUTS</span></span>

### <span data-ttu-id="0955d-137">IDigitalTwinsDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="0955d-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="0955d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0955d-138">NOTES</span></span>

<span data-ttu-id="0955d-139">別名</span><span class="sxs-lookup"><span data-stu-id="0955d-139">ALIASES</span></span>

<span data-ttu-id="0955d-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0955d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0955d-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0955d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0955d-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0955d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0955d-143">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0955d-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0955d-144">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0955d-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="0955d-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0955d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0955d-146">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="0955d-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="0955d-147">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0955d-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="0955d-148">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0955d-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="0955d-149">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0955d-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="0955d-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="0955d-150">RELATED LINKS</span></span>

