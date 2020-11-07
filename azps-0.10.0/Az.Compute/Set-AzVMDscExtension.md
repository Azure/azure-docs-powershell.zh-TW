---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: ccad3d793ec5763a4c7db44d2b5ff3583b35402b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795861"
---
# <span data-ttu-id="7d066-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7d066-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="7d066-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d066-102">SYNOPSIS</span></span>
<span data-ttu-id="7d066-103">在虛擬機器上配置 DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="7d066-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="7d066-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d066-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d066-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d066-105">DESCRIPTION</span></span>
<span data-ttu-id="7d066-106">AzVMDscExtension Cmdlet 會在資源群組中的虛擬機器上 **設定** Windows PowerShell 所需的狀態設定 (DSC) 延伸。</span><span class="sxs-lookup"><span data-stu-id="7d066-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="7d066-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d066-107">EXAMPLES</span></span>

### <span data-ttu-id="7d066-108">範例1：設定 DSC 延伸</span><span class="sxs-lookup"><span data-stu-id="7d066-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="7d066-109">這個命令會將名為 VM07 的虛擬機器上的 DSC 延伸設定為從名為 Stg 的儲存空間帳戶和預設容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="7d066-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="7d066-110">命令會調用名為 ConfigName 的配置。</span><span class="sxs-lookup"><span data-stu-id="7d066-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="7d066-111">先前已使用 **Publish AzVMDscConfiguration** 上傳 Sample.ps1.zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d066-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="7d066-112">範例2：使用配置資料設定 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="7d066-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="7d066-113">這個命令會在名為 VM13 的虛擬機器上設定副檔名，以從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="7d066-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="7d066-114">配置名為 ConfigName 的命令，並指定設定資料和引數。</span><span class="sxs-lookup"><span data-stu-id="7d066-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="7d066-115">先前已使用 **Publish AzVMDscConfiguration** 上傳 Sample.ps1.zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d066-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="7d066-116">範例3：設定具有自動更新之設定資料的 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="7d066-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="7d066-117">這個命令會在名為 VM22 的虛擬機器上設定副檔名，以從名為 Stg 的儲存空間帳戶和名為 WindowsPowerShellDSC 的容器下載 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="7d066-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="7d066-118">此命令會調用名為 ConfigName 的設定，並指定配置資料和引數。</span><span class="sxs-lookup"><span data-stu-id="7d066-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="7d066-119">這個命令也可自動將延伸處理常式更新為最新版本。</span><span class="sxs-lookup"><span data-stu-id="7d066-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="7d066-120">先前是使用 **Publish AzVMDscConfiguration** 上傳的 Sample.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="7d066-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="7d066-121">參數</span><span class="sxs-lookup"><span data-stu-id="7d066-121">PARAMETERS</span></span>

### <span data-ttu-id="7d066-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="7d066-122">-ArchiveBlobName</span></span>
<span data-ttu-id="7d066-123">指定先前由 Publish-AzVMDscConfiguration Cmdlet 上傳的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="7d066-124">-ArchiveContainerName</span></span>
<span data-ttu-id="7d066-125">Species 配置封存所在之 Azure 儲存體容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d066-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="7d066-127">指定包含配置封存之儲存空間帳戶的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="7d066-128">如果儲存空間帳戶和虛擬機器都在相同的資源群組中，則此參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7d066-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7d066-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="7d066-130">指定用來下載 ArchiveBlobName 的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7d066-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="7d066-132">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="7d066-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-133">-自動更新</span><span class="sxs-lookup"><span data-stu-id="7d066-133">-AutoUpdate</span></span>
<span data-ttu-id="7d066-134">指定 *version* 參數所指定的延伸處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="7d066-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="7d066-135">根據預設，延伸處理常式不會 autoupdated。</span><span class="sxs-lookup"><span data-stu-id="7d066-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="7d066-136">使用 *自動* 更新參數，即可將延伸處理常式自動更新為最新版本，以及何時可用。</span><span class="sxs-lookup"><span data-stu-id="7d066-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="7d066-137">-ConfigurationArgument</span></span>
<span data-ttu-id="7d066-138">指定包含配置函數引數的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7d066-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="7d066-139">-ConfigurationData</span></span>
<span data-ttu-id="7d066-140">指定 psd1 檔案的路徑，該檔案會指定設定的資料。</span><span class="sxs-lookup"><span data-stu-id="7d066-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7d066-141">-ConfigurationName</span></span>
<span data-ttu-id="7d066-142">指定 DSC 延伸設定的配置名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="7d066-143">-DataCollection</span></span>
<span data-ttu-id="7d066-144">指定資料收集類型。</span><span class="sxs-lookup"><span data-stu-id="7d066-144">Specifies the data collection type.</span></span>
<span data-ttu-id="7d066-145">此參數可接受的值為： [啟用] 與 [停用]。</span><span class="sxs-lookup"><span data-stu-id="7d066-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d066-146">-DefaultProfile</span></span>
<span data-ttu-id="7d066-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d066-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d066-148">-Force</span><span class="sxs-lookup"><span data-stu-id="7d066-148">-Force</span></span>
<span data-ttu-id="7d066-149">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7d066-149">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-150">-位置</span><span class="sxs-lookup"><span data-stu-id="7d066-150">-Location</span></span>
<span data-ttu-id="7d066-151">指定資源延伸的路徑。</span><span class="sxs-lookup"><span data-stu-id="7d066-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d066-152">-Name</span></span>
<span data-ttu-id="7d066-153">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="7d066-154">預設值為 Microsoft Powershell。</span><span class="sxs-lookup"><span data-stu-id="7d066-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d066-155">-ResourceGroupName</span></span>
<span data-ttu-id="7d066-156">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-156">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7d066-157">-版本</span><span class="sxs-lookup"><span data-stu-id="7d066-157">-Version</span></span>
<span data-ttu-id="7d066-158">指定 Set-AzVMDscExtension 套用設定的 DSC 副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="7d066-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d066-159">-VMName</span></span>
<span data-ttu-id="7d066-160">指定安裝 DSC 延伸處理常式的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7d066-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="7d066-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="7d066-161">-WmfVersion</span></span>
<span data-ttu-id="7d066-162">指定 WMF 版本。</span><span class="sxs-lookup"><span data-stu-id="7d066-162">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-163">-確認</span><span class="sxs-lookup"><span data-stu-id="7d066-163">-Confirm</span></span>
<span data-ttu-id="7d066-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d066-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d066-165">-WhatIf</span></span>
<span data-ttu-id="7d066-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d066-166">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7d066-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d066-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d066-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d066-168">CommonParameters</span></span>
<span data-ttu-id="7d066-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d066-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d066-170">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d066-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d066-171">輸入</span><span class="sxs-lookup"><span data-stu-id="7d066-171">INPUTS</span></span>

### <span data-ttu-id="7d066-172">所有</span><span class="sxs-lookup"><span data-stu-id="7d066-172">None</span></span>
<span data-ttu-id="7d066-173">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7d066-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d066-174">輸出</span><span class="sxs-lookup"><span data-stu-id="7d066-174">OUTPUTS</span></span>

### <span data-ttu-id="7d066-175">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7d066-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7d066-176">筆記</span><span class="sxs-lookup"><span data-stu-id="7d066-176">NOTES</span></span>

## <span data-ttu-id="7d066-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d066-177">RELATED LINKS</span></span>

[<span data-ttu-id="7d066-178">AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7d066-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="7d066-179">移除-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7d066-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="7d066-180">發佈-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d066-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


