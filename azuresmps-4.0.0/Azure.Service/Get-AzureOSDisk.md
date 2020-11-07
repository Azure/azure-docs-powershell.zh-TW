---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967778"
---
# <span data-ttu-id="a7299-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="a7299-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="a7299-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7299-102">SYNOPSIS</span></span>
<span data-ttu-id="a7299-103">取得 Azure 虛擬機器的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="a7299-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="a7299-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7299-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a7299-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7299-105">DESCRIPTION</span></span>
<span data-ttu-id="a7299-106">**AzureOSDisk** Cmdlet 會取得 Azure 虛擬機器的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="a7299-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="a7299-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7299-107">EXAMPLES</span></span>

### <span data-ttu-id="a7299-108">範例1：取得作業系統磁片</span><span class="sxs-lookup"><span data-stu-id="a7299-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="a7299-109">這個命令會透過使用 **VirtualMachine02 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7299-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a7299-110">命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7299-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a7299-111">目前的 Cmdlet 會取得該虛擬機器的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="a7299-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="a7299-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7299-112">PARAMETERS</span></span>

### <span data-ttu-id="a7299-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a7299-113">-InformationAction</span></span>
<span data-ttu-id="a7299-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a7299-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a7299-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a7299-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7299-116">持續</span><span class="sxs-lookup"><span data-stu-id="a7299-116">Continue</span></span>
- <span data-ttu-id="a7299-117">理會</span><span class="sxs-lookup"><span data-stu-id="a7299-117">Ignore</span></span>
- <span data-ttu-id="a7299-118">看</span><span class="sxs-lookup"><span data-stu-id="a7299-118">Inquire</span></span>
- <span data-ttu-id="a7299-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a7299-119">SilentlyContinue</span></span>
- <span data-ttu-id="a7299-120">停止</span><span class="sxs-lookup"><span data-stu-id="a7299-120">Stop</span></span>
- <span data-ttu-id="a7299-121">封存</span><span class="sxs-lookup"><span data-stu-id="a7299-121">Suspend</span></span>

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

### <span data-ttu-id="a7299-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a7299-122">-InformationVariable</span></span>
<span data-ttu-id="a7299-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a7299-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a7299-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a7299-124">-Profile</span></span>
<span data-ttu-id="a7299-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7299-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7299-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a7299-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7299-127">-VM</span><span class="sxs-lookup"><span data-stu-id="a7299-127">-VM</span></span>
<span data-ttu-id="a7299-128">指定此 Cmdlet 取得作業系統磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7299-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="a7299-129">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7299-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="a7299-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7299-130">CommonParameters</span></span>
<span data-ttu-id="a7299-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7299-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7299-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7299-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7299-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a7299-133">INPUTS</span></span>

## <span data-ttu-id="a7299-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a7299-134">OUTPUTS</span></span>

## <span data-ttu-id="a7299-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a7299-135">NOTES</span></span>

## <span data-ttu-id="a7299-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7299-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7299-137">AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="a7299-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="a7299-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="a7299-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


