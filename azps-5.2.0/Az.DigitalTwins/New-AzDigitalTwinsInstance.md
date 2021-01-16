---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279692"
---
# <span data-ttu-id="ba9f0-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ba9f0-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="ba9f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9f0-103">建立或更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="ba9f0-104">修改屬性的一般模式是檢索 DigitalTwinsInstance 和安全性中繼資料，然後將它們與新主體中修改過的值加以結合，以更新 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ba9f0-105">句法</span><span class="sxs-lookup"><span data-stu-id="ba9f0-105">SYNTAX</span></span>

### <span data-ttu-id="ba9f0-106">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ba9f0-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba9f0-107">建立</span><span class="sxs-lookup"><span data-stu-id="ba9f0-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba9f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="ba9f0-108">DESCRIPTION</span></span>
<span data-ttu-id="ba9f0-109">建立或更新 DigitalTwinsInstance 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="ba9f0-110">修改屬性的一般模式是檢索 DigitalTwinsInstance 和安全性中繼資料，然後將它們與新主體中修改過的值加以結合，以更新 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ba9f0-111">示例</span><span class="sxs-lookup"><span data-stu-id="ba9f0-111">EXAMPLES</span></span>

### <span data-ttu-id="ba9f0-112">範例1：依預設建立 AzDigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="ba9f0-113">依預設建立 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ba9f0-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="ba9f0-114">範例2：依 AzDigitalTwins 物件建立 AzDigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="ba9f0-115">依 AzDigitalTwins 物件建立 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ba9f0-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="ba9f0-116">參數</span><span class="sxs-lookup"><span data-stu-id="ba9f0-116">PARAMETERS</span></span>

### <span data-ttu-id="ba9f0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9f0-117">-AsJob</span></span>
<span data-ttu-id="ba9f0-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ba9f0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ba9f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9f0-119">-DefaultProfile</span></span>
<span data-ttu-id="ba9f0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9f0-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="ba9f0-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="ba9f0-122">DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="ba9f0-123">若要建立，請參閱 DIGITALTWINSCREATE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba9f0-124">-位置</span><span class="sxs-lookup"><span data-stu-id="ba9f0-124">-Location</span></span>
<span data-ttu-id="ba9f0-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-125">The resource location.</span></span>

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

### <span data-ttu-id="ba9f0-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba9f0-126">-NoWait</span></span>
<span data-ttu-id="ba9f0-127">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ba9f0-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba9f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="ba9f0-129">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ba9f0-130">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="ba9f0-130">-ResourceName</span></span>
<span data-ttu-id="ba9f0-131">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ba9f0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba9f0-132">-SubscriptionId</span></span>
<span data-ttu-id="ba9f0-133">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="ba9f0-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba9f0-134">-Tag</span></span>
<span data-ttu-id="ba9f0-135">資源標記。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-135">The resource tags.</span></span>

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

### <span data-ttu-id="ba9f0-136">-確認</span><span class="sxs-lookup"><span data-stu-id="ba9f0-136">-Confirm</span></span>
<span data-ttu-id="ba9f0-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9f0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9f0-138">-WhatIf</span></span>
<span data-ttu-id="ba9f0-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba9f0-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9f0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9f0-141">CommonParameters</span></span>
<span data-ttu-id="ba9f0-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9f0-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9f0-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ba9f0-144">INPUTS</span></span>

### <span data-ttu-id="ba9f0-145">IDigitalTwinsDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ba9f0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ba9f0-146">OUTPUTS</span></span>

### <span data-ttu-id="ba9f0-147">IDigitalTwinsDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ba9f0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ba9f0-148">NOTES</span></span>

<span data-ttu-id="ba9f0-149">別名</span><span class="sxs-lookup"><span data-stu-id="ba9f0-149">ALIASES</span></span>

<span data-ttu-id="ba9f0-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ba9f0-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba9f0-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba9f0-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba9f0-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> ： DigitalTwins 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="ba9f0-154">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="ba9f0-155">`[Tag <IDigitalTwinsResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="ba9f0-156">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="ba9f0-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="ba9f0-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba9f0-157">RELATED LINKS</span></span>

