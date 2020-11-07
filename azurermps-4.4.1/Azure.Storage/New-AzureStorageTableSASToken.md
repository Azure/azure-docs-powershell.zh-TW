---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626520"
---
# <span data-ttu-id="923dc-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="923dc-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="923dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="923dc-102">SYNOPSIS</span></span>
<span data-ttu-id="923dc-103">針對 Azure 儲存空間資料表產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="923dc-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="923dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="923dc-104">SYNTAX</span></span>

### <span data-ttu-id="923dc-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="923dc-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="923dc-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="923dc-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="923dc-107">說明</span><span class="sxs-lookup"><span data-stu-id="923dc-107">DESCRIPTION</span></span>
<span data-ttu-id="923dc-108">**新的-AzureStorageTableSASToken** Cmdlet 會針對 Azure 儲存空間資料表 (SAS) 權杖產生共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="923dc-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="923dc-109">示例</span><span class="sxs-lookup"><span data-stu-id="923dc-109">EXAMPLES</span></span>

### <span data-ttu-id="923dc-110">範例1：產生對資料表擁有完整許可權的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="923dc-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="923dc-111">這個命令會產生一個對名為 ContosoResources 的資料表擁有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="923dc-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="923dc-112">該權杖用於讀取、新增、更新和刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="923dc-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="923dc-113">範例2：為一系列分區產生 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="923dc-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="923dc-114">這個命令會產生一個名為 ContosoResources 的資料表擁有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="923dc-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="923dc-115">此命令會將權杖限制為 *StartPartitionKey* 和 *EndPartitionKey* 參數指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="923dc-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="923dc-116">範例3：產生具有已儲存的表格存取原則的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="923dc-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="923dc-117">這個命令會為名為 ContosoResources 的資料表產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="923dc-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="923dc-118">此命令會指定儲存的存取原則，名為 ClientPolicy01。</span><span class="sxs-lookup"><span data-stu-id="923dc-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="923dc-119">參數</span><span class="sxs-lookup"><span data-stu-id="923dc-119">PARAMETERS</span></span>

### <span data-ttu-id="923dc-120">-內容</span><span class="sxs-lookup"><span data-stu-id="923dc-120">-Context</span></span>
<span data-ttu-id="923dc-121">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="923dc-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="923dc-122">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="923dc-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="923dc-123">-EndPartitionKey</span></span>
<span data-ttu-id="923dc-124">指定此 Cmdlet 所建立之權杖之範圍結尾的分區鍵。</span><span class="sxs-lookup"><span data-stu-id="923dc-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="923dc-125">-EndRowKey</span></span>
<span data-ttu-id="923dc-126">指定此 Cmdlet 所建立之標記之範圍結尾的列鍵。</span><span class="sxs-lookup"><span data-stu-id="923dc-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="923dc-127">-ExpiryTime</span></span>
<span data-ttu-id="923dc-128">指定 SAS 權杖的到期時間。</span><span class="sxs-lookup"><span data-stu-id="923dc-128">Specifies when the SAS token expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="923dc-129">-FullUri</span></span>
<span data-ttu-id="923dc-130">指示這個 Cmdlet 會傳回含 SAS 權杖的完整佇列 URI。</span><span class="sxs-lookup"><span data-stu-id="923dc-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="923dc-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="923dc-131">-IPAddressOrRange</span></span>
<span data-ttu-id="923dc-132">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="923dc-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="923dc-133">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="923dc-133">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="923dc-134">-Name</span></span>
<span data-ttu-id="923dc-135">指定 Azure 儲存空間資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="923dc-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="923dc-136">這個 Cmdlet 會針對此參數指定的資料表建立 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="923dc-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-137">-許可權</span><span class="sxs-lookup"><span data-stu-id="923dc-137">-Permission</span></span>
<span data-ttu-id="923dc-138">指定 Azure 儲存空間資料表的許可權。</span><span class="sxs-lookup"><span data-stu-id="923dc-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-139">-原則</span><span class="sxs-lookup"><span data-stu-id="923dc-139">-Policy</span></span>
<span data-ttu-id="923dc-140">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="923dc-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="923dc-141">-Protocol</span></span>
<span data-ttu-id="923dc-142">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="923dc-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="923dc-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="923dc-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="923dc-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="923dc-144">HttpsOnly</span></span>
* <span data-ttu-id="923dc-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="923dc-145">HttpsOrHttp</span></span>

<span data-ttu-id="923dc-146">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="923dc-146">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="923dc-147">-StartPartitionKey</span></span>
<span data-ttu-id="923dc-148">指定此 Cmdlet 所建立之權杖之範圍起始的分區鍵。</span><span class="sxs-lookup"><span data-stu-id="923dc-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="923dc-149">-StartRowKey</span></span>
<span data-ttu-id="923dc-150">指定此 Cmdlet 所建立之標記之範圍起始的列索引鍵。</span><span class="sxs-lookup"><span data-stu-id="923dc-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="923dc-151">-StartTime</span></span>
<span data-ttu-id="923dc-152">指定 SAS 權杖變為有效的時間。</span><span class="sxs-lookup"><span data-stu-id="923dc-152">Specifies when the SAS token becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923dc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923dc-153">CommonParameters</span></span>
<span data-ttu-id="923dc-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="923dc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923dc-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="923dc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923dc-156">輸入</span><span class="sxs-lookup"><span data-stu-id="923dc-156">INPUTS</span></span>

### <span data-ttu-id="923dc-157">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="923dc-157">IStorageContext</span></span>

<span data-ttu-id="923dc-158">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="923dc-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="923dc-159">字串</span><span class="sxs-lookup"><span data-stu-id="923dc-159">String</span></span>

<span data-ttu-id="923dc-160">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="923dc-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="923dc-161">輸出</span><span class="sxs-lookup"><span data-stu-id="923dc-161">OUTPUTS</span></span>

### <span data-ttu-id="923dc-162">System.object</span><span class="sxs-lookup"><span data-stu-id="923dc-162">System.String</span></span>

## <span data-ttu-id="923dc-163">筆記</span><span class="sxs-lookup"><span data-stu-id="923dc-163">NOTES</span></span>

## <span data-ttu-id="923dc-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="923dc-164">RELATED LINKS</span></span>

[<span data-ttu-id="923dc-165">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="923dc-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
