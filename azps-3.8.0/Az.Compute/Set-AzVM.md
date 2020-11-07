---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956861"
---
# <span data-ttu-id="c9a3f-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="c9a3f-101">Set-AzVM</span></span>

## <span data-ttu-id="c9a3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a3f-103">將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="c9a3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9a3f-104">SYNTAX</span></span>

### <span data-ttu-id="c9a3f-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="c9a3f-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3f-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3f-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3f-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a3f-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a3f-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9a3f-111">說明</span><span class="sxs-lookup"><span data-stu-id="c9a3f-111">DESCRIPTION</span></span>
<span data-ttu-id="c9a3f-112">**AzVM** Cmdlet 會將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="c9a3f-113">在執行此 Cmdlet 之前，請先登入虛擬機器，然後使用 Sysprep 來準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="c9a3f-114">示例</span><span class="sxs-lookup"><span data-stu-id="c9a3f-114">EXAMPLES</span></span>

### <span data-ttu-id="c9a3f-115">範例1：將虛擬機器標示為一般化</span><span class="sxs-lookup"><span data-stu-id="c9a3f-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="c9a3f-116">這個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="c9a3f-117">參數</span><span class="sxs-lookup"><span data-stu-id="c9a3f-117">PARAMETERS</span></span>

### <span data-ttu-id="c9a3f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9a3f-118">-AsJob</span></span>
<span data-ttu-id="c9a3f-119">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c9a3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a3f-120">-DefaultProfile</span></span>
<span data-ttu-id="c9a3f-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9a3f-122">-通用化</span><span class="sxs-lookup"><span data-stu-id="c9a3f-122">-Generalized</span></span>
<span data-ttu-id="c9a3f-123">表示此 Cmdlet 會將虛擬機器標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="c9a3f-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c9a3f-124">-Id</span></span>
<span data-ttu-id="c9a3f-125">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a3f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9a3f-126">-Name</span></span>
<span data-ttu-id="c9a3f-127">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a3f-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c9a3f-128">-NoWait</span></span>
<span data-ttu-id="c9a3f-129">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c9a3f-130">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c9a3f-131">-重新套用</span><span class="sxs-lookup"><span data-stu-id="c9a3f-131">-Reapply</span></span>
<span data-ttu-id="c9a3f-132">若要重新套用虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-132">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="c9a3f-133">-重新部署</span><span class="sxs-lookup"><span data-stu-id="c9a3f-133">-Redeploy</span></span>
<span data-ttu-id="c9a3f-134">表示此 Cmdlet 會手動將虛擬機器 redeploys 至不同的 Azure 主機，以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="c9a3f-135">如果您重新部署虛擬機器，它會重新開機，這會導致暫時的磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="c9a3f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a3f-136">-ResourceGroupName</span></span>
<span data-ttu-id="c9a3f-137">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a3f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a3f-138">CommonParameters</span></span>
<span data-ttu-id="c9a3f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a3f-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9a3f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a3f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c9a3f-141">INPUTS</span></span>

### <span data-ttu-id="c9a3f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c9a3f-142">System.String</span></span>

## <span data-ttu-id="c9a3f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c9a3f-143">OUTPUTS</span></span>

### <span data-ttu-id="c9a3f-144">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c9a3f-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="c9a3f-145">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c9a3f-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9a3f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c9a3f-146">NOTES</span></span>

## <span data-ttu-id="c9a3f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9a3f-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9a3f-148">AzVM</span><span class="sxs-lookup"><span data-stu-id="c9a3f-148">Get-AzVM</span></span>](./Get-AzVM.md)


