---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8cdc8e49a78c4f2c2bfb88d42fe710ad783df97f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911237"
---
# <span data-ttu-id="3ae0f-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="3ae0f-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="3ae0f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ae0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae0f-103">建立或更新專用雲端</span><span class="sxs-lookup"><span data-stu-id="3ae0f-103">Create or update a private cloud</span></span>

## <span data-ttu-id="3ae0f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ae0f-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ae0f-105">描述</span><span class="sxs-lookup"><span data-stu-id="3ae0f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae0f-106">建立或更新專用雲端</span><span class="sxs-lookup"><span data-stu-id="3ae0f-106">Create or update a private cloud</span></span>

## <span data-ttu-id="3ae0f-107">例子</span><span class="sxs-lookup"><span data-stu-id="3ae0f-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae0f-108">範例 1：建立私人雲端</span><span class="sxs-lookup"><span data-stu-id="3ae0f-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="3ae0f-109">建立私人雲端</span><span class="sxs-lookup"><span data-stu-id="3ae0f-109">Create private cloud</span></span>

## <span data-ttu-id="3ae0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ae0f-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae0f-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="3ae0f-111">-AcceptEULA</span></span>
<span data-ttu-id="3ae0f-112">接受 AVS 的 EULA，未提供此參數即會彈出法律術語</span><span class="sxs-lookup"><span data-stu-id="3ae0f-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="3ae0f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ae0f-113">-AsJob</span></span>
<span data-ttu-id="3ae0f-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="3ae0f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3ae0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae0f-115">-DefaultProfile</span></span>
<span data-ttu-id="3ae0f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae0f-117">-網際網路</span><span class="sxs-lookup"><span data-stu-id="3ae0f-117">-Internet</span></span>
<span data-ttu-id="3ae0f-118">啟用或停用網際網路連接</span><span class="sxs-lookup"><span data-stu-id="3ae0f-118">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="3ae0f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="3ae0f-119">-Location</span></span>
<span data-ttu-id="3ae0f-120">資源位置</span><span class="sxs-lookup"><span data-stu-id="3ae0f-120">Resource location</span></span>

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

### <span data-ttu-id="3ae0f-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="3ae0f-121">-ManagementClusterSize</span></span>
<span data-ttu-id="3ae0f-122">組大小</span><span class="sxs-lookup"><span data-stu-id="3ae0f-122">The cluster size</span></span>

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

### <span data-ttu-id="3ae0f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ae0f-123">-Name</span></span>
<span data-ttu-id="3ae0f-124">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="3ae0f-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="3ae0f-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="3ae0f-125">-NetworkBlock</span></span>
<span data-ttu-id="3ae0f-126">您訂閱和內部部署中的 VNet 位址區塊應該是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="3ae0f-127">確認 CIDR 格式符合 (A.B.C.D/X) 其中 A、B、C、D 介於 0 到 255 之間，而 X 介於 0 到 22 之間</span><span class="sxs-lookup"><span data-stu-id="3ae0f-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="3ae0f-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ae0f-128">-NoWait</span></span>
<span data-ttu-id="3ae0f-129">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="3ae0f-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ae0f-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="3ae0f-130">-NsxtPassword</span></span>
<span data-ttu-id="3ae0f-131">或者，在建立私人雲端時設定 NSX-T Manager 密碼</span><span class="sxs-lookup"><span data-stu-id="3ae0f-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="3ae0f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae0f-132">-ResourceGroupName</span></span>
<span data-ttu-id="3ae0f-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-133">The name of the resource group.</span></span>
<span data-ttu-id="3ae0f-134">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3ae0f-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="3ae0f-135">-Sku</span></span>
<span data-ttu-id="3ae0f-136">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="3ae0f-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ae0f-137">-SubscriptionId</span></span>
<span data-ttu-id="3ae0f-138">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3ae0f-139">-標記</span><span class="sxs-lookup"><span data-stu-id="3ae0f-139">-Tag</span></span>
<span data-ttu-id="3ae0f-140">資源標記</span><span class="sxs-lookup"><span data-stu-id="3ae0f-140">Resource tags</span></span>

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

### <span data-ttu-id="3ae0f-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="3ae0f-141">-VcenterPassword</span></span>
<span data-ttu-id="3ae0f-142">或者，在建立專用雲端時設定 vCenter 系統管理員密碼</span><span class="sxs-lookup"><span data-stu-id="3ae0f-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="3ae0f-143">-確認</span><span class="sxs-lookup"><span data-stu-id="3ae0f-143">-Confirm</span></span>
<span data-ttu-id="3ae0f-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae0f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae0f-145">-WhatIf</span></span>
<span data-ttu-id="3ae0f-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae0f-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae0f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae0f-148">CommonParameters</span></span>
<span data-ttu-id="3ae0f-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ae0f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae0f-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae0f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae0f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="3ae0f-151">INPUTS</span></span>

## <span data-ttu-id="3ae0f-152">輸出</span><span class="sxs-lookup"><span data-stu-id="3ae0f-152">OUTPUTS</span></span>

### <span data-ttu-id="3ae0f-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="3ae0f-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="3ae0f-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3ae0f-154">NOTES</span></span>

<span data-ttu-id="3ae0f-155">別名</span><span class="sxs-lookup"><span data-stu-id="3ae0f-155">ALIASES</span></span>

## <span data-ttu-id="3ae0f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ae0f-156">RELATED LINKS</span></span>

