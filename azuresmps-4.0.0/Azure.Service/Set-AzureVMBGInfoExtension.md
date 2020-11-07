---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967489"
---
# <span data-ttu-id="11eda-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="11eda-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="11eda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11eda-102">SYNOPSIS</span></span>
<span data-ttu-id="11eda-103">為虛擬機器設定 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="11eda-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="11eda-104">句法</span><span class="sxs-lookup"><span data-stu-id="11eda-104">SYNTAX</span></span>

### <span data-ttu-id="11eda-105">SetBGInfoExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="11eda-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="11eda-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="11eda-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="11eda-107">說明</span><span class="sxs-lookup"><span data-stu-id="11eda-107">DESCRIPTION</span></span>
<span data-ttu-id="11eda-108">**AzureVMBGInfoExtension** Cmdlet 會為虛擬機器設定 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="11eda-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="11eda-109">示例</span><span class="sxs-lookup"><span data-stu-id="11eda-109">EXAMPLES</span></span>

### <span data-ttu-id="11eda-110">範例1：為虛擬機器設定 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="11eda-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="11eda-111">這個命令會為指定的虛擬機器設定 BGInfo 延伸，儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="11eda-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="11eda-112">參數</span><span class="sxs-lookup"><span data-stu-id="11eda-112">PARAMETERS</span></span>

### <span data-ttu-id="11eda-113">-停用</span><span class="sxs-lookup"><span data-stu-id="11eda-113">-Disable</span></span>
<span data-ttu-id="11eda-114">表示此 Cmdlet 會停用延伸狀態。</span><span class="sxs-lookup"><span data-stu-id="11eda-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eda-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11eda-115">-InformationAction</span></span>
<span data-ttu-id="11eda-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="11eda-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11eda-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11eda-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11eda-118">持續</span><span class="sxs-lookup"><span data-stu-id="11eda-118">Continue</span></span>
- <span data-ttu-id="11eda-119">理會</span><span class="sxs-lookup"><span data-stu-id="11eda-119">Ignore</span></span>
- <span data-ttu-id="11eda-120">看</span><span class="sxs-lookup"><span data-stu-id="11eda-120">Inquire</span></span>
- <span data-ttu-id="11eda-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11eda-121">SilentlyContinue</span></span>
- <span data-ttu-id="11eda-122">停止</span><span class="sxs-lookup"><span data-stu-id="11eda-122">Stop</span></span>
- <span data-ttu-id="11eda-123">封存</span><span class="sxs-lookup"><span data-stu-id="11eda-123">Suspend</span></span>

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

### <span data-ttu-id="11eda-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11eda-124">-InformationVariable</span></span>
<span data-ttu-id="11eda-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="11eda-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="11eda-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="11eda-126">-Profile</span></span>
<span data-ttu-id="11eda-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="11eda-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11eda-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="11eda-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11eda-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="11eda-129">-ReferenceName</span></span>
<span data-ttu-id="11eda-130">指定 BGInfo 延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="11eda-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="11eda-131">這個參數是使用者定義的字串，可以用來代表延伸。</span><span class="sxs-lookup"><span data-stu-id="11eda-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="11eda-132">它是在第一次將延伸新增至虛擬機器時指定。</span><span class="sxs-lookup"><span data-stu-id="11eda-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="11eda-133">您可以在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="11eda-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eda-134">-卸載</span><span class="sxs-lookup"><span data-stu-id="11eda-134">-Uninstall</span></span>
<span data-ttu-id="11eda-135">表示此 Cmdlet 會卸載 BGInfo 延伸。</span><span class="sxs-lookup"><span data-stu-id="11eda-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eda-136">-版本</span><span class="sxs-lookup"><span data-stu-id="11eda-136">-Version</span></span>
<span data-ttu-id="11eda-137">指定 BGInfo 延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="11eda-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eda-138">-VM</span><span class="sxs-lookup"><span data-stu-id="11eda-138">-VM</span></span>
<span data-ttu-id="11eda-139">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="11eda-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="11eda-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11eda-140">CommonParameters</span></span>
<span data-ttu-id="11eda-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11eda-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11eda-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11eda-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11eda-143">輸入</span><span class="sxs-lookup"><span data-stu-id="11eda-143">INPUTS</span></span>

## <span data-ttu-id="11eda-144">輸出</span><span class="sxs-lookup"><span data-stu-id="11eda-144">OUTPUTS</span></span>

## <span data-ttu-id="11eda-145">筆記</span><span class="sxs-lookup"><span data-stu-id="11eda-145">NOTES</span></span>

## <span data-ttu-id="11eda-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="11eda-146">RELATED LINKS</span></span>

[<span data-ttu-id="11eda-147">AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="11eda-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="11eda-148">移除-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="11eda-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


