---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398235"
---
# <span data-ttu-id="78b2d-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78b2d-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="78b2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="78b2d-103">設定虛擬機器上的 Azure SQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="78b2d-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="78b2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="78b2d-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78b2d-105">描述</span><span class="sxs-lookup"><span data-stu-id="78b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="78b2d-106">**Set-AzCMSqlServerExtension** Cmdlet 會設定虛擬機器上的 AzureSQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="78b2d-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="78b2d-107">例子</span><span class="sxs-lookup"><span data-stu-id="78b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="78b2d-108">範例 1：在虛擬機器上設定自動修補設定</span><span class="sxs-lookup"><span data-stu-id="78b2d-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="78b2d-109">第一個命令會使用 **New-AzureCMSqlServerAutoPatchingConfig** Cmdlet 來建立組組物件。</span><span class="sxs-lookup"><span data-stu-id="78b2d-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="78b2d-110">該命令將組$AutoPatchingConfig變數。</span><span class="sxs-lookup"><span data-stu-id="78b2d-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="78b2d-111">第二個命令會使用 Get-AzVM Cmdlet，在名為 Service02 的服務上，獲得名為 VirtualMachine11 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="78b2d-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="78b2d-112">該命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="78b2d-113">目前的 Cmdlet 會針對虛擬機器$AutoPatchingConfig自動修補設定。</span><span class="sxs-lookup"><span data-stu-id="78b2d-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="78b2d-114">該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="78b2d-115">範例 2：在虛擬機器上設定自動備份設定</span><span class="sxs-lookup"><span data-stu-id="78b2d-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="78b2d-116">第一個命令會使用 **New-AzureCMSqlServerAutoBackupConfig** Cmdlet 建立組組物件。</span><span class="sxs-lookup"><span data-stu-id="78b2d-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="78b2d-117">命令會儲存此$AutoBackupConfig變數。</span><span class="sxs-lookup"><span data-stu-id="78b2d-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="78b2d-118">第二個命令會獲得名為 Service02 的服務上名為 VirtualMachine11 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="78b2d-119">目前的 Cmdlet 會設定$AutoBackupConfig的自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="78b2d-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="78b2d-120">該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="78b2d-121">範例 3：停用虛擬機器上的 SQL Server 擴充功能</span><span class="sxs-lookup"><span data-stu-id="78b2d-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="78b2d-122">此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="78b2d-123">該命令會停用該虛擬機器上的 SQL Server 虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="78b2d-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="78b2d-124">範例 4：卸載特定虛擬機器上的 SQL Server 擴充功能</span><span class="sxs-lookup"><span data-stu-id="78b2d-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="78b2d-125">此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="78b2d-126">該命令會卸載該虛擬機器上的 SQL Server 虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="78b2d-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="78b2d-127">參數</span><span class="sxs-lookup"><span data-stu-id="78b2d-127">PARAMETERS</span></span>

### <span data-ttu-id="78b2d-128">-自動BackupSettings</span><span class="sxs-lookup"><span data-stu-id="78b2d-128">-AutoBackupSettings</span></span>
<span data-ttu-id="78b2d-129">指定 SQL Server 自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="78b2d-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="78b2d-130">若要建立 **AutoBackupSettings 物件** ，請使用 New-AzureVMSqlServerAutoBackupConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-131">-自動修補設定</span><span class="sxs-lookup"><span data-stu-id="78b2d-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="78b2d-132">指定自動 SQL Server 修補設定。</span><span class="sxs-lookup"><span data-stu-id="78b2d-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="78b2d-133">若要建立 **AutoPatchingSettings 物件** ，請使用 New-AzureVMSqlServerAutoPatchingConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78b2d-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b2d-134">-DefaultProfile</span></span>
<span data-ttu-id="78b2d-135">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78b2d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="78b2d-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-137">-位置</span><span class="sxs-lookup"><span data-stu-id="78b2d-137">-Location</span></span>
<span data-ttu-id="78b2d-138">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="78b2d-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="78b2d-139">-Name</span></span>
<span data-ttu-id="78b2d-140">指定擴充功能 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="78b2d-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="78b2d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b2d-141">-ResourceGroupName</span></span>
<span data-ttu-id="78b2d-142">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="78b2d-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-143">-版本</span><span class="sxs-lookup"><span data-stu-id="78b2d-143">-Version</span></span>
<span data-ttu-id="78b2d-144">指定 SQL Server 擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="78b2d-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="78b2d-145">-VMName</span></span>
<span data-ttu-id="78b2d-146">指定此 Cmdlet 設定 SQL Server 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="78b2d-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b2d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b2d-147">CommonParameters</span></span>
<span data-ttu-id="78b2d-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78b2d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b2d-149">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="78b2d-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b2d-150">輸入</span><span class="sxs-lookup"><span data-stu-id="78b2d-150">INPUTS</span></span>

### <span data-ttu-id="78b2d-151">沒有</span><span class="sxs-lookup"><span data-stu-id="78b2d-151">None</span></span>
<span data-ttu-id="78b2d-152">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="78b2d-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78b2d-153">輸出</span><span class="sxs-lookup"><span data-stu-id="78b2d-153">OUTPUTS</span></span>

### <span data-ttu-id="78b2d-154">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78b2d-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="78b2d-155">筆記</span><span class="sxs-lookup"><span data-stu-id="78b2d-155">NOTES</span></span>

## <span data-ttu-id="78b2d-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="78b2d-156">RELATED LINKS</span></span>

[<span data-ttu-id="78b2d-157">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="78b2d-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="78b2d-158">Get-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78b2d-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="78b2d-159">New-AzureMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="78b2d-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="78b2d-160">New-AzureMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="78b2d-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="78b2d-161">Remove-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="78b2d-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="78b2d-162">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="78b2d-162">Update-AzVM</span></span>](./Update-AzVM.md)


