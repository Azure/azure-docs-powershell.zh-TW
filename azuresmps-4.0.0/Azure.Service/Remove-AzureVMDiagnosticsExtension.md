---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966950"
---
# <span data-ttu-id="2ea35-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2ea35-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="2ea35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ea35-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea35-103">從虛擬機器移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="2ea35-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="2ea35-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ea35-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ea35-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ea35-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea35-106">**AzureVMDiagnosticsExtension** Cmdlet 會從虛擬機器中移除 Microsoft Azure 診斷擴展外掛程式。</span><span class="sxs-lookup"><span data-stu-id="2ea35-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="2ea35-107">您必須將這個 Cmdlet 的輸出傳遞給 **更新-add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ea35-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="2ea35-108">示例</span><span class="sxs-lookup"><span data-stu-id="2ea35-108">EXAMPLES</span></span>

### <span data-ttu-id="2ea35-109">範例1：從虛擬機器移除 Azure 診斷延伸</span><span class="sxs-lookup"><span data-stu-id="2ea35-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="2ea35-110">此命令會從虛擬機器中移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="2ea35-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="2ea35-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ea35-111">PARAMETERS</span></span>

### <span data-ttu-id="2ea35-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ea35-112">-InformationAction</span></span>
<span data-ttu-id="2ea35-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2ea35-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ea35-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2ea35-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ea35-115">持續</span><span class="sxs-lookup"><span data-stu-id="2ea35-115">Continue</span></span>
- <span data-ttu-id="2ea35-116">理會</span><span class="sxs-lookup"><span data-stu-id="2ea35-116">Ignore</span></span>
- <span data-ttu-id="2ea35-117">看</span><span class="sxs-lookup"><span data-stu-id="2ea35-117">Inquire</span></span>
- <span data-ttu-id="2ea35-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ea35-118">SilentlyContinue</span></span>
- <span data-ttu-id="2ea35-119">停止</span><span class="sxs-lookup"><span data-stu-id="2ea35-119">Stop</span></span>
- <span data-ttu-id="2ea35-120">封存</span><span class="sxs-lookup"><span data-stu-id="2ea35-120">Suspend</span></span>

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

### <span data-ttu-id="2ea35-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ea35-121">-InformationVariable</span></span>
<span data-ttu-id="2ea35-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2ea35-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ea35-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2ea35-123">-Profile</span></span>
<span data-ttu-id="2ea35-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2ea35-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ea35-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2ea35-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ea35-126">-VM</span><span class="sxs-lookup"><span data-stu-id="2ea35-126">-VM</span></span>
<span data-ttu-id="2ea35-127">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="2ea35-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2ea35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea35-128">CommonParameters</span></span>
<span data-ttu-id="2ea35-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ea35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea35-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ea35-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea35-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2ea35-131">INPUTS</span></span>

## <span data-ttu-id="2ea35-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2ea35-132">OUTPUTS</span></span>

## <span data-ttu-id="2ea35-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2ea35-133">NOTES</span></span>

## <span data-ttu-id="2ea35-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ea35-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ea35-135">AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2ea35-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="2ea35-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2ea35-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="2ea35-137">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="2ea35-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


