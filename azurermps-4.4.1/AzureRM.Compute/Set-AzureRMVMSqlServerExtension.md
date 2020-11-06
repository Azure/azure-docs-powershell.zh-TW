---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a89a2fc342bf1a3ed6e311057f55bb83c80be210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447143"
---
# <span data-ttu-id="c39b6-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c39b6-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="c39b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c39b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c39b6-103">在虛擬機器上設定 Azure SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="c39b6-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c39b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c39b6-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c39b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c39b6-105">DESCRIPTION</span></span>
<span data-ttu-id="c39b6-106">**AzureRmVMSqlServerExtension** Cmdlet 會在虛擬機器上設定 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="c39b6-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="c39b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="c39b6-107">EXAMPLES</span></span>

### <span data-ttu-id="c39b6-108">範例1：在虛擬機器上設定自動修補設定</span><span class="sxs-lookup"><span data-stu-id="c39b6-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="c39b6-109">第一個命令會使用 **AzureVMSqlServerAutoPatchingConfig** Cmdlet 建立設定物件。</span><span class="sxs-lookup"><span data-stu-id="c39b6-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="c39b6-110">該命令會將設定儲存在 $AutoPatchingConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="c39b6-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="c39b6-111">第二個命令會透過使用 Get-AzureRmVM Cmdlet，在名為 Service02 的服務上，取得名為 VirtualMachine11 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c39b6-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="c39b6-112">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="c39b6-113">目前的 Cmdlet 會針對虛擬機器設定 $AutoPatchingConfig 中的自動修補設定。</span><span class="sxs-lookup"><span data-stu-id="c39b6-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="c39b6-114">命令會將虛擬機器傳遞到 Update-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="c39b6-115">範例2：在虛擬機器上設定自動備份設定</span><span class="sxs-lookup"><span data-stu-id="c39b6-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="c39b6-116">第一個命令會使用 **AzureVMSqlServerAutoBackupConfig** Cmdlet 建立設定物件。</span><span class="sxs-lookup"><span data-stu-id="c39b6-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="c39b6-117">該命令會將設定儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="c39b6-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="c39b6-118">第二個命令會在名為 Service02 的服務上取得名為 VirtualMachine11 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="c39b6-119">目前的 Cmdlet 會在虛擬機器的 $AutoBackupConfig 中設定自動備份設定。</span><span class="sxs-lookup"><span data-stu-id="c39b6-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="c39b6-120">命令會將虛擬機器傳遞到 Update-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="c39b6-121">範例3：停用虛擬機器上的 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="c39b6-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="c39b6-122">這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="c39b6-123">此命令會在該虛擬機器上停用 SQL Server 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="c39b6-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="c39b6-124">範例4：卸載特定虛擬機器上的 SQL Server extension （機器翻譯）</span><span class="sxs-lookup"><span data-stu-id="c39b6-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="c39b6-125">這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="c39b6-126">此命令會卸載該虛擬機器上的 SQL Server 虛擬機器延伸。</span><span class="sxs-lookup"><span data-stu-id="c39b6-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="c39b6-127">參數</span><span class="sxs-lookup"><span data-stu-id="c39b6-127">PARAMETERS</span></span>

### <span data-ttu-id="c39b6-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="c39b6-128">-AutoBackupSettings</span></span>
<span data-ttu-id="c39b6-129">指定自動 SQL Server 備份設定。</span><span class="sxs-lookup"><span data-stu-id="c39b6-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="c39b6-130">若要建立 **AutoBackupSettings** 物件，請使用 New-AzureVMSqlServerAutoBackupConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="c39b6-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="c39b6-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="c39b6-132">指定自動 SQL Server 修補設定。</span><span class="sxs-lookup"><span data-stu-id="c39b6-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="c39b6-133">若要建立 **AutoPatchingSettings** 物件，請使用 New-AzureVMSqlServerAutoPatchingConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39b6-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="c39b6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39b6-134">-DefaultProfile</span></span>
<span data-ttu-id="c39b6-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c39b6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39b6-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="c39b6-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="c39b6-137">-位置</span><span class="sxs-lookup"><span data-stu-id="c39b6-137">-Location</span></span>
<span data-ttu-id="c39b6-138">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="c39b6-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="c39b6-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="c39b6-139">-Name</span></span>
<span data-ttu-id="c39b6-140">指定副檔名的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c39b6-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="c39b6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39b6-141">-ResourceGroupName</span></span>
<span data-ttu-id="c39b6-142">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c39b6-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c39b6-143">-版本</span><span class="sxs-lookup"><span data-stu-id="c39b6-143">-Version</span></span>
<span data-ttu-id="c39b6-144">指定 SQL Server 延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="c39b6-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="c39b6-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="c39b6-145">-VMName</span></span>
<span data-ttu-id="c39b6-146">指定此 Cmdlet 設定 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c39b6-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="c39b6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39b6-147">CommonParameters</span></span>
<span data-ttu-id="c39b6-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c39b6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39b6-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c39b6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39b6-150">輸入</span><span class="sxs-lookup"><span data-stu-id="c39b6-150">INPUTS</span></span>

## <span data-ttu-id="c39b6-151">輸出</span><span class="sxs-lookup"><span data-stu-id="c39b6-151">OUTPUTS</span></span>

## <span data-ttu-id="c39b6-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c39b6-152">NOTES</span></span>

## <span data-ttu-id="c39b6-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c39b6-153">RELATED LINKS</span></span>

[<span data-ttu-id="c39b6-154">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c39b6-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c39b6-155">AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c39b6-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="c39b6-156">新-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c39b6-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="c39b6-157">新-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c39b6-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="c39b6-158">移除-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c39b6-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="c39b6-159">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c39b6-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

