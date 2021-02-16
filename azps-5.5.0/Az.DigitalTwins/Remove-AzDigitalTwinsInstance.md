---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsInstance.md
ms.openlocfilehash: 495fecf922bc27eb43849b7ba6e44793c572b8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133270"
---
# <span data-ttu-id="ec46c-101">Remove-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ec46c-101">Remove-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="ec46c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec46c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec46c-103">刪除 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ec46c-103">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ec46c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec46c-104">SYNTAX</span></span>

### <span data-ttu-id="ec46c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ec46c-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec46c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec46c-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec46c-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec46c-107">DESCRIPTION</span></span>
<span data-ttu-id="ec46c-108">刪除 DigitalTwinsInstance。</span><span class="sxs-lookup"><span data-stu-id="ec46c-108">Delete a DigitalTwinsInstance.</span></span>

## <span data-ttu-id="ec46c-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec46c-109">EXAMPLES</span></span>

### <span data-ttu-id="ec46c-110">範例1：依名稱移除 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ec46c-110">Example 1: Remove an AzDigitalTwinsInstance by name</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin


```

<span data-ttu-id="ec46c-111">這個命令會依名稱移除 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ec46c-111">This command removes an AzDigitalTwinsInstance by name</span></span>

### <span data-ttu-id="ec46c-112">範例2：以 InputObject 移除 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ec46c-112">Example 2: Remove an AzDigitalTwinsInstance by InputObject</span></span>
```powershell
PS C:\> $GetAzDigitalTwins =  Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsInstance -InputObject $GetAzDigitalTwins


```

<span data-ttu-id="ec46c-113">這個命令會依名稱移除 AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="ec46c-113">This command removes an AzDigitalTwinsInstance by name</span></span>

## <span data-ttu-id="ec46c-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec46c-114">PARAMETERS</span></span>

### <span data-ttu-id="ec46c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec46c-115">-AsJob</span></span>
<span data-ttu-id="ec46c-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ec46c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ec46c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec46c-117">-DefaultProfile</span></span>
<span data-ttu-id="ec46c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec46c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec46c-119">-InputObject</span></span>
<span data-ttu-id="ec46c-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ec46c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec46c-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec46c-121">-NoWait</span></span>
<span data-ttu-id="ec46c-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ec46c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec46c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec46c-123">-PassThru</span></span>
<span data-ttu-id="ec46c-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ec46c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec46c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec46c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec46c-126">包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46c-127">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="ec46c-127">-ResourceName</span></span>
<span data-ttu-id="ec46c-128">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec46c-129">-SubscriptionId</span></span>
<span data-ttu-id="ec46c-130">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec46c-130">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec46c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ec46c-131">-Confirm</span></span>
<span data-ttu-id="ec46c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec46c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec46c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec46c-133">-WhatIf</span></span>
<span data-ttu-id="ec46c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec46c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec46c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec46c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec46c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec46c-136">CommonParameters</span></span>
<span data-ttu-id="ec46c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec46c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec46c-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec46c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec46c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ec46c-139">INPUTS</span></span>

### <span data-ttu-id="ec46c-140">IDigitalTwinsIdentity （DigitalTwins）的</span><span class="sxs-lookup"><span data-stu-id="ec46c-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ec46c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ec46c-141">OUTPUTS</span></span>

### <span data-ttu-id="ec46c-142">IDigitalTwinsDescription （DigitalTwins）。 Api20201031。</span><span class="sxs-lookup"><span data-stu-id="ec46c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="ec46c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ec46c-143">NOTES</span></span>

<span data-ttu-id="ec46c-144">別名</span><span class="sxs-lookup"><span data-stu-id="ec46c-144">ALIASES</span></span>

<span data-ttu-id="ec46c-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ec46c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec46c-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ec46c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec46c-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ec46c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec46c-148">INPUTOBJECT <IDigitalTwinsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ec46c-148">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec46c-149">`[EndpointName <String>]`：端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-149">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ec46c-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ec46c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec46c-151">`[Location <String>]`： DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="ec46c-151">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ec46c-152">`[ResourceGroupName <String>]`：包含 DigitalTwinsInstance 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ec46c-153">`[ResourceName <String>]`： DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec46c-153">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ec46c-154">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec46c-154">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ec46c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec46c-155">RELATED LINKS</span></span>

