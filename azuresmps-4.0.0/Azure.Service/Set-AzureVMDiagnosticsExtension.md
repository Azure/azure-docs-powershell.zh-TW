---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967484"
---
# <span data-ttu-id="5090e-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5090e-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5090e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5090e-102">SYNOPSIS</span></span>
<span data-ttu-id="5090e-103">在虛擬機器上配置 Azure Diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="5090e-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5090e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5090e-104">SYNTAX</span></span>

### <span data-ttu-id="5090e-105">SetDiagnosticsExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="5090e-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5090e-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="5090e-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5090e-107">說明</span><span class="sxs-lookup"><span data-stu-id="5090e-107">DESCRIPTION</span></span>
<span data-ttu-id="5090e-108">**AzureVMDiagnosticsExtension** Cmdlet 會在虛擬機器上配置 Microsoft Azure 診斷擴展外掛程式。</span><span class="sxs-lookup"><span data-stu-id="5090e-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5090e-109">示例</span><span class="sxs-lookup"><span data-stu-id="5090e-109">EXAMPLES</span></span>

### <span data-ttu-id="5090e-110">範例1：建立已套用 Azure Diagnostics 延伸的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5090e-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="5090e-111">這些命令會在虛擬機器上啟用 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="5090e-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="5090e-112">範例2：在現有的虛擬機器上啟用 Azure 診斷延伸</span><span class="sxs-lookup"><span data-stu-id="5090e-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="5090e-113">第一個命令使用 **add-azurevm** Cmdlet 來取得虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5090e-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="5090e-114">第二個命令使用 **AzureVMDiagnosticsExtension** Cmdlet 來更新虛擬機器設定，以包括 Azure Diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="5090e-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="5090e-115">最後一個命令會將更新的設定套用至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5090e-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="5090e-116">參數</span><span class="sxs-lookup"><span data-stu-id="5090e-116">PARAMETERS</span></span>

### <span data-ttu-id="5090e-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="5090e-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="5090e-118">指定診斷設定的路徑。</span><span class="sxs-lookup"><span data-stu-id="5090e-118">Specifies a path for the diagnostics configuration.</span></span>

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

### <span data-ttu-id="5090e-119">-停用</span><span class="sxs-lookup"><span data-stu-id="5090e-119">-Disable</span></span>
<span data-ttu-id="5090e-120">表示此 Cmdlet 會停用虛擬機器上的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="5090e-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5090e-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5090e-121">-InformationAction</span></span>
<span data-ttu-id="5090e-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="5090e-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5090e-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5090e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5090e-124">持續</span><span class="sxs-lookup"><span data-stu-id="5090e-124">Continue</span></span>
- <span data-ttu-id="5090e-125">理會</span><span class="sxs-lookup"><span data-stu-id="5090e-125">Ignore</span></span>
- <span data-ttu-id="5090e-126">看</span><span class="sxs-lookup"><span data-stu-id="5090e-126">Inquire</span></span>
- <span data-ttu-id="5090e-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5090e-127">SilentlyContinue</span></span>
- <span data-ttu-id="5090e-128">停止</span><span class="sxs-lookup"><span data-stu-id="5090e-128">Stop</span></span>
- <span data-ttu-id="5090e-129">封存</span><span class="sxs-lookup"><span data-stu-id="5090e-129">Suspend</span></span>

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

### <span data-ttu-id="5090e-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5090e-130">-InformationVariable</span></span>
<span data-ttu-id="5090e-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="5090e-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5090e-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5090e-132">-Profile</span></span>
<span data-ttu-id="5090e-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5090e-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5090e-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5090e-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5090e-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="5090e-135">-ReferenceName</span></span>
<span data-ttu-id="5090e-136">指定診斷延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="5090e-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5090e-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="5090e-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="5090e-138">指定儲存空間帳戶端點。</span><span class="sxs-lookup"><span data-stu-id="5090e-138">Specifies a storage account endpoint.</span></span>

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

### <span data-ttu-id="5090e-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5090e-139">-StorageAccountKey</span></span>
<span data-ttu-id="5090e-140">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="5090e-140">Specifies a storage account key.</span></span>

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

### <span data-ttu-id="5090e-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5090e-141">-StorageAccountName</span></span>
<span data-ttu-id="5090e-142">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5090e-142">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="5090e-143">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5090e-143">-StorageContext</span></span>
<span data-ttu-id="5090e-144">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5090e-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5090e-145">-版本</span><span class="sxs-lookup"><span data-stu-id="5090e-145">-Version</span></span>
<span data-ttu-id="5090e-146">將擴充版本指定為字串。</span><span class="sxs-lookup"><span data-stu-id="5090e-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5090e-147">-VM</span><span class="sxs-lookup"><span data-stu-id="5090e-147">-VM</span></span>
<span data-ttu-id="5090e-148">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="5090e-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5090e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5090e-149">CommonParameters</span></span>
<span data-ttu-id="5090e-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5090e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5090e-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5090e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5090e-152">輸入</span><span class="sxs-lookup"><span data-stu-id="5090e-152">INPUTS</span></span>

## <span data-ttu-id="5090e-153">輸出</span><span class="sxs-lookup"><span data-stu-id="5090e-153">OUTPUTS</span></span>

## <span data-ttu-id="5090e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="5090e-154">NOTES</span></span>

## <span data-ttu-id="5090e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="5090e-155">RELATED LINKS</span></span>

[<span data-ttu-id="5090e-156">AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5090e-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5090e-157">移除-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5090e-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5090e-158">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5090e-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


