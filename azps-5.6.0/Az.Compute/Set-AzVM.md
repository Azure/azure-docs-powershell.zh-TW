---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b42f456b45de0e78b9d9e0c371dca950ada88ded
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908297"
---
# <span data-ttu-id="82271-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="82271-101">Set-AzVM</span></span>

## <span data-ttu-id="82271-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82271-102">SYNOPSIS</span></span>
<span data-ttu-id="82271-103">將虛擬機器標記為通用。</span><span class="sxs-lookup"><span data-stu-id="82271-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="82271-104">語法</span><span class="sxs-lookup"><span data-stu-id="82271-104">SYNTAX</span></span>

### <span data-ttu-id="82271-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="82271-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82271-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82271-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82271-108">模擬EvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82271-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82271-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82271-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82271-112">模擬EvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="82271-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82271-113">描述</span><span class="sxs-lookup"><span data-stu-id="82271-113">DESCRIPTION</span></span>
<span data-ttu-id="82271-114">**Set-AzMS** Cmdlet 將虛擬機器標記為通用。</span><span class="sxs-lookup"><span data-stu-id="82271-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="82271-115">執行此 Cmdlet 之前，請登入虛擬機器並使用 Sysprep 準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="82271-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="82271-116">例子</span><span class="sxs-lookup"><span data-stu-id="82271-116">EXAMPLES</span></span>

### <span data-ttu-id="82271-117">範例 1：將虛擬機器標記為通用</span><span class="sxs-lookup"><span data-stu-id="82271-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="82271-118">此命令將 VirtualMachine07 的虛擬機器標記為通用。</span><span class="sxs-lookup"><span data-stu-id="82271-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="82271-119">參數</span><span class="sxs-lookup"><span data-stu-id="82271-119">PARAMETERS</span></span>

### <span data-ttu-id="82271-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82271-120">-AsJob</span></span>
<span data-ttu-id="82271-121">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="82271-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="82271-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82271-122">-DefaultProfile</span></span>
<span data-ttu-id="82271-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="82271-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82271-124">-一般化</span><span class="sxs-lookup"><span data-stu-id="82271-124">-Generalized</span></span>
<span data-ttu-id="82271-125">表示此 Cmdlet 將虛擬機器標記為通用。</span><span class="sxs-lookup"><span data-stu-id="82271-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="82271-126">-Id</span><span class="sxs-lookup"><span data-stu-id="82271-126">-Id</span></span>
<span data-ttu-id="82271-127">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82271-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="82271-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="82271-128">-Name</span></span>
<span data-ttu-id="82271-129">指定此 Cmdlet 操作之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="82271-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="82271-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82271-130">-NoWait</span></span>
<span data-ttu-id="82271-131">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="82271-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="82271-132">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="82271-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="82271-133">-重新應用程式</span><span class="sxs-lookup"><span data-stu-id="82271-133">-Reapply</span></span>
<span data-ttu-id="82271-134">若要重新應用程式虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="82271-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="82271-135">-重新部署</span><span class="sxs-lookup"><span data-stu-id="82271-135">-Redeploy</span></span>
<span data-ttu-id="82271-136">表示此 Cmdlet 手動將虛擬機器重新部署到不同的 Azure 主機以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="82271-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="82271-137">如果您重新部署虛擬機器，虛擬機器會重新開機，這導致暫時磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="82271-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="82271-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82271-138">-ResourceGroupName</span></span>
<span data-ttu-id="82271-139">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="82271-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="82271-140">-模擬Eviction</span><span class="sxs-lookup"><span data-stu-id="82271-140">-SimulateEviction</span></span>
<span data-ttu-id="82271-141">表示此 Cmdlet 模擬了 spot 虛擬機器的模擬。</span><span class="sxs-lookup"><span data-stu-id="82271-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="82271-142">系統將在呼叫 API 的 30 分鐘內完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="82271-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="82271-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82271-143">CommonParameters</span></span>
<span data-ttu-id="82271-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82271-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82271-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82271-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82271-146">輸入</span><span class="sxs-lookup"><span data-stu-id="82271-146">INPUTS</span></span>

### <span data-ttu-id="82271-147">System.String</span><span class="sxs-lookup"><span data-stu-id="82271-147">System.String</span></span>

## <span data-ttu-id="82271-148">輸出</span><span class="sxs-lookup"><span data-stu-id="82271-148">OUTPUTS</span></span>

### <span data-ttu-id="82271-149">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="82271-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="82271-150">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="82271-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="82271-151">筆記</span><span class="sxs-lookup"><span data-stu-id="82271-151">NOTES</span></span>

## <span data-ttu-id="82271-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="82271-152">RELATED LINKS</span></span>

[<span data-ttu-id="82271-153">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="82271-153">Get-AzVM</span></span>](./Get-AzVM.md)


