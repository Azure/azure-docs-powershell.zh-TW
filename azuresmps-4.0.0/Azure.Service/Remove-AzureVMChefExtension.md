---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966951"
---
# <span data-ttu-id="b8c60-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b8c60-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="b8c60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c60-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c60-103">移除在虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="b8c60-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b8c60-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c60-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8c60-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8c60-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c60-106">**AzureVMChefExtension** Cmdlet 會刪除在虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="b8c60-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b8c60-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8c60-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c60-108">範例1：移除在指定的虛擬機器上套用的主廚延伸</span><span class="sxs-lookup"><span data-stu-id="b8c60-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="b8c60-109">這個命令會移除在虛擬機器上套用的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="b8c60-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b8c60-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8c60-110">PARAMETERS</span></span>

### <span data-ttu-id="b8c60-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8c60-111">-InformationAction</span></span>
<span data-ttu-id="b8c60-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b8c60-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8c60-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b8c60-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c60-114">持續</span><span class="sxs-lookup"><span data-stu-id="b8c60-114">Continue</span></span>
- <span data-ttu-id="b8c60-115">理會</span><span class="sxs-lookup"><span data-stu-id="b8c60-115">Ignore</span></span>
- <span data-ttu-id="b8c60-116">看</span><span class="sxs-lookup"><span data-stu-id="b8c60-116">Inquire</span></span>
- <span data-ttu-id="b8c60-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8c60-117">SilentlyContinue</span></span>
- <span data-ttu-id="b8c60-118">停止</span><span class="sxs-lookup"><span data-stu-id="b8c60-118">Stop</span></span>
- <span data-ttu-id="b8c60-119">封存</span><span class="sxs-lookup"><span data-stu-id="b8c60-119">Suspend</span></span>

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

### <span data-ttu-id="b8c60-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8c60-120">-InformationVariable</span></span>
<span data-ttu-id="b8c60-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b8c60-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8c60-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b8c60-122">-Profile</span></span>
<span data-ttu-id="b8c60-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b8c60-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8c60-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b8c60-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8c60-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b8c60-125">-VM</span></span>
<span data-ttu-id="b8c60-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="b8c60-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b8c60-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c60-127">CommonParameters</span></span>
<span data-ttu-id="b8c60-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c60-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c60-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8c60-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c60-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c60-130">INPUTS</span></span>

## <span data-ttu-id="b8c60-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c60-131">OUTPUTS</span></span>

## <span data-ttu-id="b8c60-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c60-132">NOTES</span></span>

## <span data-ttu-id="b8c60-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c60-133">RELATED LINKS</span></span>

[<span data-ttu-id="b8c60-134">AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b8c60-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="b8c60-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b8c60-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


