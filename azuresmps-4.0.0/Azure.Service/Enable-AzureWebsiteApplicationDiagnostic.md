---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967128"
---
# <span data-ttu-id="0bb22-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0bb22-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="0bb22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bb22-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb22-103">啟用 Azure 網站上的應用程式診斷。</span><span class="sxs-lookup"><span data-stu-id="0bb22-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="0bb22-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bb22-104">SYNTAX</span></span>

### <span data-ttu-id="0bb22-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb22-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0bb22-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb22-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0bb22-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb22-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0bb22-108">說明</span><span class="sxs-lookup"><span data-stu-id="0bb22-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb22-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bb22-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0bb22-110">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="0bb22-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0bb22-111">在 Azure 網站上啟用應用程式診斷，並允許您在檔案系統或 Azure 儲存空間上設定記錄的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0bb22-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="0bb22-112">示例</span><span class="sxs-lookup"><span data-stu-id="0bb22-112">EXAMPLES</span></span>

### <span data-ttu-id="0bb22-113">範例1：使用檔案系統啟用診斷</span><span class="sxs-lookup"><span data-stu-id="0bb22-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="0bb22-114">這個範例可讓應用程式以詳細的層級在檔案系統上進行記錄。</span><span class="sxs-lookup"><span data-stu-id="0bb22-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="0bb22-115">範例2：使用 Azure 儲存空間啟用記錄功能</span><span class="sxs-lookup"><span data-stu-id="0bb22-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="0bb22-116">這個範例可讓應用程式記錄使用名為「我的帳戶」且記錄層級設定為資訊的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0bb22-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="0bb22-117">參數</span><span class="sxs-lookup"><span data-stu-id="0bb22-117">PARAMETERS</span></span>

### <span data-ttu-id="0bb22-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="0bb22-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-119">檔案</span><span class="sxs-lookup"><span data-stu-id="0bb22-119">-File</span></span>
<span data-ttu-id="0bb22-120">指定您要使用檔案系統來儲存記錄檔。</span><span class="sxs-lookup"><span data-stu-id="0bb22-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0bb22-121">-LogLevel</span></span>
<span data-ttu-id="0bb22-122">要儲存的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="0bb22-122">The log level to store.</span></span>
<span data-ttu-id="0bb22-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0bb22-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0bb22-124">出錯</span><span class="sxs-lookup"><span data-stu-id="0bb22-124">Error</span></span>
- <span data-ttu-id="0bb22-125">警告</span><span class="sxs-lookup"><span data-stu-id="0bb22-125">Warning</span></span>
- <span data-ttu-id="0bb22-126">錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="0bb22-126">Information</span></span>
- <span data-ttu-id="0bb22-127">冗長</span><span class="sxs-lookup"><span data-stu-id="0bb22-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bb22-128">-Name</span></span>
<span data-ttu-id="0bb22-129">指定 Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bb22-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="0bb22-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb22-130">-PassThru</span></span>
<span data-ttu-id="0bb22-131">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="0bb22-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0bb22-132">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="0bb22-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bb22-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0bb22-133">-Profile</span></span>
<span data-ttu-id="0bb22-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0bb22-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0bb22-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0bb22-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0bb22-136">-槽</span><span class="sxs-lookup"><span data-stu-id="0bb22-136">-Slot</span></span>
<span data-ttu-id="0bb22-137">指定槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bb22-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="0bb22-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0bb22-138">-StorageAccountName</span></span>
<span data-ttu-id="0bb22-139">儲存記錄所用的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0bb22-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="0bb22-140">如果沒有指定，則會使用 CurrentStorageAccount。</span><span class="sxs-lookup"><span data-stu-id="0bb22-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="0bb22-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="0bb22-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="0bb22-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb22-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb22-144">CommonParameters</span></span>
<span data-ttu-id="0bb22-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bb22-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb22-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bb22-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb22-147">輸入</span><span class="sxs-lookup"><span data-stu-id="0bb22-147">INPUTS</span></span>

## <span data-ttu-id="0bb22-148">輸出</span><span class="sxs-lookup"><span data-stu-id="0bb22-148">OUTPUTS</span></span>

## <span data-ttu-id="0bb22-149">筆記</span><span class="sxs-lookup"><span data-stu-id="0bb22-149">NOTES</span></span>

## <span data-ttu-id="0bb22-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bb22-150">RELATED LINKS</span></span>

[<span data-ttu-id="0bb22-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0bb22-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="0bb22-152">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0bb22-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0bb22-153">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0bb22-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0bb22-154">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0bb22-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="0bb22-155">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0bb22-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


