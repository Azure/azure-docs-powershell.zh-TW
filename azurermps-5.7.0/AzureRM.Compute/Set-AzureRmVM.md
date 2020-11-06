---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444700"
---
# <span data-ttu-id="434fc-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="434fc-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="434fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="434fc-102">SYNOPSIS</span></span>
<span data-ttu-id="434fc-103">將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="434fc-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="434fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="434fc-104">SYNTAX</span></span>

### <span data-ttu-id="434fc-105">GeneralizeResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="434fc-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434fc-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="434fc-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434fc-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="434fc-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434fc-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="434fc-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="434fc-109">說明</span><span class="sxs-lookup"><span data-stu-id="434fc-109">DESCRIPTION</span></span>
<span data-ttu-id="434fc-110">**AzureRmVM** Cmdlet 會將虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="434fc-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="434fc-111">在執行此 Cmdlet 之前，請先登入虛擬機器，然後使用 Sysprep 來準備硬碟。</span><span class="sxs-lookup"><span data-stu-id="434fc-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="434fc-112">示例</span><span class="sxs-lookup"><span data-stu-id="434fc-112">EXAMPLES</span></span>

### <span data-ttu-id="434fc-113">範例1：將虛擬機器標示為一般化</span><span class="sxs-lookup"><span data-stu-id="434fc-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="434fc-114">這個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="434fc-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="434fc-115">參數</span><span class="sxs-lookup"><span data-stu-id="434fc-115">PARAMETERS</span></span>

### <span data-ttu-id="434fc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="434fc-116">-AsJob</span></span>
<span data-ttu-id="434fc-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="434fc-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434fc-118">-DefaultProfile</span></span>
<span data-ttu-id="434fc-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="434fc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-120">-通用化</span><span class="sxs-lookup"><span data-stu-id="434fc-120">-Generalized</span></span>
<span data-ttu-id="434fc-121">表示此 Cmdlet 會將虛擬機器標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="434fc-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="434fc-122">-Id</span></span>
<span data-ttu-id="434fc-123">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="434fc-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="434fc-124">-Name</span></span>
<span data-ttu-id="434fc-125">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="434fc-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-126">-重新部署</span><span class="sxs-lookup"><span data-stu-id="434fc-126">-Redeploy</span></span>
<span data-ttu-id="434fc-127">表示此 Cmdlet 會手動將虛擬機器 redeploys 至不同的 Azure 主機，以修正任何問題。</span><span class="sxs-lookup"><span data-stu-id="434fc-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="434fc-128">如果您重新部署虛擬機器，它會重新開機，這會導致暫時的磁片磁碟機資料遺失。</span><span class="sxs-lookup"><span data-stu-id="434fc-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="434fc-130">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="434fc-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434fc-131">CommonParameters</span></span>
<span data-ttu-id="434fc-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="434fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434fc-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="434fc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434fc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="434fc-134">INPUTS</span></span>

### <span data-ttu-id="434fc-135">所有</span><span class="sxs-lookup"><span data-stu-id="434fc-135">None</span></span>
<span data-ttu-id="434fc-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="434fc-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="434fc-137">輸出</span><span class="sxs-lookup"><span data-stu-id="434fc-137">OUTPUTS</span></span>

### <span data-ttu-id="434fc-138">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="434fc-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="434fc-139">筆記</span><span class="sxs-lookup"><span data-stu-id="434fc-139">NOTES</span></span>

## <span data-ttu-id="434fc-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="434fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="434fc-141">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="434fc-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


