---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966892"
---
# <span data-ttu-id="2966f-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2966f-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="2966f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2966f-102">SYNOPSIS</span></span>
<span data-ttu-id="2966f-103">設定虛擬機器的資源延伸。</span><span class="sxs-lookup"><span data-stu-id="2966f-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="2966f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2966f-104">SYNTAX</span></span>

### <span data-ttu-id="2966f-105">SetByExtensionName (預設) </span><span class="sxs-lookup"><span data-stu-id="2966f-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2966f-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="2966f-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2966f-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="2966f-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2966f-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="2966f-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2966f-109">說明</span><span class="sxs-lookup"><span data-stu-id="2966f-109">DESCRIPTION</span></span>
<span data-ttu-id="2966f-110">**AzureVMExtension** Cmdlet 會設定虛擬機器的資源延伸。</span><span class="sxs-lookup"><span data-stu-id="2966f-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="2966f-111">示例</span><span class="sxs-lookup"><span data-stu-id="2966f-111">EXAMPLES</span></span>

### <span data-ttu-id="2966f-112">範例1：建立已套用資源延伸的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2966f-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="2966f-113">這個命令會建立已套用資源延伸的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2966f-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="2966f-114">參數</span><span class="sxs-lookup"><span data-stu-id="2966f-114">PARAMETERS</span></span>

### <span data-ttu-id="2966f-115">-停用</span><span class="sxs-lookup"><span data-stu-id="2966f-115">-Disable</span></span>
<span data-ttu-id="2966f-116">表示此 Cmdlet 會停用延伸狀態。</span><span class="sxs-lookup"><span data-stu-id="2966f-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="2966f-117">-ExtensionName</span></span>
<span data-ttu-id="2966f-118">指定虛擬機器的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2966f-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2966f-119">-ForceUpdate</span></span>
<span data-ttu-id="2966f-120">指示當設定尚未更新時，此 Cmdlet 會將配置重新套用到延伸。</span><span class="sxs-lookup"><span data-stu-id="2966f-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2966f-121">-InformationAction</span></span>
<span data-ttu-id="2966f-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2966f-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2966f-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2966f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2966f-124">持續</span><span class="sxs-lookup"><span data-stu-id="2966f-124">Continue</span></span>
- <span data-ttu-id="2966f-125">理會</span><span class="sxs-lookup"><span data-stu-id="2966f-125">Ignore</span></span>
- <span data-ttu-id="2966f-126">看</span><span class="sxs-lookup"><span data-stu-id="2966f-126">Inquire</span></span>
- <span data-ttu-id="2966f-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2966f-127">SilentlyContinue</span></span>
- <span data-ttu-id="2966f-128">停止</span><span class="sxs-lookup"><span data-stu-id="2966f-128">Stop</span></span>
- <span data-ttu-id="2966f-129">封存</span><span class="sxs-lookup"><span data-stu-id="2966f-129">Suspend</span></span>

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

### <span data-ttu-id="2966f-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2966f-130">-InformationVariable</span></span>
<span data-ttu-id="2966f-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2966f-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2966f-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="2966f-132">-PrivateConfigKey</span></span>
<span data-ttu-id="2966f-133">指定私人配置金鑰。</span><span class="sxs-lookup"><span data-stu-id="2966f-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="2966f-134">-PrivateConfigPath</span></span>
<span data-ttu-id="2966f-135">指定私人配置路徑。</span><span class="sxs-lookup"><span data-stu-id="2966f-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2966f-136">-PrivateConfiguration</span></span>
<span data-ttu-id="2966f-137">指定私人配置文字。</span><span class="sxs-lookup"><span data-stu-id="2966f-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2966f-138">-Profile</span></span>
<span data-ttu-id="2966f-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2966f-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2966f-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2966f-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2966f-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="2966f-141">-PublicConfigKey</span></span>
<span data-ttu-id="2966f-142">指定公用配置金鑰。</span><span class="sxs-lookup"><span data-stu-id="2966f-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="2966f-143">-PublicConfigPath</span></span>
<span data-ttu-id="2966f-144">指定公用配置路徑。</span><span class="sxs-lookup"><span data-stu-id="2966f-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="2966f-145">-PublicConfiguration</span></span>
<span data-ttu-id="2966f-146">指定公用配置文字。</span><span class="sxs-lookup"><span data-stu-id="2966f-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2966f-147">-Publisher</span></span>
<span data-ttu-id="2966f-148">指定副檔名的發行者。</span><span class="sxs-lookup"><span data-stu-id="2966f-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="2966f-149">-ReferenceName</span></span>
<span data-ttu-id="2966f-150">指定延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="2966f-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="2966f-151">這是使用者定義的字串，可以用來代表延伸。</span><span class="sxs-lookup"><span data-stu-id="2966f-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="2966f-152">第一次將延伸新增至虛擬機器時，您必須指定它。</span><span class="sxs-lookup"><span data-stu-id="2966f-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="2966f-153">針對後續更新，您需要在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="2966f-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="2966f-154">指派給延伸的 ReferenceName 會使用 **add-azurevm** Cmdlet 傳回。</span><span class="sxs-lookup"><span data-stu-id="2966f-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-155">-卸載</span><span class="sxs-lookup"><span data-stu-id="2966f-155">-Uninstall</span></span>
<span data-ttu-id="2966f-156">表示此 Cmdlet 會從虛擬機器中卸載資源延伸。</span><span class="sxs-lookup"><span data-stu-id="2966f-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-157">-版本</span><span class="sxs-lookup"><span data-stu-id="2966f-157">-Version</span></span>
<span data-ttu-id="2966f-158">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2966f-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2966f-159">-VM</span><span class="sxs-lookup"><span data-stu-id="2966f-159">-VM</span></span>
<span data-ttu-id="2966f-160">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="2966f-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2966f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2966f-161">CommonParameters</span></span>
<span data-ttu-id="2966f-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2966f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2966f-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2966f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2966f-164">輸入</span><span class="sxs-lookup"><span data-stu-id="2966f-164">INPUTS</span></span>

## <span data-ttu-id="2966f-165">輸出</span><span class="sxs-lookup"><span data-stu-id="2966f-165">OUTPUTS</span></span>

## <span data-ttu-id="2966f-166">筆記</span><span class="sxs-lookup"><span data-stu-id="2966f-166">NOTES</span></span>

## <span data-ttu-id="2966f-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="2966f-167">RELATED LINKS</span></span>

[<span data-ttu-id="2966f-168">AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2966f-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="2966f-169">移除-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2966f-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="2966f-170">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="2966f-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


