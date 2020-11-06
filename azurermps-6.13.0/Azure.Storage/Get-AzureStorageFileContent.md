---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448513"
---
# <span data-ttu-id="dad34-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dad34-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="dad34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dad34-102">SYNOPSIS</span></span>
<span data-ttu-id="dad34-103">下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad34-104">句法</span><span class="sxs-lookup"><span data-stu-id="dad34-104">SYNTAX</span></span>

### <span data-ttu-id="dad34-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="dad34-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad34-106">共用</span><span class="sxs-lookup"><span data-stu-id="dad34-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad34-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="dad34-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dad34-108">檔案</span><span class="sxs-lookup"><span data-stu-id="dad34-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad34-109">說明</span><span class="sxs-lookup"><span data-stu-id="dad34-109">DESCRIPTION</span></span>
<span data-ttu-id="dad34-110">**AzureStorageFileContent** Cmdlet 會下載檔案的內容，然後將檔案儲存到您指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="dad34-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="dad34-111">這個 Cmdlet 不會傳回檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="dad34-112">示例</span><span class="sxs-lookup"><span data-stu-id="dad34-112">EXAMPLES</span></span>

### <span data-ttu-id="dad34-113">範例1：從資料夾下載檔案</span><span class="sxs-lookup"><span data-stu-id="dad34-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="dad34-114">這個命令會將資料夾 ContosoWorkingFolder 中名為 CurrentDataFile 的檔案從 [檔案共用] ContosoShare06 下載到 [目前] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="dad34-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="dad34-115">範例2：下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="dad34-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="dad34-116">這個範例會下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="dad34-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="dad34-117">參數</span><span class="sxs-lookup"><span data-stu-id="dad34-117">PARAMETERS</span></span>

### <span data-ttu-id="dad34-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="dad34-118">-CheckMd5</span></span>
<span data-ttu-id="dad34-119">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-120">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-121">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-122">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="dad34-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dad34-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dad34-124">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-125">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-126">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-127">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dad34-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dad34-129">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-130">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-131">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-132">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-133">-內容</span><span class="sxs-lookup"><span data-stu-id="dad34-133">-Context</span></span>
<span data-ttu-id="dad34-134">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-135">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-136">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-137">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad34-138">-DefaultProfile</span></span>
<span data-ttu-id="dad34-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dad34-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad34-140">-目的地</span><span class="sxs-lookup"><span data-stu-id="dad34-140">-Destination</span></span>
<span data-ttu-id="dad34-141">指定目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="dad34-141">Specifies the destination path.</span></span>
<span data-ttu-id="dad34-142">這個 Cmdlet 會將檔案內容下載到此參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="dad34-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="dad34-143">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-144">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-145">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-146">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="dad34-147">-Directory</span></span>
<span data-ttu-id="dad34-148">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="dad34-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="dad34-149">這個 Cmdlet 會取得此參數指定之資料夾中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="dad34-150">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dad34-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="dad34-151">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="dad34-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-152">檔案</span><span class="sxs-lookup"><span data-stu-id="dad34-152">-File</span></span>
<span data-ttu-id="dad34-153">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="dad34-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="dad34-154">這個 Cmdlet 會取得此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="dad34-155">若要取得 **CloudFile** 物件，請使用 Get-AzureStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dad34-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-156">-Force</span><span class="sxs-lookup"><span data-stu-id="dad34-156">-Force</span></span>
<span data-ttu-id="dad34-157">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-158">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-159">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-160">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="dad34-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dad34-161">-PassThru</span></span>
<span data-ttu-id="dad34-162">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-163">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-164">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-165">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="dad34-166">-Path</span><span class="sxs-lookup"><span data-stu-id="dad34-166">-Path</span></span>
<span data-ttu-id="dad34-167">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="dad34-167">Specifies the path of a file.</span></span>
<span data-ttu-id="dad34-168">這個 Cmdlet 會取得此參數所指定之檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="dad34-169">如果檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dad34-169">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dad34-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dad34-171">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="dad34-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="dad34-172">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="dad34-173">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="dad34-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="dad34-174">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="dad34-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-175">-共用</span><span class="sxs-lookup"><span data-stu-id="dad34-175">-Share</span></span>
<span data-ttu-id="dad34-176">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="dad34-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dad34-177">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="dad34-178">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dad34-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="dad34-179">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-179">This object contains the storage context.</span></span>
<span data-ttu-id="dad34-180">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="dad34-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-181">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="dad34-181">-ShareName</span></span>
<span data-ttu-id="dad34-182">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="dad34-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="dad34-183">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="dad34-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad34-184">-確認</span><span class="sxs-lookup"><span data-stu-id="dad34-184">-Confirm</span></span>
<span data-ttu-id="dad34-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dad34-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad34-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad34-186">-WhatIf</span></span>
<span data-ttu-id="dad34-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dad34-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad34-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dad34-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad34-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad34-189">CommonParameters</span></span>
<span data-ttu-id="dad34-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dad34-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad34-191">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dad34-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad34-192">輸入</span><span class="sxs-lookup"><span data-stu-id="dad34-192">INPUTS</span></span>

### <span data-ttu-id="dad34-193">[WindowsAzure] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="dad34-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="dad34-194">參數：共用 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dad34-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="dad34-195">[WindowsAzure] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="dad34-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="dad34-196">參數：目錄 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dad34-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="dad34-197">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="dad34-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="dad34-198">參數：檔案 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dad34-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="dad34-199">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="dad34-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dad34-200">輸出</span><span class="sxs-lookup"><span data-stu-id="dad34-200">OUTPUTS</span></span>

### <span data-ttu-id="dad34-201">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="dad34-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="dad34-202">筆記</span><span class="sxs-lookup"><span data-stu-id="dad34-202">NOTES</span></span>

## <span data-ttu-id="dad34-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="dad34-203">RELATED LINKS</span></span>

[<span data-ttu-id="dad34-204">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="dad34-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="dad34-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dad34-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


