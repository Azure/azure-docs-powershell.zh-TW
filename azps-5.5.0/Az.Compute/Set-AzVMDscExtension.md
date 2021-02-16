---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138595"
---
# <span data-ttu-id="d9197-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9197-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="d9197-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9197-102">SYNOPSIS</span></span>
<span data-ttu-id="d9197-103">在虛擬機器上配置 DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="d9197-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d9197-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9197-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9197-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9197-105">DESCRIPTION</span></span>
<span data-ttu-id="d9197-106">AzVMDscExtension Cmdlet 會在資源群組中的虛擬機器上 **設定** Windows PowerShell 所需的狀態設定 (DSC) 延伸。</span><span class="sxs-lookup"><span data-stu-id="d9197-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="d9197-107">示例</span><span class="sxs-lookup"><span data-stu-id="d9197-107">EXAMPLES</span></span>

### <span data-ttu-id="d9197-108">範例1：設定 DSC 延伸</span><span class="sxs-lookup"><span data-stu-id="d9197-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d9197-109">這個命令會將名為 VM07 的虛擬機器上的 DSC 延伸設定為從名為 Stg 的儲存空間帳戶和預設容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="d9197-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="d9197-110">命令會調用名為 ConfigName 的配置。</span><span class="sxs-lookup"><span data-stu-id="d9197-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="d9197-111">先前已使用 **Publish AzVMDscConfiguration** 上傳 Sample.ps1.zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="d9197-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d9197-112">範例2：使用配置資料設定 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="d9197-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d9197-113">這個命令會在名為 VM13 的虛擬機器上設定副檔名，以從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="d9197-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d9197-114">配置名為 ConfigName 的命令，並指定設定資料和引數。</span><span class="sxs-lookup"><span data-stu-id="d9197-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d9197-115">先前已使用 **Publish AzVMDscConfiguration** 上傳 Sample.ps1.zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="d9197-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d9197-116">範例3：設定具有自動更新之設定資料的 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="d9197-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="d9197-117">這個命令會在名為 VM22 的虛擬機器上設定副檔名，以從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="d9197-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d9197-118">此命令會調用名為 ConfigName 的設定，並指定配置資料和引數。</span><span class="sxs-lookup"><span data-stu-id="d9197-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d9197-119">這個命令也可自動將延伸處理常式更新為最新版本。</span><span class="sxs-lookup"><span data-stu-id="d9197-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="d9197-120">先前是使用 **Publish AzVMDscConfiguration** 上傳的 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="d9197-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="d9197-121">參數</span><span class="sxs-lookup"><span data-stu-id="d9197-121">PARAMETERS</span></span>

