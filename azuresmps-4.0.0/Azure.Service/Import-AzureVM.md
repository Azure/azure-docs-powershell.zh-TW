---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967701"
---
# <span data-ttu-id="6ae57-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6ae57-101">Import-AzureVM</span></span>

## <span data-ttu-id="6ae57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ae57-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae57-103">從檔案匯入 Azure 虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="6ae57-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="6ae57-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ae57-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ae57-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ae57-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae57-106">**Import-add-azurevm** Cmdlet 會從 XML 檔案匯入先前儲存的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="6ae57-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="6ae57-107">如果您想要從匯入的資料開始建立虛擬機器，這個 Cmdlet 很有用。</span><span class="sxs-lookup"><span data-stu-id="6ae57-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="6ae57-108">執行 **Export** ，接著再按下 **Remove** ，然後按下 **add-azurevm** 來重新建立虛擬機器，可能會導致產生的虛擬機器與原始的 IP 位址不同。</span><span class="sxs-lookup"><span data-stu-id="6ae57-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="6ae57-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ae57-109">EXAMPLES</span></span>

### <span data-ttu-id="6ae57-110">範例1：匯入虛擬機器狀態</span><span class="sxs-lookup"><span data-stu-id="6ae57-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="6ae57-111">這個命令會從 VMstate.xml 檔案匯入虛擬機器的狀態，然後在指定的雲端服務中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6ae57-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="6ae57-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ae57-112">PARAMETERS</span></span>

### <span data-ttu-id="6ae57-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ae57-113">-InformationAction</span></span>
<span data-ttu-id="6ae57-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6ae57-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ae57-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6ae57-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ae57-116">持續</span><span class="sxs-lookup"><span data-stu-id="6ae57-116">Continue</span></span>
- <span data-ttu-id="6ae57-117">理會</span><span class="sxs-lookup"><span data-stu-id="6ae57-117">Ignore</span></span>
- <span data-ttu-id="6ae57-118">看</span><span class="sxs-lookup"><span data-stu-id="6ae57-118">Inquire</span></span>
- <span data-ttu-id="6ae57-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ae57-119">SilentlyContinue</span></span>
- <span data-ttu-id="6ae57-120">停止</span><span class="sxs-lookup"><span data-stu-id="6ae57-120">Stop</span></span>
- <span data-ttu-id="6ae57-121">封存</span><span class="sxs-lookup"><span data-stu-id="6ae57-121">Suspend</span></span>

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

### <span data-ttu-id="6ae57-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ae57-122">-InformationVariable</span></span>
<span data-ttu-id="6ae57-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6ae57-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ae57-124">-Path</span><span class="sxs-lookup"><span data-stu-id="6ae57-124">-Path</span></span>
<span data-ttu-id="6ae57-125">指定具有先前儲存的虛擬機器狀態的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6ae57-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae57-126">CommonParameters</span></span>
<span data-ttu-id="6ae57-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ae57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae57-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ae57-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae57-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6ae57-129">INPUTS</span></span>

## <span data-ttu-id="6ae57-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6ae57-130">OUTPUTS</span></span>

## <span data-ttu-id="6ae57-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6ae57-131">NOTES</span></span>

## <span data-ttu-id="6ae57-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ae57-132">RELATED LINKS</span></span>

[<span data-ttu-id="6ae57-133">Export-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ae57-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="6ae57-134">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ae57-134">New-AzureVM</span></span>](./New-AzureVM.md)


