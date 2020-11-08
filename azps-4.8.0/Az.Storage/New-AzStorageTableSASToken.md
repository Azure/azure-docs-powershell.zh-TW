---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129730"
---
# <span data-ttu-id="4e946-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="4e946-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="4e946-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e946-102">SYNOPSIS</span></span>
<span data-ttu-id="4e946-103">針對 Azure 儲存空間資料表產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4e946-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="4e946-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e946-104">SYNTAX</span></span>

### <span data-ttu-id="4e946-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4e946-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e946-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4e946-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e946-107">說明</span><span class="sxs-lookup"><span data-stu-id="4e946-107">DESCRIPTION</span></span>
<span data-ttu-id="4e946-108">**新的-AzStorageTableSASToken** Cmdlet 會針對 Azure 儲存空間資料表 (SAS) 權杖產生共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="4e946-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="4e946-109">示例</span><span class="sxs-lookup"><span data-stu-id="4e946-109">EXAMPLES</span></span>

### <span data-ttu-id="4e946-110">範例1：產生對資料表擁有完整許可權的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="4e946-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="4e946-111">這個命令會產生一個對名為 ContosoResources 的資料表擁有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4e946-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="4e946-112">該權杖用於讀取、新增、更新和刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="4e946-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="4e946-113">範例2：為一系列分區產生 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="4e946-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="4e946-114">這個命令會產生一個名為 ContosoResources 的資料表擁有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4e946-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="4e946-115">此命令會將權杖限制為 *StartPartitionKey* 和 *EndPartitionKey* 參數指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="4e946-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="4e946-116">範例3：產生具有已儲存的表格存取原則的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="4e946-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="4e946-117">這個命令會為名為 ContosoResources 的資料表產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4e946-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="4e946-118">此命令會指定儲存的存取原則，名為 ClientPolicy01。</span><span class="sxs-lookup"><span data-stu-id="4e946-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="4e946-119">參數</span><span class="sxs-lookup"><span data-stu-id="4e946-119">PARAMETERS</span></span>

### <span data-ttu-id="4e946-120">-內容</span><span class="sxs-lookup"><span data-stu-id="4e946-120">-Context</span></span>
<span data-ttu-id="4e946-121">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4e946-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e946-122">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e946-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4e946-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e946-123">-DefaultProfile</span></span>
<span data-ttu-id="4e946-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e946-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e946-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="4e946-125">-EndPartitionKey</span></span>
<span data-ttu-id="4e946-126">指定此 Cmdlet 所建立之權杖之範圍結尾的分區鍵。</span><span class="sxs-lookup"><span data-stu-id="4e946-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="4e946-127">-EndRowKey</span></span>
<span data-ttu-id="4e946-128">指定此 Cmdlet 所建立之標記之範圍結尾的列鍵。</span><span class="sxs-lookup"><span data-stu-id="4e946-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4e946-129">-ExpiryTime</span></span>
<span data-ttu-id="4e946-130">指定 SAS 權杖的到期時間。</span><span class="sxs-lookup"><span data-stu-id="4e946-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="4e946-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4e946-131">-FullUri</span></span>
<span data-ttu-id="4e946-132">指示這個 Cmdlet 會傳回含 SAS 權杖的完整佇列 URI。</span><span class="sxs-lookup"><span data-stu-id="4e946-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="4e946-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4e946-133">-IPAddressOrRange</span></span>
<span data-ttu-id="4e946-134">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="4e946-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4e946-135">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="4e946-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="4e946-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e946-136">-Name</span></span>
<span data-ttu-id="4e946-137">指定 Azure 儲存空間資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e946-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="4e946-138">這個 Cmdlet 會針對此參數指定的資料表建立 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4e946-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-139">-許可權</span><span class="sxs-lookup"><span data-stu-id="4e946-139">-Permission</span></span>
<span data-ttu-id="4e946-140">指定 Azure 儲存空間資料表的許可權。</span><span class="sxs-lookup"><span data-stu-id="4e946-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="4e946-141">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="4e946-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4e946-142">-原則</span><span class="sxs-lookup"><span data-stu-id="4e946-142">-Policy</span></span>
<span data-ttu-id="4e946-143">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="4e946-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="4e946-144">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4e946-144">-Protocol</span></span>
<span data-ttu-id="4e946-145">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4e946-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4e946-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4e946-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4e946-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4e946-147">HttpsOnly</span></span>
* <span data-ttu-id="4e946-148">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="4e946-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="4e946-149">-StartPartitionKey</span></span>
<span data-ttu-id="4e946-150">指定此 Cmdlet 所建立之權杖之範圍起始的分區鍵。</span><span class="sxs-lookup"><span data-stu-id="4e946-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="4e946-151">-StartRowKey</span></span>
<span data-ttu-id="4e946-152">指定此 Cmdlet 所建立之標記之範圍起始的列索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4e946-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e946-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4e946-153">-StartTime</span></span>
<span data-ttu-id="4e946-154">指定 SAS 權杖變為有效的時間。</span><span class="sxs-lookup"><span data-stu-id="4e946-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="4e946-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e946-155">CommonParameters</span></span>
<span data-ttu-id="4e946-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e946-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e946-157">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e946-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e946-158">輸入</span><span class="sxs-lookup"><span data-stu-id="4e946-158">INPUTS</span></span>

### <span data-ttu-id="4e946-159">System.object</span><span class="sxs-lookup"><span data-stu-id="4e946-159">System.String</span></span>

### <span data-ttu-id="4e946-160">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="4e946-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e946-161">輸出</span><span class="sxs-lookup"><span data-stu-id="4e946-161">OUTPUTS</span></span>

### <span data-ttu-id="4e946-162">System.object</span><span class="sxs-lookup"><span data-stu-id="4e946-162">System.String</span></span>

## <span data-ttu-id="4e946-163">筆記</span><span class="sxs-lookup"><span data-stu-id="4e946-163">NOTES</span></span>

## <span data-ttu-id="4e946-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e946-164">RELATED LINKS</span></span>

[<span data-ttu-id="4e946-165">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4e946-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)