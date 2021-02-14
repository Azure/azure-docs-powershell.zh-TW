---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143358"
---
# <span data-ttu-id="a6724-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6724-101">Set-AzVM</span></span>

## <span data-ttu-id="a6724-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6724-102">SYNOPSIS</span></span>
<span data-ttu-id="a6724-103">將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="a6724-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="a6724-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6724-104">SYNTAX</span></span>

### <span data-ttu-id="a6724-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="a6724-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6724-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6724-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6724-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6724-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6724-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6724-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6724-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a6724-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6724-113">說明</span><span class="sxs-lookup"><span data-stu-id="a6724-113">DESCRIPTION</span></span>
<span data-ttu-id="a6724-114">**AzVM** Cmdlet 會將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="a6724-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="a6724-115">在執行此 Cmdlet 之前，請先登入虛擬機器，然後使用 Sysprep 來準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="a6724-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="a6724-116">示例</span><span class="sxs-lookup"><span data-stu-id="a6724-116">EXAMPLES</span></span>

### <span data-ttu-id="a6724-117">範例1：將虛擬機器標示為一般化</span><span class="sxs-lookup"><span data-stu-id="a6724-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="a6724-118">這個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="a6724-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="a6724-119">參數</span><span class="sxs-lookup"><span data-stu-id="a6724-119">PARAMETERS</span></span>

### <span data-ttu-id="a6724-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6724-120">-AsJob</span></span>
<span data-ttu-id="a6724-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a6724-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6724-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6724-122">-DefaultProfile</span></span>
<span data-ttu-id="a6724-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6724-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-124">-通用化</span><span class="sxs-lookup"><span data-stu-id="a6724-124">-Generalized</span></span>
<span data-ttu-id="a6724-125">表示此 Cmdlet 會將虛擬機器標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="a6724-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a6724-126">-Id</span></span>
<span data-ttu-id="a6724-127">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6724-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6724-128">-Name</span></span>
<span data-ttu-id="a6724-129">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="a6724-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6724-130">-NoWait</span></span>
<span data-ttu-id="a6724-131">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="a6724-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a6724-132">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="a6724-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-133">-重新套用</span><span class="sxs-lookup"><span data-stu-id="a6724-133">-Reapply</span></span>
<span data-ttu-id="a6724-134">若要重新套用虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a6724-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-135">-重新部署</span><span class="sxs-lookup"><span data-stu-id="a6724-135">-Redeploy</span></span>
<span data-ttu-id="a6724-136">表示此 Cmdlet 會手動將虛擬機器 redeploys 至不同的 Azure 主機，以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="a6724-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="a6724-137">如果您重新部署虛擬機器，它會重新開機，這會導致暫時的磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="a6724-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6724-138">-ResourceGroupName</span></span>
<span data-ttu-id="a6724-139">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6724-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="a6724-140">-SimulateEviction</span></span>
<span data-ttu-id="a6724-141">表示此 Cmdlet 會類比位置虛擬機器的逐出。</span><span class="sxs-lookup"><span data-stu-id="a6724-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="a6724-142">逐出將在呼叫 API 30 分鐘內發生。</span><span class="sxs-lookup"><span data-stu-id="a6724-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6724-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6724-143">CommonParameters</span></span>
<span data-ttu-id="a6724-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6724-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6724-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6724-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6724-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a6724-146">INPUTS</span></span>

### <span data-ttu-id="a6724-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a6724-147">System.String</span></span>

## <span data-ttu-id="a6724-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a6724-148">OUTPUTS</span></span>

### <span data-ttu-id="a6724-149">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a6724-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a6724-150">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a6724-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a6724-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a6724-151">NOTES</span></span>

## <span data-ttu-id="a6724-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6724-152">RELATED LINKS</span></span>

[<span data-ttu-id="a6724-153">AzVM</span><span class="sxs-lookup"><span data-stu-id="a6724-153">Get-AzVM</span></span>](./Get-AzVM.md)


