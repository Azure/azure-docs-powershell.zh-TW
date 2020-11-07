---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966947"
---
# <span data-ttu-id="324f8-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="324f8-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="324f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="324f8-102">SYNOPSIS</span></span>
<span data-ttu-id="324f8-103">從虛擬機器中移除資源延伸。</span><span class="sxs-lookup"><span data-stu-id="324f8-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="324f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="324f8-104">SYNTAX</span></span>

### <span data-ttu-id="324f8-105">RemoveByExtensionName (預設) </span><span class="sxs-lookup"><span data-stu-id="324f8-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="324f8-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="324f8-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="324f8-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="324f8-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="324f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="324f8-108">DESCRIPTION</span></span>
<span data-ttu-id="324f8-109">**AzureVMExtension** Cmdlet 會從虛擬機器中移除資源延伸。</span><span class="sxs-lookup"><span data-stu-id="324f8-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="324f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="324f8-110">EXAMPLES</span></span>

### <span data-ttu-id="324f8-111">範例1：使用特定名稱和發行者移除延伸</span><span class="sxs-lookup"><span data-stu-id="324f8-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="324f8-112">這個命令會移除具有指定名稱與發行者的延伸。</span><span class="sxs-lookup"><span data-stu-id="324f8-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="324f8-113">範例2：移除特定虛擬機器中的所有延伸</span><span class="sxs-lookup"><span data-stu-id="324f8-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="324f8-114">這個命令會從指定的虛擬機器中移除所有延伸，並儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="324f8-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="324f8-115">參數</span><span class="sxs-lookup"><span data-stu-id="324f8-115">PARAMETERS</span></span>

### <span data-ttu-id="324f8-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="324f8-116">-ExtensionName</span></span>
<span data-ttu-id="324f8-117">指定此 Cmdlet 移除的副檔名。</span><span class="sxs-lookup"><span data-stu-id="324f8-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f8-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="324f8-118">-InformationAction</span></span>
<span data-ttu-id="324f8-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="324f8-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="324f8-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="324f8-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="324f8-121">持續</span><span class="sxs-lookup"><span data-stu-id="324f8-121">Continue</span></span>
- <span data-ttu-id="324f8-122">理會</span><span class="sxs-lookup"><span data-stu-id="324f8-122">Ignore</span></span>
- <span data-ttu-id="324f8-123">看</span><span class="sxs-lookup"><span data-stu-id="324f8-123">Inquire</span></span>
- <span data-ttu-id="324f8-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="324f8-124">SilentlyContinue</span></span>
- <span data-ttu-id="324f8-125">停止</span><span class="sxs-lookup"><span data-stu-id="324f8-125">Stop</span></span>
- <span data-ttu-id="324f8-126">封存</span><span class="sxs-lookup"><span data-stu-id="324f8-126">Suspend</span></span>

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

### <span data-ttu-id="324f8-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="324f8-127">-InformationVariable</span></span>
<span data-ttu-id="324f8-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="324f8-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="324f8-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="324f8-129">-Profile</span></span>
<span data-ttu-id="324f8-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="324f8-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="324f8-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="324f8-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="324f8-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="324f8-132">-Publisher</span></span>
<span data-ttu-id="324f8-133">指定副檔名發行者。</span><span class="sxs-lookup"><span data-stu-id="324f8-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f8-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="324f8-134">-ReferenceName</span></span>
<span data-ttu-id="324f8-135">指定延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="324f8-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f8-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="324f8-136">-RemoveAll</span></span>
<span data-ttu-id="324f8-137">表示此 Cmdlet 會從虛擬機器中移除所有資源延伸。</span><span class="sxs-lookup"><span data-stu-id="324f8-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f8-138">-VM</span><span class="sxs-lookup"><span data-stu-id="324f8-138">-VM</span></span>
<span data-ttu-id="324f8-139">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="324f8-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="324f8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324f8-140">CommonParameters</span></span>
<span data-ttu-id="324f8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="324f8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324f8-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="324f8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324f8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="324f8-143">INPUTS</span></span>

## <span data-ttu-id="324f8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="324f8-144">OUTPUTS</span></span>

## <span data-ttu-id="324f8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="324f8-145">NOTES</span></span>

## <span data-ttu-id="324f8-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="324f8-146">RELATED LINKS</span></span>

[<span data-ttu-id="324f8-147">AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="324f8-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="324f8-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="324f8-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


