---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: 337dcb1718cf48488115e38052c0fdfed73edc3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450389"
---
# <span data-ttu-id="c1ce9-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="c1ce9-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="c1ce9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ce9-103">針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ce9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1ce9-104">SYNTAX</span></span>

### <span data-ttu-id="c1ce9-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c1ce9-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1ce9-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c1ce9-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1ce9-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1ce9-107">DESCRIPTION</span></span>
<span data-ttu-id="c1ce9-108">**新的-AzureStorageQueueSASToken** Cmdlet 會針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="c1ce9-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1ce9-109">EXAMPLES</span></span>

### <span data-ttu-id="c1ce9-110">範例1：使用完整許可權產生佇列 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="c1ce9-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="c1ce9-111">這個範例會產生擁有完整許可權的佇列 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="c1ce9-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1ce9-112">PARAMETERS</span></span>

### <span data-ttu-id="c1ce9-113">-內容</span><span class="sxs-lookup"><span data-stu-id="c1ce9-113">-Context</span></span>
<span data-ttu-id="c1ce9-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c1ce9-115">您可以 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c1ce9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ce9-116">-DefaultProfile</span></span>
<span data-ttu-id="c1ce9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1ce9-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c1ce9-118">-ExpiryTime</span></span>
<span data-ttu-id="c1ce9-119">指定共用存取簽章何時失效。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="c1ce9-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c1ce9-120">-FullUri</span></span>
<span data-ttu-id="c1ce9-121">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c1ce9-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c1ce9-122">-IPAddressOrRange</span></span>
<span data-ttu-id="c1ce9-123">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c1ce9-124">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="c1ce9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1ce9-125">-Name</span></span>
<span data-ttu-id="c1ce9-126">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ce9-127">-許可權</span><span class="sxs-lookup"><span data-stu-id="c1ce9-127">-Permission</span></span>
<span data-ttu-id="c1ce9-128">指定儲存佇列的許可權。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="c1ce9-129">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c1ce9-130">-原則</span><span class="sxs-lookup"><span data-stu-id="c1ce9-130">-Policy</span></span>
<span data-ttu-id="c1ce9-131">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="c1ce9-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c1ce9-132">-Protocol</span></span>
<span data-ttu-id="c1ce9-133">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c1ce9-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c1ce9-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c1ce9-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c1ce9-135">HttpsOnly</span></span>
* <span data-ttu-id="c1ce9-136">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c1ce9-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c1ce9-137">-StartTime</span></span>
<span data-ttu-id="c1ce9-138">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c1ce9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ce9-139">CommonParameters</span></span>
<span data-ttu-id="c1ce9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ce9-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1ce9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ce9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c1ce9-142">INPUTS</span></span>

### <span data-ttu-id="c1ce9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c1ce9-143">System.String</span></span>

### <span data-ttu-id="c1ce9-144">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c1ce9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1ce9-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c1ce9-145">OUTPUTS</span></span>

### <span data-ttu-id="c1ce9-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c1ce9-146">System.String</span></span>

## <span data-ttu-id="c1ce9-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c1ce9-147">NOTES</span></span>

## <span data-ttu-id="c1ce9-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1ce9-148">RELATED LINKS</span></span>
