---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967976"
---
# <span data-ttu-id="ce06a-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ce06a-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="ce06a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce06a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce06a-103">從輸入圖像內容取得磁片設定集物件。</span><span class="sxs-lookup"><span data-stu-id="ce06a-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="ce06a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce06a-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ce06a-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce06a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce06a-106">**AzureVMImageDiskConfigSet** Cmdlet 會從輸入影像內容取得磁片設定集物件。</span><span class="sxs-lookup"><span data-stu-id="ce06a-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="ce06a-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce06a-107">EXAMPLES</span></span>

### <span data-ttu-id="ce06a-108">範例1：從虛擬機器取得磁片設定集物件</span><span class="sxs-lookup"><span data-stu-id="ce06a-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="ce06a-109">這個命令會從虛擬機器中取得磁片設定集物件。</span><span class="sxs-lookup"><span data-stu-id="ce06a-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="ce06a-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce06a-110">PARAMETERS</span></span>

### <span data-ttu-id="ce06a-111">-ImageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ce06a-111">-ImageContext</span></span>
<span data-ttu-id="ce06a-112">指定虛擬機器影像內容。</span><span class="sxs-lookup"><span data-stu-id="ce06a-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce06a-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ce06a-113">-InformationAction</span></span>
<span data-ttu-id="ce06a-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ce06a-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ce06a-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ce06a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce06a-116">持續</span><span class="sxs-lookup"><span data-stu-id="ce06a-116">Continue</span></span>
- <span data-ttu-id="ce06a-117">理會</span><span class="sxs-lookup"><span data-stu-id="ce06a-117">Ignore</span></span>
- <span data-ttu-id="ce06a-118">看</span><span class="sxs-lookup"><span data-stu-id="ce06a-118">Inquire</span></span>
- <span data-ttu-id="ce06a-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ce06a-119">SilentlyContinue</span></span>
- <span data-ttu-id="ce06a-120">停止</span><span class="sxs-lookup"><span data-stu-id="ce06a-120">Stop</span></span>
- <span data-ttu-id="ce06a-121">封存</span><span class="sxs-lookup"><span data-stu-id="ce06a-121">Suspend</span></span>

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

### <span data-ttu-id="ce06a-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ce06a-122">-InformationVariable</span></span>
<span data-ttu-id="ce06a-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ce06a-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ce06a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce06a-124">CommonParameters</span></span>
<span data-ttu-id="ce06a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce06a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce06a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce06a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce06a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ce06a-127">INPUTS</span></span>

## <span data-ttu-id="ce06a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ce06a-128">OUTPUTS</span></span>

### <span data-ttu-id="ce06a-129">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ce06a-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="ce06a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ce06a-130">NOTES</span></span>

## <span data-ttu-id="ce06a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce06a-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce06a-132">新-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ce06a-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="ce06a-133">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ce06a-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


