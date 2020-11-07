---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966981"
---
# <span data-ttu-id="d99d6-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d99d6-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="d99d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d99d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d99d6-103">取得在虛擬機器上套用的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="d99d6-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d99d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d99d6-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d99d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="d99d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d99d6-106">**AzureVMAccessExtension** Cmdlet 會取得在虛擬機器上套用的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="d99d6-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d99d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="d99d6-107">EXAMPLES</span></span>

### <span data-ttu-id="d99d6-108">範例1：取得虛擬機器的 VMAccess 延伸功能</span><span class="sxs-lookup"><span data-stu-id="d99d6-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="d99d6-109">這個命令會取得虛擬機器的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="d99d6-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="d99d6-110">參數</span><span class="sxs-lookup"><span data-stu-id="d99d6-110">PARAMETERS</span></span>

### <span data-ttu-id="d99d6-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d99d6-111">-InformationAction</span></span>
<span data-ttu-id="d99d6-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="d99d6-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d99d6-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d99d6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d99d6-114">持續</span><span class="sxs-lookup"><span data-stu-id="d99d6-114">Continue</span></span>
- <span data-ttu-id="d99d6-115">理會</span><span class="sxs-lookup"><span data-stu-id="d99d6-115">Ignore</span></span>
- <span data-ttu-id="d99d6-116">看</span><span class="sxs-lookup"><span data-stu-id="d99d6-116">Inquire</span></span>
- <span data-ttu-id="d99d6-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d99d6-117">SilentlyContinue</span></span>
- <span data-ttu-id="d99d6-118">停止</span><span class="sxs-lookup"><span data-stu-id="d99d6-118">Stop</span></span>
- <span data-ttu-id="d99d6-119">封存</span><span class="sxs-lookup"><span data-stu-id="d99d6-119">Suspend</span></span>

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

### <span data-ttu-id="d99d6-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d99d6-120">-InformationVariable</span></span>
<span data-ttu-id="d99d6-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="d99d6-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d99d6-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d99d6-122">-Profile</span></span>
<span data-ttu-id="d99d6-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d99d6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d99d6-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d99d6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d99d6-125">-VM</span><span class="sxs-lookup"><span data-stu-id="d99d6-125">-VM</span></span>
<span data-ttu-id="d99d6-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="d99d6-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d99d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99d6-127">CommonParameters</span></span>
<span data-ttu-id="d99d6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d99d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99d6-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d99d6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99d6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d99d6-130">INPUTS</span></span>

## <span data-ttu-id="d99d6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d99d6-131">OUTPUTS</span></span>

## <span data-ttu-id="d99d6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d99d6-132">NOTES</span></span>

## <span data-ttu-id="d99d6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d99d6-133">RELATED LINKS</span></span>

[<span data-ttu-id="d99d6-134">移除-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d99d6-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="d99d6-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d99d6-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


