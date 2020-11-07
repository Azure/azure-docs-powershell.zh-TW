---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967295"
---
# <span data-ttu-id="0b901-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="0b901-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="0b901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b901-102">SYNOPSIS</span></span>
<span data-ttu-id="0b901-103">為虛擬機器設定 Puppet 延伸。</span><span class="sxs-lookup"><span data-stu-id="0b901-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="0b901-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b901-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b901-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b901-105">DESCRIPTION</span></span>
<span data-ttu-id="0b901-106">**AzureVMPuppetExtension** Cmdlet 會為虛擬機器設定 Puppet 延伸。</span><span class="sxs-lookup"><span data-stu-id="0b901-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="0b901-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b901-107">EXAMPLES</span></span>

### <span data-ttu-id="0b901-108">範例1：為虛擬機器設定 Puppet 延伸</span><span class="sxs-lookup"><span data-stu-id="0b901-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="0b901-109">這個範例會為指定的虛擬機器設定 Puppet 延伸，$VM 儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="0b901-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="0b901-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b901-110">PARAMETERS</span></span>

### <span data-ttu-id="0b901-111">-停用</span><span class="sxs-lookup"><span data-stu-id="0b901-111">-Disable</span></span>
<span data-ttu-id="0b901-112">表示此 Cmdlet 會停用延伸狀態。</span><span class="sxs-lookup"><span data-stu-id="0b901-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b901-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0b901-113">-InformationAction</span></span>
<span data-ttu-id="0b901-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0b901-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b901-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0b901-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b901-116">持續</span><span class="sxs-lookup"><span data-stu-id="0b901-116">Continue</span></span>
- <span data-ttu-id="0b901-117">理會</span><span class="sxs-lookup"><span data-stu-id="0b901-117">Ignore</span></span>
- <span data-ttu-id="0b901-118">看</span><span class="sxs-lookup"><span data-stu-id="0b901-118">Inquire</span></span>
- <span data-ttu-id="0b901-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0b901-119">SilentlyContinue</span></span>
- <span data-ttu-id="0b901-120">停止</span><span class="sxs-lookup"><span data-stu-id="0b901-120">Stop</span></span>
- <span data-ttu-id="0b901-121">封存</span><span class="sxs-lookup"><span data-stu-id="0b901-121">Suspend</span></span>

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

### <span data-ttu-id="0b901-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0b901-122">-InformationVariable</span></span>
<span data-ttu-id="0b901-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0b901-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0b901-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0b901-124">-Profile</span></span>
<span data-ttu-id="0b901-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0b901-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b901-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0b901-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b901-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="0b901-127">-PuppetMasterServer</span></span>
<span data-ttu-id="0b901-128">指定 puppet 主伺服器 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0b901-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b901-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="0b901-129">-ReferenceName</span></span>
<span data-ttu-id="0b901-130">指定延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="0b901-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="0b901-131">這是使用者定義的字串，用來代表延伸。</span><span class="sxs-lookup"><span data-stu-id="0b901-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="0b901-132">它是在第一次將延伸新增至虛擬機器時指定。</span><span class="sxs-lookup"><span data-stu-id="0b901-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="0b901-133">針對後續更新，您必須在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="0b901-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="0b901-134">指派給延伸的 ReferenceName 會使用 **add-azurevm** Cmdlet 傳回。</span><span class="sxs-lookup"><span data-stu-id="0b901-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b901-135">-版本</span><span class="sxs-lookup"><span data-stu-id="0b901-135">-Version</span></span>
<span data-ttu-id="0b901-136">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="0b901-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="0b901-137">-VM</span><span class="sxs-lookup"><span data-stu-id="0b901-137">-VM</span></span>
<span data-ttu-id="0b901-138">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0b901-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="0b901-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b901-139">CommonParameters</span></span>
<span data-ttu-id="0b901-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b901-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b901-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b901-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b901-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0b901-142">INPUTS</span></span>

## <span data-ttu-id="0b901-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0b901-143">OUTPUTS</span></span>

## <span data-ttu-id="0b901-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0b901-144">NOTES</span></span>

## <span data-ttu-id="0b901-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b901-145">RELATED LINKS</span></span>

[<span data-ttu-id="0b901-146">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0b901-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


