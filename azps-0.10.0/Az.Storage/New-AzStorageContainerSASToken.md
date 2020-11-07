---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: d09fbb09170aa78579f05fb28d544bb29f98fcc8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795108"
---
# <span data-ttu-id="7f469-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7f469-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="7f469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f469-102">SYNOPSIS</span></span>
<span data-ttu-id="7f469-103">針對 Azure 儲存空間容器產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="7f469-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="7f469-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f469-104">SYNTAX</span></span>

### <span data-ttu-id="7f469-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="7f469-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f469-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="7f469-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f469-107">說明</span><span class="sxs-lookup"><span data-stu-id="7f469-107">DESCRIPTION</span></span>
<span data-ttu-id="7f469-108">**新的-AzStorageContainerSASToken** Cmdlet 會針對 Azure 儲存體容器 (SAS) 權杖產生共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="7f469-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="7f469-109">示例</span><span class="sxs-lookup"><span data-stu-id="7f469-109">EXAMPLES</span></span>

### <span data-ttu-id="7f469-110">範例1：使用完整容器許可權產生容器 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="7f469-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="7f469-111">這個範例會產生含完整容器許可權的容器 SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="7f469-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="7f469-112">範例2：依管道產生多個容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="7f469-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="7f469-113">這個範例會使用管線產生多個容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="7f469-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="7f469-114">範例3：使用共用存取原則產生容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="7f469-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="7f469-115">這個範例會產生含共用存取原則的容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="7f469-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="7f469-116">參數</span><span class="sxs-lookup"><span data-stu-id="7f469-116">PARAMETERS</span></span>

### <span data-ttu-id="7f469-117">-內容</span><span class="sxs-lookup"><span data-stu-id="7f469-117">-Context</span></span>
<span data-ttu-id="7f469-118">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="7f469-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7f469-119">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="7f469-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7f469-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f469-120">-DefaultProfile</span></span>
<span data-ttu-id="7f469-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f469-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f469-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7f469-122">-ExpiryTime</span></span>
<span data-ttu-id="7f469-123">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="7f469-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="7f469-124">如果使用者設定開始時間，但不是到期時間，到期時間會設定為開始時間加上1小時。</span><span class="sxs-lookup"><span data-stu-id="7f469-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="7f469-125">如果未指定 [開始時間] 和 [到期時間]，則會將到期時間設定為目前的時間加上一個小時。</span><span class="sxs-lookup"><span data-stu-id="7f469-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="7f469-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7f469-126">-FullUri</span></span>
<span data-ttu-id="7f469-127">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="7f469-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="7f469-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7f469-128">-IPAddressOrRange</span></span>
<span data-ttu-id="7f469-129">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="7f469-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7f469-130">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="7f469-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="7f469-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f469-131">-Name</span></span>
<span data-ttu-id="7f469-132">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="7f469-132">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="7f469-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="7f469-133">-Permission</span></span>
<span data-ttu-id="7f469-134">指定儲存容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="7f469-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="7f469-135">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="7f469-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7f469-136">-原則</span><span class="sxs-lookup"><span data-stu-id="7f469-136">-Policy</span></span>
<span data-ttu-id="7f469-137">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="7f469-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="7f469-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="7f469-138">-Protocol</span></span>
<span data-ttu-id="7f469-139">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7f469-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7f469-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7f469-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7f469-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7f469-141">HttpsOnly</span></span>
* <span data-ttu-id="7f469-142">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="7f469-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f469-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7f469-143">-StartTime</span></span>
<span data-ttu-id="7f469-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="7f469-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="7f469-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f469-145">CommonParameters</span></span>
<span data-ttu-id="7f469-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f469-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f469-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f469-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f469-148">輸入</span><span class="sxs-lookup"><span data-stu-id="7f469-148">INPUTS</span></span>

### <span data-ttu-id="7f469-149">System.object</span><span class="sxs-lookup"><span data-stu-id="7f469-149">System.String</span></span>

### <span data-ttu-id="7f469-150">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="7f469-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f469-151">輸出</span><span class="sxs-lookup"><span data-stu-id="7f469-151">OUTPUTS</span></span>

### <span data-ttu-id="7f469-152">System.object</span><span class="sxs-lookup"><span data-stu-id="7f469-152">System.String</span></span>

## <span data-ttu-id="7f469-153">筆記</span><span class="sxs-lookup"><span data-stu-id="7f469-153">NOTES</span></span>

## <span data-ttu-id="7f469-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f469-154">RELATED LINKS</span></span>

[<span data-ttu-id="7f469-155">新-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7f469-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