### <span data-ttu-id="d9197-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="d9197-122">-ArchiveBlobName</span></span>
<span data-ttu-id="d9197-123">指定先前由 Publish-AzVMDscConfiguration Cmdlet 上傳的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="d9197-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="d9197-124">-ArchiveContainerName</span></span>
<span data-ttu-id="d9197-125">Species 配置封存所在之 Azure 儲存體容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="d9197-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9197-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="d9197-127">指定包含配置封存之儲存空間帳戶的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="d9197-128">如果儲存空間帳戶和虛擬機器都在相同的資源群組中，則此參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d9197-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="d9197-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9197-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="d9197-130">指定用來下載 ArchiveBlobName 的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="d9197-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9197-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="d9197-132">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="d9197-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="d9197-133">-自動更新</span><span class="sxs-lookup"><span data-stu-id="d9197-133">-AutoUpdate</span></span>
<span data-ttu-id="d9197-134">指定 *version* 參數所指定的延伸處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="d9197-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="d9197-135">根據預設，延伸處理常式不會 autoupdated。</span><span class="sxs-lookup"><span data-stu-id="d9197-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="d9197-136">使用 *自動* 更新參數，即可將延伸處理常式自動更新為最新版本，以及何時可用。</span><span class="sxs-lookup"><span data-stu-id="d9197-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="d9197-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="d9197-137">-ConfigurationArgument</span></span>
<span data-ttu-id="d9197-138">指定包含配置函數引數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d9197-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="d9197-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d9197-139">-ConfigurationData</span></span>
<span data-ttu-id="d9197-140">指定 psd1 檔案的路徑，該檔案會指定設定的資料。</span><span class="sxs-lookup"><span data-stu-id="d9197-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="d9197-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d9197-141">-ConfigurationName</span></span>
<span data-ttu-id="d9197-142">指定 DSC 延伸設定的配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="d9197-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="d9197-143">-DataCollection</span></span>
<span data-ttu-id="d9197-144">指定資料收集類型。</span><span class="sxs-lookup"><span data-stu-id="d9197-144">Specifies the data collection type.</span></span>
<span data-ttu-id="d9197-145">此參數可接受的值為： [啟用] 與 [停用]。</span><span class="sxs-lookup"><span data-stu-id="d9197-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="d9197-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9197-146">-DefaultProfile</span></span>
<span data-ttu-id="d9197-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9197-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9197-148">-Force</span><span class="sxs-lookup"><span data-stu-id="d9197-148">-Force</span></span>
<span data-ttu-id="d9197-149">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d9197-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9197-150">-位置</span><span class="sxs-lookup"><span data-stu-id="d9197-150">-Location</span></span>
<span data-ttu-id="d9197-151">指定資源延伸的路徑。</span><span class="sxs-lookup"><span data-stu-id="d9197-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="d9197-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9197-152">-Name</span></span>
<span data-ttu-id="d9197-153">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d9197-154">預設值為 Microsoft Powershell。</span><span class="sxs-lookup"><span data-stu-id="d9197-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="d9197-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9197-155">-NoWait</span></span>
<span data-ttu-id="d9197-156">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="d9197-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d9197-157">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="d9197-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d9197-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9197-158">-ResourceGroupName</span></span>
<span data-ttu-id="d9197-159">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d9197-160">-版本</span><span class="sxs-lookup"><span data-stu-id="d9197-160">-Version</span></span>
<span data-ttu-id="d9197-161">指定 Set-AzVMDscExtension 套用設定的 DSC 副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="d9197-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="d9197-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="d9197-162">-VMName</span></span>
<span data-ttu-id="d9197-163">指定安裝 DSC 延伸處理常式的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d9197-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="d9197-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="d9197-164">-WmfVersion</span></span>
<span data-ttu-id="d9197-165">指定 WMF 版本。</span><span class="sxs-lookup"><span data-stu-id="d9197-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="d9197-166">-確認</span><span class="sxs-lookup"><span data-stu-id="d9197-166">-Confirm</span></span>
<span data-ttu-id="d9197-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9197-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9197-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9197-168">-WhatIf</span></span>
<span data-ttu-id="d9197-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9197-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9197-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9197-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9197-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9197-171">CommonParameters</span></span>
<span data-ttu-id="d9197-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9197-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9197-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9197-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9197-174">輸入</span><span class="sxs-lookup"><span data-stu-id="d9197-174">INPUTS</span></span>

### <span data-ttu-id="d9197-175">System.object</span><span class="sxs-lookup"><span data-stu-id="d9197-175">System.String</span></span>

### <span data-ttu-id="d9197-176">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9197-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9197-177">輸出</span><span class="sxs-lookup"><span data-stu-id="d9197-177">OUTPUTS</span></span>

### <span data-ttu-id="d9197-178">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d9197-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d9197-179">筆記</span><span class="sxs-lookup"><span data-stu-id="d9197-179">NOTES</span></span>

## <span data-ttu-id="d9197-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9197-180">RELATED LINKS</span></span>

[<span data-ttu-id="d9197-181">AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9197-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="d9197-182">移除-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d9197-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="d9197-183">發佈-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9197-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


