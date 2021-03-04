---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 9aa895245f491e7b7ee077d083f052cd7e4e46e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910254"
---
# <span data-ttu-id="30cf9-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="30cf9-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="30cf9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="30cf9-103">設定虛擬機器上的 Azure SQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="30cf9-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="30cf9-104">語法</span><span class="sxs-lookup"><span data-stu-id="30cf9-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30cf9-105">描述</span><span class="sxs-lookup"><span data-stu-id="30cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="30cf9-106">**Set-AzCMSqlServerExtension** Cmdlet 會設定虛擬機器上的 AzureSQL Server 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="30cf9-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="30cf9-107">例子</span><span class="sxs-lookup"><span data-stu-id="30cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="30cf9-108">範例 1：在虛擬機器上設定自動修補設定</span><span class="sxs-lookup"><span data-stu-id="30cf9-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="30cf9-109">第一個命令會使用 **New-AzCMSqlServerAutoPatchingConfig** Cmdlet 來建立組組物件。</span><span class="sxs-lookup"><span data-stu-id="30cf9-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="30cf9-110">該命令將組$AutoPatchingConfig變數。</span><span class="sxs-lookup"><span data-stu-id="30cf9-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="30cf9-111">第二個命令會使用 Get-AzVM Cmdlet，在名為 Service02 的服務上，獲得名為 VirtualMachine11 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="30cf9-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="30cf9-112">該命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="30cf9-113">目前的 Cmdlet 會針對虛擬機器$AutoPatchingConfig自動修補設定。</span><span class="sxs-lookup"><span data-stu-id="30cf9-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="30cf9-114">該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="30cf9-115">範例 2：在虛擬機器上設定自動備份設定</span><span class="sxs-lookup"><span data-stu-id="30cf9-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="30cf9-116">第一個命令會使用 **New-AzCMSqlServerAutoBackupConfig Cmdlet 建立** 組組物件。</span><span class="sxs-lookup"><span data-stu-id="30cf9-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="30cf9-117">該命令將組$AutoBackupConfig變數。</span><span class="sxs-lookup"><span data-stu-id="30cf9-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="30cf9-118">第二個命令會獲得名為 Service02 的服務上名為 VirtualMachine11 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="30cf9-119">目前的 Cmdlet 會設定$AutoBackupConfig的自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="30cf9-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="30cf9-120">該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="30cf9-121">範例 3：停用虛擬機器上的 SQL Server 擴充功能</span><span class="sxs-lookup"><span data-stu-id="30cf9-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="30cf9-122">此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="30cf9-123">該命令會停用該虛擬機器上的 SQL Server 虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="30cf9-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="30cf9-124">範例 4：卸載特定虛擬機器上的 SQL Server 擴充功能</span><span class="sxs-lookup"><span data-stu-id="30cf9-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="30cf9-125">此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="30cf9-126">該命令會卸載該虛擬機器上的 SQL Server 虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="30cf9-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="30cf9-127">參數</span><span class="sxs-lookup"><span data-stu-id="30cf9-127">PARAMETERS</span></span>

### <span data-ttu-id="30cf9-128">-自動BackupSettings</span><span class="sxs-lookup"><span data-stu-id="30cf9-128">-AutoBackupSettings</span></span>
<span data-ttu-id="30cf9-129">指定 SQL Server 自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="30cf9-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="30cf9-130">若要建立 **AutoBackupSettings 物件** ，請使用 New-AzVMSqlServerAutoBackupConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-131">-自動修補設定</span><span class="sxs-lookup"><span data-stu-id="30cf9-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="30cf9-132">指定自動 SQL Server 修補設定。</span><span class="sxs-lookup"><span data-stu-id="30cf9-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="30cf9-133">若要建立 **AutoPatchingSettings 物件** ，請使用 New-AzVMSqlServerAutoPatchingConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30cf9-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cf9-134">-DefaultProfile</span></span>
<span data-ttu-id="30cf9-135">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30cf9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="30cf9-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-137">-位置</span><span class="sxs-lookup"><span data-stu-id="30cf9-137">-Location</span></span>
<span data-ttu-id="30cf9-138">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="30cf9-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="30cf9-139">-Name</span></span>
<span data-ttu-id="30cf9-140">指定擴充功能 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="30cf9-140">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30cf9-141">-ResourceGroupName</span></span>
<span data-ttu-id="30cf9-142">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="30cf9-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-143">-版本</span><span class="sxs-lookup"><span data-stu-id="30cf9-143">-Version</span></span>
<span data-ttu-id="30cf9-144">指定 SQL Server 擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="30cf9-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="30cf9-145">-VMName</span></span>
<span data-ttu-id="30cf9-146">指定此 Cmdlet 設定 SQL Server 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="30cf9-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30cf9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cf9-147">CommonParameters</span></span>
<span data-ttu-id="30cf9-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30cf9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cf9-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30cf9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cf9-150">輸入</span><span class="sxs-lookup"><span data-stu-id="30cf9-150">INPUTS</span></span>

### <span data-ttu-id="30cf9-151">System.String</span><span class="sxs-lookup"><span data-stu-id="30cf9-151">System.String</span></span>

### <span data-ttu-id="30cf9-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="30cf9-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="30cf9-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="30cf9-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="30cf9-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="30cf9-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="30cf9-155">輸出</span><span class="sxs-lookup"><span data-stu-id="30cf9-155">OUTPUTS</span></span>

### <span data-ttu-id="30cf9-156">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="30cf9-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="30cf9-157">筆記</span><span class="sxs-lookup"><span data-stu-id="30cf9-157">NOTES</span></span>

## <span data-ttu-id="30cf9-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="30cf9-158">RELATED LINKS</span></span>

[<span data-ttu-id="30cf9-159">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="30cf9-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="30cf9-160">Get-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="30cf9-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="30cf9-161">New-AzMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="30cf9-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="30cf9-162">New-AzMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="30cf9-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="30cf9-163">Remove-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="30cf9-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="30cf9-164">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="30cf9-164">Update-AzVM</span></span>](./Update-AzVM.md)


