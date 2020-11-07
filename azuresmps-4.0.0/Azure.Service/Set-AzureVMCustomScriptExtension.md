---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967483"
---
# <span data-ttu-id="3f7f7-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f7f7-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="3f7f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7f7-103">設定 Azure 虛擬機器自訂腳本延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="3f7f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f7f7-104">SYNTAX</span></span>

### <span data-ttu-id="3f7f7-105">SetCustomScriptExtensionByContainerAndFileNames (預設) </span><span class="sxs-lookup"><span data-stu-id="3f7f7-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f7f7-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f7f7-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f7f7-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f7f7-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f7f7-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="3f7f7-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f7f7-109">說明</span><span class="sxs-lookup"><span data-stu-id="3f7f7-109">DESCRIPTION</span></span>
<span data-ttu-id="3f7f7-110">**AzureVMCustomScriptExtension** Cmdlet 會設定 Azure 虛擬機器自訂腳本副檔名的資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="3f7f7-111">示例</span><span class="sxs-lookup"><span data-stu-id="3f7f7-111">EXAMPLES</span></span>

### <span data-ttu-id="3f7f7-112">範例1：為虛擬機器自訂腳本延伸設定資訊</span><span class="sxs-lookup"><span data-stu-id="3f7f7-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="3f7f7-113">這個命令會設定虛擬機器自訂腳本延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="3f7f7-114">範例2：使用檔路徑設定虛擬機器自訂腳本延伸的資訊</span><span class="sxs-lookup"><span data-stu-id="3f7f7-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="3f7f7-115">這個命令會使用多個檔案 Url 來設定虛擬機器自訂腳本延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="3f7f7-116">參數</span><span class="sxs-lookup"><span data-stu-id="3f7f7-116">PARAMETERS</span></span>

### <span data-ttu-id="3f7f7-117">-引數</span><span class="sxs-lookup"><span data-stu-id="3f7f7-117">-Argument</span></span>
<span data-ttu-id="3f7f7-118">指定一個字串，提供此 Cmdlet 在虛擬機器上執行的引數。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-119">-容器</span><span class="sxs-lookup"><span data-stu-id="3f7f7-119">-ContainerName</span></span>
<span data-ttu-id="3f7f7-120">在儲存空間帳戶中指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-121">-停用</span><span class="sxs-lookup"><span data-stu-id="3f7f7-121">-Disable</span></span>
<span data-ttu-id="3f7f7-122">表示此 Cmdlet 會停用延伸狀態。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="3f7f7-123">-FileName</span></span>
<span data-ttu-id="3f7f7-124">指定一個字串陣列，其中包含指定容器中 blob 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="3f7f7-125">-FileUri</span></span>
<span data-ttu-id="3f7f7-126">指定包含 blob 檔案之 Url 的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="3f7f7-127">-ForceUpdate</span></span>
<span data-ttu-id="3f7f7-128">表示當設定尚未更新時，此 Cmdlet 會將配置重新套用到延伸。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f7f7-129">-InformationAction</span></span>
<span data-ttu-id="3f7f7-130">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f7f7-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3f7f7-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f7f7-132">持續</span><span class="sxs-lookup"><span data-stu-id="3f7f7-132">Continue</span></span>
- <span data-ttu-id="3f7f7-133">理會</span><span class="sxs-lookup"><span data-stu-id="3f7f7-133">Ignore</span></span>
- <span data-ttu-id="3f7f7-134">看</span><span class="sxs-lookup"><span data-stu-id="3f7f7-134">Inquire</span></span>
- <span data-ttu-id="3f7f7-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f7f7-135">SilentlyContinue</span></span>
- <span data-ttu-id="3f7f7-136">停止</span><span class="sxs-lookup"><span data-stu-id="3f7f7-136">Stop</span></span>
- <span data-ttu-id="3f7f7-137">封存</span><span class="sxs-lookup"><span data-stu-id="3f7f7-137">Suspend</span></span>

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

### <span data-ttu-id="3f7f7-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f7f7-138">-InformationVariable</span></span>
<span data-ttu-id="3f7f7-139">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f7f7-140">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3f7f7-140">-Profile</span></span>
<span data-ttu-id="3f7f7-141">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f7f7-142">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f7f7-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="3f7f7-143">-ReferenceName</span></span>
<span data-ttu-id="3f7f7-144">指定延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="3f7f7-145">這個參數是使用者定義的字串，可以用來代表延伸。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="3f7f7-146">它是在第一次將延伸新增至虛擬機器時指定。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="3f7f7-147">針對後續更新，您需要在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="3f7f7-148">指派給延伸的 *ReferenceName* 會使用 **add-azurevm** Cmdlet 傳回。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-149">-執行</span><span class="sxs-lookup"><span data-stu-id="3f7f7-149">-Run</span></span>
<span data-ttu-id="3f7f7-150">指定此 Cmdlet 由虛擬機器上的擴展所執行的命令。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="3f7f7-151">僅支援 "powershell.exe"。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f7f7-152">-StorageAccountKey</span></span>
<span data-ttu-id="3f7f7-153">指定儲存空間帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="3f7f7-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3f7f7-154">-StorageAccountName</span></span>
<span data-ttu-id="3f7f7-155">指定目前訂閱中的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7f7-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="3f7f7-157">指定儲存服務端點。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-158">-卸載</span><span class="sxs-lookup"><span data-stu-id="3f7f7-158">-Uninstall</span></span>
<span data-ttu-id="3f7f7-159">表示此 Cmdlet 會從虛擬機器卸載自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-160">-版本</span><span class="sxs-lookup"><span data-stu-id="3f7f7-160">-Version</span></span>
<span data-ttu-id="3f7f7-161">指定自訂腳本副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7f7-162">-VM</span><span class="sxs-lookup"><span data-stu-id="3f7f7-162">-VM</span></span>
<span data-ttu-id="3f7f7-163">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3f7f7-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7f7-164">CommonParameters</span></span>
<span data-ttu-id="3f7f7-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7f7-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f7f7-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7f7-167">輸入</span><span class="sxs-lookup"><span data-stu-id="3f7f7-167">INPUTS</span></span>

## <span data-ttu-id="3f7f7-168">輸出</span><span class="sxs-lookup"><span data-stu-id="3f7f7-168">OUTPUTS</span></span>

## <span data-ttu-id="3f7f7-169">筆記</span><span class="sxs-lookup"><span data-stu-id="3f7f7-169">NOTES</span></span>

## <span data-ttu-id="3f7f7-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f7f7-170">RELATED LINKS</span></span>

[<span data-ttu-id="3f7f7-171">AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f7f7-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="3f7f7-172">移除-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f7f7-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="3f7f7-173">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="3f7f7-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


