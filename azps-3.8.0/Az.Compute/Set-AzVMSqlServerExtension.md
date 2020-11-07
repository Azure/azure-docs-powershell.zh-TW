---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797809"
---
# <span data-ttu-id="7ddd7-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7ddd7-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="7ddd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ddd7-102">SYNOPSIS</span></span>
<span data-ttu-id="7ddd7-103">在虛擬機器上設定 Azure SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7ddd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ddd7-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ddd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ddd7-105">DESCRIPTION</span></span>
<span data-ttu-id="7ddd7-106">**AzVMSqlServerExtension** Cmdlet 會在虛擬機器上設定 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7ddd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ddd7-107">EXAMPLES</span></span>

### <span data-ttu-id="7ddd7-108">範例1：在虛擬機器上設定自動修補設定</span><span class="sxs-lookup"><span data-stu-id="7ddd7-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="7ddd7-109">第一個命令會使用 **AzVMSqlServerAutoPatchingConfig** Cmdlet 建立設定物件。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="7ddd7-110">該命令會將設定儲存在 $AutoPatchingConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="7ddd7-111">第二個命令會透過使用 Get-AzVM Cmdlet，在名為 Service02 的服務上，取得名為 VirtualMachine11 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="7ddd7-112">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7ddd7-113">目前的 Cmdlet 會針對虛擬機器設定 $AutoPatchingConfig 中的自動修補設定。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="7ddd7-114">命令會將虛擬機器傳遞到 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="7ddd7-115">範例2：在虛擬機器上設定自動備份設定</span><span class="sxs-lookup"><span data-stu-id="7ddd7-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="7ddd7-116">第一個命令會使用 **AzVMSqlServerAutoBackupConfig** Cmdlet 建立設定物件。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="7ddd7-117">該命令會將設定儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="7ddd7-118">第二個命令會在名為 Service02 的服務上取得名為 VirtualMachine11 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="7ddd7-119">目前的 Cmdlet 會在虛擬機器的 $AutoBackupConfig 中設定自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="7ddd7-120">命令會將虛擬機器傳遞到 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="7ddd7-121">範例3：停用虛擬機器上的 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="7ddd7-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="7ddd7-122">這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="7ddd7-123">此命令會在該虛擬機器上停用 SQL Server 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="7ddd7-124">範例4：卸載特定虛擬機器上的 SQL Server extension （機器翻譯）</span><span class="sxs-lookup"><span data-stu-id="7ddd7-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="7ddd7-125">這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="7ddd7-126">此命令會卸載該虛擬機器上的 SQL Server 虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="7ddd7-127">參數</span><span class="sxs-lookup"><span data-stu-id="7ddd7-127">PARAMETERS</span></span>

### <span data-ttu-id="7ddd7-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="7ddd7-128">-AutoBackupSettings</span></span>
<span data-ttu-id="7ddd7-129">指定自動 SQL Server 備份設定。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="7ddd7-130">若要建立 **AutoBackupSettings** 物件，請使用 New-AzVMSqlServerAutoBackupConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="7ddd7-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="7ddd7-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="7ddd7-132">指定自動 SQL Server 修補設定。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="7ddd7-133">若要建立 **AutoPatchingSettings** 物件，請使用 New-AzVMSqlServerAutoPatchingConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="7ddd7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ddd7-134">-DefaultProfile</span></span>
<span data-ttu-id="7ddd7-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ddd7-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="7ddd7-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="7ddd7-137">-位置</span><span class="sxs-lookup"><span data-stu-id="7ddd7-137">-Location</span></span>
<span data-ttu-id="7ddd7-138">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7ddd7-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ddd7-139">-Name</span></span>
<span data-ttu-id="7ddd7-140">指定副檔名的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="7ddd7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ddd7-141">-ResourceGroupName</span></span>
<span data-ttu-id="7ddd7-142">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7ddd7-143">-版本</span><span class="sxs-lookup"><span data-stu-id="7ddd7-143">-Version</span></span>
<span data-ttu-id="7ddd7-144">指定 SQL Server 延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="7ddd7-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="7ddd7-145">-VMName</span></span>
<span data-ttu-id="7ddd7-146">指定此 Cmdlet 設定 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="7ddd7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ddd7-147">CommonParameters</span></span>
<span data-ttu-id="7ddd7-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ddd7-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ddd7-150">輸入</span><span class="sxs-lookup"><span data-stu-id="7ddd7-150">INPUTS</span></span>

### <span data-ttu-id="7ddd7-151">System.object</span><span class="sxs-lookup"><span data-stu-id="7ddd7-151">System.String</span></span>

### <span data-ttu-id="7ddd7-152">AutoPatchingSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="7ddd7-153">AutoBackupSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="7ddd7-154">KeyVaultCredentialSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="7ddd7-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="7ddd7-155">輸出</span><span class="sxs-lookup"><span data-stu-id="7ddd7-155">OUTPUTS</span></span>

### <span data-ttu-id="7ddd7-156">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7ddd7-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7ddd7-157">筆記</span><span class="sxs-lookup"><span data-stu-id="7ddd7-157">NOTES</span></span>

## <span data-ttu-id="7ddd7-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ddd7-158">RELATED LINKS</span></span>

[<span data-ttu-id="7ddd7-159">AzVM</span><span class="sxs-lookup"><span data-stu-id="7ddd7-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7ddd7-160">AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7ddd7-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="7ddd7-161">新-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="7ddd7-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="7ddd7-162">新-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="7ddd7-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="7ddd7-163">移除-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7ddd7-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="7ddd7-164">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ddd7-164">Update-AzVM</span></span>](./Update-AzVM.md)


