---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794834"
---
# <span data-ttu-id="c0e26-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-101">Stop-AzVM</span></span>

## <span data-ttu-id="c0e26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0e26-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e26-103">停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c0e26-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="c0e26-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0e26-104">SYNTAX</span></span>

### <span data-ttu-id="c0e26-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="c0e26-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e26-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c0e26-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e26-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0e26-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e26-108">**AzVM** Cmdlet 會停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c0e26-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="c0e26-109">示例</span><span class="sxs-lookup"><span data-stu-id="c0e26-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e26-110">範例1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="c0e26-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="c0e26-111">這個命令會在 ResourceGroup11 中停止名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c0e26-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="c0e26-112">參數</span><span class="sxs-lookup"><span data-stu-id="c0e26-112">PARAMETERS</span></span>

### <span data-ttu-id="c0e26-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0e26-113">-AsJob</span></span>
<span data-ttu-id="c0e26-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="c0e26-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0e26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e26-115">-DefaultProfile</span></span>
<span data-ttu-id="c0e26-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0e26-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e26-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0e26-117">-Force</span></span>
<span data-ttu-id="c0e26-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c0e26-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0e26-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c0e26-119">-Id</span></span>
<span data-ttu-id="c0e26-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e26-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e26-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0e26-121">-Name</span></span>
<span data-ttu-id="c0e26-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e26-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="c0e26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e26-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0e26-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e26-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e26-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="c0e26-125">-StayProvisioned</span></span>
<span data-ttu-id="c0e26-126">這個 Cmdlet 會停止 VMSS 中的所有虛擬機器，但不會解除配置。</span><span class="sxs-lookup"><span data-stu-id="c0e26-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="c0e26-127">帳戶會針對已停止的虛擬機器收取費用。</span><span class="sxs-lookup"><span data-stu-id="c0e26-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="c0e26-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c0e26-128">-Confirm</span></span>
<span data-ttu-id="c0e26-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0e26-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e26-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e26-130">-WhatIf</span></span>
<span data-ttu-id="c0e26-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0e26-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0e26-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e26-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e26-133">CommonParameters</span></span>
<span data-ttu-id="c0e26-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0e26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e26-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0e26-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e26-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c0e26-136">INPUTS</span></span>

### <span data-ttu-id="c0e26-137">所有</span><span class="sxs-lookup"><span data-stu-id="c0e26-137">None</span></span>
<span data-ttu-id="c0e26-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c0e26-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0e26-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c0e26-139">OUTPUTS</span></span>

### <span data-ttu-id="c0e26-140">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c0e26-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="c0e26-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c0e26-141">NOTES</span></span>

## <span data-ttu-id="c0e26-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0e26-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0e26-143">AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c0e26-144">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="c0e26-145">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="c0e26-146">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="c0e26-147">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="c0e26-148">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="c0e26-148">Update-AzVM</span></span>](./Update-AzVM.md)


