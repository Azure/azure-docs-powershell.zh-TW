---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 09cbfb953118e5d6e29f2af25cd4653939135f07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915081"
---
# <span data-ttu-id="5388b-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5388b-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="5388b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5388b-102">SYNOPSIS</span></span>
<span data-ttu-id="5388b-103">產生 Azure 儲存容器的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="5388b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5388b-104">SYNTAX</span></span>

### <span data-ttu-id="5388b-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5388b-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5388b-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5388b-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5388b-107">描述</span><span class="sxs-lookup"><span data-stu-id="5388b-107">DESCRIPTION</span></span>
<span data-ttu-id="5388b-108">**New-AzStorageContainerSASToken** Cmdlet 會為 Azure 儲存容器產生共用存取簽章 (SAS) 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="5388b-109">例子</span><span class="sxs-lookup"><span data-stu-id="5388b-109">EXAMPLES</span></span>

### <span data-ttu-id="5388b-110">範例 1：產生具有完整容器許可權的容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="5388b-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="5388b-111">此範例會產生具有完整容器許可權的容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="5388b-112">範例 2：根據管線產生多個容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="5388b-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="5388b-113">此範例會使用管線產生多個容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="5388b-114">範例 3：使用共用存取策略產生容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="5388b-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="5388b-115">此範例會使用共用存取策略產生容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="5388b-116">範例 3：根據 OAuth 驗證，使用儲存內容產生使用者身分識別容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="5388b-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="5388b-117">此範例會根據 OAuth 驗證產生具有儲存內容的使用者身分識別容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="5388b-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="5388b-118">參數</span><span class="sxs-lookup"><span data-stu-id="5388b-118">PARAMETERS</span></span>

### <span data-ttu-id="5388b-119">-內容</span><span class="sxs-lookup"><span data-stu-id="5388b-119">-Context</span></span>
<span data-ttu-id="5388b-120">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="5388b-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5388b-121">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="5388b-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="5388b-122">當儲存內容是以 OAuth 驗證為基礎時，會產生使用者身分識別容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="5388b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5388b-123">-DefaultProfile</span></span>
<span data-ttu-id="5388b-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5388b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5388b-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5388b-125">-ExpiryTime</span></span>
<span data-ttu-id="5388b-126">指定共用存取簽章變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="5388b-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="5388b-127">如果使用者設定開始時間，但未設定到期時間，則到期時間會設定為開始時間加上一小時。</span><span class="sxs-lookup"><span data-stu-id="5388b-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="5388b-128">如果未指定開始時間或到期時間，則到期時間會設定為目前的時間加上一小時。</span><span class="sxs-lookup"><span data-stu-id="5388b-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="5388b-129">當儲存內容是以 OAuth 驗證為基礎時，過期時間必須在目前時間之後 7 天內，而且不能早于目前時間。</span><span class="sxs-lookup"><span data-stu-id="5388b-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="5388b-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5388b-130">-FullUri</span></span>
<span data-ttu-id="5388b-131">表示此 Cmdlet 會返回完整的 Blob URI 和共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="5388b-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="5388b-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5388b-132">-IPAddressOrRange</span></span>
<span data-ttu-id="5388b-133">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="5388b-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5388b-134">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="5388b-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="5388b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="5388b-135">-Name</span></span>
<span data-ttu-id="5388b-136">指定 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="5388b-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="5388b-137">-許可權</span><span class="sxs-lookup"><span data-stu-id="5388b-137">-Permission</span></span>
<span data-ttu-id="5388b-138">指定儲存容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="5388b-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="5388b-139">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="5388b-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="5388b-140">-策略</span><span class="sxs-lookup"><span data-stu-id="5388b-140">-Policy</span></span>
<span data-ttu-id="5388b-141">指定 Azure 儲存的 Access 策略。</span><span class="sxs-lookup"><span data-stu-id="5388b-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="5388b-142">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="5388b-142">-Protocol</span></span>
<span data-ttu-id="5388b-143">指定要求允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5388b-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5388b-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5388b-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5388b-145">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="5388b-145">HttpsOnly</span></span>
* <span data-ttu-id="5388b-146">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="5388b-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5388b-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5388b-147">-StartTime</span></span>
<span data-ttu-id="5388b-148">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="5388b-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="5388b-149">-確認</span><span class="sxs-lookup"><span data-stu-id="5388b-149">-Confirm</span></span>
<span data-ttu-id="5388b-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5388b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5388b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5388b-151">-WhatIf</span></span>
<span data-ttu-id="5388b-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5388b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5388b-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5388b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5388b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5388b-154">CommonParameters</span></span>
<span data-ttu-id="5388b-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5388b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5388b-156">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5388b-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5388b-157">輸入</span><span class="sxs-lookup"><span data-stu-id="5388b-157">INPUTS</span></span>

### <span data-ttu-id="5388b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="5388b-158">System.String</span></span>

### <span data-ttu-id="5388b-159">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5388b-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5388b-160">輸出</span><span class="sxs-lookup"><span data-stu-id="5388b-160">OUTPUTS</span></span>

### <span data-ttu-id="5388b-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5388b-161">System.String</span></span>

## <span data-ttu-id="5388b-162">筆記</span><span class="sxs-lookup"><span data-stu-id="5388b-162">NOTES</span></span>

## <span data-ttu-id="5388b-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="5388b-163">RELATED LINKS</span></span>

[<span data-ttu-id="5388b-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5388b-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
