---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443084"
---
# <span data-ttu-id="4ed80-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="4ed80-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="4ed80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ed80-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed80-103">針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="4ed80-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="4ed80-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ed80-104">SYNTAX</span></span>

### <span data-ttu-id="4ed80-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4ed80-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="4ed80-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4ed80-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4ed80-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ed80-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed80-108">**新的-AzureStorageQueueSASToken** Cmdlet 會針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="4ed80-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="4ed80-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ed80-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed80-110">範例1：使用完整許可權產生佇列 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="4ed80-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="4ed80-111">這個範例會產生擁有完整許可權的佇列 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="4ed80-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="4ed80-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ed80-112">PARAMETERS</span></span>

### <span data-ttu-id="4ed80-113">-內容</span><span class="sxs-lookup"><span data-stu-id="4ed80-113">-Context</span></span>
<span data-ttu-id="4ed80-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4ed80-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4ed80-115">您可以 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="4ed80-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4ed80-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4ed80-116">-ExpiryTime</span></span>
<span data-ttu-id="4ed80-117">指定共用存取簽章何時失效。</span><span class="sxs-lookup"><span data-stu-id="4ed80-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="4ed80-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4ed80-118">-FullUri</span></span>
<span data-ttu-id="4ed80-119">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="4ed80-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4ed80-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4ed80-120">-IPAddressOrRange</span></span>
<span data-ttu-id="4ed80-121">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="4ed80-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4ed80-122">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="4ed80-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="4ed80-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ed80-123">-Name</span></span>
<span data-ttu-id="4ed80-124">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="4ed80-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed80-125">-許可權</span><span class="sxs-lookup"><span data-stu-id="4ed80-125">-Permission</span></span>
<span data-ttu-id="4ed80-126">指定儲存佇列的許可權。</span><span class="sxs-lookup"><span data-stu-id="4ed80-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="4ed80-127">-原則</span><span class="sxs-lookup"><span data-stu-id="4ed80-127">-Policy</span></span>
<span data-ttu-id="4ed80-128">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="4ed80-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="4ed80-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4ed80-129">-Protocol</span></span>
<span data-ttu-id="4ed80-130">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4ed80-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4ed80-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4ed80-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4ed80-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4ed80-132">HttpsOnly</span></span>
* <span data-ttu-id="4ed80-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="4ed80-133">HttpsOrHttp</span></span>

<span data-ttu-id="4ed80-134">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="4ed80-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4ed80-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4ed80-135">-StartTime</span></span>
<span data-ttu-id="4ed80-136">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="4ed80-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4ed80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed80-137">CommonParameters</span></span>
<span data-ttu-id="4ed80-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ed80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed80-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ed80-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed80-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4ed80-140">INPUTS</span></span>

## <span data-ttu-id="4ed80-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4ed80-141">OUTPUTS</span></span>

## <span data-ttu-id="4ed80-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4ed80-142">NOTES</span></span>

## <span data-ttu-id="4ed80-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ed80-143">RELATED LINKS</span></span>

