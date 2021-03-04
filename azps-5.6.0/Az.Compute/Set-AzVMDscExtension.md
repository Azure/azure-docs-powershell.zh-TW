---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: facd5a3637dcb1a8a392171468dd890279ba0f74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903298"
---
# <span data-ttu-id="647aa-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="647aa-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="647aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="647aa-102">SYNOPSIS</span></span>
<span data-ttu-id="647aa-103">設定虛擬機器上的 DSC 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="647aa-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="647aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="647aa-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="647aa-105">描述</span><span class="sxs-lookup"><span data-stu-id="647aa-105">DESCRIPTION</span></span>
<span data-ttu-id="647aa-106">**Set-Az VIRTUALDscExtension** Cmdlet 會設定資源群組中虛擬機器上的 Windows PowerShell 需要狀態設定 (DSC) 副檔名。</span><span class="sxs-lookup"><span data-stu-id="647aa-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="647aa-107">例子</span><span class="sxs-lookup"><span data-stu-id="647aa-107">EXAMPLES</span></span>

### <span data-ttu-id="647aa-108">範例 1：設定 DSC 擴充功能</span><span class="sxs-lookup"><span data-stu-id="647aa-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="647aa-109">此命令會設定名為 VM07 的虛擬機器上的 DSC 副檔名，Sample.ps1.zip從名為 Stg 和預設容器的儲存空間帳戶下載資料。</span><span class="sxs-lookup"><span data-stu-id="647aa-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="647aa-110">該命令會叫用名為 ConfigName 的組配置。</span><span class="sxs-lookup"><span data-stu-id="647aa-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="647aa-111">此Sample.ps1.zip先前是使用 **Publish-AzCONFIGDscConfiguration 上傳** 的。</span><span class="sxs-lookup"><span data-stu-id="647aa-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="647aa-112">範例 2：使用設定資料設定 DSC 擴充功能</span><span class="sxs-lookup"><span data-stu-id="647aa-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="647aa-113">此命令在名為 VM13 的虛擬機器上設定副檔名，Sample.ps1.zip從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載資料。</span><span class="sxs-lookup"><span data-stu-id="647aa-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="647aa-114">命令名稱為 ConfigName 的組配置，並指定組組資料和引數。</span><span class="sxs-lookup"><span data-stu-id="647aa-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="647aa-115">此Sample.ps1.zip先前是使用 **Publish-AzCONFIGDscConfiguration 上傳** 的。</span><span class="sxs-lookup"><span data-stu-id="647aa-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="647aa-116">範例 3：設定具有自動更新之設定資料的 DSC 擴充功能</span><span class="sxs-lookup"><span data-stu-id="647aa-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="647aa-117">此命令在名為 VM22 的虛擬機器上設定副檔名，Sample.ps1.zip從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載資料。</span><span class="sxs-lookup"><span data-stu-id="647aa-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="647aa-118">該命令會叫用名為 ConfigName 的群組原則，並指定組組資料和引數。</span><span class="sxs-lookup"><span data-stu-id="647aa-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="647aa-119">此命令也會啟用將擴充功能處理常式自動更新為最新版本。</span><span class="sxs-lookup"><span data-stu-id="647aa-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="647aa-120">此Sample.ps1.zip先前是使用 **Publish-AzEVDscConfiguration 上傳**。</span><span class="sxs-lookup"><span data-stu-id="647aa-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="647aa-121">參數</span><span class="sxs-lookup"><span data-stu-id="647aa-121">PARAMETERS</span></span>

