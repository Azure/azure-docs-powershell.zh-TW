---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443404"
---
# <span data-ttu-id="b39fd-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b39fd-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="b39fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b39fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b39fd-103">針對 Azure 儲存空間容器產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="b39fd-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="b39fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b39fd-104">SYNTAX</span></span>

### <span data-ttu-id="b39fd-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b39fd-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="b39fd-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b39fd-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="b39fd-107">說明</span><span class="sxs-lookup"><span data-stu-id="b39fd-107">DESCRIPTION</span></span>
<span data-ttu-id="b39fd-108">**新的-AzureStorageContainerSASToken** Cmdlet 會針對 Azure 儲存體容器 (SAS) 權杖產生共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="b39fd-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="b39fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="b39fd-109">EXAMPLES</span></span>

### <span data-ttu-id="b39fd-110">範例1：使用完整容器許可權產生容器 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="b39fd-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="b39fd-111">這個範例會產生含完整容器許可權的容器 SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="b39fd-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="b39fd-112">範例2：依管道產生多個容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="b39fd-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="b39fd-113">這個範例會使用管線產生多個容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="b39fd-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="b39fd-114">範例3：使用共用存取原則產生容器 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="b39fd-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="b39fd-115">這個範例會產生含共用存取原則的容器 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="b39fd-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="b39fd-116">參數</span><span class="sxs-lookup"><span data-stu-id="b39fd-116">PARAMETERS</span></span>

### <span data-ttu-id="b39fd-117">-內容</span><span class="sxs-lookup"><span data-stu-id="b39fd-117">-Context</span></span>
<span data-ttu-id="b39fd-118">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b39fd-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b39fd-119">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="b39fd-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b39fd-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b39fd-120">-ExpiryTime</span></span>
<span data-ttu-id="b39fd-121">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="b39fd-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="b39fd-122">如果使用者設定開始時間，但不是到期時間，到期時間會設定為開始時間加上1小時。</span><span class="sxs-lookup"><span data-stu-id="b39fd-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="b39fd-123">如果未指定 [開始時間] 和 [到期時間]，則會將到期時間設定為目前的時間加上一個小時。</span><span class="sxs-lookup"><span data-stu-id="b39fd-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="b39fd-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b39fd-124">-FullUri</span></span>
<span data-ttu-id="b39fd-125">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="b39fd-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b39fd-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b39fd-126">-IPAddressOrRange</span></span>
<span data-ttu-id="b39fd-127">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="b39fd-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b39fd-128">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="b39fd-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="b39fd-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b39fd-129">-Name</span></span>
<span data-ttu-id="b39fd-130">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="b39fd-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b39fd-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="b39fd-131">-Permission</span></span>
<span data-ttu-id="b39fd-132">指定儲存容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="b39fd-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="b39fd-133">-原則</span><span class="sxs-lookup"><span data-stu-id="b39fd-133">-Policy</span></span>
<span data-ttu-id="b39fd-134">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="b39fd-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="b39fd-135">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b39fd-135">-Protocol</span></span>
<span data-ttu-id="b39fd-136">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b39fd-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b39fd-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b39fd-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b39fd-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b39fd-138">HttpsOnly</span></span>
* <span data-ttu-id="b39fd-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="b39fd-139">HttpsOrHttp</span></span>

<span data-ttu-id="b39fd-140">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="b39fd-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b39fd-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b39fd-141">-StartTime</span></span>
<span data-ttu-id="b39fd-142">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="b39fd-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b39fd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39fd-143">CommonParameters</span></span>
<span data-ttu-id="b39fd-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b39fd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39fd-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b39fd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39fd-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b39fd-146">INPUTS</span></span>

## <span data-ttu-id="b39fd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b39fd-147">OUTPUTS</span></span>

## <span data-ttu-id="b39fd-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b39fd-148">NOTES</span></span>

## <span data-ttu-id="b39fd-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b39fd-149">RELATED LINKS</span></span>

[<span data-ttu-id="b39fd-150">新-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b39fd-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
