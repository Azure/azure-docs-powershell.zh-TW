---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967989"
---
# <span data-ttu-id="8cb16-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8cb16-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="8cb16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cb16-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb16-103">取得虛擬機器上的 Azure 診斷延伸設定。</span><span class="sxs-lookup"><span data-stu-id="8cb16-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="8cb16-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cb16-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8cb16-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cb16-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb16-106">**AzureVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Microsoft Azure 診斷延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="8cb16-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="8cb16-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cb16-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb16-108">範例1：取得套用至虛擬機器的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="8cb16-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="8cb16-109">這個命令會取得套用至指定虛擬機器的診斷延伸，$VM 儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="8cb16-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="8cb16-110">參數</span><span class="sxs-lookup"><span data-stu-id="8cb16-110">PARAMETERS</span></span>

### <span data-ttu-id="8cb16-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8cb16-111">-InformationAction</span></span>
<span data-ttu-id="8cb16-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8cb16-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8cb16-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8cb16-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8cb16-114">持續</span><span class="sxs-lookup"><span data-stu-id="8cb16-114">Continue</span></span>
- <span data-ttu-id="8cb16-115">理會</span><span class="sxs-lookup"><span data-stu-id="8cb16-115">Ignore</span></span>
- <span data-ttu-id="8cb16-116">看</span><span class="sxs-lookup"><span data-stu-id="8cb16-116">Inquire</span></span>
- <span data-ttu-id="8cb16-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8cb16-117">SilentlyContinue</span></span>
- <span data-ttu-id="8cb16-118">停止</span><span class="sxs-lookup"><span data-stu-id="8cb16-118">Stop</span></span>
- <span data-ttu-id="8cb16-119">封存</span><span class="sxs-lookup"><span data-stu-id="8cb16-119">Suspend</span></span>

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

### <span data-ttu-id="8cb16-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8cb16-120">-InformationVariable</span></span>
<span data-ttu-id="8cb16-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8cb16-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8cb16-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8cb16-122">-Profile</span></span>
<span data-ttu-id="8cb16-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cb16-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cb16-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8cb16-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cb16-125">-VM</span><span class="sxs-lookup"><span data-stu-id="8cb16-125">-VM</span></span>
<span data-ttu-id="8cb16-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="8cb16-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8cb16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb16-127">CommonParameters</span></span>
<span data-ttu-id="8cb16-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cb16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb16-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cb16-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb16-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8cb16-130">INPUTS</span></span>

## <span data-ttu-id="8cb16-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8cb16-131">OUTPUTS</span></span>

## <span data-ttu-id="8cb16-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8cb16-132">NOTES</span></span>

## <span data-ttu-id="8cb16-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cb16-133">RELATED LINKS</span></span>

[<span data-ttu-id="8cb16-134">移除-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8cb16-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="8cb16-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8cb16-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


