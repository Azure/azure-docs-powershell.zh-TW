---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613176"
---
# <span data-ttu-id="447f9-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="447f9-101">Set-AzVM</span></span>

## <span data-ttu-id="447f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="447f9-102">SYNOPSIS</span></span>
<span data-ttu-id="447f9-103">將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="447f9-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="447f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="447f9-104">SYNTAX</span></span>

### <span data-ttu-id="447f9-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="447f9-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="447f9-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="447f9-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="447f9-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="447f9-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="447f9-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="447f9-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="447f9-109">說明</span><span class="sxs-lookup"><span data-stu-id="447f9-109">DESCRIPTION</span></span>
<span data-ttu-id="447f9-110">**AzVM** Cmdlet 會將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="447f9-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="447f9-111">在執行此 Cmdlet 之前，請先登入虛擬機器，然後使用 Sysprep 來準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="447f9-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="447f9-112">示例</span><span class="sxs-lookup"><span data-stu-id="447f9-112">EXAMPLES</span></span>

### <span data-ttu-id="447f9-113">範例1：將虛擬機器標示為一般化</span><span class="sxs-lookup"><span data-stu-id="447f9-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="447f9-114">這個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="447f9-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="447f9-115">參數</span><span class="sxs-lookup"><span data-stu-id="447f9-115">PARAMETERS</span></span>

### <span data-ttu-id="447f9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="447f9-116">-AsJob</span></span>
<span data-ttu-id="447f9-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="447f9-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="447f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447f9-118">-DefaultProfile</span></span>
<span data-ttu-id="447f9-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="447f9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="447f9-120">-通用化</span><span class="sxs-lookup"><span data-stu-id="447f9-120">-Generalized</span></span>
<span data-ttu-id="447f9-121">表示此 Cmdlet 會將虛擬機器標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="447f9-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="447f9-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="447f9-122">-Id</span></span>
<span data-ttu-id="447f9-123">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="447f9-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447f9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="447f9-124">-Name</span></span>
<span data-ttu-id="447f9-125">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="447f9-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447f9-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="447f9-126">-NoWait</span></span>
<span data-ttu-id="447f9-127">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="447f9-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="447f9-128">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="447f9-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447f9-129">-重新部署</span><span class="sxs-lookup"><span data-stu-id="447f9-129">-Redeploy</span></span>
<span data-ttu-id="447f9-130">表示此 Cmdlet 會手動將虛擬機器 redeploys 至不同的 Azure 主機，以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="447f9-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="447f9-131">如果您重新部署虛擬機器，它會重新開機，這會導致暫時的磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="447f9-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="447f9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447f9-132">-ResourceGroupName</span></span>
<span data-ttu-id="447f9-133">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="447f9-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447f9-134">CommonParameters</span></span>
<span data-ttu-id="447f9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="447f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447f9-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="447f9-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447f9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="447f9-137">INPUTS</span></span>

### <span data-ttu-id="447f9-138">System.object</span><span class="sxs-lookup"><span data-stu-id="447f9-138">System.String</span></span>

## <span data-ttu-id="447f9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="447f9-139">OUTPUTS</span></span>

### <span data-ttu-id="447f9-140">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="447f9-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="447f9-141">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="447f9-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="447f9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="447f9-142">NOTES</span></span>

## <span data-ttu-id="447f9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="447f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="447f9-144">AzVM</span><span class="sxs-lookup"><span data-stu-id="447f9-144">Get-AzVM</span></span>](./Get-AzVM.md)


