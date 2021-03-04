---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910177"
---
# <span data-ttu-id="7193a-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="7193a-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="7193a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7193a-102">SYNOPSIS</span></span>
<span data-ttu-id="7193a-103">建立或更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7193a-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="7193a-104">修改屬性的一般模式是，要取回 DigitalTwinsInstance 和安全性中繼資料，然後將它們與新內文中的修改值合併，以更新 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="7193a-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="7193a-105">語法</span><span class="sxs-lookup"><span data-stu-id="7193a-105">SYNTAX</span></span>

### <span data-ttu-id="7193a-106">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7193a-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7193a-107">創建</span><span class="sxs-lookup"><span data-stu-id="7193a-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7193a-108">描述</span><span class="sxs-lookup"><span data-stu-id="7193a-108">DESCRIPTION</span></span>
<span data-ttu-id="7193a-109">建立或更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7193a-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="7193a-110">修改屬性的一般模式是，要取回 DigitalTwinsInstance 和安全性中繼資料，然後將它們與新內文中的修改值合併，以更新 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="7193a-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="7193a-111">例子</span><span class="sxs-lookup"><span data-stu-id="7193a-111">EXAMPLES</span></span>

### <span data-ttu-id="7193a-112">範例 1：根據預設建立 AzDigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="7193a-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="7193a-113">根據預設，建立 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="7193a-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="7193a-114">範例 2：建立 AzDigitalTwinsInstance by AzDigitalTwins Object。</span><span class="sxs-lookup"><span data-stu-id="7193a-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="7193a-115">使用 AzDigitalTwins Object 建立 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="7193a-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="7193a-116">參數</span><span class="sxs-lookup"><span data-stu-id="7193a-116">PARAMETERS</span></span>

### <span data-ttu-id="7193a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7193a-117">-AsJob</span></span>
<span data-ttu-id="7193a-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="7193a-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7193a-119">-DefaultProfile</span></span>
<span data-ttu-id="7193a-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7193a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7193a-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="7193a-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="7193a-122">DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="7193a-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="7193a-123">若要建構，請參閱 DIGITALTWINSCREATE 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7193a-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-124">-位置</span><span class="sxs-lookup"><span data-stu-id="7193a-124">-Location</span></span>
<span data-ttu-id="7193a-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="7193a-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7193a-126">-NoWait</span></span>
<span data-ttu-id="7193a-127">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="7193a-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7193a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7193a-129">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7193a-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7193a-130">-ResourceName</span></span>
<span data-ttu-id="7193a-131">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7193a-131">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7193a-132">-SubscriptionId</span></span>
<span data-ttu-id="7193a-133">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7193a-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-134">-標記</span><span class="sxs-lookup"><span data-stu-id="7193a-134">-Tag</span></span>
<span data-ttu-id="7193a-135">資源標記。</span><span class="sxs-lookup"><span data-stu-id="7193a-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7193a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="7193a-136">-Confirm</span></span>
<span data-ttu-id="7193a-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7193a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7193a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7193a-138">-WhatIf</span></span>
<span data-ttu-id="7193a-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7193a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7193a-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7193a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7193a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7193a-141">CommonParameters</span></span>
<span data-ttu-id="7193a-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7193a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7193a-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7193a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7193a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="7193a-144">INPUTS</span></span>

### <span data-ttu-id="7193a-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="7193a-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="7193a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7193a-146">OUTPUTS</span></span>

### <span data-ttu-id="7193a-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="7193a-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="7193a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7193a-148">NOTES</span></span>

<span data-ttu-id="7193a-149">別名</span><span class="sxs-lookup"><span data-stu-id="7193a-149">ALIASES</span></span>

<span data-ttu-id="7193a-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7193a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7193a-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7193a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7193a-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7193a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7193a-153"><IDigitalTwinsDescription>DIGITALTWINSCREATE：DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="7193a-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="7193a-154">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="7193a-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="7193a-155">`[Tag <IDigitalTwinsResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="7193a-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="7193a-156">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="7193a-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="7193a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="7193a-157">RELATED LINKS</span></span>

