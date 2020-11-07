---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966977"
---
# <span data-ttu-id="6d022-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6d022-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="6d022-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d022-102">SYNOPSIS</span></span>
<span data-ttu-id="6d022-103">從 Azure 虛擬機器自訂腳本副檔名取得資訊。</span><span class="sxs-lookup"><span data-stu-id="6d022-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="6d022-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d022-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d022-105">說明</span><span class="sxs-lookup"><span data-stu-id="6d022-105">DESCRIPTION</span></span>
<span data-ttu-id="6d022-106">**AzureVMCustomScriptExtension** Cmdlet 會從 Azure 虛擬電腦自訂腳本延伸取得資訊。</span><span class="sxs-lookup"><span data-stu-id="6d022-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="6d022-107">示例</span><span class="sxs-lookup"><span data-stu-id="6d022-107">EXAMPLES</span></span>

### <span data-ttu-id="6d022-108">範例1：取得 Azure 虛擬機器腳本延伸</span><span class="sxs-lookup"><span data-stu-id="6d022-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="6d022-109">這個命令會取得 $VM 變數中儲存的 Azure 虛擬機器腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="6d022-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="6d022-110">參數</span><span class="sxs-lookup"><span data-stu-id="6d022-110">PARAMETERS</span></span>

### <span data-ttu-id="6d022-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6d022-111">-InformationAction</span></span>
<span data-ttu-id="6d022-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6d022-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6d022-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6d022-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d022-114">持續</span><span class="sxs-lookup"><span data-stu-id="6d022-114">Continue</span></span>
- <span data-ttu-id="6d022-115">理會</span><span class="sxs-lookup"><span data-stu-id="6d022-115">Ignore</span></span>
- <span data-ttu-id="6d022-116">看</span><span class="sxs-lookup"><span data-stu-id="6d022-116">Inquire</span></span>
- <span data-ttu-id="6d022-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d022-117">SilentlyContinue</span></span>
- <span data-ttu-id="6d022-118">停止</span><span class="sxs-lookup"><span data-stu-id="6d022-118">Stop</span></span>
- <span data-ttu-id="6d022-119">封存</span><span class="sxs-lookup"><span data-stu-id="6d022-119">Suspend</span></span>

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

### <span data-ttu-id="6d022-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d022-120">-InformationVariable</span></span>
<span data-ttu-id="6d022-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6d022-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6d022-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6d022-122">-Profile</span></span>
<span data-ttu-id="6d022-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6d022-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d022-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6d022-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d022-125">-VM</span><span class="sxs-lookup"><span data-stu-id="6d022-125">-VM</span></span>
<span data-ttu-id="6d022-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="6d022-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="6d022-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d022-127">CommonParameters</span></span>
<span data-ttu-id="6d022-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d022-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d022-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d022-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d022-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6d022-130">INPUTS</span></span>

## <span data-ttu-id="6d022-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6d022-131">OUTPUTS</span></span>

## <span data-ttu-id="6d022-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6d022-132">NOTES</span></span>

## <span data-ttu-id="6d022-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d022-133">RELATED LINKS</span></span>

[<span data-ttu-id="6d022-134">移除-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6d022-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="6d022-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6d022-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


