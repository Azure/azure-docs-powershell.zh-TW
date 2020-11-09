---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286711"
---
# <span data-ttu-id="93a25-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="93a25-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="93a25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93a25-102">SYNOPSIS</span></span>
<span data-ttu-id="93a25-103">建立或更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="93a25-103">Create or update a private cloud</span></span>

## <span data-ttu-id="93a25-104">句法</span><span class="sxs-lookup"><span data-stu-id="93a25-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93a25-105">說明</span><span class="sxs-lookup"><span data-stu-id="93a25-105">DESCRIPTION</span></span>
<span data-ttu-id="93a25-106">建立或更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="93a25-106">Create or update a private cloud</span></span>

## <span data-ttu-id="93a25-107">示例</span><span class="sxs-lookup"><span data-stu-id="93a25-107">EXAMPLES</span></span>

### <span data-ttu-id="93a25-108">範例1：建立私有雲端</span><span class="sxs-lookup"><span data-stu-id="93a25-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="93a25-109">建立私有雲端</span><span class="sxs-lookup"><span data-stu-id="93a25-109">Create private cloud</span></span>

## <span data-ttu-id="93a25-110">參數</span><span class="sxs-lookup"><span data-stu-id="93a25-110">PARAMETERS</span></span>

### <span data-ttu-id="93a25-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93a25-111">-AsJob</span></span>
<span data-ttu-id="93a25-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="93a25-112">Run the command as a job</span></span>

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

### <span data-ttu-id="93a25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a25-113">-DefaultProfile</span></span>
<span data-ttu-id="93a25-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93a25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a25-115">-網際網路</span><span class="sxs-lookup"><span data-stu-id="93a25-115">-Internet</span></span>
<span data-ttu-id="93a25-116">已啟用或停用網際網路連線</span><span class="sxs-lookup"><span data-stu-id="93a25-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-117">-位置</span><span class="sxs-lookup"><span data-stu-id="93a25-117">-Location</span></span>
<span data-ttu-id="93a25-118">資源位置</span><span class="sxs-lookup"><span data-stu-id="93a25-118">Resource location</span></span>

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

### <span data-ttu-id="93a25-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="93a25-119">-ManagementClusterSize</span></span>
<span data-ttu-id="93a25-120">群集大小</span><span class="sxs-lookup"><span data-stu-id="93a25-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="93a25-121">-Name</span></span>
<span data-ttu-id="93a25-122">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="93a25-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="93a25-123">-NetworkBlock</span></span>
<span data-ttu-id="93a25-124">在您的訂閱和內部部署中，位址區塊應該是在 VNet 中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="93a25-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="93a25-125">請確定 CIDR 格式符合 (A、B、C、D 在0到255之間，而 X 介於0和22之間的) </span><span class="sxs-lookup"><span data-stu-id="93a25-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="93a25-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93a25-126">-NoWait</span></span>
<span data-ttu-id="93a25-127">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="93a25-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93a25-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="93a25-128">-NsxtPassword</span></span>
<span data-ttu-id="93a25-129">或者，您也可以在建立私有雲端時，設定 NSX T 管理員密碼</span><span class="sxs-lookup"><span data-stu-id="93a25-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a25-130">-ResourceGroupName</span></span>
<span data-ttu-id="93a25-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93a25-131">The name of the resource group.</span></span>
<span data-ttu-id="93a25-132">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="93a25-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="93a25-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="93a25-133">-Sku</span></span>
<span data-ttu-id="93a25-134">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="93a25-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="93a25-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93a25-135">-SubscriptionId</span></span>
<span data-ttu-id="93a25-136">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="93a25-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="93a25-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="93a25-137">-Tag</span></span>
<span data-ttu-id="93a25-138">資源標記</span><span class="sxs-lookup"><span data-stu-id="93a25-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="93a25-139">-VcenterPassword</span></span>
<span data-ttu-id="93a25-140">或者，您也可以在建立私有雲端時設定 vCenter 管理員密碼</span><span class="sxs-lookup"><span data-stu-id="93a25-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a25-141">-確認</span><span class="sxs-lookup"><span data-stu-id="93a25-141">-Confirm</span></span>
<span data-ttu-id="93a25-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93a25-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a25-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a25-143">-WhatIf</span></span>
<span data-ttu-id="93a25-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93a25-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a25-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93a25-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a25-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a25-146">CommonParameters</span></span>
<span data-ttu-id="93a25-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93a25-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a25-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93a25-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a25-149">輸入</span><span class="sxs-lookup"><span data-stu-id="93a25-149">INPUTS</span></span>

## <span data-ttu-id="93a25-150">輸出</span><span class="sxs-lookup"><span data-stu-id="93a25-150">OUTPUTS</span></span>

### <span data-ttu-id="93a25-151">IPrivateCloud 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="93a25-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="93a25-152">筆記</span><span class="sxs-lookup"><span data-stu-id="93a25-152">NOTES</span></span>

<span data-ttu-id="93a25-153">別名</span><span class="sxs-lookup"><span data-stu-id="93a25-153">ALIASES</span></span>

## <span data-ttu-id="93a25-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="93a25-154">RELATED LINKS</span></span>

