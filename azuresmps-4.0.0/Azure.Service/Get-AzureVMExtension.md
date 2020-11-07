---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967979"
---
# <span data-ttu-id="265d4-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="265d4-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="265d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="265d4-102">SYNOPSIS</span></span>
<span data-ttu-id="265d4-103">取得套用至虛擬機器的資源延伸。</span><span class="sxs-lookup"><span data-stu-id="265d4-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="265d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="265d4-104">SYNTAX</span></span>

### <span data-ttu-id="265d4-105">ListByReferenceName (預設) </span><span class="sxs-lookup"><span data-stu-id="265d4-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="265d4-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="265d4-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="265d4-107">說明</span><span class="sxs-lookup"><span data-stu-id="265d4-107">DESCRIPTION</span></span>
<span data-ttu-id="265d4-108">**AzureVMExtension** Cmdlet 會取得已套用至虛擬機器的資源延伸。</span><span class="sxs-lookup"><span data-stu-id="265d4-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="265d4-109">示例</span><span class="sxs-lookup"><span data-stu-id="265d4-109">EXAMPLES</span></span>

### <span data-ttu-id="265d4-110">範例1：取得套用至虛擬機器的資源延伸</span><span class="sxs-lookup"><span data-stu-id="265d4-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="265d4-111">這個命令會取得套用至指定虛擬機器的資源延伸，$VM 儲存于變數中。</span><span class="sxs-lookup"><span data-stu-id="265d4-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="265d4-112">參數</span><span class="sxs-lookup"><span data-stu-id="265d4-112">PARAMETERS</span></span>

### <span data-ttu-id="265d4-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="265d4-113">-ExtensionName</span></span>
<span data-ttu-id="265d4-114">指定虛擬機器延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="265d4-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265d4-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="265d4-115">-InformationAction</span></span>
<span data-ttu-id="265d4-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="265d4-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="265d4-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="265d4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="265d4-118">持續</span><span class="sxs-lookup"><span data-stu-id="265d4-118">Continue</span></span>
- <span data-ttu-id="265d4-119">理會</span><span class="sxs-lookup"><span data-stu-id="265d4-119">Ignore</span></span>
- <span data-ttu-id="265d4-120">看</span><span class="sxs-lookup"><span data-stu-id="265d4-120">Inquire</span></span>
- <span data-ttu-id="265d4-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="265d4-121">SilentlyContinue</span></span>
- <span data-ttu-id="265d4-122">停止</span><span class="sxs-lookup"><span data-stu-id="265d4-122">Stop</span></span>
- <span data-ttu-id="265d4-123">封存</span><span class="sxs-lookup"><span data-stu-id="265d4-123">Suspend</span></span>

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

### <span data-ttu-id="265d4-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="265d4-124">-InformationVariable</span></span>
<span data-ttu-id="265d4-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="265d4-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="265d4-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="265d4-126">-Profile</span></span>
<span data-ttu-id="265d4-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="265d4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="265d4-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="265d4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="265d4-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="265d4-129">-Publisher</span></span>
<span data-ttu-id="265d4-130">指定副檔名的發行者。</span><span class="sxs-lookup"><span data-stu-id="265d4-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265d4-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="265d4-131">-ReferenceName</span></span>
<span data-ttu-id="265d4-132">指定延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="265d4-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265d4-133">-版本</span><span class="sxs-lookup"><span data-stu-id="265d4-133">-Version</span></span>
<span data-ttu-id="265d4-134">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="265d4-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265d4-135">-VM</span><span class="sxs-lookup"><span data-stu-id="265d4-135">-VM</span></span>
<span data-ttu-id="265d4-136">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="265d4-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="265d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265d4-137">CommonParameters</span></span>
<span data-ttu-id="265d4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="265d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265d4-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="265d4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265d4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="265d4-140">INPUTS</span></span>

## <span data-ttu-id="265d4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="265d4-141">OUTPUTS</span></span>

## <span data-ttu-id="265d4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="265d4-142">NOTES</span></span>

## <span data-ttu-id="265d4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="265d4-143">RELATED LINKS</span></span>

[<span data-ttu-id="265d4-144">移除-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="265d4-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="265d4-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="265d4-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


