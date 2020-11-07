---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966978"
---
# <span data-ttu-id="0218c-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="0218c-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="0218c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0218c-102">SYNOPSIS</span></span>
<span data-ttu-id="0218c-103">取得在虛擬機器上套用的 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="0218c-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="0218c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0218c-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0218c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0218c-105">DESCRIPTION</span></span>
<span data-ttu-id="0218c-106">**AzureVMBGInfoExtension** Cmdlet 會取得在虛擬機器上套用的 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="0218c-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="0218c-107">示例</span><span class="sxs-lookup"><span data-stu-id="0218c-107">EXAMPLES</span></span>

### <span data-ttu-id="0218c-108">範例1：取得在指定的虛擬機器上套用的 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="0218c-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="0218c-109">這個命令會取得在指定的虛擬機器上套用的 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="0218c-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="0218c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0218c-110">PARAMETERS</span></span>

### <span data-ttu-id="0218c-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0218c-111">-InformationAction</span></span>
<span data-ttu-id="0218c-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0218c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0218c-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0218c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0218c-114">持續</span><span class="sxs-lookup"><span data-stu-id="0218c-114">Continue</span></span>
- <span data-ttu-id="0218c-115">理會</span><span class="sxs-lookup"><span data-stu-id="0218c-115">Ignore</span></span>
- <span data-ttu-id="0218c-116">看</span><span class="sxs-lookup"><span data-stu-id="0218c-116">Inquire</span></span>
- <span data-ttu-id="0218c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0218c-117">SilentlyContinue</span></span>
- <span data-ttu-id="0218c-118">停止</span><span class="sxs-lookup"><span data-stu-id="0218c-118">Stop</span></span>
- <span data-ttu-id="0218c-119">封存</span><span class="sxs-lookup"><span data-stu-id="0218c-119">Suspend</span></span>

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

### <span data-ttu-id="0218c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0218c-120">-InformationVariable</span></span>
<span data-ttu-id="0218c-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0218c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0218c-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0218c-122">-Profile</span></span>
<span data-ttu-id="0218c-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0218c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0218c-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0218c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0218c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="0218c-125">-VM</span></span>
<span data-ttu-id="0218c-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0218c-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="0218c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0218c-127">CommonParameters</span></span>
<span data-ttu-id="0218c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0218c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0218c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0218c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0218c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0218c-130">INPUTS</span></span>

## <span data-ttu-id="0218c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0218c-131">OUTPUTS</span></span>

## <span data-ttu-id="0218c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0218c-132">NOTES</span></span>

## <span data-ttu-id="0218c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0218c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0218c-134">移除-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="0218c-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="0218c-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="0218c-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


