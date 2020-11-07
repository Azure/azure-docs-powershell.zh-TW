---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968854"
---
# <span data-ttu-id="26f9f-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="26f9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="26f9f-103">移除虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="26f9f-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="26f9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f9f-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f9f-105">說明</span><span class="sxs-lookup"><span data-stu-id="26f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="26f9f-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="26f9f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="26f9f-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f9f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="26f9f-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="26f9f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="26f9f-109">**WAPackVM** Cmdlet 會移除虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="26f9f-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="26f9f-110">示例</span><span class="sxs-lookup"><span data-stu-id="26f9f-110">EXAMPLES</span></span>

### <span data-ttu-id="26f9f-111">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="26f9f-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="26f9f-112">第一個命令會使用 **WAPackVM** Cmdlet 取得名為 ContosoV126 的虛擬機器，然後將該物件儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="26f9f-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="26f9f-113">第二個命令會移除 $VirtualMachine 中儲存的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f9f-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="26f9f-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f9f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="26f9f-115">範例2：不需確認即移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="26f9f-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="26f9f-116">第一個命令會使用 **WAPackVM** Cmdlet 取得名為 ContosoV126 的虛擬機器，然後將該物件儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="26f9f-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="26f9f-117">第二個命令會移除 $VirtualMachine 中儲存的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f9f-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="26f9f-118">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="26f9f-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="26f9f-119">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f9f-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="26f9f-120">參數</span><span class="sxs-lookup"><span data-stu-id="26f9f-120">PARAMETERS</span></span>

### <span data-ttu-id="26f9f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="26f9f-121">-Force</span></span>
<span data-ttu-id="26f9f-122">表示 Cmdlet 會移除虛擬機器，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f9f-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="26f9f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f9f-123">-PassThru</span></span>
<span data-ttu-id="26f9f-124">表示 Cmdlet 傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="26f9f-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="26f9f-125">如果操作成功，則 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="26f9f-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="26f9f-126">否則，它會傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="26f9f-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="26f9f-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="26f9f-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26f9f-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="26f9f-128">-Profile</span></span>
<span data-ttu-id="26f9f-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="26f9f-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26f9f-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="26f9f-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-131">-VM</span><span class="sxs-lookup"><span data-stu-id="26f9f-131">-VM</span></span>
<span data-ttu-id="26f9f-132">指定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f9f-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="26f9f-133">若要取得虛擬機器，請使用 **WAPackVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f9f-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="26f9f-134">-Confirm</span></span>
<span data-ttu-id="26f9f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f9f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f9f-136">-WhatIf</span></span>
<span data-ttu-id="26f9f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f9f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f9f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f9f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f9f-139">CommonParameters</span></span>
<span data-ttu-id="26f9f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f9f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26f9f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f9f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="26f9f-142">INPUTS</span></span>

## <span data-ttu-id="26f9f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="26f9f-143">OUTPUTS</span></span>

## <span data-ttu-id="26f9f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="26f9f-144">NOTES</span></span>

## <span data-ttu-id="26f9f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f9f-145">RELATED LINKS</span></span>

[<span data-ttu-id="26f9f-146">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="26f9f-147">新-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="26f9f-148">重新開機-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="26f9f-149">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="26f9f-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="26f9f-151">開始-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="26f9f-152">停止 WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="26f9f-153">暫停-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="26f9f-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


