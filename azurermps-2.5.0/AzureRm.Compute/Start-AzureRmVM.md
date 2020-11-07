---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801334"
---
# <span data-ttu-id="aec1c-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="aec1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aec1c-102">SYNOPSIS</span></span>
<span data-ttu-id="aec1c-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aec1c-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="aec1c-104">SYNTAX</span></span>

### <span data-ttu-id="aec1c-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="aec1c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec1c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aec1c-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec1c-107">說明</span><span class="sxs-lookup"><span data-stu-id="aec1c-107">DESCRIPTION</span></span>
<span data-ttu-id="aec1c-108">**AzureRmVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aec1c-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="aec1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="aec1c-109">EXAMPLES</span></span>

### <span data-ttu-id="aec1c-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="aec1c-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="aec1c-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aec1c-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="aec1c-112">參數</span><span class="sxs-lookup"><span data-stu-id="aec1c-112">PARAMETERS</span></span>

### <span data-ttu-id="aec1c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aec1c-113">-AsJob</span></span>
<span data-ttu-id="aec1c-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="aec1c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aec1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec1c-115">-DefaultProfile</span></span>
<span data-ttu-id="aec1c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aec1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec1c-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="aec1c-117">-Id</span></span>
<span data-ttu-id="aec1c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aec1c-118">The resource group name.</span></span>

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

### <span data-ttu-id="aec1c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="aec1c-119">-Name</span></span>
<span data-ttu-id="aec1c-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="aec1c-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="aec1c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec1c-121">-ResourceGroupName</span></span>
<span data-ttu-id="aec1c-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aec1c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aec1c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="aec1c-123">-Confirm</span></span>
<span data-ttu-id="aec1c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aec1c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec1c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec1c-125">-WhatIf</span></span>
<span data-ttu-id="aec1c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aec1c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aec1c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aec1c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec1c-128">CommonParameters</span></span>
<span data-ttu-id="aec1c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aec1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec1c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aec1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec1c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="aec1c-131">INPUTS</span></span>

### <span data-ttu-id="aec1c-132">所有</span><span class="sxs-lookup"><span data-stu-id="aec1c-132">None</span></span>
<span data-ttu-id="aec1c-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="aec1c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aec1c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="aec1c-134">OUTPUTS</span></span>

### <span data-ttu-id="aec1c-135">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="aec1c-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="aec1c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="aec1c-136">NOTES</span></span>

## <span data-ttu-id="aec1c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="aec1c-137">RELATED LINKS</span></span>

[<span data-ttu-id="aec1c-138">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="aec1c-139">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="aec1c-140">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="aec1c-141">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="aec1c-142">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="aec1c-143">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aec1c-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


