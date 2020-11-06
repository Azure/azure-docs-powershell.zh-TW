---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 562f9e4fac97421c53e07c4789d16b23d90a5ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614563"
---
# <span data-ttu-id="16dfe-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="16dfe-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="16dfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="16dfe-103">針對 Azure 儲存區 blob 產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="16dfe-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="16dfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="16dfe-104">SYNTAX</span></span>

### <span data-ttu-id="16dfe-105">BlobNameWithPermission (預設) </span><span class="sxs-lookup"><span data-stu-id="16dfe-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16dfe-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16dfe-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="16dfe-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16dfe-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="16dfe-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16dfe-109">說明</span><span class="sxs-lookup"><span data-stu-id="16dfe-109">DESCRIPTION</span></span>
<span data-ttu-id="16dfe-110">**AzStorageBlobSASToken** Cmdlet 會針對 Azure 儲存區 blob 產生 (SAS) 權杖的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="16dfe-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="16dfe-111">示例</span><span class="sxs-lookup"><span data-stu-id="16dfe-111">EXAMPLES</span></span>

### <span data-ttu-id="16dfe-112">範例1：使用完整 blob 許可權產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="16dfe-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="16dfe-113">這個範例會產生含完整 blob 許可權的 blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="16dfe-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="16dfe-114">範例2：使用生命時間產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="16dfe-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="16dfe-115">這個範例會產生含生命時間的 blob SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="16dfe-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="16dfe-116">參數</span><span class="sxs-lookup"><span data-stu-id="16dfe-116">PARAMETERS</span></span>

### <span data-ttu-id="16dfe-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="16dfe-117">-Blob</span></span>
<span data-ttu-id="16dfe-118">指定儲存區 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="16dfe-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="16dfe-119">-CloudBlob</span></span>
<span data-ttu-id="16dfe-120">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="16dfe-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="16dfe-121">若要取得 **CloudBlob** 物件，請使用 [AzStorageBlob](./Get-AzStorageBlob.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16dfe-121">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-122">-容器</span><span class="sxs-lookup"><span data-stu-id="16dfe-122">-Container</span></span>
<span data-ttu-id="16dfe-123">指定儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="16dfe-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-124">-內容</span><span class="sxs-lookup"><span data-stu-id="16dfe-124">-Context</span></span>
<span data-ttu-id="16dfe-125">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="16dfe-125">Specifies the storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dfe-126">-DefaultProfile</span></span>
<span data-ttu-id="16dfe-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16dfe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16dfe-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="16dfe-128">-ExpiryTime</span></span>
<span data-ttu-id="16dfe-129">指定共用存取簽章的到期時間。</span><span class="sxs-lookup"><span data-stu-id="16dfe-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="16dfe-130">-FullUri</span></span>
<span data-ttu-id="16dfe-131">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="16dfe-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="16dfe-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="16dfe-132">-IPAddressOrRange</span></span>
<span data-ttu-id="16dfe-133">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="16dfe-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="16dfe-134">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="16dfe-134">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-135">-許可權</span><span class="sxs-lookup"><span data-stu-id="16dfe-135">-Permission</span></span>
<span data-ttu-id="16dfe-136">指定儲存 blob 的許可權。</span><span class="sxs-lookup"><span data-stu-id="16dfe-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="16dfe-137">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="16dfe-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-138">-原則</span><span class="sxs-lookup"><span data-stu-id="16dfe-138">-Policy</span></span>
<span data-ttu-id="16dfe-139">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="16dfe-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-140">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="16dfe-140">-Protocol</span></span>
<span data-ttu-id="16dfe-141">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="16dfe-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="16dfe-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="16dfe-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="16dfe-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="16dfe-143">HttpsOnly</span></span>
* <span data-ttu-id="16dfe-144">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="16dfe-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="16dfe-145">-StartTime</span></span>
<span data-ttu-id="16dfe-146">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="16dfe-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dfe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dfe-147">CommonParameters</span></span>
<span data-ttu-id="16dfe-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16dfe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dfe-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16dfe-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dfe-150">輸入</span><span class="sxs-lookup"><span data-stu-id="16dfe-150">INPUTS</span></span>

### <span data-ttu-id="16dfe-151">[WindowsAzure] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="16dfe-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="16dfe-152">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="16dfe-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16dfe-153">輸出</span><span class="sxs-lookup"><span data-stu-id="16dfe-153">OUTPUTS</span></span>

### <span data-ttu-id="16dfe-154">System.object</span><span class="sxs-lookup"><span data-stu-id="16dfe-154">System.String</span></span>

## <span data-ttu-id="16dfe-155">筆記</span><span class="sxs-lookup"><span data-stu-id="16dfe-155">NOTES</span></span>

## <span data-ttu-id="16dfe-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="16dfe-156">RELATED LINKS</span></span>

[<span data-ttu-id="16dfe-157">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="16dfe-157">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="16dfe-158">新-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="16dfe-158">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
