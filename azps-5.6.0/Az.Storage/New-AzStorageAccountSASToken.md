---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915106"
---
# <span data-ttu-id="dd6f3-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="dd6f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6f3-103">建立帳戶層級的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="dd6f3-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd6f3-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6f3-105">描述</span><span class="sxs-lookup"><span data-stu-id="dd6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6f3-106">**New-AzStorageSASToken Cmdlet** 會建立帳戶層級的共用存取簽章 (AZURE) 帳戶的 SAS) 權杖。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="dd6f3-107">您可以使用 SAS 權杖來委派多個服務的許可權，或委派物件層級 SAS 權杖中未提供之服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="dd6f3-108">例子</span><span class="sxs-lookup"><span data-stu-id="dd6f3-108">EXAMPLES</span></span>

### <span data-ttu-id="dd6f3-109">範例 1：建立具有完整許可權的帳戶層級 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="dd6f3-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="dd6f3-110">此命令會建立具有完整許可權的帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="dd6f3-111">範例 2：為 IP 位址範圍建立帳戶層級的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="dd6f3-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="dd6f3-112">此命令會針對來自指定 IP 位址範圍的 HTTPS 要求建立帳戶層級的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="dd6f3-113">參數</span><span class="sxs-lookup"><span data-stu-id="dd6f3-113">PARAMETERS</span></span>

### <span data-ttu-id="dd6f3-114">-內容</span><span class="sxs-lookup"><span data-stu-id="dd6f3-114">-Context</span></span>
<span data-ttu-id="dd6f3-115">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dd6f3-116">您可以使用 New-AzStorageContext Cmdlet 取得 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="dd6f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6f3-117">-DefaultProfile</span></span>
<span data-ttu-id="dd6f3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6f3-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dd6f3-119">-ExpiryTime</span></span>
<span data-ttu-id="dd6f3-120">指定共用存取簽章變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="dd6f3-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="dd6f3-121">-IPAddressOrRange</span></span>
<span data-ttu-id="dd6f3-122">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="dd6f3-123">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="dd6f3-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="dd6f3-124">-Permission</span></span>
<span data-ttu-id="dd6f3-125">指定儲存空間帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="dd6f3-126">許可權只有在符合指定的資源類型時才能有效。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="dd6f3-127">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="dd6f3-128">有關可接受的許可權值詳細資訊，請參閱建構帳戶 SAS http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="dd6f3-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="dd6f3-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="dd6f3-129">-Protocol</span></span>
<span data-ttu-id="dd6f3-130">指定針對帳戶 SAS 要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="dd6f3-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dd6f3-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd6f3-132">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="dd6f3-132">HttpsOnly</span></span>
- <span data-ttu-id="dd6f3-133">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="dd6f3-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dd6f3-134">-ResourceType</span></span>
<span data-ttu-id="dd6f3-135">指定 SAS 權杖中可用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="dd6f3-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dd6f3-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd6f3-137">沒有</span><span class="sxs-lookup"><span data-stu-id="dd6f3-137">None</span></span>
- <span data-ttu-id="dd6f3-138">服務</span><span class="sxs-lookup"><span data-stu-id="dd6f3-138">Service</span></span>
- <span data-ttu-id="dd6f3-139">容器</span><span class="sxs-lookup"><span data-stu-id="dd6f3-139">Container</span></span>
- <span data-ttu-id="dd6f3-140">物件</span><span class="sxs-lookup"><span data-stu-id="dd6f3-140">Object</span></span>

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

### <span data-ttu-id="dd6f3-141">-服務</span><span class="sxs-lookup"><span data-stu-id="dd6f3-141">-Service</span></span>
<span data-ttu-id="dd6f3-142">指定服務。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-142">Specifies the service.</span></span>
<span data-ttu-id="dd6f3-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dd6f3-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd6f3-144">沒有</span><span class="sxs-lookup"><span data-stu-id="dd6f3-144">None</span></span>
- <span data-ttu-id="dd6f3-145">Blob</span><span class="sxs-lookup"><span data-stu-id="dd6f3-145">Blob</span></span>
- <span data-ttu-id="dd6f3-146">檔</span><span class="sxs-lookup"><span data-stu-id="dd6f3-146">File</span></span>
- <span data-ttu-id="dd6f3-147">佇列</span><span class="sxs-lookup"><span data-stu-id="dd6f3-147">Queue</span></span>
- <span data-ttu-id="dd6f3-148">表</span><span class="sxs-lookup"><span data-stu-id="dd6f3-148">Table</span></span>

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

### <span data-ttu-id="dd6f3-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd6f3-149">-StartTime</span></span>
<span data-ttu-id="dd6f3-150">指定時間 ，做為 **DateTime** 物件，在該物件中，SAS 會變為有效。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="dd6f3-151">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="dd6f3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6f3-152">CommonParameters</span></span>
<span data-ttu-id="dd6f3-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6f3-154">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dd6f3-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6f3-155">輸入</span><span class="sxs-lookup"><span data-stu-id="dd6f3-155">INPUTS</span></span>

### <span data-ttu-id="dd6f3-156">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dd6f3-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd6f3-157">輸出</span><span class="sxs-lookup"><span data-stu-id="dd6f3-157">OUTPUTS</span></span>

### <span data-ttu-id="dd6f3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="dd6f3-158">System.String</span></span>

## <span data-ttu-id="dd6f3-159">筆記</span><span class="sxs-lookup"><span data-stu-id="dd6f3-159">NOTES</span></span>

## <span data-ttu-id="dd6f3-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd6f3-160">RELATED LINKS</span></span>

[<span data-ttu-id="dd6f3-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="dd6f3-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="dd6f3-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="dd6f3-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="dd6f3-165">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="dd6f3-166">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="dd6f3-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


