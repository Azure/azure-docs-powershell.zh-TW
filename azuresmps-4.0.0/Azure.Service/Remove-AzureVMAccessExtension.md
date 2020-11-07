---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966956"
---
# <span data-ttu-id="41d03-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="41d03-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="41d03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41d03-102">SYNOPSIS</span></span>
<span data-ttu-id="41d03-103">移除在虛擬機器上套用的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="41d03-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="41d03-104">句法</span><span class="sxs-lookup"><span data-stu-id="41d03-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41d03-105">說明</span><span class="sxs-lookup"><span data-stu-id="41d03-105">DESCRIPTION</span></span>
<span data-ttu-id="41d03-106">**AzureVMAccessExtension** Cmdlet 會移除在虛擬機器上套用的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="41d03-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="41d03-107">示例</span><span class="sxs-lookup"><span data-stu-id="41d03-107">EXAMPLES</span></span>

### <span data-ttu-id="41d03-108">範例1：從虛擬機器移除 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="41d03-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="41d03-109">這個命令會從虛擬機器中移除 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="41d03-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="41d03-110">參數</span><span class="sxs-lookup"><span data-stu-id="41d03-110">PARAMETERS</span></span>

### <span data-ttu-id="41d03-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41d03-111">-InformationAction</span></span>
<span data-ttu-id="41d03-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="41d03-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41d03-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="41d03-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41d03-114">持續</span><span class="sxs-lookup"><span data-stu-id="41d03-114">Continue</span></span>
- <span data-ttu-id="41d03-115">理會</span><span class="sxs-lookup"><span data-stu-id="41d03-115">Ignore</span></span>
- <span data-ttu-id="41d03-116">看</span><span class="sxs-lookup"><span data-stu-id="41d03-116">Inquire</span></span>
- <span data-ttu-id="41d03-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41d03-117">SilentlyContinue</span></span>
- <span data-ttu-id="41d03-118">停止</span><span class="sxs-lookup"><span data-stu-id="41d03-118">Stop</span></span>
- <span data-ttu-id="41d03-119">封存</span><span class="sxs-lookup"><span data-stu-id="41d03-119">Suspend</span></span>

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

### <span data-ttu-id="41d03-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41d03-120">-InformationVariable</span></span>
<span data-ttu-id="41d03-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="41d03-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41d03-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="41d03-122">-Profile</span></span>
<span data-ttu-id="41d03-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="41d03-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41d03-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="41d03-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41d03-125">-VM</span><span class="sxs-lookup"><span data-stu-id="41d03-125">-VM</span></span>
<span data-ttu-id="41d03-126">指定這個 Cmdlet 移除 VMAccess 延伸的永久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="41d03-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="41d03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d03-127">CommonParameters</span></span>
<span data-ttu-id="41d03-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41d03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d03-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41d03-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d03-130">輸入</span><span class="sxs-lookup"><span data-stu-id="41d03-130">INPUTS</span></span>

## <span data-ttu-id="41d03-131">輸出</span><span class="sxs-lookup"><span data-stu-id="41d03-131">OUTPUTS</span></span>

## <span data-ttu-id="41d03-132">筆記</span><span class="sxs-lookup"><span data-stu-id="41d03-132">NOTES</span></span>

## <span data-ttu-id="41d03-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="41d03-133">RELATED LINKS</span></span>

[<span data-ttu-id="41d03-134">AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="41d03-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="41d03-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="41d03-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


