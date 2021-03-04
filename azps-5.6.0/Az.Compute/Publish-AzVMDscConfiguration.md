---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: a57ed6bb12a1357ebd8d9b4f090bd1d551f3c554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911165"
---
# <span data-ttu-id="24cf6-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="24cf6-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="24cf6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="24cf6-103">將 DSC 腳本上傳到 Azure Blob 儲存體。</span><span class="sxs-lookup"><span data-stu-id="24cf6-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="24cf6-104">語法</span><span class="sxs-lookup"><span data-stu-id="24cf6-104">SYNTAX</span></span>

### <span data-ttu-id="24cf6-105">上傳存檔 (預設) </span><span class="sxs-lookup"><span data-stu-id="24cf6-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24cf6-106">建立存檔</span><span class="sxs-lookup"><span data-stu-id="24cf6-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cf6-107">描述</span><span class="sxs-lookup"><span data-stu-id="24cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="24cf6-108">**Publish-Az VIRTUALDscConfiguration Cmdlet** 會上傳您想要的狀態組態 (DSC) 腳本至 Azure Blob 儲存空間，之後可以使用 Set-AzVMDscExtension Cmdlet 將腳本新用至 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="24cf6-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="24cf6-109">例子</span><span class="sxs-lookup"><span data-stu-id="24cf6-109">EXAMPLES</span></span>

### <span data-ttu-id="24cf6-110">範例 1：建立 .zip 套件上傳至 Azure 儲存空間</span><span class="sxs-lookup"><span data-stu-id="24cf6-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="24cf6-111">此命令會為給定腳本和任何從屬資源模組建立 .zip 套件，並將其上傳到 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="24cf6-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="24cf6-112">範例 2：建立 .zip 封裝，然後儲存到本地檔案</span><span class="sxs-lookup"><span data-stu-id="24cf6-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="24cf6-113">此命令會為指定腳本和任何從屬資源模組建立 .zip 套件，並儲存在名為 .\MyConfiguration.ps1.zip 的本地.\MyConfiguration.ps1.zip。</span><span class="sxs-lookup"><span data-stu-id="24cf6-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="24cf6-114">範例 3：新增組配置至存檔，然後將它上傳到儲存空間</span><span class="sxs-lookup"><span data-stu-id="24cf6-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="24cf6-115">此命令會將名為 Sample.ps1 的組配置新增到組配置存檔，以上傳至 Azure 儲存空間，並略過從屬資源模組。</span><span class="sxs-lookup"><span data-stu-id="24cf6-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="24cf6-116">範例 4：新增組配置和組組資料至存檔，然後將它上傳到儲存空間</span><span class="sxs-lookup"><span data-stu-id="24cf6-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="24cf6-117">此命令會將名為 Sample.ps1 的組SampleData.psd1 組組資料新增到組配置存檔，以上傳到 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="24cf6-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="24cf6-118">範例 5：新增組配置、組組資料和其他內容至存檔，然後將它上傳到儲存空間</span><span class="sxs-lookup"><span data-stu-id="24cf6-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="24cf6-119">此命令會新增名為 Sample.ps1 的組SampleData.psd、組SampleData.psd1，以及將其他內容新增到組配置存檔，以上傳到 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="24cf6-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="24cf6-120">參數</span><span class="sxs-lookup"><span data-stu-id="24cf6-120">PARAMETERS</span></span>

### <span data-ttu-id="24cf6-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="24cf6-121">-AdditionalPath</span></span>
<span data-ttu-id="24cf6-122">指定要納入組案存檔之檔案或目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="24cf6-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="24cf6-123">它會連同組配置一起下載到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="24cf6-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="24cf6-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="24cf6-125">指定指定組案資料的 .psd1 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="24cf6-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="24cf6-126">這會新增到組配置存檔，然後傳遞到組組函數。</span><span class="sxs-lookup"><span data-stu-id="24cf6-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="24cf6-127">它會由透過 Cmdlet 提供的組Set-AzVMDscExtension路徑所覆蓋</span><span class="sxs-lookup"><span data-stu-id="24cf6-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="24cf6-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="24cf6-128">-ConfigurationPath</span></span>
<span data-ttu-id="24cf6-129">指定包含一或多個組配置的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="24cf6-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="24cf6-130">檔案可以是 Windows PowerShell 腳本 (.ps1) 或 Windows PowerShell 模組 (.psm1) 檔案。</span><span class="sxs-lookup"><span data-stu-id="24cf6-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="24cf6-131">-ContainerName</span></span>
<span data-ttu-id="24cf6-132">指定已上傳組配置的 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="24cf6-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cf6-133">-DefaultProfile</span></span>
<span data-ttu-id="24cf6-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24cf6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cf6-135">-強制</span><span class="sxs-lookup"><span data-stu-id="24cf6-135">-Force</span></span>
<span data-ttu-id="24cf6-136">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="24cf6-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24cf6-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="24cf6-137">-OutputArchivePath</span></span>
<span data-ttu-id="24cf6-138">指定要撰寫組案存檔的 .zip 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="24cf6-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="24cf6-139">使用這個參數時，設定腳本不會上傳到 Azure Blob 儲存體。</span><span class="sxs-lookup"><span data-stu-id="24cf6-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cf6-140">-ResourceGroupName</span></span>
<span data-ttu-id="24cf6-141">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="24cf6-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="24cf6-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="24cf6-143">表示此 Cmdlet 排除組配置存檔中的 DSC 資源相依性。</span><span class="sxs-lookup"><span data-stu-id="24cf6-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="24cf6-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24cf6-144">-StorageAccountName</span></span>
<span data-ttu-id="24cf6-145">指定用來將設定腳本上傳到 ContainerName 參數所指定的 *容器的 Azure* 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="24cf6-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="24cf6-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="24cf6-147">指定儲存終點的尾碼。</span><span class="sxs-lookup"><span data-stu-id="24cf6-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24cf6-148">-確認</span><span class="sxs-lookup"><span data-stu-id="24cf6-148">-Confirm</span></span>
<span data-ttu-id="24cf6-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24cf6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cf6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cf6-150">-WhatIf</span></span>
<span data-ttu-id="24cf6-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24cf6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cf6-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24cf6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cf6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cf6-153">CommonParameters</span></span>
<span data-ttu-id="24cf6-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24cf6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cf6-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24cf6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cf6-156">輸入</span><span class="sxs-lookup"><span data-stu-id="24cf6-156">INPUTS</span></span>

### <span data-ttu-id="24cf6-157">System.String</span><span class="sxs-lookup"><span data-stu-id="24cf6-157">System.String</span></span>

### <span data-ttu-id="24cf6-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="24cf6-158">System.String[]</span></span>

## <span data-ttu-id="24cf6-159">輸出</span><span class="sxs-lookup"><span data-stu-id="24cf6-159">OUTPUTS</span></span>

### <span data-ttu-id="24cf6-160">System.String</span><span class="sxs-lookup"><span data-stu-id="24cf6-160">System.String</span></span>

## <span data-ttu-id="24cf6-161">筆記</span><span class="sxs-lookup"><span data-stu-id="24cf6-161">NOTES</span></span>

## <span data-ttu-id="24cf6-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="24cf6-162">RELATED LINKS</span></span>

[<span data-ttu-id="24cf6-163">Get-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="24cf6-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="24cf6-164">Remove-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="24cf6-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="24cf6-165">Set-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="24cf6-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


