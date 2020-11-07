---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967893"
---
# <span data-ttu-id="8a048-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8a048-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="8a048-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a048-102">SYNOPSIS</span></span>
<span data-ttu-id="8a048-103">從虛擬機器中移除 Azure DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="8a048-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="8a048-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a048-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a048-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a048-105">DESCRIPTION</span></span>
<span data-ttu-id="8a048-106">**AzureVMDscExtension** Cmdlet 會從虛擬機器中移除 Azure DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="8a048-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="8a048-107">這個 Cmdlet 的輸出需要以管道傳送方式傳送給 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a048-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="8a048-108">示例</span><span class="sxs-lookup"><span data-stu-id="8a048-108">EXAMPLES</span></span>

### <span data-ttu-id="8a048-109">範例1：從虛擬機器移除 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="8a048-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="8a048-110">此命令會從虛擬機器中移除 Azure DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="8a048-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="8a048-111">參數</span><span class="sxs-lookup"><span data-stu-id="8a048-111">PARAMETERS</span></span>

### <span data-ttu-id="8a048-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a048-112">-InformationAction</span></span>
<span data-ttu-id="8a048-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8a048-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a048-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8a048-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a048-115">持續</span><span class="sxs-lookup"><span data-stu-id="8a048-115">Continue</span></span>
- <span data-ttu-id="8a048-116">理會</span><span class="sxs-lookup"><span data-stu-id="8a048-116">Ignore</span></span>
- <span data-ttu-id="8a048-117">看</span><span class="sxs-lookup"><span data-stu-id="8a048-117">Inquire</span></span>
- <span data-ttu-id="8a048-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a048-118">SilentlyContinue</span></span>
- <span data-ttu-id="8a048-119">停止</span><span class="sxs-lookup"><span data-stu-id="8a048-119">Stop</span></span>
- <span data-ttu-id="8a048-120">封存</span><span class="sxs-lookup"><span data-stu-id="8a048-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a048-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a048-121">-InformationVariable</span></span>
<span data-ttu-id="8a048-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8a048-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a048-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8a048-123">-Profile</span></span>
<span data-ttu-id="8a048-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a048-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a048-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8a048-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a048-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8a048-126">-VM</span></span>
<span data-ttu-id="8a048-127">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="8a048-127">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a048-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8a048-128">-Confirm</span></span>
<span data-ttu-id="8a048-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a048-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a048-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a048-130">-WhatIf</span></span>
<span data-ttu-id="8a048-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a048-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a048-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a048-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a048-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a048-133">CommonParameters</span></span>
<span data-ttu-id="8a048-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a048-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a048-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a048-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a048-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8a048-136">INPUTS</span></span>

## <span data-ttu-id="8a048-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8a048-137">OUTPUTS</span></span>

## <span data-ttu-id="8a048-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8a048-138">NOTES</span></span>

## <span data-ttu-id="8a048-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a048-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a048-140">AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8a048-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="8a048-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8a048-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="8a048-142">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="8a048-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


