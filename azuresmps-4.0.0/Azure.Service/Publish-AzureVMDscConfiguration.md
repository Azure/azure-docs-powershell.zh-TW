---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967328"
---
# <span data-ttu-id="11ef5-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11ef5-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="11ef5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="11ef5-103">將所需的狀態設定腳本發佈至 Azure blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="11ef5-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="11ef5-104">句法</span><span class="sxs-lookup"><span data-stu-id="11ef5-104">SYNTAX</span></span>

### <span data-ttu-id="11ef5-105">UploadArchive (預設) </span><span class="sxs-lookup"><span data-stu-id="11ef5-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11ef5-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="11ef5-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ef5-107">說明</span><span class="sxs-lookup"><span data-stu-id="11ef5-107">DESCRIPTION</span></span>
<span data-ttu-id="11ef5-108">**AzureVMDscConfiguration** Cmdlet 會將所需的狀態設定腳本發佈至 azure blob 儲存空間，稍後可使用 **AzureVMDscExtension** Cmdlet 將其套用至 azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11ef5-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="11ef5-109">示例</span><span class="sxs-lookup"><span data-stu-id="11ef5-109">EXAMPLES</span></span>

### <span data-ttu-id="11ef5-110">範例1：將 state configuration 腳本發佈到 blob 儲存體</span><span class="sxs-lookup"><span data-stu-id="11ef5-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="11ef5-111">這個命令會針對指定的腳本及任何相依資源模組建立 .zip 套件，並將其上傳到 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="11ef5-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="11ef5-112">範例2：將 state configuration 腳本發佈到本機檔案</span><span class="sxs-lookup"><span data-stu-id="11ef5-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="11ef5-113">這個命令會針對指定的腳本及任何相依資源模組建立 .zip 套件，並將其儲存在本機檔案 .\MyConfiguration.ps1.zip 中。</span><span class="sxs-lookup"><span data-stu-id="11ef5-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="11ef5-114">參數</span><span class="sxs-lookup"><span data-stu-id="11ef5-114">PARAMETERS</span></span>

### <span data-ttu-id="11ef5-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="11ef5-115">-AdditionalPath</span></span>
<span data-ttu-id="11ef5-116">指定其他路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="11ef5-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="11ef5-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="11ef5-118">指定此 Cmdlet 寫入配置封存的本機 .zip 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="11ef5-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="11ef5-119">如果您使用這個參數，就不會將配置腳本上傳到 Azure blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="11ef5-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="11ef5-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="11ef5-121">指定配置資料路徑。</span><span class="sxs-lookup"><span data-stu-id="11ef5-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="11ef5-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="11ef5-122">-ConfigurationPath</span></span>
<span data-ttu-id="11ef5-123">指定包含一或多個設定的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="11ef5-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="11ef5-124">此檔案可以是 Windows PowerShell 腳本 ( ps1 檔案) 、module ( psm1 檔案) ，或是包含一組 Windows PowerShell 模組的封存 ( .zip 檔案) ，且每個模組都在不同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="11ef5-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-125">-容器</span><span class="sxs-lookup"><span data-stu-id="11ef5-125">-ContainerName</span></span>
<span data-ttu-id="11ef5-126">指定要上傳配置的 Azure 存儲容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="11ef5-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="11ef5-127">-Force</span></span>
<span data-ttu-id="11ef5-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="11ef5-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11ef5-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11ef5-129">-InformationAction</span></span>
<span data-ttu-id="11ef5-130">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="11ef5-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11ef5-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11ef5-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11ef5-132">持續</span><span class="sxs-lookup"><span data-stu-id="11ef5-132">Continue</span></span>
- <span data-ttu-id="11ef5-133">理會</span><span class="sxs-lookup"><span data-stu-id="11ef5-133">Ignore</span></span>
- <span data-ttu-id="11ef5-134">看</span><span class="sxs-lookup"><span data-stu-id="11ef5-134">Inquire</span></span>
- <span data-ttu-id="11ef5-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11ef5-135">SilentlyContinue</span></span>
- <span data-ttu-id="11ef5-136">停止</span><span class="sxs-lookup"><span data-stu-id="11ef5-136">Stop</span></span>
- <span data-ttu-id="11ef5-137">封存</span><span class="sxs-lookup"><span data-stu-id="11ef5-137">Suspend</span></span>

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

### <span data-ttu-id="11ef5-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11ef5-138">-InformationVariable</span></span>
<span data-ttu-id="11ef5-139">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="11ef5-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="11ef5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11ef5-140">-PassThru</span></span>
<span data-ttu-id="11ef5-141">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="11ef5-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11ef5-142">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="11ef5-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11ef5-143">-設定檔</span><span class="sxs-lookup"><span data-stu-id="11ef5-143">-Profile</span></span>
<span data-ttu-id="11ef5-144">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="11ef5-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11ef5-145">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="11ef5-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11ef5-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="11ef5-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="11ef5-147">表示此 Cmdlet 會跳過相依性偵測。</span><span class="sxs-lookup"><span data-stu-id="11ef5-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="11ef5-148">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="11ef5-148">-StorageContext</span></span>
<span data-ttu-id="11ef5-149">指定 Azure 儲存區內容，提供用來將設定腳本上傳到 *容器參數所* 指定之容器的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="11ef5-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="11ef5-150">此內容提供對容器的寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="11ef5-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="11ef5-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="11ef5-152">指定存儲端點的尾碼，例如 core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="11ef5-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ef5-153">-確認</span><span class="sxs-lookup"><span data-stu-id="11ef5-153">-Confirm</span></span>
<span data-ttu-id="11ef5-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11ef5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ef5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ef5-155">-WhatIf</span></span>
<span data-ttu-id="11ef5-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11ef5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ef5-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11ef5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ef5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ef5-158">CommonParameters</span></span>
<span data-ttu-id="11ef5-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11ef5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ef5-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11ef5-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ef5-161">輸入</span><span class="sxs-lookup"><span data-stu-id="11ef5-161">INPUTS</span></span>

## <span data-ttu-id="11ef5-162">輸出</span><span class="sxs-lookup"><span data-stu-id="11ef5-162">OUTPUTS</span></span>

## <span data-ttu-id="11ef5-163">筆記</span><span class="sxs-lookup"><span data-stu-id="11ef5-163">NOTES</span></span>

## <span data-ttu-id="11ef5-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="11ef5-164">RELATED LINKS</span></span>

[<span data-ttu-id="11ef5-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="11ef5-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


