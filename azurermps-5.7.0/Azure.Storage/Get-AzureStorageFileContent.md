---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449468"
---
# <span data-ttu-id="3dbcd-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3dbcd-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="3dbcd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbcd-103">下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dbcd-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dbcd-104">SYNTAX</span></span>

### <span data-ttu-id="3dbcd-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="3dbcd-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dbcd-106">共用</span><span class="sxs-lookup"><span data-stu-id="3dbcd-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dbcd-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="3dbcd-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dbcd-108">檔案</span><span class="sxs-lookup"><span data-stu-id="3dbcd-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dbcd-109">說明</span><span class="sxs-lookup"><span data-stu-id="3dbcd-109">DESCRIPTION</span></span>
<span data-ttu-id="3dbcd-110">**AzureStorageFileContent** Cmdlet 會下載檔案的內容，然後將檔案儲存到您指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="3dbcd-111">這個 Cmdlet 不會傳回檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="3dbcd-112">示例</span><span class="sxs-lookup"><span data-stu-id="3dbcd-112">EXAMPLES</span></span>

### <span data-ttu-id="3dbcd-113">範例1：從資料夾下載檔案</span><span class="sxs-lookup"><span data-stu-id="3dbcd-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="3dbcd-114">這個命令會將資料夾 ContosoWorkingFolder 中名為 CurrentDataFile 的檔案從 [檔案共用] ContosoShare06 下載到 [目前] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="3dbcd-115">範例2：下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="3dbcd-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="3dbcd-116">這個範例會下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="3dbcd-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="3dbcd-117">參數</span><span class="sxs-lookup"><span data-stu-id="3dbcd-117">PARAMETERS</span></span>

### <span data-ttu-id="3dbcd-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="3dbcd-118">-CheckMd5</span></span>
<span data-ttu-id="3dbcd-119">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-120">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-121">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-122">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3dbcd-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3dbcd-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3dbcd-124">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-125">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-126">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-127">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3dbcd-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3dbcd-129">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-130">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-131">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-132">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-133">-內容</span><span class="sxs-lookup"><span data-stu-id="3dbcd-133">-Context</span></span>
<span data-ttu-id="3dbcd-134">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-135">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-136">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-137">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-138">-目的地</span><span class="sxs-lookup"><span data-stu-id="3dbcd-138">-Destination</span></span>
<span data-ttu-id="3dbcd-139">指定目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-139">Specifies the destination path.</span></span>
<span data-ttu-id="3dbcd-140">這個 Cmdlet 會將檔案內容下載到此參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="3dbcd-141">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-142">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-143">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-144">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-145">-Directory</span><span class="sxs-lookup"><span data-stu-id="3dbcd-145">-Directory</span></span>
<span data-ttu-id="3dbcd-146">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3dbcd-147">這個 Cmdlet 會取得此參數指定之資料夾中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="3dbcd-148">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3dbcd-149">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-150">檔案</span><span class="sxs-lookup"><span data-stu-id="3dbcd-150">-File</span></span>
<span data-ttu-id="3dbcd-151">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="3dbcd-152">這個 Cmdlet 會取得此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="3dbcd-153">若要取得 **CloudFile** 物件，請使用 Get-AzureStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-154">-Force</span><span class="sxs-lookup"><span data-stu-id="3dbcd-154">-Force</span></span>
<span data-ttu-id="3dbcd-155">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-156">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-157">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-158">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3dbcd-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dbcd-159">-PassThru</span></span>
<span data-ttu-id="3dbcd-160">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-161">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-162">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-163">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3dbcd-164">-Path</span><span class="sxs-lookup"><span data-stu-id="3dbcd-164">-Path</span></span>
<span data-ttu-id="3dbcd-165">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-165">Specifies the path of a file.</span></span>
<span data-ttu-id="3dbcd-166">這個 Cmdlet 會取得此參數所指定之檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="3dbcd-167">如果檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3dbcd-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3dbcd-169">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3dbcd-170">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3dbcd-171">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3dbcd-172">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-173">-共用</span><span class="sxs-lookup"><span data-stu-id="3dbcd-173">-Share</span></span>
<span data-ttu-id="3dbcd-174">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3dbcd-175">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="3dbcd-176">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3dbcd-177">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-177">This object contains the storage context.</span></span>
<span data-ttu-id="3dbcd-178">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-179">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="3dbcd-179">-ShareName</span></span>
<span data-ttu-id="3dbcd-180">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="3dbcd-181">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbcd-182">-確認</span><span class="sxs-lookup"><span data-stu-id="3dbcd-182">-Confirm</span></span>
<span data-ttu-id="3dbcd-183">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dbcd-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dbcd-184">-WhatIf</span></span>
<span data-ttu-id="3dbcd-185">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dbcd-186">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dbcd-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbcd-187">CommonParameters</span></span>
<span data-ttu-id="3dbcd-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbcd-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dbcd-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbcd-190">輸入</span><span class="sxs-lookup"><span data-stu-id="3dbcd-190">INPUTS</span></span>

### <span data-ttu-id="3dbcd-191">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3dbcd-191">IStorageContext</span></span>

<span data-ttu-id="3dbcd-192">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dbcd-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3dbcd-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3dbcd-193">CloudFileDirectory</span></span>

<span data-ttu-id="3dbcd-194">形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dbcd-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="3dbcd-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="3dbcd-195">CloudFile</span></span>

<span data-ttu-id="3dbcd-196">形參 "File" 接受管線中 "CloudFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dbcd-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="3dbcd-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3dbcd-197">CloudFileShare</span></span>

<span data-ttu-id="3dbcd-198">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dbcd-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="3dbcd-199">輸出</span><span class="sxs-lookup"><span data-stu-id="3dbcd-199">OUTPUTS</span></span>

## <span data-ttu-id="3dbcd-200">筆記</span><span class="sxs-lookup"><span data-stu-id="3dbcd-200">NOTES</span></span>

## <span data-ttu-id="3dbcd-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dbcd-201">RELATED LINKS</span></span>

[<span data-ttu-id="3dbcd-202">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3dbcd-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3dbcd-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3dbcd-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


