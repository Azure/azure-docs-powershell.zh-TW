---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795143"
---
# <span data-ttu-id="26e38-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26e38-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="26e38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26e38-102">SYNOPSIS</span></span>
<span data-ttu-id="26e38-103">下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="26e38-104">句法</span><span class="sxs-lookup"><span data-stu-id="26e38-104">SYNTAX</span></span>

### <span data-ttu-id="26e38-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="26e38-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e38-106">共用</span><span class="sxs-lookup"><span data-stu-id="26e38-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e38-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="26e38-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e38-108">檔案</span><span class="sxs-lookup"><span data-stu-id="26e38-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26e38-109">說明</span><span class="sxs-lookup"><span data-stu-id="26e38-109">DESCRIPTION</span></span>
<span data-ttu-id="26e38-110">**AzStorageFileContent** Cmdlet 會下載檔案的內容，然後將檔案儲存到您指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="26e38-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="26e38-111">這個 Cmdlet 不會傳回檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="26e38-112">示例</span><span class="sxs-lookup"><span data-stu-id="26e38-112">EXAMPLES</span></span>

### <span data-ttu-id="26e38-113">範例1：從資料夾下載檔案</span><span class="sxs-lookup"><span data-stu-id="26e38-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="26e38-114">這個命令會將資料夾 ContosoWorkingFolder 中名為 CurrentDataFile 的檔案從 [檔案共用] ContosoShare06 下載到 [目前] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="26e38-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="26e38-115">範例2：下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="26e38-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="26e38-116">這個範例會下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="26e38-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="26e38-117">參數</span><span class="sxs-lookup"><span data-stu-id="26e38-117">PARAMETERS</span></span>

### <span data-ttu-id="26e38-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="26e38-118">-CheckMd5</span></span>
<span data-ttu-id="26e38-119">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-120">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-121">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-122">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26e38-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="26e38-124">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-125">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-126">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-127">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="26e38-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="26e38-129">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-130">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-131">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-132">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-133">-內容</span><span class="sxs-lookup"><span data-stu-id="26e38-133">-Context</span></span>
<span data-ttu-id="26e38-134">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-135">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-136">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-137">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e38-138">-DefaultProfile</span></span>
<span data-ttu-id="26e38-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26e38-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e38-140">-目的地</span><span class="sxs-lookup"><span data-stu-id="26e38-140">-Destination</span></span>
<span data-ttu-id="26e38-141">指定目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="26e38-141">Specifies the destination path.</span></span>
<span data-ttu-id="26e38-142">這個 Cmdlet 會將檔案內容下載到此參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="26e38-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="26e38-143">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-144">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-145">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-146">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="26e38-147">-Directory</span></span>
<span data-ttu-id="26e38-148">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="26e38-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="26e38-149">這個 Cmdlet 會取得此參數指定之資料夾中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="26e38-150">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e38-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="26e38-151">您也可以使用 Get-AzStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="26e38-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="26e38-152">檔案</span><span class="sxs-lookup"><span data-stu-id="26e38-152">-File</span></span>
<span data-ttu-id="26e38-153">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="26e38-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="26e38-154">這個 Cmdlet 會取得此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="26e38-155">若要取得 **CloudFile** 物件，請使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e38-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="26e38-156">-Force</span><span class="sxs-lookup"><span data-stu-id="26e38-156">-Force</span></span>
<span data-ttu-id="26e38-157">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-158">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-159">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-160">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e38-161">-PassThru</span></span>
<span data-ttu-id="26e38-162">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-163">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-164">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-165">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-166">-Path</span><span class="sxs-lookup"><span data-stu-id="26e38-166">-Path</span></span>
<span data-ttu-id="26e38-167">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="26e38-167">Specifies the path of a file.</span></span>
<span data-ttu-id="26e38-168">這個 Cmdlet 會取得此參數所指定之檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="26e38-169">如果檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="26e38-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="26e38-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26e38-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="26e38-171">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="26e38-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="26e38-172">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="26e38-173">如果您指定現有檔案的路徑，而您沒有指定 *Force* ，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="26e38-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="26e38-174">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="26e38-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="26e38-175">-共用</span><span class="sxs-lookup"><span data-stu-id="26e38-175">-Share</span></span>
<span data-ttu-id="26e38-176">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="26e38-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="26e38-177">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="26e38-178">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e38-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="26e38-179">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-179">This object contains the storage context.</span></span>
<span data-ttu-id="26e38-180">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="26e38-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="26e38-181">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="26e38-181">-ShareName</span></span>
<span data-ttu-id="26e38-182">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="26e38-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="26e38-183">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="26e38-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="26e38-184">-確認</span><span class="sxs-lookup"><span data-stu-id="26e38-184">-Confirm</span></span>
<span data-ttu-id="26e38-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26e38-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e38-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e38-186">-WhatIf</span></span>
<span data-ttu-id="26e38-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26e38-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e38-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e38-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e38-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e38-189">CommonParameters</span></span>
<span data-ttu-id="26e38-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26e38-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e38-191">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26e38-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e38-192">輸入</span><span class="sxs-lookup"><span data-stu-id="26e38-192">INPUTS</span></span>

### <span data-ttu-id="26e38-193">[WindowsAz] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="26e38-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="26e38-194">參數：共用 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="26e38-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="26e38-195">[WindowsAz] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="26e38-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="26e38-196">參數：目錄 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="26e38-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="26e38-197">[WindowsAz] CloudFile</span><span class="sxs-lookup"><span data-stu-id="26e38-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="26e38-198">參數：檔案 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="26e38-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="26e38-199">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="26e38-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="26e38-200">輸出</span><span class="sxs-lookup"><span data-stu-id="26e38-200">OUTPUTS</span></span>

### <span data-ttu-id="26e38-201">[WindowsAz] CloudFile</span><span class="sxs-lookup"><span data-stu-id="26e38-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="26e38-202">筆記</span><span class="sxs-lookup"><span data-stu-id="26e38-202">NOTES</span></span>

## <span data-ttu-id="26e38-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="26e38-203">RELATED LINKS</span></span>

[<span data-ttu-id="26e38-204">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="26e38-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="26e38-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26e38-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


