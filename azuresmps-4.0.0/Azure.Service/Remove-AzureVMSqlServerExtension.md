---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966940"
---
# <span data-ttu-id="c8ee0-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c8ee0-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="c8ee0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ee0-103">從虛擬機器物件中移除 Azure 虛擬機器 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="c8ee0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8ee0-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8ee0-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ee0-106">**AzureVMSqlServerExtension** Cmdlet 會從虛擬機器物件中移除 Azure 虛擬機器 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="c8ee0-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ee0-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="c8ee0-108">1:</span></span>
```

```

## <span data-ttu-id="c8ee0-109">參數</span><span class="sxs-lookup"><span data-stu-id="c8ee0-109">PARAMETERS</span></span>

### <span data-ttu-id="c8ee0-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8ee0-110">-InformationAction</span></span>
<span data-ttu-id="c8ee0-111">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8ee0-112">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8ee0-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8ee0-113">持續</span><span class="sxs-lookup"><span data-stu-id="c8ee0-113">Continue</span></span>
- <span data-ttu-id="c8ee0-114">理會</span><span class="sxs-lookup"><span data-stu-id="c8ee0-114">Ignore</span></span>
- <span data-ttu-id="c8ee0-115">看</span><span class="sxs-lookup"><span data-stu-id="c8ee0-115">Inquire</span></span>
- <span data-ttu-id="c8ee0-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8ee0-116">SilentlyContinue</span></span>
- <span data-ttu-id="c8ee0-117">停止</span><span class="sxs-lookup"><span data-stu-id="c8ee0-117">Stop</span></span>
- <span data-ttu-id="c8ee0-118">封存</span><span class="sxs-lookup"><span data-stu-id="c8ee0-118">Suspend</span></span>

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

### <span data-ttu-id="c8ee0-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8ee0-119">-InformationVariable</span></span>
<span data-ttu-id="c8ee0-120">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8ee0-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c8ee0-121">-Profile</span></span>
<span data-ttu-id="c8ee0-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8ee0-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8ee0-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c8ee0-124">-VM</span></span>
<span data-ttu-id="c8ee0-125">指定這個 Cmdlet 移除副檔名的永久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="c8ee0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ee0-126">CommonParameters</span></span>
<span data-ttu-id="c8ee0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ee0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8ee0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ee0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c8ee0-129">INPUTS</span></span>

## <span data-ttu-id="c8ee0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c8ee0-130">OUTPUTS</span></span>

## <span data-ttu-id="c8ee0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c8ee0-131">NOTES</span></span>

## <span data-ttu-id="c8ee0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8ee0-132">RELATED LINKS</span></span>

[<span data-ttu-id="c8ee0-133">AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c8ee0-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="c8ee0-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c8ee0-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


