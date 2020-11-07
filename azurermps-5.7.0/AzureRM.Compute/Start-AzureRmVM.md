---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624191"
---
# <span data-ttu-id="8f7fb-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="8f7fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7fb-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f7fb-104">SYNTAX</span></span>

### <span data-ttu-id="8f7fb-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="8f7fb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7fb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8f7fb-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="8f7fb-107">DESCRIPTION</span></span>
<span data-ttu-id="8f7fb-108">**AzureRmVM** Cmdlet 會啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="8f7fb-109">示例</span><span class="sxs-lookup"><span data-stu-id="8f7fb-109">EXAMPLES</span></span>

### <span data-ttu-id="8f7fb-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8f7fb-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8f7fb-111">這個命令會在 ResourceGroup11 中啟動名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8f7fb-112">參數</span><span class="sxs-lookup"><span data-stu-id="8f7fb-112">PARAMETERS</span></span>

### <span data-ttu-id="8f7fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f7fb-113">-AsJob</span></span>
<span data-ttu-id="8f7fb-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8f7fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7fb-115">-DefaultProfile</span></span>
<span data-ttu-id="8f7fb-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7fb-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8f7fb-117">-Id</span></span>
<span data-ttu-id="8f7fb-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-118">The resource group name.</span></span>

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

### <span data-ttu-id="8f7fb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f7fb-119">-Name</span></span>
<span data-ttu-id="8f7fb-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="8f7fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f7fb-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8f7fb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8f7fb-123">-Confirm</span></span>
<span data-ttu-id="8f7fb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7fb-125">-WhatIf</span></span>
<span data-ttu-id="8f7fb-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f7fb-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7fb-128">CommonParameters</span></span>
<span data-ttu-id="8f7fb-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7fb-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7fb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8f7fb-131">INPUTS</span></span>

### <span data-ttu-id="8f7fb-132">所有</span><span class="sxs-lookup"><span data-stu-id="8f7fb-132">None</span></span>
<span data-ttu-id="8f7fb-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8f7fb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f7fb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8f7fb-134">OUTPUTS</span></span>

### <span data-ttu-id="8f7fb-135">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8f7fb-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8f7fb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8f7fb-136">NOTES</span></span>

## <span data-ttu-id="8f7fb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f7fb-137">RELATED LINKS</span></span>

[<span data-ttu-id="8f7fb-138">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8f7fb-139">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8f7fb-140">移除-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="8f7fb-141">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8f7fb-142">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="8f7fb-143">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f7fb-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


