---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968842"
---
# <span data-ttu-id="8d5c8-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="8d5c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5c8-103">停止虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="8d5c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d5c8-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8d5c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5c8-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8d5c8-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8d5c8-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8d5c8-109">**WAPackVM** Cmdlet 會停止虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="8d5c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="8d5c8-110">EXAMPLES</span></span>

### <span data-ttu-id="8d5c8-111">範例1：停止虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8d5c8-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="8d5c8-112">第一個命令會使用 **WAPackVM** Cmdlet 取得名為 ContosoV126 的虛擬機器，然後將該物件儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8d5c8-113">第二個命令會停止 $VirtualMachine 中儲存的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="8d5c8-114">參數</span><span class="sxs-lookup"><span data-stu-id="8d5c8-114">PARAMETERS</span></span>

### <span data-ttu-id="8d5c8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d5c8-115">-PassThru</span></span>
<span data-ttu-id="8d5c8-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8d5c8-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d5c8-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8d5c8-118">-Profile</span></span>
<span data-ttu-id="8d5c8-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d5c8-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d5c8-121">-關閉</span><span class="sxs-lookup"><span data-stu-id="8d5c8-121">-Shutdown</span></span>
<span data-ttu-id="8d5c8-122">表示 Cmdlet 會關閉虛擬機器的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="8d5c8-123">-VM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-123">-VM</span></span>
<span data-ttu-id="8d5c8-124">指定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="8d5c8-125">若要取得虛擬機器，請使用 **WAPackVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="8d5c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5c8-126">CommonParameters</span></span>
<span data-ttu-id="8d5c8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5c8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d5c8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5c8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8d5c8-129">INPUTS</span></span>

## <span data-ttu-id="8d5c8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8d5c8-130">OUTPUTS</span></span>

## <span data-ttu-id="8d5c8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8d5c8-131">NOTES</span></span>

## <span data-ttu-id="8d5c8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d5c8-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d5c8-133">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8d5c8-134">新-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8d5c8-135">移除-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="8d5c8-136">重新開機-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8d5c8-137">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8d5c8-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="8d5c8-139">開始-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8d5c8-140">暫停-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8d5c8-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


