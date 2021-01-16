---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273584"
---
# <span data-ttu-id="73ebd-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="73ebd-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="73ebd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="73ebd-103">刪除指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="73ebd-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="73ebd-104">句法</span><span class="sxs-lookup"><span data-stu-id="73ebd-104">SYNTAX</span></span>

### <span data-ttu-id="73ebd-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="73ebd-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="73ebd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73ebd-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73ebd-107">說明</span><span class="sxs-lookup"><span data-stu-id="73ebd-107">DESCRIPTION</span></span>
<span data-ttu-id="73ebd-108">刪除指定的 Azure 專用 HSM。</span><span class="sxs-lookup"><span data-stu-id="73ebd-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="73ebd-109">示例</span><span class="sxs-lookup"><span data-stu-id="73ebd-109">EXAMPLES</span></span>

### <span data-ttu-id="73ebd-110">範例1：依名稱移除專用 HSM</span><span class="sxs-lookup"><span data-stu-id="73ebd-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="73ebd-111">此 commnad 會依名稱 (HSM) 移除硬體安全模組。</span><span class="sxs-lookup"><span data-stu-id="73ebd-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="73ebd-112">範例2：移除專用的 HSM （依物件）</span><span class="sxs-lookup"><span data-stu-id="73ebd-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="73ebd-113">此 commnad 會移除專用的 HSM by 物件。</span><span class="sxs-lookup"><span data-stu-id="73ebd-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="73ebd-114">參數</span><span class="sxs-lookup"><span data-stu-id="73ebd-114">PARAMETERS</span></span>

### <span data-ttu-id="73ebd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73ebd-115">-AsJob</span></span>
<span data-ttu-id="73ebd-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="73ebd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="73ebd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ebd-117">-DefaultProfile</span></span>
<span data-ttu-id="73ebd-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73ebd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ebd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73ebd-119">-InputObject</span></span>
<span data-ttu-id="73ebd-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="73ebd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ebd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="73ebd-121">-Name</span></span>
<span data-ttu-id="73ebd-122">要刪除的專用 HSM 的名稱</span><span class="sxs-lookup"><span data-stu-id="73ebd-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="73ebd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73ebd-123">-NoWait</span></span>
<span data-ttu-id="73ebd-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="73ebd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="73ebd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73ebd-125">-PassThru</span></span>
<span data-ttu-id="73ebd-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="73ebd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73ebd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ebd-127">-ResourceGroupName</span></span>
<span data-ttu-id="73ebd-128">專用 HSM 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73ebd-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="73ebd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73ebd-129">-SubscriptionId</span></span>
<span data-ttu-id="73ebd-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="73ebd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="73ebd-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="73ebd-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73ebd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="73ebd-132">-Confirm</span></span>
<span data-ttu-id="73ebd-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ebd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ebd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ebd-134">-WhatIf</span></span>
<span data-ttu-id="73ebd-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73ebd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ebd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ebd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ebd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ebd-137">CommonParameters</span></span>
<span data-ttu-id="73ebd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73ebd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ebd-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73ebd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ebd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="73ebd-140">INPUTS</span></span>

### <span data-ttu-id="73ebd-141">IDedicatedHsmIdentity （DedicatedHsm）的</span><span class="sxs-lookup"><span data-stu-id="73ebd-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="73ebd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="73ebd-142">OUTPUTS</span></span>

### <span data-ttu-id="73ebd-143">System.object</span><span class="sxs-lookup"><span data-stu-id="73ebd-143">System.Boolean</span></span>

## <span data-ttu-id="73ebd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="73ebd-144">NOTES</span></span>

<span data-ttu-id="73ebd-145">別名</span><span class="sxs-lookup"><span data-stu-id="73ebd-145">ALIASES</span></span>

<span data-ttu-id="73ebd-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="73ebd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73ebd-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="73ebd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73ebd-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="73ebd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73ebd-149">INPUTOBJECT <IDedicatedHsmIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="73ebd-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73ebd-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="73ebd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73ebd-151">`[Name <String>]`：專用 Hsm 的名稱</span><span class="sxs-lookup"><span data-stu-id="73ebd-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="73ebd-152">`[ResourceGroupName <String>]`：資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73ebd-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="73ebd-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="73ebd-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="73ebd-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="73ebd-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="73ebd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="73ebd-155">RELATED LINKS</span></span>

