---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966954"
---
# <span data-ttu-id="a034a-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a034a-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="a034a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a034a-102">SYNOPSIS</span></span>
<span data-ttu-id="a034a-103">移除在虛擬機器上套用的 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="a034a-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a034a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a034a-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a034a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a034a-105">DESCRIPTION</span></span>
<span data-ttu-id="a034a-106">**AzureVMBGInfoExtension** Cmdlet 會移除在虛擬機器上套用的 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="a034a-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a034a-107">示例</span><span class="sxs-lookup"><span data-stu-id="a034a-107">EXAMPLES</span></span>

### <span data-ttu-id="a034a-108">範例1：移除虛擬機器上的 BGInfo 延伸功能</span><span class="sxs-lookup"><span data-stu-id="a034a-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="a034a-109">這個命令會移除在虛擬機器上套用的 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="a034a-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a034a-110">參數</span><span class="sxs-lookup"><span data-stu-id="a034a-110">PARAMETERS</span></span>

### <span data-ttu-id="a034a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a034a-111">-InformationAction</span></span>
<span data-ttu-id="a034a-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a034a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a034a-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a034a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a034a-114">持續</span><span class="sxs-lookup"><span data-stu-id="a034a-114">Continue</span></span>
- <span data-ttu-id="a034a-115">理會</span><span class="sxs-lookup"><span data-stu-id="a034a-115">Ignore</span></span>
- <span data-ttu-id="a034a-116">看</span><span class="sxs-lookup"><span data-stu-id="a034a-116">Inquire</span></span>
- <span data-ttu-id="a034a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a034a-117">SilentlyContinue</span></span>
- <span data-ttu-id="a034a-118">停止</span><span class="sxs-lookup"><span data-stu-id="a034a-118">Stop</span></span>
- <span data-ttu-id="a034a-119">封存</span><span class="sxs-lookup"><span data-stu-id="a034a-119">Suspend</span></span>

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

### <span data-ttu-id="a034a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a034a-120">-InformationVariable</span></span>
<span data-ttu-id="a034a-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a034a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a034a-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a034a-122">-Profile</span></span>
<span data-ttu-id="a034a-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a034a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a034a-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a034a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a034a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="a034a-125">-VM</span></span>
<span data-ttu-id="a034a-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="a034a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a034a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a034a-127">CommonParameters</span></span>
<span data-ttu-id="a034a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a034a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a034a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a034a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a034a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a034a-130">INPUTS</span></span>

## <span data-ttu-id="a034a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a034a-131">OUTPUTS</span></span>

## <span data-ttu-id="a034a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a034a-132">NOTES</span></span>

## <span data-ttu-id="a034a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a034a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a034a-134">AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a034a-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="a034a-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a034a-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


