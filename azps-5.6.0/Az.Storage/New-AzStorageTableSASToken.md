---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: 65a90f703f142a01429fb215bd5c66bef74bb4c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916463"
---
# <span data-ttu-id="eaa12-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="eaa12-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="eaa12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eaa12-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa12-103">產生 Azure 儲存體資料表的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="eaa12-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="eaa12-104">語法</span><span class="sxs-lookup"><span data-stu-id="eaa12-104">SYNTAX</span></span>

### <span data-ttu-id="eaa12-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="eaa12-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa12-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="eaa12-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa12-107">描述</span><span class="sxs-lookup"><span data-stu-id="eaa12-107">DESCRIPTION</span></span>
<span data-ttu-id="eaa12-108">**New-AzStorageTableSASToken Cmdlet** 會為 Azure 儲存 (SAS) 權杖產生共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="eaa12-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="eaa12-109">例子</span><span class="sxs-lookup"><span data-stu-id="eaa12-109">EXAMPLES</span></span>

### <span data-ttu-id="eaa12-110">範例 1：產生具有資料表完整許可權的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="eaa12-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="eaa12-111">此命令會針對名為 ContosoResources 之資料表產生具有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="eaa12-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="eaa12-112">該權杖適用于讀取、新增、更新及刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="eaa12-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="eaa12-113">範例 2：產生磁碟分割範圍的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="eaa12-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="eaa12-114">此命令會針對名為 ContosoResources 之資料表產生具有完整許可權的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="eaa12-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="eaa12-115">命令將權杖限制于 *StartPartitionKey* 和 *EndPartitionKey* 參數指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="eaa12-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="eaa12-116">範例 3：產生具有資料表儲存存取策略的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="eaa12-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="eaa12-117">此命令會為名為 ContosoResources 的表格產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="eaa12-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="eaa12-118">命令會指定名為 ClientPolicy01 的已儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="eaa12-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="eaa12-119">參數</span><span class="sxs-lookup"><span data-stu-id="eaa12-119">PARAMETERS</span></span>

### <span data-ttu-id="eaa12-120">-內容</span><span class="sxs-lookup"><span data-stu-id="eaa12-120">-Context</span></span>
<span data-ttu-id="eaa12-121">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="eaa12-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eaa12-122">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaa12-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eaa12-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa12-123">-DefaultProfile</span></span>
<span data-ttu-id="eaa12-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaa12-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaa12-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="eaa12-125">-EndPartitionKey</span></span>
<span data-ttu-id="eaa12-126">指定此 Cmdlet 所建立之權杖範圍結尾的分割鍵。</span><span class="sxs-lookup"><span data-stu-id="eaa12-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eaa12-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="eaa12-127">-EndRowKey</span></span>
<span data-ttu-id="eaa12-128">指定此 Cmdlet 所建立之權杖範圍結尾的列鍵。</span><span class="sxs-lookup"><span data-stu-id="eaa12-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eaa12-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eaa12-129">-ExpiryTime</span></span>
<span data-ttu-id="eaa12-130">指定 SAS 權杖到期的時間。</span><span class="sxs-lookup"><span data-stu-id="eaa12-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="eaa12-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="eaa12-131">-FullUri</span></span>
<span data-ttu-id="eaa12-132">表示此 Cmdlet 會使用 SAS 權杖來返回完整佇列 URI。</span><span class="sxs-lookup"><span data-stu-id="eaa12-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="eaa12-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="eaa12-133">-IPAddressOrRange</span></span>
<span data-ttu-id="eaa12-134">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="eaa12-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="eaa12-135">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="eaa12-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="eaa12-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="eaa12-136">-Name</span></span>
<span data-ttu-id="eaa12-137">指定 Azure 儲存體資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaa12-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="eaa12-138">此 Cmdlet 會為此參數指定的資料表建立 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="eaa12-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="eaa12-139">-許可權</span><span class="sxs-lookup"><span data-stu-id="eaa12-139">-Permission</span></span>
<span data-ttu-id="eaa12-140">指定 Azure 儲存空間資料表的許可權。</span><span class="sxs-lookup"><span data-stu-id="eaa12-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="eaa12-141">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="eaa12-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="eaa12-142">-策略</span><span class="sxs-lookup"><span data-stu-id="eaa12-142">-Policy</span></span>
<span data-ttu-id="eaa12-143">指定儲存的存取策略，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="eaa12-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="eaa12-144">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="eaa12-144">-Protocol</span></span>
<span data-ttu-id="eaa12-145">指定要求允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="eaa12-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="eaa12-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="eaa12-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="eaa12-147">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="eaa12-147">HttpsOnly</span></span>
* <span data-ttu-id="eaa12-148">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="eaa12-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="eaa12-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="eaa12-149">-StartPartitionKey</span></span>
<span data-ttu-id="eaa12-150">指定此 Cmdlet 所建立之權杖範圍起始的分割鍵。</span><span class="sxs-lookup"><span data-stu-id="eaa12-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eaa12-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="eaa12-151">-StartRowKey</span></span>
<span data-ttu-id="eaa12-152">指定此 Cmdlet 所建立之權杖範圍起始的列鍵。</span><span class="sxs-lookup"><span data-stu-id="eaa12-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eaa12-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eaa12-153">-StartTime</span></span>
<span data-ttu-id="eaa12-154">指定 SAS 權杖何時生效。</span><span class="sxs-lookup"><span data-stu-id="eaa12-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="eaa12-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa12-155">CommonParameters</span></span>
<span data-ttu-id="eaa12-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eaa12-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa12-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eaa12-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa12-158">輸入</span><span class="sxs-lookup"><span data-stu-id="eaa12-158">INPUTS</span></span>

### <span data-ttu-id="eaa12-159">System.String</span><span class="sxs-lookup"><span data-stu-id="eaa12-159">System.String</span></span>

### <span data-ttu-id="eaa12-160">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="eaa12-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eaa12-161">輸出</span><span class="sxs-lookup"><span data-stu-id="eaa12-161">OUTPUTS</span></span>

### <span data-ttu-id="eaa12-162">System.String</span><span class="sxs-lookup"><span data-stu-id="eaa12-162">System.String</span></span>

## <span data-ttu-id="eaa12-163">筆記</span><span class="sxs-lookup"><span data-stu-id="eaa12-163">NOTES</span></span>

## <span data-ttu-id="eaa12-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaa12-164">RELATED LINKS</span></span>

[<span data-ttu-id="eaa12-165">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="eaa12-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
