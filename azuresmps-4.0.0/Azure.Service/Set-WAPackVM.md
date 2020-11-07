---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968831"
---
# <span data-ttu-id="bb7de-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-101">Set-WAPackVM</span></span>

## <span data-ttu-id="bb7de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb7de-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7de-103">變更虛擬機器的大小屬性。</span><span class="sxs-lookup"><span data-stu-id="bb7de-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="bb7de-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb7de-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb7de-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb7de-105">DESCRIPTION</span></span>
<span data-ttu-id="bb7de-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="bb7de-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="bb7de-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb7de-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bb7de-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="bb7de-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bb7de-109">**WAPackVM** Cmdlet 會變更虛擬機器的大小屬性。</span><span class="sxs-lookup"><span data-stu-id="bb7de-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="bb7de-110">示例</span><span class="sxs-lookup"><span data-stu-id="bb7de-110">EXAMPLES</span></span>

### <span data-ttu-id="bb7de-111">範例1：指定虛擬機器的大小</span><span class="sxs-lookup"><span data-stu-id="bb7de-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="bb7de-112">第一個命令會使用 **WAPackVM** Cmdlet 取得名為 ContosoV126 的虛擬機器，然後將該物件儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="bb7de-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="bb7de-113">第二個命令會使用 **WAPackVMSizeProfile** Cmdlet 取得名為 MediumSizeVM 的大小設定檔，然後將該物件儲存在 $SizeProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="bb7de-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="bb7de-114">最後一個命令會將儲存在 $SizeProfile 中的大小設定檔，指派給儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bb7de-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="bb7de-115">參數</span><span class="sxs-lookup"><span data-stu-id="bb7de-115">PARAMETERS</span></span>

### <span data-ttu-id="bb7de-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb7de-116">-PassThru</span></span>
<span data-ttu-id="bb7de-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="bb7de-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb7de-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bb7de-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb7de-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bb7de-119">-Profile</span></span>
<span data-ttu-id="bb7de-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb7de-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb7de-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bb7de-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb7de-122">-VM</span><span class="sxs-lookup"><span data-stu-id="bb7de-122">-VM</span></span>
<span data-ttu-id="bb7de-123">指定虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bb7de-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="bb7de-124">若要取得虛擬機器，請使用 **WAPackVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb7de-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="bb7de-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="bb7de-125">-VMSizeProfile</span></span>
<span data-ttu-id="bb7de-126">將虛擬機器的大小設定檔指定為 **HardwareProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb7de-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="bb7de-127">若要取得大小設定檔，請使用 **WAPackVMSizeProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb7de-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7de-128">CommonParameters</span></span>
<span data-ttu-id="bb7de-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb7de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7de-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb7de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7de-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bb7de-131">INPUTS</span></span>

## <span data-ttu-id="bb7de-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bb7de-132">OUTPUTS</span></span>

## <span data-ttu-id="bb7de-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bb7de-133">NOTES</span></span>

## <span data-ttu-id="bb7de-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb7de-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb7de-135">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="bb7de-136">新-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="bb7de-137">移除-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="bb7de-138">重新開機-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="bb7de-139">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="bb7de-140">開始-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="bb7de-141">停止 WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="bb7de-142">暫停-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="bb7de-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="bb7de-143">WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="bb7de-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


