---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967257"
---
# <span data-ttu-id="670b8-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="670b8-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="670b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="670b8-102">SYNOPSIS</span></span>
<span data-ttu-id="670b8-103">為虛擬機器設定 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="670b8-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="670b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="670b8-104">SYNTAX</span></span>

### <span data-ttu-id="670b8-105">EnableAccessExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="670b8-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="670b8-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="670b8-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="670b8-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="670b8-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="670b8-108">說明</span><span class="sxs-lookup"><span data-stu-id="670b8-108">DESCRIPTION</span></span>
<span data-ttu-id="670b8-109">**AzureVMAccessExtension** Cmdlet 會將虛擬機器 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="670b8-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="670b8-110">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="670b8-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="670b8-111">示例</span><span class="sxs-lookup"><span data-stu-id="670b8-111">EXAMPLES</span></span>

### <span data-ttu-id="670b8-112">範例1：設定套用至指定虛擬機器的 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="670b8-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="670b8-113">這個命令會將 VMAccess 延伸套用至指定的虛擬機器，並儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="670b8-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="670b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="670b8-114">PARAMETERS</span></span>

### <span data-ttu-id="670b8-115">-停用</span><span class="sxs-lookup"><span data-stu-id="670b8-115">-Disable</span></span>
<span data-ttu-id="670b8-116">表示此 Cmdlet 會將延伸狀態設定為 [停用]。</span><span class="sxs-lookup"><span data-stu-id="670b8-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="670b8-117">-ForceUpdate</span></span>
<span data-ttu-id="670b8-118">表示當設定尚未更新時，此 Cmdlet 會將配置重新應用到延伸。</span><span class="sxs-lookup"><span data-stu-id="670b8-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="670b8-119">-InformationAction</span></span>
<span data-ttu-id="670b8-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="670b8-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="670b8-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="670b8-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="670b8-122">持續</span><span class="sxs-lookup"><span data-stu-id="670b8-122">Continue</span></span>
- <span data-ttu-id="670b8-123">理會</span><span class="sxs-lookup"><span data-stu-id="670b8-123">Ignore</span></span>
- <span data-ttu-id="670b8-124">看</span><span class="sxs-lookup"><span data-stu-id="670b8-124">Inquire</span></span>
- <span data-ttu-id="670b8-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="670b8-125">SilentlyContinue</span></span>
- <span data-ttu-id="670b8-126">停止</span><span class="sxs-lookup"><span data-stu-id="670b8-126">Stop</span></span>
- <span data-ttu-id="670b8-127">封存</span><span class="sxs-lookup"><span data-stu-id="670b8-127">Suspend</span></span>

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

### <span data-ttu-id="670b8-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="670b8-128">-InformationVariable</span></span>
<span data-ttu-id="670b8-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="670b8-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="670b8-130">-Password</span><span class="sxs-lookup"><span data-stu-id="670b8-130">-Password</span></span>
<span data-ttu-id="670b8-131">指定重新設置虛擬機器認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="670b8-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="670b8-132">-Profile</span></span>
<span data-ttu-id="670b8-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="670b8-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="670b8-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="670b8-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="670b8-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="670b8-135">-ReferenceName</span></span>
<span data-ttu-id="670b8-136">指定存取延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="670b8-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="670b8-137">這是使用者定義的字串，用來代表延伸。</span><span class="sxs-lookup"><span data-stu-id="670b8-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="670b8-138">它是在第一次將延伸新增至虛擬機器時指定。</span><span class="sxs-lookup"><span data-stu-id="670b8-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="670b8-139">針對後續更新，您應該在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="670b8-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="670b8-140">指派給延伸的 *ReferenceName* 會使用 **add-azurevm** Cmdlet 傳回。</span><span class="sxs-lookup"><span data-stu-id="670b8-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="670b8-141">-卸載</span><span class="sxs-lookup"><span data-stu-id="670b8-141">-Uninstall</span></span>
<span data-ttu-id="670b8-142">指示此 Cmdlet 是否已卸載存取擴展外掛程式。</span><span class="sxs-lookup"><span data-stu-id="670b8-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="670b8-143">-UserName</span></span>
<span data-ttu-id="670b8-144">指定此 Cmdlet 用來重設虛擬機器認證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="670b8-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-145">-版本</span><span class="sxs-lookup"><span data-stu-id="670b8-145">-Version</span></span>
<span data-ttu-id="670b8-146">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="670b8-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670b8-147">-VM</span><span class="sxs-lookup"><span data-stu-id="670b8-147">-VM</span></span>
<span data-ttu-id="670b8-148">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="670b8-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="670b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670b8-149">CommonParameters</span></span>
<span data-ttu-id="670b8-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="670b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670b8-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="670b8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670b8-152">輸入</span><span class="sxs-lookup"><span data-stu-id="670b8-152">INPUTS</span></span>

## <span data-ttu-id="670b8-153">輸出</span><span class="sxs-lookup"><span data-stu-id="670b8-153">OUTPUTS</span></span>

## <span data-ttu-id="670b8-154">筆記</span><span class="sxs-lookup"><span data-stu-id="670b8-154">NOTES</span></span>

## <span data-ttu-id="670b8-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="670b8-155">RELATED LINKS</span></span>

[<span data-ttu-id="670b8-156">AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="670b8-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="670b8-157">移除-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="670b8-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


