---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958548"
---
# <span data-ttu-id="3d8be-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3d8be-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="3d8be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d8be-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8be-103">針對 Azure 儲存空間容器產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="3d8be-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="3d8be-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d8be-104">SYNTAX</span></span>

### <span data-ttu-id="3d8be-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3d8be-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d8be-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3d8be-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d8be-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d8be-107">DESCRIPTION</span></span>
<span data-ttu-id="3d8be-108">**新的-AzStorageContainerSASToken** Cmdlet 會針對 Azure 儲存體容器 (SAS) 權杖產生共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="3d8be-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="3d8be-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d8be-109">EXAMPLES</span></span>

### <span data-ttu-id="3d8be-110">範例1：使用完整容器許可權產生容器 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="3d8be-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="3d8be-111">這個範例會產生含完整容器許可權的容器 SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="3d8be-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="3d8be-112">範例2：依管道產生多個容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="3d8be-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="3d8be-113">這個範例會使用管線產生多個容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="3d8be-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="3d8be-114">範例3：使用共用存取原則產生容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="3d8be-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="3d8be-115">這個範例會產生含共用存取原則的容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="3d8be-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="3d8be-116">範例3：根據 OAuth 驗證產生含儲存內容的使用者身分識別容器 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="3d8be-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="3d8be-117">這個範例會根據 OAuth 驗證產生一個含儲存內容的使用者身分識別容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="3d8be-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="3d8be-118">參數</span><span class="sxs-lookup"><span data-stu-id="3d8be-118">PARAMETERS</span></span>

### <span data-ttu-id="3d8be-119">-內容</span><span class="sxs-lookup"><span data-stu-id="3d8be-119">-Context</span></span>
<span data-ttu-id="3d8be-120">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3d8be-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3d8be-121">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3d8be-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="3d8be-122">當儲存內容是以 OAuth 驗證為基礎時，會產生使用者身分識別容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="3d8be-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="3d8be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8be-123">-DefaultProfile</span></span>
<span data-ttu-id="3d8be-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d8be-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8be-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d8be-125">-ExpiryTime</span></span>
<span data-ttu-id="3d8be-126">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="3d8be-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="3d8be-127">如果使用者設定開始時間，但不是到期時間，到期時間會設定為開始時間加上1小時。</span><span class="sxs-lookup"><span data-stu-id="3d8be-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="3d8be-128">如果未指定 [開始時間] 和 [到期時間]，則會將到期時間設定為目前的時間加上一個小時。</span><span class="sxs-lookup"><span data-stu-id="3d8be-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="3d8be-129">當儲存內容是以 OAuth 驗證為基礎時，到期時間必須是與目前時間的7天，且不得早于目前時間。</span><span class="sxs-lookup"><span data-stu-id="3d8be-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="3d8be-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3d8be-130">-FullUri</span></span>
<span data-ttu-id="3d8be-131">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="3d8be-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3d8be-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3d8be-132">-IPAddressOrRange</span></span>
<span data-ttu-id="3d8be-133">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="3d8be-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3d8be-134">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="3d8be-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="3d8be-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d8be-135">-Name</span></span>
<span data-ttu-id="3d8be-136">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3d8be-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-137">-許可權</span><span class="sxs-lookup"><span data-stu-id="3d8be-137">-Permission</span></span>
<span data-ttu-id="3d8be-138">指定儲存容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="3d8be-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="3d8be-139">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="3d8be-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-140">-原則</span><span class="sxs-lookup"><span data-stu-id="3d8be-140">-Policy</span></span>
<span data-ttu-id="3d8be-141">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="3d8be-141">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-142">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3d8be-142">-Protocol</span></span>
<span data-ttu-id="3d8be-143">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3d8be-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3d8be-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3d8be-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3d8be-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3d8be-145">HttpsOnly</span></span>
* <span data-ttu-id="3d8be-146">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="3d8be-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3d8be-147">-StartTime</span></span>
<span data-ttu-id="3d8be-148">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="3d8be-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3d8be-149">-確認</span><span class="sxs-lookup"><span data-stu-id="3d8be-149">-Confirm</span></span>
<span data-ttu-id="3d8be-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d8be-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8be-151">-WhatIf</span></span>
<span data-ttu-id="3d8be-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d8be-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d8be-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d8be-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8be-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8be-154">CommonParameters</span></span>
<span data-ttu-id="3d8be-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d8be-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8be-156">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d8be-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8be-157">輸入</span><span class="sxs-lookup"><span data-stu-id="3d8be-157">INPUTS</span></span>

### <span data-ttu-id="3d8be-158">System.object</span><span class="sxs-lookup"><span data-stu-id="3d8be-158">System.String</span></span>

### <span data-ttu-id="3d8be-159">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3d8be-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3d8be-160">輸出</span><span class="sxs-lookup"><span data-stu-id="3d8be-160">OUTPUTS</span></span>

### <span data-ttu-id="3d8be-161">System.object</span><span class="sxs-lookup"><span data-stu-id="3d8be-161">System.String</span></span>

## <span data-ttu-id="3d8be-162">筆記</span><span class="sxs-lookup"><span data-stu-id="3d8be-162">NOTES</span></span>

## <span data-ttu-id="3d8be-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d8be-163">RELATED LINKS</span></span>

[<span data-ttu-id="3d8be-164">新-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3d8be-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)