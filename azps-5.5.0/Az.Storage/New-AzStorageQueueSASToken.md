---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136882"
---
# <span data-ttu-id="dd5ff-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="dd5ff-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="dd5ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5ff-103">針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="dd5ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd5ff-104">SYNTAX</span></span>

### <span data-ttu-id="dd5ff-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="dd5ff-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd5ff-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="dd5ff-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd5ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd5ff-107">DESCRIPTION</span></span>
<span data-ttu-id="dd5ff-108">**新的-AzStorageQueueSASToken** Cmdlet 會針對 Azure 儲存空間佇列產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="dd5ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="dd5ff-109">EXAMPLES</span></span>

### <span data-ttu-id="dd5ff-110">範例1：使用完整許可權產生佇列 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="dd5ff-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="dd5ff-111">這個範例會產生擁有完整許可權的佇列 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="dd5ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd5ff-112">PARAMETERS</span></span>

### <span data-ttu-id="dd5ff-113">-內容</span><span class="sxs-lookup"><span data-stu-id="dd5ff-113">-Context</span></span>
<span data-ttu-id="dd5ff-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dd5ff-115">您可以 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dd5ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5ff-116">-DefaultProfile</span></span>
<span data-ttu-id="dd5ff-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5ff-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dd5ff-118">-ExpiryTime</span></span>
<span data-ttu-id="dd5ff-119">指定共用存取簽章何時失效。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="dd5ff-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="dd5ff-120">-FullUri</span></span>
<span data-ttu-id="dd5ff-121">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="dd5ff-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="dd5ff-122">-IPAddressOrRange</span></span>
<span data-ttu-id="dd5ff-123">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="dd5ff-124">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="dd5ff-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd5ff-125">-Name</span></span>
<span data-ttu-id="dd5ff-126">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="dd5ff-127">-許可權</span><span class="sxs-lookup"><span data-stu-id="dd5ff-127">-Permission</span></span>
<span data-ttu-id="dd5ff-128">指定儲存佇列的許可權。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="dd5ff-129">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="dd5ff-130">-原則</span><span class="sxs-lookup"><span data-stu-id="dd5ff-130">-Policy</span></span>
<span data-ttu-id="dd5ff-131">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="dd5ff-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="dd5ff-132">-Protocol</span></span>
<span data-ttu-id="dd5ff-133">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="dd5ff-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dd5ff-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="dd5ff-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="dd5ff-135">HttpsOnly</span></span>
* <span data-ttu-id="dd5ff-136">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="dd5ff-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd5ff-137">-StartTime</span></span>
<span data-ttu-id="dd5ff-138">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="dd5ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ff-139">CommonParameters</span></span>
<span data-ttu-id="dd5ff-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5ff-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd5ff-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5ff-142">輸入</span><span class="sxs-lookup"><span data-stu-id="dd5ff-142">INPUTS</span></span>

### <span data-ttu-id="dd5ff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="dd5ff-143">System.String</span></span>

### <span data-ttu-id="dd5ff-144">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="dd5ff-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd5ff-145">輸出</span><span class="sxs-lookup"><span data-stu-id="dd5ff-145">OUTPUTS</span></span>

### <span data-ttu-id="dd5ff-146">System.object</span><span class="sxs-lookup"><span data-stu-id="dd5ff-146">System.String</span></span>

## <span data-ttu-id="dd5ff-147">筆記</span><span class="sxs-lookup"><span data-stu-id="dd5ff-147">NOTES</span></span>

## <span data-ttu-id="dd5ff-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd5ff-148">RELATED LINKS</span></span>
