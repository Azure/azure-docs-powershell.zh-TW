---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133379"
---
# <span data-ttu-id="6d000-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="6d000-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="6d000-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d000-102">SYNOPSIS</span></span>
<span data-ttu-id="6d000-103">建立或更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="6d000-103">Create or update a private cloud</span></span>

## <span data-ttu-id="6d000-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d000-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d000-105">說明</span><span class="sxs-lookup"><span data-stu-id="6d000-105">DESCRIPTION</span></span>
<span data-ttu-id="6d000-106">建立或更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="6d000-106">Create or update a private cloud</span></span>

## <span data-ttu-id="6d000-107">示例</span><span class="sxs-lookup"><span data-stu-id="6d000-107">EXAMPLES</span></span>

### <span data-ttu-id="6d000-108">範例1：建立私有雲端</span><span class="sxs-lookup"><span data-stu-id="6d000-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="6d000-109">建立私有雲端</span><span class="sxs-lookup"><span data-stu-id="6d000-109">Create private cloud</span></span>

## <span data-ttu-id="6d000-110">參數</span><span class="sxs-lookup"><span data-stu-id="6d000-110">PARAMETERS</span></span>

### <span data-ttu-id="6d000-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="6d000-111">-AcceptEULA</span></span>
<span data-ttu-id="6d000-112">接受 AVS 的 EULA，法律詞彙將會彈出，但不提供此參數</span><span class="sxs-lookup"><span data-stu-id="6d000-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="6d000-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d000-113">-AsJob</span></span>
<span data-ttu-id="6d000-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6d000-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6d000-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d000-115">-DefaultProfile</span></span>
<span data-ttu-id="6d000-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d000-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d000-117">-網際網路</span><span class="sxs-lookup"><span data-stu-id="6d000-117">-Internet</span></span>
<span data-ttu-id="6d000-118">已啟用或停用網際網路連線</span><span class="sxs-lookup"><span data-stu-id="6d000-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d000-119">-位置</span><span class="sxs-lookup"><span data-stu-id="6d000-119">-Location</span></span>
<span data-ttu-id="6d000-120">資源位置</span><span class="sxs-lookup"><span data-stu-id="6d000-120">Resource location</span></span>

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

### <span data-ttu-id="6d000-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="6d000-121">-ManagementClusterSize</span></span>
<span data-ttu-id="6d000-122">群集大小</span><span class="sxs-lookup"><span data-stu-id="6d000-122">The cluster size</span></span>

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

### <span data-ttu-id="6d000-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d000-123">-Name</span></span>
<span data-ttu-id="6d000-124">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="6d000-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="6d000-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="6d000-125">-NetworkBlock</span></span>
<span data-ttu-id="6d000-126">在您的訂閱和內部部署中，位址區塊應該是在 VNet 中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6d000-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="6d000-127">請確定 CIDR 格式符合 (A、B、C、D 在0到255之間，而 X 介於0和22之間的) </span><span class="sxs-lookup"><span data-stu-id="6d000-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="6d000-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d000-128">-NoWait</span></span>
<span data-ttu-id="6d000-129">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6d000-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d000-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="6d000-130">-NsxtPassword</span></span>
<span data-ttu-id="6d000-131">或者，您也可以在建立私有雲端時，設定 NSX T 管理員密碼</span><span class="sxs-lookup"><span data-stu-id="6d000-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="6d000-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d000-132">-ResourceGroupName</span></span>
<span data-ttu-id="6d000-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d000-133">The name of the resource group.</span></span>
<span data-ttu-id="6d000-134">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6d000-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6d000-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="6d000-135">-Sku</span></span>
<span data-ttu-id="6d000-136">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d000-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="6d000-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d000-137">-SubscriptionId</span></span>
<span data-ttu-id="6d000-138">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="6d000-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6d000-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d000-139">-Tag</span></span>
<span data-ttu-id="6d000-140">資源標記</span><span class="sxs-lookup"><span data-stu-id="6d000-140">Resource tags</span></span>

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

### <span data-ttu-id="6d000-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="6d000-141">-VcenterPassword</span></span>
<span data-ttu-id="6d000-142">或者，您也可以在建立私有雲端時設定 vCenter 管理員密碼</span><span class="sxs-lookup"><span data-stu-id="6d000-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="6d000-143">-確認</span><span class="sxs-lookup"><span data-stu-id="6d000-143">-Confirm</span></span>
<span data-ttu-id="6d000-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d000-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d000-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d000-145">-WhatIf</span></span>
<span data-ttu-id="6d000-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d000-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d000-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d000-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d000-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d000-148">CommonParameters</span></span>
<span data-ttu-id="6d000-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d000-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d000-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d000-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d000-151">輸入</span><span class="sxs-lookup"><span data-stu-id="6d000-151">INPUTS</span></span>

## <span data-ttu-id="6d000-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6d000-152">OUTPUTS</span></span>

### <span data-ttu-id="6d000-153">IPrivateCloud 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="6d000-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="6d000-154">筆記</span><span class="sxs-lookup"><span data-stu-id="6d000-154">NOTES</span></span>

<span data-ttu-id="6d000-155">別名</span><span class="sxs-lookup"><span data-stu-id="6d000-155">ALIASES</span></span>

## <span data-ttu-id="6d000-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d000-156">RELATED LINKS</span></span>

