---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: 9ee07fc931e0760332456a83538621ded608049b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625327"
---
# <span data-ttu-id="348ef-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="348ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="348ef-102">SYNOPSIS</span></span>
<span data-ttu-id="348ef-103">停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="348ef-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="348ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="348ef-104">SYNTAX</span></span>

### <span data-ttu-id="348ef-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="348ef-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="348ef-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="348ef-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="348ef-107">說明</span><span class="sxs-lookup"><span data-stu-id="348ef-107">DESCRIPTION</span></span>
<span data-ttu-id="348ef-108">**AzureRmVM** Cmdlet 會停止 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="348ef-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="348ef-109">示例</span><span class="sxs-lookup"><span data-stu-id="348ef-109">EXAMPLES</span></span>

### <span data-ttu-id="348ef-110">範例1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="348ef-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="348ef-111">這個命令會在 ResourceGroup11 中停止名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="348ef-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="348ef-112">參數</span><span class="sxs-lookup"><span data-stu-id="348ef-112">PARAMETERS</span></span>

### <span data-ttu-id="348ef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="348ef-113">-AsJob</span></span>
<span data-ttu-id="348ef-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="348ef-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="348ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348ef-115">-DefaultProfile</span></span>
<span data-ttu-id="348ef-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="348ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348ef-117">-Force</span><span class="sxs-lookup"><span data-stu-id="348ef-117">-Force</span></span>
<span data-ttu-id="348ef-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="348ef-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="348ef-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="348ef-119">-Id</span></span>
<span data-ttu-id="348ef-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="348ef-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348ef-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="348ef-121">-Name</span></span>
<span data-ttu-id="348ef-122">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="348ef-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="348ef-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="348ef-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="348ef-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="348ef-125">-StayProvisioned</span></span>
<span data-ttu-id="348ef-126">這個 Cmdlet 會停止 VMSS 中的所有虛擬機器，但不會解除配置。</span><span class="sxs-lookup"><span data-stu-id="348ef-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="348ef-127">帳戶會針對已停止的虛擬機器收取費用。</span><span class="sxs-lookup"><span data-stu-id="348ef-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="348ef-128">-確認</span><span class="sxs-lookup"><span data-stu-id="348ef-128">-Confirm</span></span>
<span data-ttu-id="348ef-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="348ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="348ef-130">-WhatIf</span></span>
<span data-ttu-id="348ef-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="348ef-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="348ef-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="348ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348ef-133">CommonParameters</span></span>
<span data-ttu-id="348ef-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="348ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348ef-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="348ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348ef-136">輸入</span><span class="sxs-lookup"><span data-stu-id="348ef-136">INPUTS</span></span>

### <span data-ttu-id="348ef-137">System.object</span><span class="sxs-lookup"><span data-stu-id="348ef-137">System.String</span></span>

## <span data-ttu-id="348ef-138">輸出</span><span class="sxs-lookup"><span data-stu-id="348ef-138">OUTPUTS</span></span>

### <span data-ttu-id="348ef-139">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="348ef-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="348ef-140">筆記</span><span class="sxs-lookup"><span data-stu-id="348ef-140">NOTES</span></span>

## <span data-ttu-id="348ef-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="348ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="348ef-142">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="348ef-143">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="348ef-144">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="348ef-145">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-145">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="348ef-146">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-146">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="348ef-147">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="348ef-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


