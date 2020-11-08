---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138623"
---
# <span data-ttu-id="1ac9b-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="1ac9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ac9b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac9b-103">建立帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="1ac9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ac9b-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ac9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ac9b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac9b-106">**新的-AzStorageSASToken** Cmdlet 會針對 Azure 儲存空間帳戶 (SAS) 權杖建立帳戶層級的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="1ac9b-107">您可以使用 SAS 權杖委派多個服務的許可權，或委派無法搭配物件層級 SAS 權杖使用之服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="1ac9b-108">示例</span><span class="sxs-lookup"><span data-stu-id="1ac9b-108">EXAMPLES</span></span>

### <span data-ttu-id="1ac9b-109">範例1：使用完整許可權建立帳戶層級 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="1ac9b-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="1ac9b-110">這個命令會建立具有完整許可權的帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="1ac9b-111">範例2：針對 IP 位址範圍建立帳戶層級 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="1ac9b-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="1ac9b-112">這個命令會針對來自指定 IP 位址範圍的 HTTPS 式要求建立帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="1ac9b-113">參數</span><span class="sxs-lookup"><span data-stu-id="1ac9b-113">PARAMETERS</span></span>

### <span data-ttu-id="1ac9b-114">-內容</span><span class="sxs-lookup"><span data-stu-id="1ac9b-114">-Context</span></span>
<span data-ttu-id="1ac9b-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1ac9b-116">您可以使用 New-AzStorageContext Cmdlet 來取得 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="1ac9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac9b-117">-DefaultProfile</span></span>
<span data-ttu-id="1ac9b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ac9b-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ac9b-119">-ExpiryTime</span></span>
<span data-ttu-id="1ac9b-120">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="1ac9b-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1ac9b-121">-IPAddressOrRange</span></span>
<span data-ttu-id="1ac9b-122">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="1ac9b-123">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="1ac9b-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="1ac9b-124">-Permission</span></span>
<span data-ttu-id="1ac9b-125">指定儲存空間帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="1ac9b-126">許可權只有符合指定的資源類型時才是有效的。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="1ac9b-127">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="1ac9b-128">如需可接受許可權值的詳細資訊，請參閱建立帳戶 SAS http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="1ac9b-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="1ac9b-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1ac9b-129">-Protocol</span></span>
<span data-ttu-id="1ac9b-130">指定以帳戶 SA 發出的要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="1ac9b-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1ac9b-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ac9b-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="1ac9b-132">HttpsOnly</span></span>
- <span data-ttu-id="1ac9b-133">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="1ac9b-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1ac9b-134">-ResourceType</span></span>
<span data-ttu-id="1ac9b-135">指定可用於 SAS 權杖的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="1ac9b-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1ac9b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ac9b-137">所有</span><span class="sxs-lookup"><span data-stu-id="1ac9b-137">None</span></span>
- <span data-ttu-id="1ac9b-138">Services</span><span class="sxs-lookup"><span data-stu-id="1ac9b-138">Service</span></span>
- <span data-ttu-id="1ac9b-139">包裝箱</span><span class="sxs-lookup"><span data-stu-id="1ac9b-139">Container</span></span>
- <span data-ttu-id="1ac9b-140">面向</span><span class="sxs-lookup"><span data-stu-id="1ac9b-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac9b-141">-服務</span><span class="sxs-lookup"><span data-stu-id="1ac9b-141">-Service</span></span>
<span data-ttu-id="1ac9b-142">指定服務。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-142">Specifies the service.</span></span>
<span data-ttu-id="1ac9b-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1ac9b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ac9b-144">所有</span><span class="sxs-lookup"><span data-stu-id="1ac9b-144">None</span></span>
- <span data-ttu-id="1ac9b-145">Blob</span><span class="sxs-lookup"><span data-stu-id="1ac9b-145">Blob</span></span>
- <span data-ttu-id="1ac9b-146">檔案</span><span class="sxs-lookup"><span data-stu-id="1ac9b-146">File</span></span>
- <span data-ttu-id="1ac9b-147">序列</span><span class="sxs-lookup"><span data-stu-id="1ac9b-147">Queue</span></span>
- <span data-ttu-id="1ac9b-148">張</span><span class="sxs-lookup"><span data-stu-id="1ac9b-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac9b-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1ac9b-149">-StartTime</span></span>
<span data-ttu-id="1ac9b-150">指定時間（以 **DateTime** 物件表示），SAS 就會生效。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="1ac9b-151">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="1ac9b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac9b-152">CommonParameters</span></span>
<span data-ttu-id="1ac9b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac9b-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ac9b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac9b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="1ac9b-155">INPUTS</span></span>

### <span data-ttu-id="1ac9b-156">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="1ac9b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1ac9b-157">輸出</span><span class="sxs-lookup"><span data-stu-id="1ac9b-157">OUTPUTS</span></span>

### <span data-ttu-id="1ac9b-158">System.object</span><span class="sxs-lookup"><span data-stu-id="1ac9b-158">System.String</span></span>

## <span data-ttu-id="1ac9b-159">筆記</span><span class="sxs-lookup"><span data-stu-id="1ac9b-159">NOTES</span></span>

## <span data-ttu-id="1ac9b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ac9b-160">RELATED LINKS</span></span>

[<span data-ttu-id="1ac9b-161">新-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="1ac9b-162">新-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="1ac9b-163">新-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="1ac9b-164">新-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="1ac9b-165">新-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="1ac9b-166">新-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="1ac9b-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)