### <span data-ttu-id="647aa-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="647aa-122">-ArchiveBlobName</span></span>
<span data-ttu-id="647aa-123">指定先前由 Cmdlet 上傳的組Publish-AzVMDscConfiguration名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="647aa-124">-ArchiveContainerName</span></span>
<span data-ttu-id="647aa-125">組配置存檔所在的 Azure 儲存容器的種名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647aa-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="647aa-127">指定包含包含組配置存檔之儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="647aa-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="647aa-128">如果儲存帳戶和虛擬機器都在同一個資源群組中，則此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="647aa-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="647aa-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="647aa-130">指定用來下載 ArchiveBlobName 的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="647aa-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="647aa-132">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="647aa-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="647aa-133">-AutoUpdate</span></span>
<span data-ttu-id="647aa-134">指定 Version 參數指定的擴充 *處理常式版本。*</span><span class="sxs-lookup"><span data-stu-id="647aa-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="647aa-135">根據預設，擴充功能處理常式不會自動upup。</span><span class="sxs-lookup"><span data-stu-id="647aa-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="647aa-136">使用 *AutoUpdate* 參數，在擴充處理常式可用時啟用自動更新至最新版本。</span><span class="sxs-lookup"><span data-stu-id="647aa-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="647aa-137">-ConfigurationArgument</span></span>
<span data-ttu-id="647aa-138">指定包含組調函數引數的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="647aa-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="647aa-139">-ConfigurationData</span></span>
<span data-ttu-id="647aa-140">指定指定組案資料的 .psd1 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="647aa-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="647aa-141">-ConfigurationName</span></span>
<span data-ttu-id="647aa-142">指定 DSC Extension 所叫用之群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="647aa-143">-DataCollection</span></span>
<span data-ttu-id="647aa-144">指定資料收集類型。</span><span class="sxs-lookup"><span data-stu-id="647aa-144">Specifies the data collection type.</span></span>
<span data-ttu-id="647aa-145">此參數可接受的值為：啟用和停用。</span><span class="sxs-lookup"><span data-stu-id="647aa-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647aa-146">-DefaultProfile</span></span>
<span data-ttu-id="647aa-147">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="647aa-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="647aa-148">-強制</span><span class="sxs-lookup"><span data-stu-id="647aa-148">-Force</span></span>
<span data-ttu-id="647aa-149">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="647aa-149">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-150">-位置</span><span class="sxs-lookup"><span data-stu-id="647aa-150">-Location</span></span>
<span data-ttu-id="647aa-151">指定資源延伸的路徑。</span><span class="sxs-lookup"><span data-stu-id="647aa-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="647aa-152">-Name</span></span>
<span data-ttu-id="647aa-153">指定代表擴充功能之 Azure Resource Manager 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="647aa-154">預設值為 Microsoft.Powershell.DSC。</span><span class="sxs-lookup"><span data-stu-id="647aa-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="647aa-155">-NoWait</span></span>
<span data-ttu-id="647aa-156">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="647aa-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="647aa-157">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="647aa-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647aa-158">-ResourceGroupName</span></span>
<span data-ttu-id="647aa-159">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="647aa-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="647aa-160">-版本</span><span class="sxs-lookup"><span data-stu-id="647aa-160">-Version</span></span>
<span data-ttu-id="647aa-161">指定您適用設定Set-AzVMDscExtension DSC 擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="647aa-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="647aa-162">-VMName</span></span>
<span data-ttu-id="647aa-163">指定安裝 DSC 擴充處理常式的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="647aa-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="647aa-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="647aa-164">-WmfVersion</span></span>
<span data-ttu-id="647aa-165">指定 WMF 版本。</span><span class="sxs-lookup"><span data-stu-id="647aa-165">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-166">-確認</span><span class="sxs-lookup"><span data-stu-id="647aa-166">-Confirm</span></span>
<span data-ttu-id="647aa-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="647aa-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647aa-168">-WhatIf</span></span>
<span data-ttu-id="647aa-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="647aa-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="647aa-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="647aa-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647aa-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647aa-171">CommonParameters</span></span>
<span data-ttu-id="647aa-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="647aa-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647aa-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="647aa-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647aa-174">輸入</span><span class="sxs-lookup"><span data-stu-id="647aa-174">INPUTS</span></span>

### <span data-ttu-id="647aa-175">System.String</span><span class="sxs-lookup"><span data-stu-id="647aa-175">System.String</span></span>

### <span data-ttu-id="647aa-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="647aa-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="647aa-177">輸出</span><span class="sxs-lookup"><span data-stu-id="647aa-177">OUTPUTS</span></span>

### <span data-ttu-id="647aa-178">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="647aa-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="647aa-179">筆記</span><span class="sxs-lookup"><span data-stu-id="647aa-179">NOTES</span></span>

## <span data-ttu-id="647aa-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="647aa-180">RELATED LINKS</span></span>

[<span data-ttu-id="647aa-181">Get-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="647aa-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="647aa-182">Remove-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="647aa-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="647aa-183">Publish-AzMSDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="647aa-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


