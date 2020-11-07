---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967236"
---
# <span data-ttu-id="98f1b-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="98f1b-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="98f1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="98f1b-103">在虛擬機器上設定 Azure SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="98f1b-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="98f1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="98f1b-104">SYNTAX</span></span>

### <span data-ttu-id="98f1b-105">EnableSqlServerExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="98f1b-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="98f1b-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="98f1b-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="98f1b-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="98f1b-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="98f1b-108">說明</span><span class="sxs-lookup"><span data-stu-id="98f1b-108">DESCRIPTION</span></span>
<span data-ttu-id="98f1b-109">**AzureVMSqlServerExtension** Cmdlet 會在虛擬機器上設定 Azure SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="98f1b-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="98f1b-110">示例</span><span class="sxs-lookup"><span data-stu-id="98f1b-110">EXAMPLES</span></span>

### <span data-ttu-id="98f1b-111">範例1：在虛擬機器上設定自動修補設定</span><span class="sxs-lookup"><span data-stu-id="98f1b-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="98f1b-112">這個命令會在 Azure 虛擬機器上設定自動修補設定。</span><span class="sxs-lookup"><span data-stu-id="98f1b-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="98f1b-113">範例2：在虛擬機器上設定自動備份設定</span><span class="sxs-lookup"><span data-stu-id="98f1b-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="98f1b-114">這個命令會在 Azure 虛擬機器上設定自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="98f1b-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="98f1b-115">範例3：停用虛擬機器上的 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="98f1b-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="98f1b-116">這個命令會在指定的虛擬機器上停用 SQL Server 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="98f1b-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="98f1b-117">範例4：卸載特定虛擬機器上的 SQL Server extension （機器翻譯）</span><span class="sxs-lookup"><span data-stu-id="98f1b-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="98f1b-118">這個命令會在名為 VMName 的虛擬機器上卸載 SQL Server 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="98f1b-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="98f1b-119">參數</span><span class="sxs-lookup"><span data-stu-id="98f1b-119">PARAMETERS</span></span>

### <span data-ttu-id="98f1b-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="98f1b-120">-AutoBackupSettings</span></span>
<span data-ttu-id="98f1b-121">指定自動 SQL Server 備份設定。</span><span class="sxs-lookup"><span data-stu-id="98f1b-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="98f1b-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="98f1b-123">指定自動 SQL Server 修補設定。</span><span class="sxs-lookup"><span data-stu-id="98f1b-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-124">-停用</span><span class="sxs-lookup"><span data-stu-id="98f1b-124">-Disable</span></span>
<span data-ttu-id="98f1b-125">表示此 Cmdlet 會停用延伸狀態。</span><span class="sxs-lookup"><span data-stu-id="98f1b-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="98f1b-126">-InformationAction</span></span>
<span data-ttu-id="98f1b-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="98f1b-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="98f1b-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="98f1b-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98f1b-129">持續</span><span class="sxs-lookup"><span data-stu-id="98f1b-129">Continue</span></span>
- <span data-ttu-id="98f1b-130">理會</span><span class="sxs-lookup"><span data-stu-id="98f1b-130">Ignore</span></span>
- <span data-ttu-id="98f1b-131">看</span><span class="sxs-lookup"><span data-stu-id="98f1b-131">Inquire</span></span>
- <span data-ttu-id="98f1b-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98f1b-132">SilentlyContinue</span></span>
- <span data-ttu-id="98f1b-133">停止</span><span class="sxs-lookup"><span data-stu-id="98f1b-133">Stop</span></span>
- <span data-ttu-id="98f1b-134">封存</span><span class="sxs-lookup"><span data-stu-id="98f1b-134">Suspend</span></span>

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

### <span data-ttu-id="98f1b-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98f1b-135">-InformationVariable</span></span>
<span data-ttu-id="98f1b-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="98f1b-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98f1b-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="98f1b-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="98f1b-138">指定金鑰保存庫認證設定。</span><span class="sxs-lookup"><span data-stu-id="98f1b-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="98f1b-139">-Profile</span></span>
<span data-ttu-id="98f1b-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="98f1b-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98f1b-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="98f1b-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98f1b-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="98f1b-142">-ReferenceName</span></span>
<span data-ttu-id="98f1b-143">指定 SQL Server 延伸的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="98f1b-143">Specifies the reference name of the SQL Server extension.</span></span>

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

### <span data-ttu-id="98f1b-144">-卸載</span><span class="sxs-lookup"><span data-stu-id="98f1b-144">-Uninstall</span></span>
<span data-ttu-id="98f1b-145">表示此 Cmdlet 會從虛擬機器卸載 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="98f1b-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f1b-146">-版本</span><span class="sxs-lookup"><span data-stu-id="98f1b-146">-Version</span></span>
<span data-ttu-id="98f1b-147">指定 Get-AzureVMSqlServerExtension 從中檢索設定的 SQL Server 延伸版本。</span><span class="sxs-lookup"><span data-stu-id="98f1b-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="98f1b-148">-VM</span><span class="sxs-lookup"><span data-stu-id="98f1b-148">-VM</span></span>
<span data-ttu-id="98f1b-149">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="98f1b-149">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="98f1b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f1b-150">CommonParameters</span></span>
<span data-ttu-id="98f1b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98f1b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f1b-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98f1b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f1b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="98f1b-153">INPUTS</span></span>

## <span data-ttu-id="98f1b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="98f1b-154">OUTPUTS</span></span>

## <span data-ttu-id="98f1b-155">筆記</span><span class="sxs-lookup"><span data-stu-id="98f1b-155">NOTES</span></span>

## <span data-ttu-id="98f1b-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="98f1b-156">RELATED LINKS</span></span>

[<span data-ttu-id="98f1b-157">AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="98f1b-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="98f1b-158">移除-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="98f1b-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


