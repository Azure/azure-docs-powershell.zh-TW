---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794841"
---
# <span data-ttu-id="f818e-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-101">Start-AzVM</span></span>

## <span data-ttu-id="f818e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f818e-102">SYNOPSIS</span></span>
<span data-ttu-id="f818e-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f818e-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f818e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f818e-104">SYNTAX</span></span>

### <span data-ttu-id="f818e-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="f818e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f818e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f818e-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f818e-107">說明</span><span class="sxs-lookup"><span data-stu-id="f818e-107">DESCRIPTION</span></span>
<span data-ttu-id="f818e-108">**AzVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f818e-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f818e-109">示例</span><span class="sxs-lookup"><span data-stu-id="f818e-109">EXAMPLES</span></span>

### <span data-ttu-id="f818e-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="f818e-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f818e-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f818e-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f818e-112">參數</span><span class="sxs-lookup"><span data-stu-id="f818e-112">PARAMETERS</span></span>

### <span data-ttu-id="f818e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f818e-113">-AsJob</span></span>
<span data-ttu-id="f818e-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="f818e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f818e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f818e-115">-DefaultProfile</span></span>
<span data-ttu-id="f818e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f818e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f818e-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f818e-117">-Id</span></span>
<span data-ttu-id="f818e-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f818e-118">The resource group name.</span></span>

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

### <span data-ttu-id="f818e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f818e-119">-Name</span></span>
<span data-ttu-id="f818e-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="f818e-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="f818e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f818e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f818e-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f818e-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f818e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f818e-123">-Confirm</span></span>
<span data-ttu-id="f818e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f818e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f818e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f818e-125">-WhatIf</span></span>
<span data-ttu-id="f818e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f818e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f818e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f818e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f818e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f818e-128">CommonParameters</span></span>
<span data-ttu-id="f818e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f818e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f818e-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f818e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f818e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f818e-131">INPUTS</span></span>

### <span data-ttu-id="f818e-132">所有</span><span class="sxs-lookup"><span data-stu-id="f818e-132">None</span></span>
<span data-ttu-id="f818e-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f818e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f818e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f818e-134">OUTPUTS</span></span>

### <span data-ttu-id="f818e-135">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f818e-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f818e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f818e-136">NOTES</span></span>

## <span data-ttu-id="f818e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f818e-137">RELATED LINKS</span></span>

[<span data-ttu-id="f818e-138">AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f818e-139">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f818e-140">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f818e-141">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f818e-142">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f818e-143">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="f818e-143">Update-AzVM</span></span>](./Update-AzVM.md)


