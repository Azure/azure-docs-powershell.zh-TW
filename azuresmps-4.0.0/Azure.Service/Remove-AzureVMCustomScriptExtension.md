---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967894"
---
# <span data-ttu-id="8fbe3-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8fbe3-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="8fbe3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbe3-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="8fbe3-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fbe3-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8fbe3-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fbe3-105">DESCRIPTION</span></span>
<span data-ttu-id="8fbe3-106">**AzureVMCustomScriptExtension** Cmdlet 會將自訂腳本副檔名從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="8fbe3-107">示例</span><span class="sxs-lookup"><span data-stu-id="8fbe3-107">EXAMPLES</span></span>

### <span data-ttu-id="8fbe3-108">範例1：移除虛擬機器自訂腳本副檔名</span><span class="sxs-lookup"><span data-stu-id="8fbe3-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="8fbe3-109">這個命令會從指定的虛擬機器中移除 Azure 虛擬機器自訂腳本副檔名，並儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="8fbe3-110">參數</span><span class="sxs-lookup"><span data-stu-id="8fbe3-110">PARAMETERS</span></span>

### <span data-ttu-id="8fbe3-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8fbe3-111">-InformationAction</span></span>
<span data-ttu-id="8fbe3-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8fbe3-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8fbe3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fbe3-114">持續</span><span class="sxs-lookup"><span data-stu-id="8fbe3-114">Continue</span></span>
- <span data-ttu-id="8fbe3-115">理會</span><span class="sxs-lookup"><span data-stu-id="8fbe3-115">Ignore</span></span>
- <span data-ttu-id="8fbe3-116">看</span><span class="sxs-lookup"><span data-stu-id="8fbe3-116">Inquire</span></span>
- <span data-ttu-id="8fbe3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8fbe3-117">SilentlyContinue</span></span>
- <span data-ttu-id="8fbe3-118">停止</span><span class="sxs-lookup"><span data-stu-id="8fbe3-118">Stop</span></span>
- <span data-ttu-id="8fbe3-119">封存</span><span class="sxs-lookup"><span data-stu-id="8fbe3-119">Suspend</span></span>

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

### <span data-ttu-id="8fbe3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8fbe3-120">-InformationVariable</span></span>
<span data-ttu-id="8fbe3-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8fbe3-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8fbe3-122">-Profile</span></span>
<span data-ttu-id="8fbe3-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8fbe3-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8fbe3-125">-VM</span><span class="sxs-lookup"><span data-stu-id="8fbe3-125">-VM</span></span>
<span data-ttu-id="8fbe3-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8fbe3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbe3-127">CommonParameters</span></span>
<span data-ttu-id="8fbe3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbe3-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fbe3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbe3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8fbe3-130">INPUTS</span></span>

## <span data-ttu-id="8fbe3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8fbe3-131">OUTPUTS</span></span>

## <span data-ttu-id="8fbe3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8fbe3-132">NOTES</span></span>

## <span data-ttu-id="8fbe3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fbe3-133">RELATED LINKS</span></span>

[<span data-ttu-id="8fbe3-134">AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8fbe3-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="8fbe3-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8fbe3-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


